{
"operationName": "myTenantRoles",
"variables": {},
"query": "query myTenantRoles {\n  myUser {\n    id\n    tenant {\n      id\n      tenantRoles {\n        id\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n}"
}

{
"data": {
"myUser": {
"id": "366f1489-bf4c-44a0-aeb4-8a676a78ebce",
"tenant": {
"id": "1c27e2eb-0b3d-424a-b8f7-37521d1175b1",
"tenantRoles": [
{
"id": "00000000-0000-0000-1111-000000000000",
"__typename": "TenantRole"
},
{
"id": "00000000-0000-0000-1111-000000000001",
"__typename": "TenantRole"
},
{
"id": "00000000-0000-0000-1111-000000000002",
"__typename": "TenantRole"
},
{
"id": "00000000-0000-0000-1111-000000000009",
"__typename": "TenantRole"
},
{
"id": "00000000-0000-0000-1111-000000000013",
"__typename": "TenantRole"
},
{
"id": "00000000-0000-0000-1111-000000000014",
"__typename": "TenantRole"
},
{
"id": "00000000-0000-0000-1111-000000000019",
"__typename": "TenantRole"
}
],
"__typename": "Tenant"
},
"__typename": "User"
}
},
"extensions": {
"traceId": "a5843cf26a9072001af8054a25b33a23"
}
}


{
"operationName": "getPermissionsOfCurrentUser",
"variables": {},
"query": "query getPermissionsOfCurrentUser {\n  permissionsOfCurrentUser {\n    key\n    __typename\n  }\n}"
}

