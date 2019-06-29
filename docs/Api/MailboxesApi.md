# Swagger\Client\MailboxesApi

All URIs are relative to *https://app.postbode.nu/api/mailbox*

Method | HTTP request | Description
------------- | ------------- | -------------
[**unnammedEndpointGet**](MailboxesApi.md#unnammedEndpointGet) | **GET** / | Get available mailboxes


# **unnammedEndpointGet**
> string unnammedEndpointGet($x_authorization)

Get available mailboxes

Get all available mailboxes which are associated with the API-Key.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\MailboxesApi();
$x_authorization = "x_authorization_example"; // string | 

try {
    $result = $api_instance->unnammedEndpointGet($x_authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MailboxesApi->unnammedEndpointGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_authorization** | **string**|  |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

