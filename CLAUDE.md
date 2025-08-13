# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an agentic framework being rebuilt from scratch for Symmedia Hub, a comprehensive cloud-based IoT ticketing and remote maintenance solution. The system implements a single-threaded agent architecture with orchestration patterns following modern AI agent design principles.

## System Architecture

### Agent Framework Design
- **Architecture Pattern**: Single-threaded agents with full context sharing (following Cognition principles)
- **Platform**: Symmedia Hub (Azure-based IoT platform)
- **Orchestration**: N8N-based agent workflows with GraphQL APIs
- **Domain**: Tenant service operations (users, customers, tenants)

### Core Components
- **Orchestrator** (`agents/orchestrator/`): Main routing agent that delegates to specialized sub-agents
- **Tenant Service Agent** (`agents/services/tenant-service/`): Domain specialist for user/tenant operations
- **N8N Tools** (`agents/services/tenant-service/n8n-tools/`): GraphQL tool definitions
- **Methodology** (`agents/methodology/`): Agent design principles and architecture patterns

### Technology Stack
- **LLM Integration**: N8N with OpenAI GPT-4.1-mini models
- **API Layer**: GraphQL (Apollo) with bearer token authentication
- **Memory**: PostgreSQL for conversation history
- **Agent Tools**: Custom GraphQL tools for data retrieval and actions

## Development Workflow

### Working with Agent Definitions
- **System Prompts**: Each agent has a system-prompt.md defining behavior and capabilities
- **Tool Configuration**: N8N tool JSON files define GraphQL queries and parameters
- **Agent Descriptions**: agent-description.md files document purpose and routing logic

### GraphQL Schema & API Issues
- **Schema Location**: `agents/services/tenant-service/graphql/limited-tenant.graphql`
- **Known Issues**: Documented in `api-state-issues.md` - pagination unreliable, use client-side counting
- **Authentication**: Bearer tokens in Authorization header
- **Endpoints**: Environment-specific GraphQL endpoints

### Agent Testing & Validation
- **Test Data**: Sample queries and responses in N8N JSON configurations
- **Environment Context**: dev/staging/prod endpoints with tenant-scoped operations
- **Error Handling**: Graceful degradation with partial information when tools fail

## Key Development Principles

### Context Engineering (Critical)
- **Full Context Sharing**: Always propagate complete conversation history and action traces
- **Single-Threaded Execution**: One primary execution thread with full context visibility
- **Action Visibility**: All agent actions carry implicit decisions that must be visible

### Agent Design Patterns
- **Start Simple**: Begin with single-agent solutions before considering multi-agent
- **Incremental Complexity**: Add capabilities step-by-step with validation
- **Fallback Strategies**: Implement robust error handling for legacy API inconsistencies
- **Tool Clarity**: Clear, documented tool interfaces with examples

### Quality Standards
- **Reliability over Features**: Prioritize working solutions over feature completeness
- **Evidence-Based**: All claims must be verifiable through testing or documentation
- **Extensible Patterns**: Design for reuse across additional services

## Agent Tool Development

### GraphQL Tool Structure
```json
{
  "toolDescription": "Clear description for AI understanding",
  "endpoint": "{{ environment-specific GraphQL endpoint }}",
  "query": "GraphQL query with proper field selection",
  "variables": "{{ parameterized inputs }}",
  "headerParametersUi": {
    "parameter": [
      {
        "name": "Authorization",
        "value": "Bearer {{ token }}"
      }
    ]
  }
}
```

### Tool Naming Conventions
- `getMyUser`: Current user information
- `getAllCustomers`: Tenant-scoped customer data
- `getCustomersByStatus`: Filtered customer queries
- `getUsersByStatus`: User activity filtering
- `getUserCount`: User statistics (client-side counting due to API limitations)

## Legacy System Considerations

### 🚨 CRITICAL API Limitations
- **Pagination BROKEN**: Pagination system currently non-functional and causes INTERNAL_ERROR
- **NO PAGINATION**: Never use `pagination` parameters or `pageInfo` - causes query failures  
- **Client-Side Counting**: Always fetch all data with `options: {}` and count in AI logic
- **Filtering**: User filtering limited to `isActive` boolean, customer filtering more robust
- **Performance**: Unknown behavior with large datasets - monitor query execution times

### Mandatory Workarounds
- **Always use `options: {}` for paginated queries** - never use pagination parameters
- Fetch complete datasets and let AI agents handle counting and filtering
- Implement graceful error handling for missing or incomplete data
- Document when pagination becomes available for future optimization

## Environment Configuration

### Development Environments
- **Development**: `gateway-development.secure-service-hub.com/graphql`
- **Staging**: `gateway-staging.secure-service-hub.com/graphql` 
- **Production**: `gateway.secure-service-hub.com/graphql`

### Required Context Variables
- `userId`: Current requesting user ID
- `tenantId`: Tenant scope for all operations
- `token`: Bearer authentication token
- `graphqlEndpoint`: Environment-specific API endpoint
- `sessionId`: Conversation session tracking
- `environment`: Current deployment environment

## Testing & Validation

### Agent Evaluation
- Test with various tenant sizes and data volumes
- Validate error handling with API failures
- Verify context propagation across agent interactions
- Monitor token usage and response times

### Schema Validation Checklist
- [ ] Test all customer status enum values (NEW, INVITED, ONBOARDED, DEMO, CONVERTED)
- [ ] Verify user status filtering (INVITED, ONBOARDED, etc.)
- [ ] Validate complex customer filter expressions
- [ ] Monitor GraphQL query performance with large datasets

## Future Extensibility

### Additional Services
- Pattern established for tenant service can be replicated for other Symmedia Hub services
- Orchestrator routing can be extended for new domain specialists
- Tool definitions follow consistent GraphQL patterns

### Scalability Considerations
- Context compression strategies for long conversations
- Efficient GraphQL query optimization
- Agent specialization without context fragmentation