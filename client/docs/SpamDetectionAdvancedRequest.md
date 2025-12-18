# CloudmersiveSpamDetectionApiClient::SpamDetectionAdvancedRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**input_string** | **String** | Input text string to detect spam against | [optional] 
**model** | **String** | Optional: Specify which AI model to use.  Possible choices are Normal and Advanced.  Default is Advanced. | [optional] 
**allow_unsolicited_sales** | **BOOLEAN** | True if unsolicited sales should be allowed, false otherwise | [optional] 
**allow_promotional_content** | **BOOLEAN** | True if promotional content should be allowed, false otherwise | [optional] 
**allow_phishing** | **BOOLEAN** | True if phishing should be allowed, false otherwise | [optional] 
**custom_policy_id** | **String** | Apply a Custom Policy for Spam Enforcement by providing the ID; to create a Custom Policy, navigate to the Cloudmersive Management Portal and select Custom Policies.  Requires Managed Instance or Private Cloud | [optional] 