{
"data": {
"permissionsOfCurrentUser": [
{
"key": "Accessmanagement.assignUserRoleToUser",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.assignedUserRolesOfUser",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.assignedUsersOfUserRole",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.feature",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.features",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.featuresOfApplication",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.featuresOfTenant",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.hasTenantFeature",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.permission",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.permissions",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.permissionsOfApplication",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.permissionsOfCurrentUser",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.scopes",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.tenantRole",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.tenantRoles",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.tenantRolesOfTenant",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.userRole",
"__typename": "Permission"
},
{
"key": "Accessmanagement.Query.userRoles",
"__typename": "Permission"
},
{
"key": "Accessmanagement.unassignUserRoleFromUser",
"__typename": "Permission"
},
{
"key": "ApplicationService.Application.Install",
"__typename": "Permission"
},
{
"key": "ApplicationService.Application.Manage",
"__typename": "Permission"
},
{
"key": "ApplicationService.Application.ManageCompatibility",
"__typename": "Permission"
},
{
"key": "ApplicationService.Application.Overview",
"__typename": "Permission"
},
{
"key": "ApplicationService.Application.Register",
"__typename": "Permission"
},
{
"key": "BillingService.Operator.Subscriptions.Read",
"__typename": "Permission"
},
{
"key": "BillingService.Serviceprovider.Subscriptions.Read",
"__typename": "Permission"
},
{
"key": "Conferencing.View",
"__typename": "Permission"
},
{
"key": "CustomerService.CreateCustomer",
"__typename": "Permission"
},
{
"key": "CustomerService.DeleteCustomer",
"__typename": "Permission"
},
{
"key": "CustomerService.GetCustomer",
"__typename": "Permission"
},
{
"key": "CustomerService.GetCustomer.Overview",
"__typename": "Permission"
},
{
"key": "CustomerService.GetCustomers",
"__typename": "Permission"
},
{
"key": "CustomerService.UpdateCustomer",
"__typename": "Permission"
},
{
"key": "DataService.DataManagement.Tenant.Read",
"__typename": "Permission"
},
{
"key": "EdgeDevice.CertificateManagement.CreateCertificate",
"__typename": "Permission"
},
{
"key": "EdgeDevice.DeviceManagement.RebootOS",
"__typename": "Permission"
},
{
"key": "EdgeDevice.DeviceManagement.UpdateOS",
"__typename": "Permission"
},
{
"key": "Filetransfer.Manage",
"__typename": "Permission"
},
{
"key": "Filetransfer.Read",
"__typename": "Permission"
},
{
"key": "Filetransfer.Write",
"__typename": "Permission"
},
{
"key": "GetCustomerStateStatistics",
"__typename": "Permission"
},
{
"key": "Help.JiraServiceDesk.View",
"__typename": "Permission"
},
{
"key": "MachinaTalk.Assistant.Overview",
"__typename": "Permission"
},
{
"key": "MachineManagement.Asset.Create",
"__typename": "Permission"
},
{
"key": "MachineManagement.Asset.Delete",
"__typename": "Permission"
},
{
"key": "MachineManagement.Asset.ManageEdgeDevice",
"__typename": "Permission"
},
{
"key": "MachineManagement.Asset.ManageFacility",
"__typename": "Permission"
},
{
"key": "MachineManagement.Asset.ManageMachineModel",
"__typename": "Permission"
},
{
"key": "MachineManagement.Asset.Overview",
"__typename": "Permission"
},
{
"key": "MachineManagement.Asset.Propose",
"__typename": "Permission"
},
{
"key": "MachineManagement.Asset.Read",
"__typename": "Permission"
},
{
"key": "MachineManagement.Asset.Update",
"__typename": "Permission"
},
{
"key": "MachineManagement.CustomerMachine.Create",
"__typename": "Permission"
},
{
"key": "MachineManagement.CustomerMachine.Delete",
"__typename": "Permission"
},
{
"key": "MachineManagement.CustomerMachine.ManageEdgeDevice",
"__typename": "Permission"
},
{
"key": "MachineManagement.CustomerMachine.ManageMachineModel",
"__typename": "Permission"
},
{
"key": "MachineManagement.CustomerMachine.Move",
"__typename": "Permission"
},
{
"key": "MachineManagement.CustomerMachine.Overview",
"__typename": "Permission"
},
{
"key": "MachineManagement.CustomerMachine.Proposal.Revoke",
"__typename": "Permission"
},
{
"key": "MachineManagement.CustomerMachine.Propose",
"__typename": "Permission"
},
{
"key": "MachineManagement.CustomerMachine.Read",
"__typename": "Permission"
},
{
"key": "MachineManagement.CustomerMachine.Update",
"__typename": "Permission"
},
{
"key": "MachineManagement.EdgeDevice.Move",
"__typename": "Permission"
},
{
"key": "MachineManagement.EdgeDevice.Overview",
"__typename": "Permission"
},
{
"key": "MachineManagement.EdgeDevice.Read",
"__typename": "Permission"
},
{
"key": "MachineManagement.EdgeDevice.Update",
"__typename": "Permission"
},
{
"key": "MachineManagement.Machine.ManageLinking",
"__typename": "Permission"
},
{
"key": "MachineManagement.Machine.Read",
"__typename": "Permission"
},
{
"key": "MachineManagement.MachineDocument.Manage",
"__typename": "Permission"
},
{
"key": "MachineManagement.MachineDocument.Manage.MachineModel",
"__typename": "Permission"
},
{
"key": "MachineManagement.MachineDocument.Read",
"__typename": "Permission"
},
{
"key": "MachineManagement.MachineModel.Create",
"__typename": "Permission"
},
{
"key": "MachineManagement.MachineModel.Delete",
"__typename": "Permission"
},
{
"key": "MachineManagement.MachineModel.Overview",
"__typename": "Permission"
},
{
"key": "MachineManagement.MachineModel.Read",
"__typename": "Permission"
},
{
"key": "MachineManagement.MachineModel.Update",
"__typename": "Permission"
},
{
"key": "MachineManagement.ServiceContract.Manage",
"__typename": "Permission"
},
{
"key": "MachineManagement.ServiceContract.Overview",
"__typename": "Permission"
},
{
"key": "MachineManagement.ServiceLicenses.Tenant.Overview",
"__typename": "Permission"
},
{
"key": "MachineManagement.ServiceLicenses.Tenant.Read",
"__typename": "Permission"
},
{
"key": "MachineManagement.Tags.Asset.Manage",
"__typename": "Permission"
},
{
"key": "MachineManagement.Tags.Asset.Overview",
"__typename": "Permission"
},
{
"key": "RAM.OperatorRemoteAccess.Create",
"__typename": "Permission"
},
{
"key": "RAM.OperatorRemoteSession.Start",
"__typename": "Permission"
},
{
"key": "RAM.RemoteAccess.Create",
"__typename": "Permission"
},
{
"key": "RAM.RemoteSession.Start",
"__typename": "Permission"
},
{
"key": "RAM.TunnelConfig.Create",
"__typename": "Permission"
},
{
"key": "RAM.TunnelConfig.Delete",
"__typename": "Permission"
},
{
"key": "RAM.TunnelConfig.Read",
"__typename": "Permission"
},
{
"key": "RAM.TunnelConfig.Update",
"__typename": "Permission"
},
{
"key": "RAM.TunnelConfigTemplate.Create",
"__typename": "Permission"
},
{
"key": "RAM.TunnelConfigTemplate.Delete",
"__typename": "Permission"
},
{
"key": "RAM.TunnelConfigTemplate.Read",
"__typename": "Permission"
},
{
"key": "RAM.TunnelConfigTemplate.Update",
"__typename": "Permission"
},
{
"key": "SCM.FollowTheSun.Manage",
"__typename": "Permission"
},
{
"key": "SCM.Operator.CreateSharedServiceCase",
"__typename": "Permission"
},
{
"key": "SCM.Operator.View",
"__typename": "Permission"
},
{
"key": "SCM.ServiceProvider.CreateInternalServiceCase",
"__typename": "Permission"
},
{
"key": "SCM.ServiceProvider.CreateSharedServiceCase",
"__typename": "Permission"
},
{
"key": "SCM.ServiceProvider.ProvideService",
"__typename": "Permission"
},
{
"key": "SCM.ServiceProvider.SetExternalId",
"__typename": "Permission"
},
{
"key": "SCM.ServiceProvider.View",
"__typename": "Permission"
},
{
"key": "SCM.TenantSettings.CustomFieldsConfiguration.Manage",
"__typename": "Permission"
},
{
"key": "SCM.TenantSettings.Manage",
"__typename": "Permission"
},
{
"key": "TenantService.Agreements.Read",
"__typename": "Permission"
},
{
"key": "TenantService.CompanySettings.Overview",
"__typename": "Permission"
},
{
"key": "TenantService.Facility.Create",
"__typename": "Permission"
},
{
"key": "TenantService.Facility.Delete",
"__typename": "Permission"
},
{
"key": "TenantService.Facility.Overview",
"__typename": "Permission"
},
{
"key": "TenantService.Facility.Read",
"__typename": "Permission"
},
{
"key": "TenantService.Facility.Update",
"__typename": "Permission"
},
{
"key": "TenantService.ServiceOrganisation.Create",
"__typename": "Permission"
},
{
"key": "TenantService.ServiceOrganisation.Delete",
"__typename": "Permission"
},
{
"key": "TenantService.ServiceOrganisation.Overview",
"__typename": "Permission"
},
{
"key": "TenantService.ServiceOrganisation.Read",
"__typename": "Permission"
},
{
"key": "TenantService.ServiceOrganisation.Update",
"__typename": "Permission"
},
{
"key": "TenantService.Tenant.CompanyCard.Overview",
"__typename": "Permission"
},
{
"key": "TenantService.Tenant.Invite",
"__typename": "Permission"
},
{
"key": "TenantService.Tenant.Read",
"__typename": "Permission"
},
{
"key": "TenantService.Tenant.Update",
"__typename": "Permission"
},
{
"key": "TenantService.Theme.Manage",
"__typename": "Permission"
},
{
"key": "TenantService.Theme.Read",
"__typename": "Permission"
},
{
"key": "TenantService.User.Delete",
"__typename": "Permission"
},
{
"key": "TenantService.User.Invite",
"__typename": "Permission"
},
{
"key": "TenantService.User.Overview",
"__typename": "Permission"
},
{
"key": "TenantService.User.Read",
"__typename": "Permission"
},
{
"key": "TenantService.User.Update",
"__typename": "Permission"
},
{
"key": "ZESS.ServiceKpiDashboard.Overview",
"__typename": "Permission"
}
]
},
"extensions": {
"traceId": "3d004f99f481b891922775ba9bf01a2e"
}
}


