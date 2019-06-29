# postbode-nu-php-client
Postbode.nu PHP API client

This API client is generated using `swagger-codegen-cli.jar`. For input a Swagger version of [the official Postman collection](https://api.postbode.nu/?version=latest) is used.

## Authentication
To make use of the API one needs a account and an API-Key

Account: https://app.postbode.nu/register
API Key: https://app.postbode.nu/settings/api -> "API Key Aanmaken"

Use API key in header:

X-Authorization: XXXXXXXXX-YOUR-API-KEY-XXXXXXXXX

## Sandbox mode
For testing purposes there is a sandbox mode.

To activate: https://app.postbode.nu/mailbox/settings -> Testomgeving

While active no letters will be send in production. After disabling only new letters will be printed and send to reciever.
