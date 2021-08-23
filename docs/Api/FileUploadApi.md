# VentureLeap\StorageService\FileUploadApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**postFileUploadCollection**](FileUploadApi.md#postfileuploadcollection) | **POST** /storage/files/upload | Creates a FileUpload resource.

# **postFileUploadCollection**
> \VentureLeap\StorageService\Model\FileUploadJsonldUploadRead postFileUploadCollection($file, $encrypt)

Creates a FileUpload resource.

Creates a FileUpload resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\StorageService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\StorageService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\StorageService\Api\FileUploadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = "file_example"; // string | 
$encrypt = true; // bool | 

try {
    $result = $apiInstance->postFileUploadCollection($file, $encrypt);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileUploadApi->postFileUploadCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **string****string**|  | [optional]
 **encrypt** | **bool**|  | [optional]

### Return type

[**\VentureLeap\StorageService\Model\FileUploadJsonldUploadRead**](../Model/FileUploadJsonldUploadRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

