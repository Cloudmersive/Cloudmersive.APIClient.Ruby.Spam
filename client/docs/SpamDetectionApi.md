# CloudmersiveSpamDetectionApiClient::SpamDetectionApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**spam_detect_file_advanced_post**](SpamDetectionApi.md#spam_detect_file_advanced_post) | **POST** /spam/detect/file/advanced | Perform advanced AI spam detection and classification against input text file.
[**spam_detect_file_post**](SpamDetectionApi.md#spam_detect_file_post) | **POST** /spam/detect/file | Perform AI spam detection and classification on an input image or document (PDF or DOCX)
[**spam_detect_form_submission_advanced_post**](SpamDetectionApi.md#spam_detect_form_submission_advanced_post) | **POST** /spam/detect/form-submission/advanced | Perform advanced AI spam detection and classification against a form submission
[**spam_detect_text_string_advanced_post**](SpamDetectionApi.md#spam_detect_text_string_advanced_post) | **POST** /spam/detect/text-string/advanced | Perform advanced AI spam detection and classification against input text string
[**spam_detect_text_string_post**](SpamDetectionApi.md#spam_detect_text_string_post) | **POST** /spam/detect/text-string | Perform AI spam detection and classification against input text string


# **spam_detect_file_advanced_post**
> SpamDetectionAdvancedResponse spam_detect_file_advanced_post(opts)

Perform advanced AI spam detection and classification against input text file.

Analyzes input content as well as embedded URLs with AI deep learning to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.  Supported file formats include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.

### Example
```ruby
# load the gem
require 'cloudmersive-spam-detection-api-client'
# setup authorization
CloudmersiveSpamDetectionApiClient.configure do |config|
  # Configure API key authorization: Apikey
  config.api_key['Apikey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Apikey'] = 'Bearer'
end

api_instance = CloudmersiveSpamDetectionApiClient::SpamDetectionApi.new

opts = { 
  model: 'Advanced', # String | Optional: Specify which AI model to use.  Possible choices are Normal and Advanced.  Default is Advanced.
  preprocessing: 'Auto', # String | Optional: Specify which preprocessing to Use.  Possible choices are None, Compatability and Auto.  Default is Auto.
  allow_phishing: false, # BOOLEAN | True if phishing should be allowed, false otherwise
  allow_unsolicited_sales: false, # BOOLEAN | True if unsolicited sales should be allowed, false otherwise
  allow_promotional_content: true, # BOOLEAN | True if promotional content should be allowed, false otherwise
  custom_policy_id: 'custom_policy_id_example', # String | Apply a Custom Policy for Spam Enforcement by providing the ID; to create a Custom Policy, navigate to the Cloudmersive Management Portal and select Custom Policies.  Requires Managed Instance or Private Cloud
  input_file: File.new('/path/to/file.txt') # File | 
}

begin
  #Perform advanced AI spam detection and classification against input text file.
  result = api_instance.spam_detect_file_advanced_post(opts)
  p result
rescue CloudmersiveSpamDetectionApiClient::ApiError => e
  puts "Exception when calling SpamDetectionApi->spam_detect_file_advanced_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | **String**| Optional: Specify which AI model to use.  Possible choices are Normal and Advanced.  Default is Advanced. | [optional] [default to Advanced]
 **preprocessing** | **String**| Optional: Specify which preprocessing to Use.  Possible choices are None, Compatability and Auto.  Default is Auto. | [optional] [default to Auto]
 **allow_phishing** | **BOOLEAN**| True if phishing should be allowed, false otherwise | [optional] [default to false]
 **allow_unsolicited_sales** | **BOOLEAN**| True if unsolicited sales should be allowed, false otherwise | [optional] [default to false]
 **allow_promotional_content** | **BOOLEAN**| True if promotional content should be allowed, false otherwise | [optional] [default to true]
 **custom_policy_id** | **String**| Apply a Custom Policy for Spam Enforcement by providing the ID; to create a Custom Policy, navigate to the Cloudmersive Management Portal and select Custom Policies.  Requires Managed Instance or Private Cloud | [optional] 
 **input_file** | **File**|  | [optional] 

### Return type

[**SpamDetectionAdvancedResponse**](SpamDetectionAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json



# **spam_detect_file_post**
> SpamDetectionResponse spam_detect_file_post(opts)

Perform AI spam detection and classification on an input image or document (PDF or DOCX)

Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 100-125 API calls depending on model selected.  Supported file formats include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.

### Example
```ruby
# load the gem
require 'cloudmersive-spam-detection-api-client'
# setup authorization
CloudmersiveSpamDetectionApiClient.configure do |config|
  # Configure API key authorization: Apikey
  config.api_key['Apikey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Apikey'] = 'Bearer'
end

api_instance = CloudmersiveSpamDetectionApiClient::SpamDetectionApi.new

opts = { 
  model: 'Advanced', # String | Model to use; default setting is Advanced
  input_file: File.new('/path/to/file.txt') # File | 
}

begin
  #Perform AI spam detection and classification on an input image or document (PDF or DOCX)
  result = api_instance.spam_detect_file_post(opts)
  p result
rescue CloudmersiveSpamDetectionApiClient::ApiError => e
  puts "Exception when calling SpamDetectionApi->spam_detect_file_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | **String**| Model to use; default setting is Advanced | [optional] [default to Advanced]
 **input_file** | **File**|  | [optional] 

### Return type

[**SpamDetectionResponse**](SpamDetectionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json



# **spam_detect_form_submission_advanced_post**
> SpamDetectionFormSubmissionAdvancedResponse spam_detect_form_submission_advanced_post(opts)

Perform advanced AI spam detection and classification against a form submission

Analyzes form input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.

### Example
```ruby
# load the gem
require 'cloudmersive-spam-detection-api-client'
# setup authorization
CloudmersiveSpamDetectionApiClient.configure do |config|
  # Configure API key authorization: Apikey
  config.api_key['Apikey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Apikey'] = 'Bearer'
end

api_instance = CloudmersiveSpamDetectionApiClient::SpamDetectionApi.new

opts = { 
  body: CloudmersiveSpamDetectionApiClient::SpamDetectionAdvancedFormSubmissionRequest.new # SpamDetectionAdvancedFormSubmissionRequest | Spam detection request
}

begin
  #Perform advanced AI spam detection and classification against a form submission
  result = api_instance.spam_detect_form_submission_advanced_post(opts)
  p result
rescue CloudmersiveSpamDetectionApiClient::ApiError => e
  puts "Exception when calling SpamDetectionApi->spam_detect_form_submission_advanced_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SpamDetectionAdvancedFormSubmissionRequest**](SpamDetectionAdvancedFormSubmissionRequest.md)| Spam detection request | [optional] 

### Return type

[**SpamDetectionFormSubmissionAdvancedResponse**](SpamDetectionFormSubmissionAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json



# **spam_detect_text_string_advanced_post**
> SpamDetectionAdvancedResponse spam_detect_text_string_advanced_post(opts)

Perform advanced AI spam detection and classification against input text string

Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.

### Example
```ruby
# load the gem
require 'cloudmersive-spam-detection-api-client'
# setup authorization
CloudmersiveSpamDetectionApiClient.configure do |config|
  # Configure API key authorization: Apikey
  config.api_key['Apikey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Apikey'] = 'Bearer'
end

api_instance = CloudmersiveSpamDetectionApiClient::SpamDetectionApi.new

opts = { 
  body: CloudmersiveSpamDetectionApiClient::SpamDetectionAdvancedRequest.new # SpamDetectionAdvancedRequest | Spam detection request
}

begin
  #Perform advanced AI spam detection and classification against input text string
  result = api_instance.spam_detect_text_string_advanced_post(opts)
  p result
rescue CloudmersiveSpamDetectionApiClient::ApiError => e
  puts "Exception when calling SpamDetectionApi->spam_detect_text_string_advanced_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SpamDetectionAdvancedRequest**](SpamDetectionAdvancedRequest.md)| Spam detection request | [optional] 

### Return type

[**SpamDetectionAdvancedResponse**](SpamDetectionAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json



# **spam_detect_text_string_post**
> SpamDetectionResponse spam_detect_text_string_post(opts)

Perform AI spam detection and classification against input text string

Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-75 API calls depending on model selected.

### Example
```ruby
# load the gem
require 'cloudmersive-spam-detection-api-client'
# setup authorization
CloudmersiveSpamDetectionApiClient.configure do |config|
  # Configure API key authorization: Apikey
  config.api_key['Apikey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Apikey'] = 'Bearer'
end

api_instance = CloudmersiveSpamDetectionApiClient::SpamDetectionApi.new

opts = { 
  body: CloudmersiveSpamDetectionApiClient::SpamDetectionRequest.new # SpamDetectionRequest | Spam detection request
}

begin
  #Perform AI spam detection and classification against input text string
  result = api_instance.spam_detect_text_string_post(opts)
  p result
rescue CloudmersiveSpamDetectionApiClient::ApiError => e
  puts "Exception when calling SpamDetectionApi->spam_detect_text_string_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SpamDetectionRequest**](SpamDetectionRequest.md)| Spam detection request | [optional] 

### Return type

[**SpamDetectionResponse**](SpamDetectionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json



