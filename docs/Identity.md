

# Identity

Model representing identity records

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** | Unique identifier for the identity record |  [optional] |
|**registryId** | **Integer** | ID of the registry associated with the identity record |  [optional] |
|**address1** | **String** | First line of the address |  [optional] |
|**address2** | **String** | Second line of the address |  [optional] |
|**town** | **String** | Town of the address |  [optional] |
|**county** | **String** | County of the address |  [optional] |
|**country** | **String** | Country of the address |  [optional] |
|**postcode** | **String** | Postcode of the address |  [optional] |
|**dob** | **LocalDate** | Date of birth |  [optional] |
|**idvtSuccess** | **Integer** | Indicates whether IDVT was successful (1 for success, 0 for failure) |  [optional] |
|**idvtIdentificationNumber** | **String** | Identification number from IDVT |  [optional] |
|**idvtDocumentType** | **String** | Type of document used for IDVT |  [optional] |
|**idvtDocumentNumber** | **String** | Document number used for IDVT |  [optional] |
|**idvtDocumentCountry** | **String** | Country of the document used for IDVT |  [optional] |
|**idvtDocumentValidUntil** | **LocalDate** | Validity date of the document used for IDVT |  [optional] |
|**idvtDocumentFirstName** | **String** | First name on the document used for IDVT |  [optional] |
|**idvtDocumentValidLastName** | **String** | Last name on the document used for IDVT |  [optional] |
|**idvtAttemptId** | **String** | ID of the IDVT attempt |  [optional] |
|**idvtContextId** | **String** | Context ID for IDVT |  [optional] |
|**idvtDocumentDob** | **LocalDate** | Date of birth on the document used for IDVT |  [optional] |
|**idvtContext** | **String** | Context of the IDVT process |  [optional] |
|**idvtCompletedAt** | **OffsetDateTime** | Timestamp when IDVT was completed |  [optional] |
|**idvtResultText** | **String** | Result text of the IDVT process |  [optional] |
|**idvtStartedAt** | **OffsetDateTime** | Timestamp when IDVT was started |  [optional] |
|**createdAt** | **OffsetDateTime** | Timestamp when the identity record was created |  [optional] |
|**updatedAt** | **OffsetDateTime** | Timestamp when the identity record was last updated |  [optional] |
|**deletedAt** | **OffsetDateTime** | Timestamp when the identity record was deleted |  [optional] |



