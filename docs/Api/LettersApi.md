# Swagger\Client\LettersApi

All URIs are relative to *https://app.postbode.nu/api/mailbox*

Method | HTTP request | Description
------------- | ------------- | -------------
[**letterCancelByMailboxIdAndLetterIdGet**](LettersApi.md#letterCancelByMailboxIdAndLetterIdGet) | **GET** /{mailbox_id}/letter/{letter_id}/cancel | Cancel letter
[**lettersByMailboxIdGet**](LettersApi.md#lettersByMailboxIdGet) | **GET** /{mailbox_id}/letters | Get letter
[**lettersByMailboxIdPost**](LettersApi.md#lettersByMailboxIdPost) | **POST** /{mailbox_id}/letters | Create letter


# **letterCancelByMailboxIdAndLetterIdGet**
> letterCancelByMailboxIdAndLetterIdGet($x_authorization, $mailbox_id, $letter_id)

Cancel letter

Cancel a letter that is being processed  ### Cancel letter paramaters  |   property             |description                           |----------------|-------------------------------| |mailbox_id     | id of the mailbox the letter got sent from              | |letter_id      | id of the letter that needs to be cancelled              |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: auth
Swagger\Client\Configuration::getDefaultConfiguration()->setUsername('YOUR_USERNAME');
Swagger\Client\Configuration::getDefaultConfiguration()->setPassword('YOUR_PASSWORD');

$api_instance = new Swagger\Client\Api\LettersApi();
$x_authorization = "x_authorization_example"; // string | 
$mailbox_id = "mailbox_id_example"; // string | 
$letter_id = "letter_id_example"; // string | 

try {
    $api_instance->letterCancelByMailboxIdAndLetterIdGet($x_authorization, $mailbox_id, $letter_id);
} catch (Exception $e) {
    echo 'Exception when calling LettersApi->letterCancelByMailboxIdAndLetterIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_authorization** | **string**|  |
 **mailbox_id** | **string**|  |
 **letter_id** | **string**|  |

### Return type

void (empty response body)

### Authorization

[auth](../../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **lettersByMailboxIdGet**
> \Swagger\Client\Model\Getletter[] lettersByMailboxIdGet($x_authorization, $mailbox_id)

Get letter

Get all letters of mailbox  ### Letter properties  |   property             |options                          |description         |----------------|-------------------------------|-----------------------------| |id     | NA              | letter id           | |mailbox_id      | NA              | mailbox id          | |envelop_id      | 2 (default) or custom   | standard 2 ( C5 window left) or custom envelop |shipping_method_id | 23 standard Sandd 24 hour delivery| see shipping methods for more options |service| send / recieved / campaign | recieve is applicable for recieving mailbox option or bounces |status | concept / in progress / sent / undeliverable | Track progress of letter |color | full color / black white |  |printing | simlex | duplex |paper_weight | 80g | 80g is standard and only option |paper_size | A4 | standard and only option |tracking_code | NA | applicable for registered letters |formatted_id | PBXXXXXX | reference id in application |shipping_id | 23 standard Sandd 24 hour delivery | see shipping methods for more options |weight | NA | weight of letter in grams |pages | NA | number of total sides |sheets | NA | number of pages (two sided)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: auth
Swagger\Client\Configuration::getDefaultConfiguration()->setUsername('YOUR_USERNAME');
Swagger\Client\Configuration::getDefaultConfiguration()->setPassword('YOUR_PASSWORD');

$api_instance = new Swagger\Client\Api\LettersApi();
$x_authorization = "x_authorization_example"; // string | 
$mailbox_id = "mailbox_id_example"; // string | 

try {
    $result = $api_instance->lettersByMailboxIdGet($x_authorization, $mailbox_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LettersApi->lettersByMailboxIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_authorization** | **string**|  |
 **mailbox_id** | **string**|  |

### Return type

[**\Swagger\Client\Model\Getletter[]**](../Model/Getletter.md)

### Authorization

[auth](../../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **lettersByMailboxIdPost**
> \Swagger\Client\Model\Postletterresponse200OK lettersByMailboxIdPost($x_authorization, $content_type, $body, $mailbox_id)

Create letter

## Send a letter    |   property             |options                          |description          |----------------|-------------------------------|-----------------------------|  |documents     | array with name and content | first document needs a valid adres on the right position in envelop window          |  |cover_address (optional)      | string \" NAME ADRES ZIP CODE COUNTRY\" (with line endings) | when provided a emty paper with adres will be generated in front of content  |envelop_id | 2 (default) or custom | standard 2 ( C5 window left) or custom envelop  |country | string ISO-3166-2 country codes | the code of the country the letter needs to be shipped to  |registered | true / false | set to true for registered mail  |send | true / false | when true will be send, when false will be placed as concept to be sent later (manual)  |color| FC (default) / BW | full color or black and White  |printing | simplex (default) / duplex | one or two sided printing  | printer | inkjet (default) / toner | printer type  | metadata | array with personalised data | Extra data that will be returned to the mailbox webhook url

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: auth
Swagger\Client\Configuration::getDefaultConfiguration()->setUsername('YOUR_USERNAME');
Swagger\Client\Configuration::getDefaultConfiguration()->setPassword('YOUR_PASSWORD');

$api_instance = new Swagger\Client\Api\LettersApi();
$x_authorization = "x_authorization_example"; // string | 
$content_type = "content_type_example"; // string | 
$body = new \Swagger\Client\Model\CreateletterRequest(); // \Swagger\Client\Model\CreateletterRequest | 
$mailbox_id = "mailbox_id_example"; // string | 

try {
    $result = $api_instance->lettersByMailboxIdPost($x_authorization, $content_type, $body, $mailbox_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LettersApi->lettersByMailboxIdPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_authorization** | **string**|  |
 **content_type** | **string**|  |
 **body** | [**\Swagger\Client\Model\CreateletterRequest**](../Model/\Swagger\Client\Model\CreateletterRequest.md)|  |
 **mailbox_id** | **string**|  |

### Return type

[**\Swagger\Client\Model\Postletterresponse200OK**](../Model/Postletterresponse200OK.md)

### Authorization

[auth](../../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

