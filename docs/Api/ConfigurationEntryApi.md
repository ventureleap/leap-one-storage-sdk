# VentureLeap\StorageService\ConfigurationEntryApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteConfigurationEntryItem**](ConfigurationEntryApi.md#deleteconfigurationentryitem) | **DELETE** /storage/configuration_entries/{uuid} | Removes the ConfigurationEntry resource.
[**getConfigurationEntryCollection**](ConfigurationEntryApi.md#getconfigurationentrycollection) | **GET** /storage/configuration_entries | Retrieves the collection of ConfigurationEntry resources.
[**getConfigurationEntryItem**](ConfigurationEntryApi.md#getconfigurationentryitem) | **GET** /storage/configuration_entries/{uuid} | Retrieves a ConfigurationEntry resource.
[**postConfigurationEntryCollection**](ConfigurationEntryApi.md#postconfigurationentrycollection) | **POST** /storage/configuration_entries | Creates a ConfigurationEntry resource.
[**putConfigurationEntryItem**](ConfigurationEntryApi.md#putconfigurationentryitem) | **PUT** /storage/configuration_entries/{uuid} | Replaces the ConfigurationEntry resource.

# **deleteConfigurationEntryItem**
> deleteConfigurationEntryItem($uuid)

Removes the ConfigurationEntry resource.

Removes the ConfigurationEntry resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new VentureLeap\StorageService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$uuid = "uuid_example"; // string | Resource identifier

try {
    $apiInstance->deleteConfigurationEntryItem($uuid);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->deleteConfigurationEntryItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| Resource identifier |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getConfigurationEntryCollection**
> \VentureLeap\StorageService\Model\InlineResponse200 getConfigurationEntryCollection($page, $pagination, $key, $sub_key, $value, $application_id)

Retrieves the collection of ConfigurationEntry resources.

Retrieves the collection of ConfigurationEntry resources.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new VentureLeap\StorageService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page = 1; // int | The collection page number
$pagination = true; // bool | Enable or disable pagination
$key = "key_example"; // string | 
$sub_key = "sub_key_example"; // string | 
$value = "value_example"; // string | 
$application_id = "application_id_example"; // string | 

try {
    $result = $apiInstance->getConfigurationEntryCollection($page, $pagination, $key, $sub_key, $value, $application_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->getConfigurationEntryCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The collection page number | [optional] [default to 1]
 **pagination** | **bool**| Enable or disable pagination | [optional]
 **key** | **string**|  | [optional]
 **sub_key** | **string**|  | [optional]
 **value** | **string**|  | [optional]
 **application_id** | **string**|  | [optional]

### Return type

[**\VentureLeap\StorageService\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getConfigurationEntryItem**
> \VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationRead getConfigurationEntryItem($uuid)

Retrieves a ConfigurationEntry resource.

Retrieves a ConfigurationEntry resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new VentureLeap\StorageService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$uuid = "uuid_example"; // string | Resource identifier

try {
    $result = $apiInstance->getConfigurationEntryItem($uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->getConfigurationEntryItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| Resource identifier |

### Return type

[**\VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationRead**](../Model/ConfigurationEntryJsonldConfigurationRead.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postConfigurationEntryCollection**
> \VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationRead postConfigurationEntryCollection($body)

Creates a ConfigurationEntry resource.

Creates a ConfigurationEntry resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new VentureLeap\StorageService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationWrite(); // \VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationWrite | The new ConfigurationEntry resource

try {
    $result = $apiInstance->postConfigurationEntryCollection($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->postConfigurationEntryCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationWrite**](../Model/ConfigurationEntryJsonldConfigurationWrite.md)| The new ConfigurationEntry resource |

### Return type

[**\VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationRead**](../Model/ConfigurationEntryJsonldConfigurationRead.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/ld+json, application/json, text/html
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postConfigurationEntryCollection**
> \VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationRead postConfigurationEntryCollection($body)

Creates a ConfigurationEntry resource.

Creates a ConfigurationEntry resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new VentureLeap\StorageService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationWrite(); // \VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationWrite | The new ConfigurationEntry resource

try {
    $result = $apiInstance->postConfigurationEntryCollection($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->postConfigurationEntryCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationWrite**](../Model/ConfigurationEntryJsonldConfigurationWrite.md)| The new ConfigurationEntry resource |

### Return type

[**\VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationRead**](../Model/ConfigurationEntryJsonldConfigurationRead.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/ld+json, application/json, text/html
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putConfigurationEntryItem**
> \VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationRead putConfigurationEntryItem($body, $uuid)

Replaces the ConfigurationEntry resource.

Replaces the ConfigurationEntry resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new VentureLeap\StorageService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationWrite(); // \VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationWrite | The updated ConfigurationEntry resource
$uuid = "uuid_example"; // string | Resource identifier

try {
    $result = $apiInstance->putConfigurationEntryItem($body, $uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->putConfigurationEntryItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationWrite**](../Model/ConfigurationEntryJsonldConfigurationWrite.md)| The updated ConfigurationEntry resource |
 **uuid** | **string**| Resource identifier |

### Return type

[**\VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationRead**](../Model/ConfigurationEntryJsonldConfigurationRead.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/ld+json, application/json, text/html
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putConfigurationEntryItem**
> \VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationRead putConfigurationEntryItem($body, $uuid)

Replaces the ConfigurationEntry resource.

Replaces the ConfigurationEntry resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new VentureLeap\StorageService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationWrite(); // \VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationWrite | The updated ConfigurationEntry resource
$uuid = "uuid_example"; // string | Resource identifier

try {
    $result = $apiInstance->putConfigurationEntryItem($body, $uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->putConfigurationEntryItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationWrite**](../Model/ConfigurationEntryJsonldConfigurationWrite.md)| The updated ConfigurationEntry resource |
 **uuid** | **string**| Resource identifier |

### Return type

[**\VentureLeap\StorageService\Model\ConfigurationEntryJsonldConfigurationRead**](../Model/ConfigurationEntryJsonldConfigurationRead.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/ld+json, application/json, text/html
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

