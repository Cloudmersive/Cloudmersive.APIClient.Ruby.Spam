# CloudmersiveSpamDetectionApiClient::SpamDetectionApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**spam_detect_text_string_advanced_post**](SpamDetectionApi.md#spam_detect_text_string_advanced_post) | **POST** /spam/detect/text-string/advanced | Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
[**spam_detect_text_string_post**](SpamDetectionApi.md#spam_detect_text_string_post) | **POST** /spam/detect/text-string | Perform AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-75 API calls depending on model selected.


# **spam_detect_text_string_advanced_post**
> SpamDetectionAdvancedResponse spam_detect_text_string_advanced_post(opts)

Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.

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
  #Perform advanced AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
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

Perform AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-75 API calls depending on model selected.

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
  #Perform AI spam detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-75 API calls depending on model selected.
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