{
"operationName": "getCustomerStateStatistics",
"variables": {
"filter": {
"and": []
}
},
"query": "query getCustomerStateStatistics($filter: CustomerFilter) {\n  customerStateStatistics(where: $filter) {\n    status\n    count\n    __typename\n  }\n}"
}

{
"data": {
"customerStateStatistics": [
{
"status": "NEW",
"count": 1,
"__typename": "CustomerStateStatistic"
},
{
"status": "INVITED",
"count": 0,
"__typename": "CustomerStateStatistic"
},
{
"status": "ONBOARDED",
"count": 6,
"__typename": "CustomerStateStatistic"
},
{
"status": "DEMO",
"count": 0,
"__typename": "CustomerStateStatistic"
},
{
"status": "CONVERTED",
"count": 0,
"__typename": "CustomerStateStatistic"
}
]
},
"extensions": {
"traceId": "7869baec81fddafb5f6b6b01d4aa4743"
}
}

{
"operationName": "tableCustomers",
"variables": {
"address": true,
"externalId": false,
"machinesCount": true,
"name": true,
"postalCode": false,
"state": false,
"status": true,
"street": false,
"websiteUrl": false,
"linkedTenant": false,
"serviceOrganisation": true,
"pageSize": 15,
"page": 0,
"sorter": [
{
"name": "ASC"
}
],
"filter": {
"and": []
}
},
"query": "query tableCustomers($page: Int!, $pageSize: Int!, $sorter: [CustomerSorter!], $filter: CustomerFilter, $address: Boolean!, $externalId: Boolean!, $linkedTenant: Boolean!, $machinesCount: Boolean!, $name: Boolean!, $postalCode: Boolean!, $serviceOrganisation: Boolean!, $state: Boolean!, $status: Boolean!, $street: Boolean!, $websiteUrl: Boolean!) {\n  customers(\n    pagination: {page: $page, pageSize: $pageSize}\n    sortBy: $sorter\n    where: $filter\n  ) {\n    data {\n      id\n      linkedTenant @include(if: $linkedTenant) {\n        id\n        name\n        __typename\n      }\n      name @include(if: $name)\n      externalId @include(if: $externalId)\n      websiteUrl @include(if: $websiteUrl)\n      status @include(if: $status)\n      address {\n        country @include(if: $address)\n        postalCode @include(if: $postalCode)\n        city @include(if: $address)\n        street @include(if: $street)\n        state @include(if: $state)\n        __typename\n      }\n      machinesCount @include(if: $machinesCount)\n      registeredMachinesCount @include(if: $machinesCount)\n      serviceOrganisation @include(if: $serviceOrganisation) {\n        id\n        name\n        __typename\n      }\n      __typename\n    }\n    pageInfo {\n      currentPage\n      fromElement\n      untilElement\n      totalElements\n      totalPages\n      __typename\n    }\n    __typename\n  }\n}"
}

