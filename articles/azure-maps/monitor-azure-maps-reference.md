---
title: Monitoring Azure Maps data reference #Required; *your official service name*  
description: Important reference material needed when you monitor Azure Maps 
author: john-janea #Required; your GitHub user alias, with correct capitalization.
ms.topic: how-to
ms.author: #Required; Microsoft alias of author; optional team alias.
ms.service: azure-maps #Required; service you are monitoring
ms.custom: subject-monitoring
ms.date: 04/27/2021 #Required; mm/dd/yyyy format.
---
<!-- VERSION 2.3
Template for monitoring data reference article for Azure services. This article is support for the main "Monitoring Azure Maps" article for the service. -->

<!-- IMPORTANT STEP 1.  Do a search and replace of Azure Maps with the name of your service. That will make the template easier to read -->

# Monitoring Azure Maps data reference

See [Monitoring Azure Maps](monitor-azure-maps.md) for details on collecting and analyzing monitoring data for Azure Maps.

## Metrics

<!-- REQUIRED if you support Metrics. If you don't, keep the section but call that out. Some services are only onboarded to logs.
<!-- Please keep headings in this order -->

<!-- 2 options here depending on the level of extra content you have. -->

<!--------------**OPTION 1 EXAMPLE** ------------------- -->

<!-- OPTION 1 - Minimum -  Link to relevant bookmarks in https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported, which is auto generated from underlying systems.  Not all metrics are published depending on whether your product group wants them to be.  If the metric is published, but descriptions are wrong of missing, contact your PM and tell them to update them  in the Azure Monitor "shoebox" manifest.  If this article is missing metrics that you and the PM know are available, both of you contact azmondocs@microsoft.com.  
-->

<!-- Example format. There should be AT LEAST one Resource Provider/Resource Type here. -->

This section lists all the automatically collected platform metrics collected for Azure Maps.  

