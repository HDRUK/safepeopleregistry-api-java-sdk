

# Affiliation

Affiliation model

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** | Model primary key |  [optional] |
|**createdAt** | **String** |  |  [optional] |
|**updatedAt** | **String** |  |  [optional] |
|**organisationId** | **Integer** | Organisational link |  [optional] |
|**memberId** | **String** | Member ID UUID |  [optional] |
|**relationship** | **String** | Textual representation of affiliation relationship |  [optional] |
|**from** | **LocalDate** | Date affiliation commenced |  [optional] |
|**to** | **LocalDate** | Date affiliation ends (or ended). Null when there is no known end date |  [optional] |
|**endDateRecordedAt** | **OffsetDateTime** | When the end date was recorded |  [optional] |
|**endDateRecordedBy** | **Integer** | The user who recorded the end date |  [optional] |
|**endDateSource** | [**EndDateSourceEnum**](#EndDateSourceEnum) | Who recorded the end date. The organisation&#39;s date wins over the user&#39;s |  [optional] |
|**leftAt** | **OffsetDateTime** | When the leaver flow ran for this affiliation |  [optional] |
|**department** | **String** | Department worked during affiliation |  [optional] |
|**role** | **String** | Role held during affiliation |  [optional] |
|**email** | **String** | Professional email held during affiliation |  [optional] |
|**ror** | **String** | The ROR.org identifier for this affiliation institute |  [optional] |
|**registryId** | **Integer** | The Registry primary key associated with this affiliation |  [optional] |
|**currentEmployer** | **Boolean** | Flag indicating if affiliation is for the current employer |  [optional] |
|**verificationCode** | **String** | Unique verification code issued for confirmation |  [optional] |
|**verificationSentAt** | **OffsetDateTime** | Timestamp when verification code was sent |  [optional] |
|**verificationConfirmedAt** | **OffsetDateTime** | Timestamp when verification was confirmed |  [optional] |
|**isVerified** | **Boolean** | Flag indicating if affiliation is verified |  [optional] |



## Enum: EndDateSourceEnum

| Name | Value |
|---- | -----|
| USER | &quot;user&quot; |
| ORGANISATION | &quot;organisation&quot; |



