# VentureLeap\StorageService\FileApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getFileCollection**](FileApi.md#getfilecollection) | **GET** /storage/files | Retrieves the collection of File resources.
[**getFileItem**](FileApi.md#getfileitem) | **GET** /storage/files/{uuid} | Retrieves a File resource.
[**patchFileItem**](FileApi.md#patchfileitem) | **PATCH** /storage/files/{uuid} | Updates the File resource.
[**putFileItem**](FileApi.md#putfileitem) | **PUT** /storage/files/{uuid} | Replaces the File resource.

# **getFileCollection**
> \VentureLeap\StorageService\Model\InlineResponse2001 getFileCollection($page, $items_per_page, $pagination, $original_file_name, $mime_type, $encrypted)

Retrieves the collection of File resources.

Retrieves the collection of File resources.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\StorageService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\StorageService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\StorageService\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number
$items_per_page = 30; // int | The number of items per page
$pagination = true; // bool | Enable or disable pagination
$original_file_name = "original_file_name_example"; // string | 
$mime_type = "mime_type_example"; // string | 
$encrypted = true; // bool | 

try {
    $result = $apiInstance->getFileCollection($page, $items_per_page, $pagination, $original_file_name, $mime_type, $encrypted);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->getFileCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The collection page number | [optional] [default to 1]
 **items_per_page** | **int**| The number of items per page | [optional] [default to 30]
 **pagination** | **bool**| Enable or disable pagination | [optional]
 **original_file_name** | **string**|  | [optional]
 **mime_type** | **string**|  | [optional]
 **encrypted** | **bool**|  | [optional]

### Return type

[**\VentureLeap\StorageService\Model\InlineResponse2001**](../Model/InlineResponse2001.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getFileItem**
> \VentureLeap\StorageService\Model\FileJsonldFileRead getFileItem($uuid)

Retrieves a File resource.

Retrieves a File resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\StorageService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\StorageService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\StorageService\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$uuid = "uuid_example"; // string | Resource identifier

try {
    $result = $apiInstance->getFileItem($uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->getFileItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| Resource identifier |

### Return type

[**\VentureLeap\StorageService\Model\FileJsonldFileRead**](../Model/FileJsonldFileRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchFileItem**
> \VentureLeap\StorageService\Model\FileJsonldFileRead patchFileItem($body, $uuid)

Updates the File resource.

Updates the File resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\StorageService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\StorageService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\StorageService\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \VentureLeap\StorageService\Model\File(); // \VentureLeap\StorageService\Model\File | The updated File resource
$uuid = "uuid_example"; // string | Resource identifier

try {
    $result = $apiInstance->patchFileItem($body, $uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->patchFileItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\StorageService\Model\File**](../Model/File.md)| The updated File resource |
 **uuid** | **string**| Resource identifier |

### Return type

[**\VentureLeap\StorageService\Model\FileJsonldFileRead**](../Model/FileJsonldFileRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/merge-patch+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putFileItem**
> \VentureLeap\StorageService\Model\FileJsonldFileRead putFileItem($body, $uuid)

Replaces the File resource.

Replaces the File resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\StorageService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\StorageService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\StorageService\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \VentureLeap\StorageService\Model\FileJsonld(); // \VentureLeap\StorageService\Model\FileJsonld | The updated File resource
$uuid = "uuid_example"; // string | Resource identifier

try {
    $result = $apiInstance->putFileItem($body, $uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->putFileItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\StorageService\Model\FileJsonld**](../Model/FileJsonld.md)| The updated File resource |
 **uuid** | **string**| Resource identifier |

### Return type

[**\VentureLeap\StorageService\Model\FileJsonldFileRead**](../Model/FileJsonldFileRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

