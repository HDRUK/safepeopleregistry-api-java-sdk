

# ValidationLog

Validation Log model

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** | Model primary key |  [optional] |
|**entityType** | **String** | Type of the primary entity associated with the validation log |  [optional] |
|**entityId** | **Integer** | ID of the primary entity associated with the validation log |  [optional] |
|**secondaryEntityType** | **String** | Type of the secondary entity associated with the validation log |  [optional] |
|**secondaryEntityId** | **Integer** | ID of the secondary entity associated with the validation log |  [optional] |
|**tertiaryEntityType** | **String** | Type of the tertiary entity associated with the validation log |  [optional] |
|**tertiaryEntityId** | **Integer** | ID of the tertiary entity associated with the validation log |  [optional] |
|**name** | **String** | Name of the validation log entry |  [optional] |
|**completedAt** | **OffsetDateTime** | Timestamp when the validation was completed (nullable) |  [optional] |
|**manuallyConfirmed** | **Boolean** | Whether the validation was manually confirmed |  [optional] |



