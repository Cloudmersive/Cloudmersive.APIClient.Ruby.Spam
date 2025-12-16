# CloudmersiveSpamDetectionApiClient::SpamDetectionFormSubmissionAdvancedResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**clean_result** | **BOOLEAN** | True if the result is not spam (clean), and false otherwise | [optional] 
**spam_risk_level** | **Float** | Overall spam risk level between 0.0 and 1.0 | [optional] 
**contains_spam** | **BOOLEAN** | True if the input text contains spam, false otherwise | [optional] 
**contains_unsolicited_sales** | **BOOLEAN** | True if the input text contains unsolicited sales, false otherwise | [optional] 
**contains_promotional_content** | **BOOLEAN** | True if the input text contains promotional content, false otherwise | [optional] 
**contains_phishing_attempt** | **BOOLEAN** | True if the input text contains a phishing attempt, false otherwise | [optional] 
**analysis_rationale** | **String** | Rationale for why the conclusion was formed | [optional] 