<!--|Metric Type | Resource Provider / Type Namespace<br/> and link to individual metrics |
|-------|-----|
| Virtual Machine | [Microsoft.Compute/virtualMachine](/azure/azure-monitor/platform/metrics-supported#microsoftcomputevirtualmachines) |
| Virtual machine scale set | [Microsoft.Compute/virtualMachinescaleset](/azure/azure-monitor/platform/metrics-supported#microsoftcomputevirtualmachinescaleset) --> 



<!--------------**OPTION 2 EXAMPLE** ----------- -->

<!--  OPTION 2 -  Link to the metrics as above, but work in extra information not found in the automated metric-supported reference article.  NOTE: YOU WILL NOW HAVE TO MANUALLY MAINTAIN THIS SECTION to make sure it stays in sync with the metrics-supported link. For highly customized example, see [CosmosDB](https://docs.microsoft.com/azure/cosmos-db/monitor-cosmos-db-reference#metrics). They even regroup the metrics into usage type vs. resource provider and type.
-->

<!-- Example format. Mimic the setup of metrics supported, but add extra information -->

### Availability Metrics

<!-- Resource Provider and Type: [Microsoft.Compute/virtualMachines](/azure/azure-monitor/platform/metrics-supported#microsoftcomputevirtualmachines) -->

|Metric (Metric Display Name)|Unit (Aggregation Type) |Description|Dimensions| Time granularities| Legacy metric mapping | Usage |
|---|---|---|---| ---| ---| ---|
| Availability (Availability) | Percent (Avg, Percentile) | Availability of the APIs| ApiName, ApiCategory| All | N/A | Used to monitor availability per API |


### Usage Metrics

<!-- Namespace- [Microsoft.Compute/virtualMachinesscaleset](/azure/azure-monitor/platform/metrics-supported#microsoftcomputevirtualmachinescalesets) -->

|Metric (Metric Display Name)|Unit (Aggregation Type) |Description|Dimensions| Time granularities| Legacy metric mapping | Usage |
|---|---|---|---| ---| ---| ---|
| Usage (Usage) | Count | Count of API calls | ApiName, ApiCategory, ResultType, ResponseCode| All | N/A | Used to monitor availability per API |

<!-- ### Storage Consumption Metrics

|Metric (Metric Display Name)|Unit (Aggregation Type) |Description|Dimensions| Time granularities| Legacy metric mapping | Usage |
|---|---|---|---| ---| ---| ---|
| MBytesConsumed (MBytesConsumed) | MB (Total) | Storage consumption for Creator services | ResourceId, CreatorResourceName, CreatorServiceName| All | N/A | Used to monitor the storage consumption per Creator Service API |-->

<!-- ### Transaction metrics

|Metric (Metric Display Name)|Unit (Aggregation Type) |Description|Dimensions| Time granularities| Legacy metric mapping | Usage |
|---|---|---|---| ---| ---| ---|
| Transactions (Transactions) | Count | Count of total transactions calls | ApiName, ApiCategory, ResultType, ResponseCode| All | N/A | Used to monitor the total number of requests per API |-->

<!-- ### Failure metrics

|Metric (Metric Display Name)|Unit (Aggregation Type) |Description|Dimensions| Time granularities| Legacy metric mapping | Usage |
|---|---|---|---| ---| ---| ---|
| FailedRequests (Failed Requests) | Count | Count of failed API calls | ApiName, ApiCategory, ResponseCode| All | N/A | Used to monitor the failures per API | -->

<!-- Add additional explanation of reference information as needed here. Link to other articles such as your Monitor Azure Maps article as appropriate. -->

<!-- Keep this text as-is -->
For more information, see a list of [all platform metrics supported in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported).



## Metric Dimensions

<!-- REQUIRED. Please  keep headings in this order -->
<!-- If you have metrics with dimensions, outline it here. If you have no dimensions, say so.  Questions email azmondocs@microsoft.com -->

Azure Maps does not have any metrics that contain dimensions.

For more information on what metric dimensions are, see [Multi-dimensional metrics](/azure/azure-monitor/platform/data-platform-metrics#multi-dimensional-metrics).

<!--*OR*

Azure Maps has the following dimensions associated with its metrics. -->

<!-- See https://docs.microsoft.com/azure/storage/common/monitor-storage-reference#metrics-dimensions for an example. Part is copied below. -->

<!-- **--------------EXAMPLE format when you have dimensions------------------**

Azure Storage supports following dimensions for metrics in Azure Monitor.

| Dimension Name | Description |
| ------------------- | ----------------- |
| **BlobType** | The type of blob for Blob metrics only. The supported values are **BlockBlob**, **PageBlob**, and **Azure Data Lake Storage**. Append blobs are included in **BlockBlob**. |
| **BlobTier** | Azure storage offers different access tiers, which allow you to store blob object data in the most cost-effective manner. See more in [Azure Storage blob tier](/azure/storage/blobs/storage-blob-storage-tiers). The supported values include: <br/> <li>**Hot**: Hot tier</li> <li>**Cool**: Cool tier</li> <li>**Archive**: Archive tier</li> <li>**Premium**: Premium tier for block blob</li> <li>**P4/P6/P10/P15/P20/P30/P40/P50/P60**: Tier types for premium page blob</li> <li>**Standard**: Tier type for standard page Blob</li> <li>**Untiered**: Tier type for general purpose v1 storage account</li> |
| **GeoType** | Transaction from Primary or Secondary cluster. The available values include **Primary** and **Secondary**. It applies to Read Access Geo Redundant Storage(RA-GRS) when reading objects from secondary tenant. | -->

## Resource logs
<!-- REQUIRED. Please  keep headings in this order -->

This section lists the types of resource logs you can collect for Azure Maps. 

<!-- List all the resource log types you can have and what they are for -->  

For reference, see a list of [all resource logs category types supported in Azure Monitor](/azure/azure-monitor/platform/resource-logs-schema).


| Name | Required | Description |
| --- | --- | --- |
| **time** | Yes | The timestamp (UTC) of the event. |
| **resourceId** | Yes | The resource ID of the resource that emitted the event. For tenant services, this is of the form /tenants/tenant-id/providers/provider-name.|
| **category** | Yes | The log category of the event. Category is the granularity at which you can enable or disable logs on a particular resource. The properties that appear within the properties blob of an event are the same within a particular log category and resource type. Typical log categories are "Audit" "Operational" "Execution" and "Request."  |
| **operationName** | Yes | The name of the operation represented by this event. If the event represents an Azure RBAC operation, this is the Azure RBAC operation name (for example, Microsoft.Storage/storageAccounts/blobServices/blobs/Read). Typically modeled in the form of a Resource Manager operation, even if they are not actual documented Resource Manager operations (Microsoft.<providerName>/<resourceType>/<subtype>/<Write/Read/Delete/Action>)    |
| **uri** | No | URI for the request if applicable. |
| **operationVersion** | No | The api-version associated with the operation, if the operationName was performed using an API (for example, http://myservice.windowsazure.net/object?api-version=2016-06-01). If there is no API that corresponds to this operation, the version represents the version of that operation in case the properties associated with the operation change in the future.|
| **operationDescription** | No | The static text description of this operation, for example "Get storage file." |
| **resultType** | No | The status of the event. Typical values include Started, In Progress, Succeeded, Failed, Active, and Resolved. |
| **resultSignature (statusCode)** | No | The sub status of the event. If this operation corresponds to a REST API call, this field is the HTTP status code of the corresponding REST call – for example: 400 Bad Request. |
| **resultDescription** | No | The static text description of the result. For example: “One or more parameters missing”, “Storage quota exceeded”.|
| **durationMs** | No | The duration of the operation in milliseconds.  |
| **callerIpAddress** | No | The caller IP address, if the operation corresponds to an API call that would come from an entity with a publicly available IP address.   |
| **correlationId** | No | A GUID used to group together a set of related events. Typically, if two events have the same operationName but two different statuses (for example "Started" and "Succeeded"), they share the same correlation ID. This may also represent other relationships between events. |
| **identity** | No | A JSON blob that describes the identity of the user or application that performed the operation. Typically, this field includes the authorization and claims / JWT token from active directory.|
| **Level** | No | The severity level of the event. Must be one of Informational, Warning, Error, or Critical.  |
| **location** | No | The region of the resource emitting the event, for example "East US" or "France South".
| **properties** | No | <br> "properties": {<br>"accountName": "testaccount1",<br> "requestUrl": "",<br> "requestHeader": "",<br> "etag": "",<br> "requestHeaderSize": 2658,<br>"requestBodySize": 0,<br>"responseHeaderSize": 295,<br>"responseBodySize": 2018<br> } |


<!-- ------------**OPTION 1 EXAMPLE** --------------------- -->

<!-- OPTION 1 - Minimum -  Link to relevant bookmarks in https://docs.microsoft.com/azure/azure-monitor/platform/resource-logs-categories, which is auto generated from the REST API.  Not all resource log types metrics are published depending on whether your product group wants them to be.  If the resource log is published, but category display names are wrong or missing, contact your PM and tell them to update them in the Azure Monitor "shoebox" manifest.  If this article is missing resource logs that you and the PM know are available, both of you contact azmondocs@microsoft.com.  
-->

<!-- Example format. There should be AT LEAST one Resource Provider/Resource Type here. -->

<!-- This section lists all the resource log category types collected for Azure Maps.  

|Resource Log Type | Resource Provider / Type Namespace<br/> and link to individual metrics |
|-------|-----|
| Web Sites | [Microsoft.web/sites](/azure/azure-monitor/platform/resource-logs-categories#microsoftwebsites) |
| Web Site Slots | [Microsoft.web/sites/slots](/azure/azure-monitor/platform/resource-logs-categories#microsoftwebsitesslots) -->

<!-- --------------**OPTION 2 EXAMPLE** ------------- -->

<!--  OPTION 2 -  Link to the resource logs as above, but work in extra information not found in the automated metric-supported reference article.  NOTE: YOU WILL NOW HAVE TO MANUALLY MAINTAIN THIS SECTION to make sure it stays in sync with the resource-log-categories link. You can group these sections however you want provided you include the proper links back to resource-log-categories article. 
-->

<!-- Example format. Add extra information -->

<!-- ### Web Sites

Resource Provider and Type: [Microsoft.web/sites](/azure/azure-monitor/platform/resource-logs-categories#microsoftwebsites)

| Category | Display Name | *TODO replace this label with other information*  |
|:---------|:-------------|------------------|
| AppServiceAppLogs   | App Service Application Logs | *TODO other important information about this type* |
| AppServiceAuditLogs | Access Audit Logs            | *TODO other important information about this type* |
|  etc.               |                              |                                                   |  

### Web Site Slots

Resource Provider and Type: [Microsoft.web/sites/slots](/azure/azure-monitor/platform/resource-logs-categories#microsoftwebsitesslots)

| Category | Display Name | *TODO replace this label with other information*  |
|:---------|:-------------|------------------|
| AppServiceAppLogs   | App Service Application Logs | *TODO other important information about this type* |
| AppServiceAuditLogs | Access Audit Logs            | *TODO other important information about this type* |
|  etc.               |                              |                                                   |  

--------------**END Examples** ------------- -->

<!-- ## Azure Monitor Logs tables
<!-- REQUIRED. Please keep heading in this order -->

<!-- This section refers to all of the Azure Monitor Logs Kusto tables relevant to Azure Maps and available for query by Log Analytics.

------------**OPTION 1 EXAMPLE** ---------------------

<!-- OPTION 1 - Minimum -  Link to relevant bookmarks in https://docs.microsoft.com/azure/azure-monitor/reference/tables/tables-resourcetype where your service tables are listed. These files are auto generated from the REST API.   If this article is missing tables that you and the PM know are available, both of you contact azmondocs@microsoft.com.  
-->

<!-- Example format. There should be AT LEAST one Resource Provider/Resource Type here. -->

<!--|Resource Type | Notes |
|-------|-----|
| [Virtual Machines](/azure/azure-monitor/reference/tables/tables-resourcetype#virtual-machines) | |
| [Virtual machine scale sets](/azure/azure-monitor/reference/tables/tables-resourcetype#virtual-machine-scale-sets) | |

--------------**OPTION 2 EXAMPLE** -------------

<!--  OPTION 2 -  List out your tables adding additional information on what each table is for. Individually link to each table using the table name.  For example, link to [AzureMetrics](https://docs.microsoft.com/azure/azure-monitor/reference/tables/azuremetrics).  

NOTE: YOU WILL NOW HAVE TO MANUALLY MAINTAIN THIS SECTION to make sure it stays in sync with the automatically generated list. You can group these sections however you want provided you include the proper links back to the proper tables. 
-->

<!-- ### Virtual Machines

| Table |  Description | *TODO replace this label with proper title for your additional information*  |
|:---------|:-------------|------------------|
| [AzureActivity](/azure/azure-monitor/reference/tables/azureactivity)   | <!-- description copied from previous link --Entries from the Azure Activity log that provides insight into any subscription-level or management group level events that have occurred in Azure. | *TODO other important information about this type |
| [AzureMetrics](/azure/azure-monitor/reference/tables/azuremetrics) | <!-- description copied from previous link Metric data emitted by Azure services that measure their health and performance.    | *TODO other important information about this type |
|  etc.               |                              |                                                   |  

### Virtual Machine Scale Sets

| Table |  Description | *TODO replace this label with other information*  |
|:---------|:-------------|------------------|
| [ADAssessmentRecommendation](/azure/azure-monitor/reference/tables/adassessmentrecommendation)   | <!-- description copied from previous link  Recommendations generated by AD assessments that are started through a scheduled task. When you schedule the assessment it runs by default every 7 days and upload the data into Azure Log Analytics | *TODO other important information about this type |
| [ADReplicationResult](/azure/azure-monitor/reference/tables/adreplicationresult) | <!-- description copied from previous link -The AD Replication Status solution regularly monitors your Active Directory environment for any replication failures.    | *TODO other important information about this type |
|  etc.               |                              |                                                   |  

<!-- Add extra information if required -->

<!-- For a reference of all Azure Monitor Logs / Log Analytics tables, see the [Azure Monitor Log Table Reference](/azure/azure-monitor/reference/tables/tables-resourcetype).

--------------**END EXAMPLES** -------------

### Diagnostics tables
<!-- REQUIRED. Please keep heading in this order -->
<!-- If your service uses the AzureDiagnostics table in Azure Monitor Logs / Log Analytics, list what fields you use and what they are for. Azure Diagnostics is over 500 columns wide with all services using the fields that are consistent across Azure Monitor and then adding extra ones just for themselves.  If it uses service specific diagnostic table, refers to that table. If it uses both, put both types of information in. Most services in the future will have their own specific table. If you have questions, contact azmondocs@microsoft.com -->

<!-- Azure Maps uses the [Azure Diagnostics](/azure/azure-monitor/reference/tables/azurediagnostics) table and the [TODO whatever additional] table to store resource log information. The following columns are relevant.

**Azure Diagnostics**

| Property | Description |
|:--- |:---|
|  |  |
|  |  |

**[TODO Service-specific table]**

| Property | Description |
|:--- |:---|
|  |  |
|  |  | -->

## Activity logs
<!-- REQUIRED. Please keep heading in this order -->


The following table lists the operations related to Azure Maps that may be created in the Activity log.

<!-- Fill in the table with the operations that can be created in the Activity log for the service. -->
| Name | Required | Description |
| --- | --- | --- |
| **operationName** | Yes | The name of the operation represented by this event. If the event represents an Azure RBAC operation, this is the Azure RBAC operation name (for example, Microsoft.Storage/storageAccounts/blobServices/blobs/Read). Typically modeled in the form of a Resource Manager operation, even if they are not actual documented Resource Manager operations (Microsoft.<providerName>/<resourceType>/<subtype>/<Write/Read/Delete/Action>)  |
| **resultType** | Yes | {<br> Success = 1,<br> ClientError = 2,<br> Failure = 3,<br> Timeout = 4<br> }   |
| **category** | Yes | {<br> Other = 0,<br> UserManagement = 1,<br> GroupManagement = 2,<br> Authentication = 3,<br> Authorization = 4,<br> RoleManagement = 5,<br> ApplicationManagement = 6,<br> KeyManagement = 7,<br> DirectoryManagement = 8,<br> ResourceManagement = 9,<br> PolicyManagement = 10,<br> DeviceManagement = 11,<br> EntitlementManagement = 12,<br> PasswordManagement = 13,<br> IdentityProtection = 14,<br> ObjectManagement = 15,<br> ProvisioningManagement = 16<br> }   |
| **targetResource** | Yes | Subscription Id<br> Resource Group Name<br> Maps Account<br> Private Atlas<br> Event Grid Filter<br>  |
| **callerIdentity** | Yes | {<br> UPN = 1,<br> PUID = 2,<br> ObjectID = 3,<br> Certificate = 4,<br> Claim = 5,<br> Username = 6,<br> KeyName = 7,<br> SubscriptionID = 8,<br> ApplicationID = 9<br> } | 
| **callerIpAddress** | No | The caller IP address, if the operation corresponds to an API call that would come from an entity with a publicly available IP address. |
| **requestId** | No | A GUID used to group together a set of related events. Typically, if two events have the same operationName but two different statuses (for example "Started" and "Succeeded"), they share the same correlation ID. This may also represent other relationships between events. |
| **resultDescription** | No | The static text description of the result. For example: "One or more parameters missing", "Storage quota exceeded". |

<!-- NOTE: This information may be hard to find or not listed anywhere.  Please ask your PM for at least an incomplete list of what type of messages could be written here. If you can't locate this, contact azmondocs@microsoft.com for help -->



For more information on the schema of Activity Log entries, see [Activity  Log schema](/azure/azure-monitor/essentials/activity-log-schema). 

<!--## Schemas
<!-- REQUIRED. Please keep heading in this order -->

<!--The following schemas are in use by Azure Maps

<!-- List the schema and their usage. This can be for resource logs, alerts, event hub formats, etc depending on what you think is important. -->

 

## See Also

<!-- replace below with the proper link to your main monitoring service article -->
- See [Monitoring Azure Maps](/monitor-azure-maps.md) for a description of monitoring Azure Azure Maps.
- See [Monitoring Azure resources with Azure Monitor](/azure/azure-monitor/essentials/monitor-azure-resources) for details on monitoring Azure resources.
