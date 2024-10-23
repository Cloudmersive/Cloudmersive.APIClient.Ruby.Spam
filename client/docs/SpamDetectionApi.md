# CloudmersiveSpamDetectionApiClient::SpamDetectionApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**spam_detect_text_string_advanced_post**](SpamDetectionApi.md#spam_detect_text_string_advanced_post) | **POST** /spam/detect/text-string/advanced | 


# **spam_detect_text_string_advanced_post**
> SpamDetectionAdvancedResponse spam_detect_text_string_advanced_post(opts)



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
  body: CloudmersiveSpamDetectionApiClient::SpamDetectionAdvancedRequest.new # SpamDetectionAdvancedRequest | 
}

begin
  result = api_instance.spam_detect_text_string_advanced_post(opts)
  p result
rescue CloudmersiveSpamDetectionApiClient::ApiError => e
  puts "Exception when calling SpamDetectionApi->spam_detect_text_string_advanced_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SpamDetectionAdvancedRequest**](SpamDetectionAdvancedRequest.md)|  | [optional] 

### Return type

[**SpamDetectionAdvancedResponse**](SpamDetectionAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json



