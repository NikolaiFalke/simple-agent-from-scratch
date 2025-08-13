# Tenant Service API State & Issues

This file tracks known issues, limitations, and misleading aspects of the Tenant Service GraphQL API.

## 📊 Pagination Issues

### ❌ PageInfo.totalElements Not Reliable
**Issue**: Pagination `pageInfo.totalElements` is not correctly implemented
**Impact**: Cannot rely on pagination counts for statistics
**Affected Tools**: 
- `getUserCount` (originally designed to use pageInfo.totalElements)
- Any tool that needs accurate counts

**Workaround**: 
- Fetch all data without pagination restrictions
- Let AI count results client-side

**Example**:
```graphql
# ❌ Don't rely on this:
usersPaginated(options: { pagination: { page: 1, pageSize: 1 } }) {
  pageInfo {
    totalElements  # ← Not accurate
  }
}

# ✅ Use this instead:
usersPaginated(options: {}) {
  data {
    id
    isActive
    # ... get all data and count on AI side
  }
}
```

## 🔍 Schema vs Reality

### ✅ Working Queries
- `myUser` - Works perfectly
- `usersPaginated(options: { filter: { isActive: Boolean } })` - Filtering works
- `customersPaginated(options: { filter: { status: { is: CustomerStatus } } })` - Status filtering works

### ⚠️ Untested/Unknown
- Complex nested filters in `CustomerFilter`
- Performance with large datasets without pagination
- Whether empty `options: {}` returns all data or has default limits

## 📝 Schema Observations

### User Types Available
From schema lines 532-543 and 518-529:
- `User` - Main user type
- `TenantUser` - Tenant-specific user (legacy?)

### Customer Status Values
From schema lines 576-582:
```
enum CustomerStatus {
  NEW
  INVITED  
  ONBOARDED
  DEMO
  CONVERTED
}
```

### User Status Values  
From schema lines 545-551:
```
enum UserStatus {
  INVITED
  INVITATION_EXPIRED
  ONBOARDED
  ONBOARDING
  DECLINED
}
```

### Filter Capabilities
- `UserFilter` (lines 181-183): Only `isActive: Boolean`
- `CustomerFilter` (lines 395-407): Complex filtering with expressions

## 🚨 Known Limitations

1. **No Direct Count Queries**: No dedicated count endpoints, must fetch all data
2. **Pagination Unreliable**: Cannot trust pageInfo for accurate statistics  
3. **Performance Unknown**: Large tenant impact on fetching all users/customers unknown
4. **Schema Assumptions**: Some fields might not be populated despite being in schema

## 📈 Performance Considerations

### Current Approach
- Fetch all data without pagination
- AI processes results for counts/filtering
- Simple and reliable but potentially inefficient

### Risks
- Large tenants might hit GraphQL query limits
- Network overhead for large datasets
- Processing time for AI to count/filter results

## 🔄 Recommended Updates

1. **Test pagination behavior** - Verify if `options: {}` has default limits
2. **Monitor performance** - Track query times with larger datasets
3. **Schema validation** - Test complex filter combinations
4. **Error handling** - Document GraphQL error patterns

## 📋 Testing Checklist

- [ ] Test getUserCount with various tenant sizes
- [ ] Verify customer filtering with all status values  
- [ ] Test usersPaginated without any options
- [ ] Monitor GraphQL query execution times
- [ ] Validate error responses for invalid filters

---

**Last Updated**: 2025-08-09
**Schema Version**: tenant-service/limited-tenant.graphql