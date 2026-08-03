

# PendingInvite

Model representing pending invites

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** | Unique identifier for the pending invite |  [optional] |
|**userId** | **Integer** | ID of the user associated with the invite |  [optional] |
|**organisationId** | **Integer** | ID of the organisation associated with the invite |  [optional] |
|**status** | **String** | Status of the invite |  [optional] |
|**inviteAcceptedAt** | **OffsetDateTime** | Timestamp when the invite was accepted |  [optional] |
|**inviteSentAt** | **OffsetDateTime** | Timestamp when the invite was sent |  [optional] |
|**inviteCode** | **String** | Unique code for the invite |  [optional] |
|**createdAt** | **OffsetDateTime** | Timestamp when the invite record was created |  [optional] |
|**updatedAt** | **OffsetDateTime** | Timestamp when the invite record was last updated |  [optional] |



