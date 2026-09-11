

# SsoTenant

An enterprise customer's SAML Identity Provider connection

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** | Model primary key |  [optional] |
|**createdAt** | **String** |  |  [optional] |
|**updatedAt** | **String** |  |  [optional] |
|**name** | **String** |  |  [optional] |
|**idpAlias** | **String** |  |  [optional] |
|**metadataUrl** | **String** |  |  [optional] |
|**entityId** | **String** |  |  [optional] |
|**metadataImportedAt** | **String** |  |  [optional] |
|**enabled** | **Boolean** |  |  [optional] |
|**spEntityId** | **String** | Keycloak&#39;s own SP entity ID - null until approved. Register this as the SAML Identifier on the customer&#39;s IdP. |  [optional] |
|**spAcsUrl** | **String** | Keycloak&#39;s ACS/reply URL for this tenant - null until approved. |  [optional] |
|**spMetadataUrl** | **String** | Downloadable SP metadata descriptor most IdPs can import directly - null until approved. |  [optional] |
|**status** | **String** | One of pending, approved, rejected |  [optional] |
|**submittedByUserId** | **Integer** | ID of the user who submitted this tenant for approval |  [optional] |
|**rejectedReason** | **String** | Reason given when status is rejected - null otherwise |  [optional] |



