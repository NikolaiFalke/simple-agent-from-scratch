# Tenant Service API State & Issues

This file tracks known issues, limitations, and misleading aspects of the Tenant Service GraphQL API.

## 🚨 CRITICAL: Pagination Partially Broken

### ⚠️ Mixed Pagination State - Data Works, Counting Broken
**Status**: Pagination parameters work for data retrieval, but `pageInfo` counting is broken
**Evidence**: Frontend examples show successful pagination usage with broken `pageInfo`
**Impact**: Can't rely on `totalElements` or `totalPages` for accurate counts

**What Works**: 
- ✅ Pagination parameters (`page`, `pageSize`) work for data retrieval
- ✅ Can fetch paginated data successfully  
- ✅ Frontend uses: `customers(pagination: {page: $page, pageSize: $pageSize})`

**What's Broken**:
- ❌ `pageInfo.totalElements` returns `null`
- ❌ `pageInfo.totalPages` returns `-1` 
- ❌ Cannot use pageInfo for counting or statistics

### 🔧 Current Agent Framework Strategy
**For counting/statistics (our use case)**:
- **OMIT options parameter entirely** - don't use `options: {}`
- Query pattern: `usersPaginated { data { ... } }` (no options)
- Let AI count results client-side  
- Never rely on `pageInfo` for counting

**For future frontend usage**:
- Pagination parameters work: `pagination: {page: 1, pageSize: 15}`
- Just don't use `pageInfo.totalElements` or `pageInfo.totalPages`

**Affected Queries**: 
- `usersPaginated` - OMIT options entirely for counting, pagination works for data display
- `customersPaginated` - OMIT options entirely for counting, pagination works for data display

### 📋 Pagination Readiness Section
**Future State**: When `pageInfo` counting is fixed, this section will be updated with:
- Working `pageInfo.totalElements` examples for accurate counting
- Performance-optimized counting strategies using pagination
- Count-specific queries without fetching all data

**Current State**: All tools avoid empty options and query aliases for reliable data fetching.
**Frontend Pattern**: Pagination works for data display, just not for counting.
**Query Alias Issue**: Query aliases with empty options may cause parsing errors.

**Working Examples**:
```graphql
# ✅ AGENT FRAMEWORK - Fetch all data for counting (NO options parameter):
usersPaginated {
  data {
    id
    isActive
    status
    # ... get all data and let AI count client-side
  }
}

# ✅ FRONTEND PATTERN - Pagination works for data display:
customers(pagination: {page: 0, pageSize: 15}, sortBy: [{name: "ASC"}]) {
  data {
    id
    name
    status
  }
  pageInfo {
    currentPage      # ← Works
    fromElement      # ← Works  
    untilElement     # ← Works
    totalElements    # ← Returns null (broken)
    totalPages       # ← Returns -1 (broken)
  }
}

# ❌ INVALID - Empty options parameter breaks query:
usersPaginated(options: {}) { ... }

# ❌ INVALID - Query alias with empty options may break:
allUsers: usersPaginated(options: {}) { ... }

# ❌ DON'T RELY ON pageInfo FOR COUNTING:
# totalElements: null, totalPages: -1
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