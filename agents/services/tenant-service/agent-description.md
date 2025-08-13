# Tenant Service Agent

**Agent Type**: Domain Specialist  
**Service Domain**: Tenant Service  
**Specialization**: User management, tenant information, customer data, invitations, company information

## N8N Tool Description
```
Tenant Service Agent - Handles user information, tenant details, customer queries, invitations, and company information. Specializes in user profiles, customer management, CRUD operations, user/customer invitations, and company tag exploration for the Symmedia Hub platform.
```

## Purpose

The Tenant Service Agent specializes in handling all queries related to:
- Current user information and profile details
- Tenant information and configuration
- Customer management, queries, and creation
- Service organisation management and creation
- Facility management and creation
- User roles and permissions
- User activity and status tracking
- User and customer invitation management
- Company information and tag exploration
- CRUD operations for tenant-scoped entities

## Capabilities

### User Information
- Retrieve current user profile (`getMyUser`)
- Get user roles and permissions
- Check user status and activity
- Access tenant-specific user details

### Customer Management
- Query customers by status
- Filter customers by various criteria
- Get customer counts and statistics
- Access customer profile information
- Create new customers with smart service org matching
- Send customer onboarding invitations

### Tenant Operations
- Retrieve tenant details and configuration
- Access tenant-specific settings
- Get tenant roles and permissions
- Query tenant-scoped data
- Explore company tags and information

### Invitation Management
- Send user invitations to join tenant
- Send customer onboarding invitations
- Smart customer ID resolution for invitations

### Service & Facility Management
- Create and manage service organisations
- Create and manage facilities
- Smart conversational CRUD workflows

## When to Use

Route requests to this agent when users ask about:
- "Who am I?" / "My user info" / "My profile"
- "Show me customers with status X"
- "How many active/inactive users?"
- "Give me all customers" / "How many customers do I have?"
- "Customer count" / "Total customers"
- "Create a customer" / "Add a new customer"
- "Create a service organisation" / "Add a service org"
- "Create a facility" / "Add a facility"
- "What service organisations do I have?"
- "What are my permissions?"
- "Tell me about my tenant"
- "Invite a user" / "Send user invitation"
- "Invite customer ABC" / "Send customer invitation" / "Onboard customer"
- "What are company tags?" / "Show me company tags"
- "What tags do we have?" / "Show me our company information"
- Any queries involving users, customers, or tenant-scoped data
- Any CRUD operations for customers, service orgs, or facilities
- Any invitation or onboarding workflows

## Tools Available

### Query Tools
- `getMyUser`: Retrieves complete current user information
- `getCustomersByStatus`: Get customers filtered by status
- `getAllCustomers`: List all customers for tenant (with counting capability)
- `getUsersByStatus`: Filter users by active/inactive status  
- `getUserCount`: Get user statistics and counts
- `getAllServiceOrganisations`: List all service organisations
- `getCompanyTags`: Retrieve company information and tags

### CRUD Tools
- `createServiceOrganisation`: Create new service organisations
- `createCustomer`: Create new customers (with smart service org matching)
- `createFacility`: Create new facilities

### Invitation Tools
- `inviteUser`: Send user invitations to join tenant
- `inviteCustomer`: Send customer onboarding invitations (with smart ID resolution)

## Response Style

- Provide clear, structured information
- Include relevant context (tenant, roles, permissions)
- Format data in user-friendly way
- Handle missing or incomplete data gracefully