{
"data": {
"customers": {
"data": [
{
"id": "171b7ce6-af80-4116-af77-8dc0d22f1557",
"name": "Consulting Test Operator",
"status": "ONBOARDED",
"address": {
"country": "FR",
"city": null,
"__typename": "Address"
},
"machinesCount": null,
"registeredMachinesCount": null,
"serviceOrganisation": {
"id": "89d2173a-2f55-4040-bb04-a063c7b89c80",
"name": "Service Frankreich",
"__typename": "ServiceOrganisation"
},
"__typename": "Customer"
},
{
"id": "086a0362-1ed1-4b24-903a-1187ac9d79e9",
"name": "drupa Operator",
"status": "ONBOARDED",
"address": {
"country": "DE",
"city": null,
"__typename": "Address"
},
"machinesCount": 1,
"registeredMachinesCount": null,
"serviceOrganisation": {
"id": "a12c7f9a-d3f8-4019-a1a7-8b3d8fe83a92",
"name": "Service Europa",
"__typename": "ServiceOrganisation"
},
"__typename": "Customer"
},
{
"id": "447f81ba-9713-459f-b7c3-a689b1eebabb",
"name": "Epsilon",
"status": "NEW",
"address": {
"country": "IT",
"city": "Torino",
"__typename": "Address"
},
"machinesCount": 1,
"registeredMachinesCount": null,
"serviceOrganisation": {
"id": "1aca771f-9ebc-493c-b76a-7f19a0345ad0",
"name": "Service Italien",
"__typename": "ServiceOrganisation"
},
"__typename": "Customer"
},
{
"id": "9b7f1c15-7190-4591-9ddc-ecc5674e69b0",
"name": "FRAME TEST",
"status": "ONBOARDED",
"address": {
"country": "AT",
"city": null,
"__typename": "Address"
},
"machinesCount": 1,
"registeredMachinesCount": 1,
"serviceOrganisation": {
"id": "a12c7f9a-d3f8-4019-a1a7-8b3d8fe83a92",
"name": "Service Europa",
"__typename": "ServiceOrganisation"
},
"__typename": "Customer"
},
{
"id": "1c1ddcb3-c86c-4f85-bd44-28cc511597ca",
"name": "Hawk Asset Solutions",
"status": "ONBOARDED",
"address": {
"country": "DE",
"city": null,
"__typename": "Address"
},
"machinesCount": 1,
"registeredMachinesCount": 1,
"serviceOrganisation": {
"id": "44612ba1-7e99-486f-9c22-f881721d45d0",
"name": "Hawk Asset Solutions Service Org",
"__typename": "ServiceOrganisation"
},
"__typename": "Customer"
},
{
"id": "f6a720bd-06b4-438c-b8f2-437355452004",
"name": "Internal Setup Customer",
"status": "ONBOARDED",
"address": {
"country": "DE",
"city": null,
"__typename": "Address"
},
"machinesCount": null,
"registeredMachinesCount": null,
"serviceOrganisation": {
"id": "6facf52e-91fd-4b80-94d7-6f57742e82f4",
"name": "Service Deutschland",
"__typename": "ServiceOrganisation"
},
"__typename": "Customer"
},
{
"id": "6471b3b9-f87d-462a-8f63-d5205a4f4022",
"name": "LFF Lern- und Forschungsfabrik ",
"status": "ONBOARDED",
"address": {
"country": "DE",
"city": "Bochum",
"__typename": "Address"
},
"machinesCount": 13,
"registeredMachinesCount": 13,
"serviceOrganisation": {
"id": "6facf52e-91fd-4b80-94d7-6f57742e82f4",
"name": "Service Deutschland",
"__typename": "ServiceOrganisation"
},
"__typename": "Customer"
}
],
"pageInfo": {
"currentPage": 0,
"fromElement": 0,
"untilElement": 14,
"totalElements": null,
"totalPages": -1,
"__typename": "PageInfo"
},
"__typename": "CustomerQueryResult"
}
},
"extensions": {
"traceId": "3cf157f5a6f2f10020fdf62a9c62b584"
}
}


{
"operationName": "customerDetail",
"variables": {
"id": "171b7ce6-af80-4116-af77-8dc0d22f1557"
},
"query": "query customerDetail($id: ID!) {\n  customer(id: $id) {\n    ...CustomerFields\n    serviceOrganisation {\n      name\n      id\n      __typename\n    }\n    __typename\n  }\n}\n\nfragment CustomerFields on Customer {\n  id\n  tenantId\n  linkedTenant {\n    id\n    name\n    __typename\n  }\n  name\n  externalId\n  websiteUrl\n  status\n  address {\n    country\n    postalCode\n    city\n    street\n    street2\n    state\n    __typename\n  }\n  __typename\n}"
}

{
"data": {
"customer": {
"id": "171b7ce6-af80-4116-af77-8dc0d22f1557",
"tenantId": "1c27e2eb-0b3d-424a-b8f7-37521d1175b1",
"linkedTenant": {
"id": "3143bd42-b97e-41cf-acaa-74009703d96b",
"name": "Consulting Test Operator",
"__typename": "Tenant"
},
"name": "Consulting Test Operator",
"externalId": "aaa",
"websiteUrl": null,
"status": "ONBOARDED",
"address": {
"country": "FR",
"postalCode": null,
"city": null,
"street": null,
"street2": null,
"state": null,
"__typename": "Address"
},
"__typename": "Customer",
"serviceOrganisation": {
"name": "Service Frankreich",
"id": "89d2173a-2f55-4040-bb04-a063c7b89c80",
"__typename": "ServiceOrganisation"
}
}
},
"extensions": {
"traceId": "cbcbde5ef7e9b68b06b5b0a251dca7cb"
}
}

