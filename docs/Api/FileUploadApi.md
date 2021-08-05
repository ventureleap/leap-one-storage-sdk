# VentureLeap\StorageService\FileUploadApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getFileUploadItem**](FileUploadApi.md#getfileuploaditem) | **GET** /storage/file_uploads/{identifier} | Retrieves a FileUpload resource.
[**postFileUploadCollection**](FileUploadApi.md#postfileuploadcollection) | **POST** /storage/file_uploads | Creates a FileUpload resource.

# **getFileUploadItem**
> getFileUploadItem($identifier)

Retrieves a FileUpload resource.

Retrieves a FileUpload resource.

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
$identifier = "identifier_example"; // string | Resource identifier

try {
    $apiInstance->getFileUploadItem($identifier);
} catch (Exception $e) {
    echo 'Exception when calling FileUploadApi->getFileUploadItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **identifier** | **string**| Resource identifier |

### Return type

void (empty response body)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postFileUploadCollection**
> \VentureLeap\StorageService\Model\FileUploadJsonldFileRead postFileUploadCollection($file)

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

try {
    $result = $apiInstance->postFileUploadCollection($file);
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

### Return type

[**\VentureLeap\StorageService\Model\FileUploadJsonldFileRead**](../Model/FileUploadJsonldFileRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

