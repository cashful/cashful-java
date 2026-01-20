

# CreateOrganizationComplianceDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**organizationId** | **String** |  |  |
|**companyRegistrationName** | **String** |  |  [optional] |
|**companyRegistrationNumber** | **String** |  |  [optional] |
|**companyTradingName** | **String** |  |  [optional] |
|**vatRegistrationNumber** | **String** |  |  [optional] |
|**industry** | **String** |  |  [optional] |
|**subIndustry** | **String** |  |  [optional] |
|**estimatedAnnualTurnover** | **String** |  |  [optional] |
|**businessDescription** | **String** | Long business description |  [optional] |
|**companyMobileMoneySettlementNumber** | **String** |  |  [optional] |
|**companyEmail** | **String** |  |  [optional] |
|**companyContactNumber** | **String** |  |  [optional] |
|**website** | **String** |  |  [optional] |
|**socialMedia** | **String** |  |  [optional] |
|**accountContactNumber** | **String** |  |  [optional] |
|**customerSupportContactNumber** | **String** |  |  [optional] |
|**customerSupportEscalationContactNumber** | **String** |  |  [optional] |
|**emergencyContactNumber** | **String** |  |  [optional] |
|**streetAddress** | **String** |  |  [optional] |
|**apartment** | **String** |  |  [optional] |
|**suburb** | **String** |  |  [optional] |
|**city** | **String** |  |  [optional] |
|**postalCode** | **String** |  |  [optional] |
|**country** | **String** |  |  [optional] |
|**bank** | **String** |  |  [optional] |
|**accountType** | **String** |  |  [optional] |
|**accountName** | **String** |  |  [optional] |
|**accountNumber** | **String** |  |  [optional] |
|**branchCode** | **String** |  |  [optional] |
|**swiftCode** | **String** |  |  [optional] |
|**certificateOfIncorporation** | **String** |  |  [optional] |
|**identityDocuments** | **String** | JSON/text representation of identity documents |  [optional] |
|**bankAccountConfirmationLetter** | **String** |  |  [optional] |
|**proofOfBusinessAddress** | **String** |  |  [optional] |
|**termsAccepted** | **Boolean** |  |  [optional] |
|**acceptedAt** | **OffsetDateTime** |  |  [optional] |
|**currentStep** | [**CurrentStepEnum**](#CurrentStepEnum) |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**isCompleted** | **Boolean** |  |  [optional] |
|**completionScore** | **BigDecimal** |  |  [optional] |



## Enum: CurrentStepEnum

| Name | Value |
|---- | -----|
| INITIATION | &quot;initiation&quot; |
| VERIFICATION | &quot;verification&quot; |
| BUSINESS_DETAILS | &quot;business_details&quot; |
| BANKING_DETAILS | &quot;banking_details&quot; |
| UPLOAD_DOCUMENTS | &quot;upload_documents&quot; |
| SIGN_AGREEMENT | &quot;sign_agreement&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| VERIFIED | &quot;verified&quot; |
| REJECTED | &quot;rejected&quot; |


## Implemented Interfaces

* Serializable