{
"operationName": "serviceOrganisations",
"variables": {},
"query": "query serviceOrganisations {\n  serviceOrganisations {\n    id\n    name\n    followTheSun {\n      providesFollowTheSunSupport\n      isCurrentlyInSchedule\n      schedule {\n        startTime\n        endTime\n        dayOfWeek\n        __typename\n      }\n      zoneId\n      dispatcher {\n        id\n        name\n        __typename\n      }\n      serviceOrganisationBlacklist {\n        id\n        name\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n}"
}

{
"data": {
"serviceOrganisations": [
{
"id": "0a7c99c6-7fcd-412c-8acf-be9d790ff87f",
"name": "Unconnected Training",
"followTheSun": {
"providesFollowTheSunSupport": false,
"isCurrentlyInSchedule": true,
"schedule": [],
"zoneId": "Europe/Berlin",
"dispatcher": [],
"serviceOrganisationBlacklist": [],
"__typename": "FollowTheSun"
},
"__typename": "ServiceOrganisation"
},
{
"id": "13f68400-8639-4866-afca-5f8f5b72dd2a",
"name": "Lyone Assistenza tecnica",
"followTheSun": {
"providesFollowTheSunSupport": true,
"isCurrentlyInSchedule": true,
"schedule": [],
"zoneId": "Europe/Rome",
"dispatcher": [
{
"id": "78d66acb-2900-49ac-b668-0fa580a3aa0d",
"name": "Bernd Bertram",
"__typename": "TenantUser"
}
],
"serviceOrganisationBlacklist": [
{
"id": "8750e2b3-7b40-40ed-b83c-7df0d29bc966",
"name": "Service Sud America",
"__typename": "ServiceOrganisation"
}
],
"__typename": "FollowTheSun"
},
"__typename": "ServiceOrganisation"
},
{
"id": "1aca771f-9ebc-493c-b76a-7f19a0345ad0",
"name": "Service Italien",
"followTheSun": {
"providesFollowTheSunSupport": true,
"isCurrentlyInSchedule": true,
"schedule": [
{
"startTime": "08:00:00",
"endTime": "17:00:00",
"dayOfWeek": 1,
"__typename": "ServiceSchedule"
},
{
"startTime": "00:00:00",
"endTime": "00:05:00",
"dayOfWeek": 7,
"__typename": "ServiceSchedule"
},
{
"startTime": "08:00:00",
"endTime": "17:00:00",
"dayOfWeek": 4,
"__typename": "ServiceSchedule"
},
{
"startTime": "08:00:00",
"endTime": "17:00:00",
"dayOfWeek": 2,
"__typename": "ServiceSchedule"
},
{
"startTime": "08:00:00",
"endTime": "17:00:00",
"dayOfWeek": 6,
"__typename": "ServiceSchedule"
},
{
"startTime": "08:00:00",
"endTime": "17:00:00",
"dayOfWeek": 5,
"__typename": "ServiceSchedule"
},
{
"startTime": "08:00:00",
"endTime": "14:00:00",
"dayOfWeek": 3,
"__typename": "ServiceSchedule"
}
],
"zoneId": "Europe/Rome",
"dispatcher": [
{
"id": "9ac93f6a-0ab5-4446-9373-53e90116a032",
"name": "Unknown user",
"__typename": "TenantUser"
}
],
"serviceOrganisationBlacklist": [],
"__typename": "FollowTheSun"
},
"__typename": "ServiceOrganisation"
},
{
"id": "44612ba1-7e99-486f-9c22-f881721d45d0",
"name": "Hawk Asset Solutions Service Org",
"followTheSun": null,
"__typename": "ServiceOrganisation"
},
{
"id": "6facf52e-91fd-4b80-94d7-6f57742e82f4",
"name": "Service Deutschland",
"followTheSun": {
"providesFollowTheSunSupport": false,
"isCurrentlyInSchedule": true,
"schedule": [],
"zoneId": "Europe/Berlin",
"dispatcher": [],
"serviceOrganisationBlacklist": [],
"__typename": "FollowTheSun"
},
"__typename": "ServiceOrganisation"
},
{
"id": "8750e2b3-7b40-40ed-b83c-7df0d29bc966",
"name": "Service Sud America",
"followTheSun": {
"providesFollowTheSunSupport": true,
"isCurrentlyInSchedule": true,
"schedule": [],
"zoneId": "Europe/Rome",
"dispatcher": [],
"serviceOrganisationBlacklist": [],
"__typename": "FollowTheSun"
},
"__typename": "ServiceOrganisation"
},
{
"id": "89d2173a-2f55-4040-bb04-a063c7b89c80",
"name": "Service Frankreich",
"followTheSun": null,
"__typename": "ServiceOrganisation"
},
{
"id": "a12c7f9a-d3f8-4019-a1a7-8b3d8fe83a92",
"name": "Service Europa",
"followTheSun": {
"providesFollowTheSunSupport": true,
"isCurrentlyInSchedule": true,
"schedule": [],
"zoneId": "Europe/Berlin",
"dispatcher": [
{
"id": "78d66acb-2900-49ac-b668-0fa580a3aa0d",
"name": "Bernd Bertram",
"__typename": "TenantUser"
}
],
"serviceOrganisationBlacklist": [],
"__typename": "FollowTheSun"
},
"__typename": "ServiceOrganisation"
},
{
"id": "a7c6d5ca-4acc-4a04-b8fe-0851519a33ab",
"name": "Epta France",
"followTheSun": {
"providesFollowTheSunSupport": true,
"isCurrentlyInSchedule": true,
"schedule": [],
"zoneId": "Europe/Rome",
"dispatcher": [],
"serviceOrganisationBlacklist": [],
"__typename": "FollowTheSun"
},
"__typename": "ServiceOrganisation"
},
{
"id": "bc9968b8-8c2f-4913-98fd-b233f354198e",
"name": "TechCorp",
"followTheSun": null,
"__typename": "ServiceOrganisation"
},
{
"id": "d22289fd-3822-438b-b9d1-5e675403b165",
"name": "Arktis",
"followTheSun": {
"providesFollowTheSunSupport": true,
"isCurrentlyInSchedule": true,
"schedule": [],
"zoneId": "Europe/Berlin",
"dispatcher": [
{
"id": "1abe70e0-6029-4c65-9062-89848c1bd8d1",
"name": "Fre Zess",
"__typename": "TenantUser"
}
],
"serviceOrganisationBlacklist": [],
"__typename": "FollowTheSun"
},
"__typename": "ServiceOrganisation"
}
]
},
"extensions": {
"traceId": "5d6d48c0ad64d9ae17e00ace1ccbc79c"
}
}

