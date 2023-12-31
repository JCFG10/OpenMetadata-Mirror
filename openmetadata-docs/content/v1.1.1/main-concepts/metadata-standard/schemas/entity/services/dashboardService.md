---
title: dashboardService
slug: /main-concepts/metadata-standard/schemas/entity/services/dashboardservice
---

# Dashboard Service

*This schema defines the Dashboard Service entity, such as Looker and Superset.*

## Properties

- **`id`**: Unique identifier of this dashboard service instance. Refer to *../../type/basic.json#/definitions/uuid*.
- **`name`**: Name that identifies this dashboard service. Refer to *../../type/basic.json#/definitions/entityName*.
- **`fullyQualifiedName`**: FullyQualifiedName same as `name`. Refer to *../../type/basic.json#/definitions/fullyQualifiedEntityName*.
- **`displayName`** *(string)*: Display Name that identifies this dashboard service.
- **`serviceType`**: Type of dashboard service such as Looker or Superset... Refer to *#/definitions/dashboardServiceType*.
- **`description`**: Description of a dashboard service instance. Refer to *../../type/basic.json#/definitions/markdown*.
- **`connection`**: Refer to *#/definitions/dashboardConnection*.
- **`pipelines`**: References to pipelines deployed for this dashboard service. Refer to *../../type/entityReferenceList.json#/definitions/entityReferenceList*.
- **`testConnectionResult`**: Last test connection results for this service. Refer to *connections/testConnectionResult.json*.
- **`tags`** *(array)*: Tags for this Dashboard Service. Default: `None`.
  - **Items**: Refer to *../../type/tagLabel.json*.
- **`owner`**: Owner of this dashboard service. Refer to *../../type/entityReference.json*.
- **`version`**: Metadata version of the entity. Refer to *../../type/entityHistory.json#/definitions/entityVersion*.
- **`updatedAt`**: Last update time corresponding to the new version of the entity in Unix epoch time milliseconds. Refer to *../../type/basic.json#/definitions/timestamp*.
- **`updatedBy`** *(string)*: User who made the update.
- **`href`**: Link to the resource corresponding to this dashboard service. Refer to *../../type/basic.json#/definitions/href*.
- **`changeDescription`**: Change that lead to this version of the entity. Refer to *../../type/entityHistory.json#/definitions/changeDescription*.
- **`deleted`** *(boolean)*: When `true` indicates the entity has been soft deleted. Default: `False`.
- **`domain`**: Domain the Dashboard service belongs to. Refer to *../../type/entityReference.json*.
## Definitions

- **`dashboardServiceType`** *(string)*: Type of Dashboard service - Superset, Looker, Redash, Tableau, Metabase, PowerBi or Mode. Must be one of: `['Superset', 'Looker', 'Tableau', 'Redash', 'Metabase', 'PowerBI', 'Mode', 'CustomDashboard', 'DomoDashboard', 'QuickSight']`.
- **`dashboardConnection`** *(object)*: Dashboard Connection. Cannot contain additional properties.
  - **`config`**


Documentation file automatically generated at 2023-07-07 05:50:35.981927.
