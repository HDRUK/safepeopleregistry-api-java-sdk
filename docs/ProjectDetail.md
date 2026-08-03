

# ProjectDetail

ProjectDetail model

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** | Model primary key |  [optional] |
|**createdAt** | **String** |  |  [optional] |
|**updatedAt** | **String** |  |  [optional] |
|**projectId** | **Integer** | Primary key of associated Project for this ProjectDetail |  [optional] |
|**datasets** | **List&lt;String&gt;** |  |  [optional] |
|**otherApprovalCommittees** | **List&lt;String&gt;** |  |  [optional] |
|**dataSensitivityLevel** | **String** |  |  [optional] |
|**legalBasisForDataArticle6** | **String** |  |  [optional] |
|**dutyOfConfidentiality** | **Boolean** |  |  [optional] |
|**nationalDataOptout** | **Boolean** |  |  [optional] |
|**requestFrequency** | [**RequestFrequencyEnum**](#RequestFrequencyEnum) |  |  [optional] |
|**datasetLinkageDescription** | **String** |  |  [optional] |
|**dataMinimisation** | **String** |  |  [optional] |
|**dataUseDescription** | **String** |  |  [optional] |
|**accessDate** | **String** |  |  [optional] |
|**accessType** | **Integer** |  |  [optional] |
|**dataPrivacy** | **String** |  |  [optional] |
|**researchOutputs** | **Object** |  |  [optional] |
|**dataAssets** | **String** |  |  [optional] |



## Enum: RequestFrequencyEnum

| Name | Value |
|---- | -----|
| ONE_OFF | &quot;ONE-OFF&quot; |
| RECURRING | &quot;RECURRING&quot; |