{
"operationName": "tableUsers",
"variables": {
"name": true,
"email": true,
"roles": true,
"status": true
},
"query": "query tableUsers($status: Boolean!, $name: Boolean!, $email: Boolean!, $roles: Boolean!) {\n  usersPaginated {\n    data {\n      id\n      identityId\n      name @include(if: $name)\n      email @include(if: $email)\n      isTechnicalUser\n      isActive\n      userInvitation @include(if: $status) {\n        url\n        expiresOn\n        __typename\n      }\n      status @include(if: $status)\n      userRoles @include(if: $roles) {\n        userRole {\n          id\n          name\n          __typename\n        }\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n}"
}

{
"data": {
"usersPaginated": {
"data": [
{
"id": "09b9033d-4c23-472a-be21-a22d0e2e071a",
"identityId": null,
"name": "Steffen Schmidt",
"email": "schmidt@innosoftgmbh.onmicrosoft.com",
"isTechnicalUser": false,
"isActive": false,
"userInvitation": null,
"status": "INVITATION_EXPIRED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "0d273f1b-9886-4864-99b5-bbe045c44592",
"identityId": "35225ca6-7ca7-4371-bedb-ec09b31190c2",
"name": "Buelow Florian",
"email": "buelow@lps.ruhr-uni-bochum.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "14b53a38-6282-47bb-9157-7bac38720ad1",
"identityId": null,
"name": "Nina v. Bassewitz",
"email": "nina.von.bassewitz@soprasteria.com",
"isTechnicalUser": false,
"isActive": false,
"userInvitation": null,
"status": "INVITATION_EXPIRED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "1abe70e0-6029-4c65-9062-89848c1bd8d1",
"identityId": "7aeb85d5-f025-4d65-8ed6-15815a6fad1a",
"name": "Fre Zess",
"email": "Fre.Zess@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000003",
"name": "Machine Operator",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000061",
"name": "Service KPI Dashboard",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "20e6a956-b23b-457b-8804-5231a09923c5",
"identityId": "fdfdd81d-755d-4ca9-b93e-4693f305f2a9",
"name": "Martin, Ebel",
"email": "Martin.Ebel@isse.ruhr-uni-bochum.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "2946022e-9401-44ed-bb26-44233399b178",
"identityId": "74811d40-1d8f-4cd3-8e08-e5379a906575",
"name": "Michael H",
"email": "Michael.Half@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000061",
"name": "Service KPI Dashboard",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "3342f9be-8e22-4b28-8914-050643be3413",
"identityId": "70ea2f87-75be-47f5-9d37-85834e9bd013",
"name": "SadiyeSZess",
"email": "SadiyeSZess@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000002",
"name": "Workshop Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "366f1489-bf4c-44a0-aeb4-8a676a78ebce",
"identityId": "6e05735c-473c-41cf-84e4-ba651ca93c22",
"name": "Nikolai Falke",
"email": "falke+zess@symmedia.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000003",
"name": "Machine Operator",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000063",
"name": "AI Assistant",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000002",
"name": "Workshop Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000061",
"name": "Service KPI Dashboard",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000047",
"name": "App Developer",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "3ed76aa1-c2d0-49c7-bc06-19c0dc892042",
"identityId": "66fa5a10-30e6-4f6f-932e-14ce6e8aa597",
"name": "Juergen RZESS",
"email": "JuergenRZESS@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "407f999b-c030-4024-a3ef-7d36e9a83164",
"identityId": "25595b7f-9a2d-4303-b378-dc921220d90a",
"name": "Ansgar Donner",
"email": "AnsgarD_Zess@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "41a3b232-0152-4470-8850-7b5adb220872",
"identityId": "7dd001b9-ab87-4e17-8f9b-78ea7f626bbe",
"name": "Kay Andorf",
"email": "kay.zess@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000047",
"name": "App Developer",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "42db06df-eda4-4b69-aaf0-66a52fda4f27",
"identityId": "28032e77-5ef1-4a60-89cb-add61cadb17d",
"name": "Robert Sueggel",
"email": "robert.sueggel@soprasteria.com",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "4642daec-f75b-48b4-8107-98f320bdf16b",
"identityId": "eb8405d4-c090-4d45-8c2f-c247a33a2a54",
"name": "Torsten Stanienda",
"email": "torsten.stanienda@soprasteria.com",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": null,
"__typename": "User"
},
{
"id": "4d45fffb-a34e-43cb-bdc3-3a30c2cb0282",
"identityId": "901d61f1-58b9-4ab9-9a25-fb54cdd9f691",
"name": "Niklas ServiceP",
"email": "NiklasServiceP@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "4e679c04-4840-493e-8089-f10e32c29e7a",
"identityId": null,
"name": "Markus Kwasny",
"email": "Kwasny@lps.ruhr-uni-bochum.de",
"isTechnicalUser": false,
"isActive": false,
"userInvitation": null,
"status": "INVITATION_EXPIRED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "536f728f-c3b5-426e-9faa-fa855729832b",
"identityId": "da1c2dea-1012-4298-af04-dc2f7dc89559",
"name": "Inga H",
"email": "ihockenbring@d-ootb.com",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000061",
"name": "Service KPI Dashboard",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "57d93dc3-f51a-4127-bcd4-f0ffe722d4e7",
"identityId": "e635a964-8964-4b9d-8e42-b803bca69f75",
"name": "Peter Beckerle",
"email": "peter.beckerle@soprasteria.com",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "58eb5220-55f4-4189-8c20-29afa062101a",
"identityId": "65318139-6ee6-4c1e-915f-23425345cc40",
"name": "FrezSer",
"email": "Frezservice@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "5a1aacd7-74c3-488a-a265-069edf35d6af",
"identityId": "09bffe45-99c5-4b24-b9b6-7ae6d65c5e9f",
"name": "Sebastian Schult",
"email": "schult@innosoftgmbh.onmicrosoft.com",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "5d031298-8211-40dc-afd2-5257f1cdaed8",
"identityId": "042f84a6-1620-489c-8b63-809cb8dd2043",
"name": "Quanos Support",
"email": "quanosSymmediaSsh@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "618502df-3b96-4398-99f6-0e5ea98a2558",
"identityId": null,
"name": "Marius, Knott",
"email": "symmedia@lps.ruhr-uni-bochum.de",
"isTechnicalUser": false,
"isActive": false,
"userInvitation": null,
"status": "INVITATION_EXPIRED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "631ff2e4-f30b-4728-8a36-c5ccdf40d0fb",
"identityId": "40283930-1015-4d16-b896-6a9e4a2bb6ae",
"name": "Vanessa H",
"email": "Vanessa_H_Zess@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "6e03d43d-e5f8-44bc-b660-43ec5cdc5954",
"identityId": null,
"name": "Robert Hellweg",
"email": "hellweg@innosoftgmbh.onmicrosoftm.com",
"isTechnicalUser": false,
"isActive": false,
"userInvitation": null,
"status": "INVITATION_EXPIRED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "724f030f-9e4b-4e69-8247-bded97c9d463",
"identityId": "d255d46c-265b-44c0-8f2c-2d18c54be1b5",
"name": "Michael.Schn.ZESS",
"email": "Michael.Schn.ZESS@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "78d66acb-2900-49ac-b668-0fa580a3aa0d",
"identityId": "aed8b16f-5fa7-45ba-a2f8-26372b6ecd5c",
"name": "Bernd Bertram",
"email": "SSH-ZESS@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000061",
"name": "Service KPI Dashboard",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "7acc10cd-3637-4672-851f-b142494a3b71",
"identityId": null,
"name": "Hans Walter Zimmermann",
"email": "zimmermann@innosoftgmbh.onmicrosoft.com",
"isTechnicalUser": false,
"isActive": false,
"userInvitation": null,
"status": "INVITATION_EXPIRED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "7f02aadf-07ea-4466-be9a-cdb28a40f50d",
"identityId": "1a9942d9-22c1-4f15-8026-e6831bdc90ea",
"name": "Merten Z.",
"email": "m.zess@outlook.com",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000003",
"name": "Machine Operator",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000002",
"name": "Workshop Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000061",
"name": "Service KPI Dashboard",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "814c64b9-e791-456f-900a-0a98dc9e34c7",
"identityId": "161bc2c5-88d4-4527-8658-664e1b2044e0",
"name": "ZESS Technical Salesforce User",
"email": "zess-technical-salesforce-user@secure-service-hub.de",
"isTechnicalUser": true,
"isActive": true,
"userInvitation": null,
"status": "INVITATION_EXPIRED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "878ce764-ea0b-485b-8241-ab01c01d699c",
"identityId": "67a21bc7-bbb0-4c5e-b067-01200f013326",
"name": "Andreas Thal Zess",
"email": "A.Thal.Zess@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000061",
"name": "Service KPI Dashboard",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "8a57a2b4-bac1-4ad0-b0c1-7c0b4ee35541",
"identityId": "e79eaa62-4beb-4c88-9ab7-691765c08cfd",
"name": "Martin W",
"email": "mwilderm@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "8c2e859a-9435-4435-8cf3-336a9c875bd2",
"identityId": "4f487a40-e92e-4ba0-b977-230ccfef4b73",
"name": "Alex A",
"email": "Alexander_A_Zess@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000061",
"name": "Service KPI Dashboard",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "9205d06e-02fa-4868-afc8-4ee3f1620f3a",
"identityId": "e8a842fc-3a39-4717-ae0b-3a96ea75975c",
"name": "Thomas HErmann",
"email": "thomas.hermer@soprasteria.com",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "9b2c6d35-0369-41c8-8d37-e3b72c93d8a8",
"identityId": "21c1ba53-8608-4cc5-b6f8-d226e9fd0322",
"name": "Hub Talk",
"email": "falke+zessbot@symmedia.de",
"isTechnicalUser": true,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000047",
"name": "App Developer",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "a27478b9-f55d-475f-a61f-fdd66eb8f2b4",
"identityId": "f334affd-52b2-45c3-ac71-e4de6757aae6",
"name": "Christian Behnert",
"email": "christian.behnert@soprasteria.com",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "a2b40570-8843-4082-a539-20e2142a592d",
"identityId": "cee08451-b10a-49be-93f6-067c540e07a5",
"name": "Eugen Zess",
"email": "Eugen.ZESS@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000061",
"name": "Service KPI Dashboard",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "c0023811-6940-4ced-91d7-fcf7d2cb30bf",
"identityId": "a4d3dac1-c4d8-449c-b193-cd5693fc0bfc",
"name": "Luis.Kress.ZESS",
"email": "Luis.Kress.ZESS@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "c54af9b2-39b5-4033-ae0c-9e8169b0b190",
"identityId": "6c598c56-2cc0-46bb-ace3-c989f50ff337",
"name": "Oliver Kollodzieski",
"email": "Oliver.Kollodzieski@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "c71ae768-741d-4d24-b6b2-b5d34efe5515",
"identityId": "20d33dff-afa0-4742-9c53-55f8b734d9c7",
"name": "Robin Haberer - Zess Service Provider",
"email": "sshdemozesshaberer@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000063",
"name": "AI Assistant",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000061",
"name": "Service KPI Dashboard",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000047",
"name": "App Developer",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "cbe2ebdd-9dd8-4a39-8863-f6aedf45964b",
"identityId": "9d4281de-f77d-49b4-a8f5-f9137ac2d628",
"name": "Nadja S",
"email": "Nadja_S_Zess@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "d074b313-fee4-44bd-8af0-4d733e7756e5",
"identityId": "b2fbc886-839b-40c2-a209-d981f34057d0",
"name": "Tim Schmidt",
"email": "tim.schmidt@soprasteria.com",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "e4472649-a440-4ae1-a62f-ce2999b649eb",
"identityId": null,
"name": "Alexander Oleksow",
"email": "oleksow@innosoftgmbh.onmicrosoft.com",
"isTechnicalUser": false,
"isActive": false,
"userInvitation": null,
"status": "INVITATION_EXPIRED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "ea6425b2-e0ab-4080-bbd2-c4c2aefbb9ae",
"identityId": "a3573858-2800-4d0c-8bce-c7f41ecf0a45",
"name": "Marius B",
"email": "Marius_B_Zess@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000061",
"name": "Service KPI Dashboard",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "ee250ffa-de7a-49f9-9f8a-5811ac3f44c4",
"identityId": "54d5098b-21e9-454c-8752-29d63cf48c49",
"name": "Michael Herzog",
"email": "herzog@lps.ruhr-uni-bochum.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
},
{
"id": "f2e97cae-b470-40d0-9846-ce1b3b82c036",
"identityId": "a16c982e-0fc8-467b-9df8-48fd35b9f29c",
"name": "Hendrik B Zess",
"email": "Hendrik_B_Zess@outlook.de",
"isTechnicalUser": false,
"isActive": true,
"userInvitation": null,
"status": "ONBOARDED",
"userRoles": [
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000061",
"name": "Service KPI Dashboard",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000001",
"name": "Tenant Admin",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000030",
"name": "Service Technician",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000027",
"name": "Master Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000026",
"name": "Customer Data Manager",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000036",
"name": "Quanos Catalog",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000029",
"name": "1st Level Support",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
},
{
"userRole": {
"id": "00000000-0000-0000-3333-000000000049",
"name": "ZESS Innosoft Field Service Management",
"__typename": "UserRole"
},
"__typename": "AssignedUserRole"
}
],
"__typename": "User"
}
],
"__typename": "UserQueryResult"
}
},
"extensions": {
"traceId": "363d17fbbeb3a5ed0df187e93e751a34"
}
}