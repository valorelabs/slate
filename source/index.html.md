---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell: cURL

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

search: true
---

# Introduction

Welcome to the Merchant Tablet API!

## Environment

> Dev

```
http://merchant-api.dev.cambi.io
```
> Staging

```
https://merchant-api.staging.cambi.io
```

> Production

```
https://merchant-api.cambi.io
```

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.

## Authentication & Header
## HTTP Status Code
## Error Code

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.

Error Code | Description
---------- | -------
1000 | X-Auth-Token missing
1001 | X-Auth-Token expired
1002 | X-Auth-Token invalid
1003 | Merchant ID missing
1004 | Invalid merchant
1005 | Merchant user doesn’t have permission for this operation
1006 | User ID missing
1007 | User ID invalid/doesn’t exist
1008 | Amount missing
1009 | Card ID missing
1010 | Card ID invalid / doesn’t exist
1011 | Not a Loyalty Card
1012 | Not a Gift Card
1013 | Card does not belong to merchant
1014 | Merchant Store ID missing
1015 | Merchant Store ID invalid / doesn’t exist
1016 | Merchant User ID missing
1017 | Merchant User ID invalid / doesn’t exist
1018 | Phone Number missing
1019 | Phone Number invalid
1020 | Item Count missing
1021 | Item Count Invalid
1022 | UserName missing
1023 | UserName invalid / doesn’t exist
1024 | Password missing
1025 | Password invalid / doesn’t exist
1026 | Merchant Name missing
1027 | Merchant Name invalid / doesn’t exist
1028 | Login Unauthorised
1029 | Soft Auth Code missing
1030 | Soft Auth Code doesn’t exist
1031 | Soft Auth Code expired
1032 | Nonce missing
1033 | Nonce invalid / doesn’t exist
1034 | Payment basket missing
1035 | Payment basket invalid
1036 | Merchant user role missing
1037 | Merchant user role invalid
1038 | Merchant status missing
1039 | Merchant status invalid
1040 | Soft Auth Code couldn’t be generated
1041 | Nonce couldn’t be generated
1042 | Days missing
1043 | Days invalid
1044 | Transaction action missing
1045 | Transaction action invalid
1046 | Transaction status missing
1047 | Transaction status invalid
1048 | Signup -> Store email missing
1049 | Signup -> Store email invalid
1050 | Signup -> confirm password missing
1051 | Signup -> confirm password invalid
1052 | Signup -> password and confirm password don’t match
1053 | Signup -> Merchant/store email already exists
1054 | Signup -> password length incorrect
1029 | soft auth code missing
1030 | soft auth code invalid
1031 | soft auth code expired
1055 | soft auth code not valid for merchant
1056 | soft auth code not valid for merchant store
1057 | Invalid consumer user id / doesn't exist
1058 | Missing consumer user id


# Authentication

## Login

> Definition

```
POST https://merchant-api.cambi.io/api/v2/authenticate
```

> Example Request

```json
{
    "userName": "scsiva",
    "password": "12345678"
}
```
> Example Response

```json
{
    "roleLabel": "Manager",
    "roleName": "manager",
    "roleId": "role::1",
    "roleDataVisibilityLevel": "STORE",
    "merchantId": "merchant::72e170ab-0d57-4a2e-8d93-7f9cac872976",
    "merchantName": "San Mateo Prime",
    "merchantStoreId": "2ad2a3fe-ae70-4977-88ef-74a41ffc7e6a",
    "merchantStoreName": "San Mateo Prime - SAN MATEO - 001",
    "userId": "user::merchant::72e170ab-0d57-4a2e-8d93-7f9cac872976::5c1060fa-7d2d-4563-8b9e-805fd9a671cb",
    "userName": "sansiva",
    "isGiftEnabled": true,
    "isLoyaltyEnabled": false,
    "isTransactionNumberEnabled": false,
    "isTransactionByPhoneNumberEnabled": true,
    "isAmountFieldEnabled": true,
    "isAutoLogoutEnabled": true,
    "autoLogoutTimer": 0,
    "loyaltyByCount": false,
    "redemptionBlock": 1,
    "conversionRate": 1,
    "conversionType": "pts",
    "accrualRate": 1,
    "minimumEligibility": 0,
    "authTokenExpiryAtMs": 1527554765941,
    "isSuccess": true,
    "message": "Logged in successfully"
}
```

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
### HTTP Endpoint

`POST https://merchant-api.cambi.io/api/v2/authenticate`

### Request JSON
Parameter | Type | Description
--------- | ------- | -----------
userName | `string` | If set to true, the result will also include cats.
password | `string` | If set to false, the result will include kittens that have already been adopted.

### Response JSON
Parameter | Type | Description
--------- | ------- | -----------
accrualRate | `int` | Sample Text
authTokenExpiryAtMs | `timestamp` | Sample Text
autoLogoutTimer | `int` | Sample Text
conversionRate | `int` | Sample Text
conversionType | `string` | Sample Text
isAmountFieldEnabled | `boolean` | Sample Text
isAutoLogoutEnabled | `boolean` | Sample Text
isGiftEnabled | `boolean` | Sample Text
isLoyaltyEnabled | `boolean` | Sample Text
isSuccess | `boolean` | Sample Text
isTransactionByPhoneNumberEnabled | `boolean` | Sample Text
isTransactionNumberEnabled | `boolean` | Sample Text
loyaltyByCount | `boolean` | Sample Text
merchantId | `uuid` | Sample Text
merchantName | `string` | Sample Text
merchantStoreId | `uuid` | Sample Text
merchantStoreName | `string` | Sample Text
message | `string` | Sample Text
minimumEligibility | `int` | Sample Text
redemptionBlock | `int` | Sample Text
roleDataVisibilityLevel | `string` | Sample Text
roleId | `string` | Sample Text
roleLabel | `string` | Sample Text
roleName | `string` | Sample Text
userId | `uuid` | Sample Text
userName | `string` | Sample Text

## Logout

> Definition

```
POST https://merchant-api.cambi.io/api/v1/logout
```

> Example Request

```json
{
    "merchantId": "scsiva",
    "merchantUserId": "12345678"
}
```
> Example Response

```json
{
    "isSuccess": true,
    "message": "12345678"
}
```

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
### HTTP Endpoint

`POST https://merchant-api.cambi.io/api/v1/logout`

### Headers
Parameter | Type | Description
--------- | ------- | -----------
merchantId | `string` | If set to true, the result will also include cats.
merchantUserId | `string` | If set to false, the result will include kittens that have already been adopted.

### Request Body
Parameter | Type | Description
--------- | ------- | -----------
merchantId | `string` | If set to true, the result will also include cats.
merchantUserId | `string` | If set to false, the result will include kittens that have already been adopted.

### Response JSON
Parameter | Type | Description
--------- | ------- | -----------
isSuccess | `string` | If set to true, the result will also include cats.
message | `string` | If set to false, the result will include kittens that have already been adopted.

# Transactions
## Recent Transactions

> Definition

```
GET https://merchant-api.cambi.io/api/v1/recentTransactions
```

> Example Request

```shell
https://merchant-api.cambi.io/api/v1/recentTransactions \
?merchantId=96b66b8d-271b-4f72-9d8e-7e20f04ba601 \
&merchantUserId=55bd41c7-6cf9-4b28-b098-fef935dd429f \ 
&days=7
```
> Example Response

```json
[
    {
        "action": "PAYMENT",
        "amount": 20.25,
        "cardId": "6ffbcf2c-4b34-49f8-823c-669dcb6b12a2",
        "cardNumber": "xx-4561",
        "cardType": "GIFT",
        "createdAt": "2018-05-25T10:03:28.425Z",
        "createdAtMs": 1527242608425,
        "discountAmount": 5,
        "discountPoints": 10,
        "docType": "payment_nonce",
        "isPromoApplied": false,
        "isSplitPayment": false,
        "issuedPointsFor": "",
        "itemCount": 10,
        "loyaltyLogId": "bbb489d2-e3a1-40b4-93f7-009bd7467b7b",
        "merchantId": "96b66b8d-271b-4f72-9d8e-7e20f04ba601",
        "merchantName": "Siva Cafe",
        "merchantStoreId": "bb3a150c-69c9-4e94-8a29-27edb98f345a",
        "merchantStoreName": "Siva Cafe - 001",
        "merchantUserId": "55bd41c7-6cf9-4b28-b098-fef935dd429f",
        "merchantUserName": "scsiva",
        "mobileNumber": "xx-1567",
        "paidWith": "OTHER",
        "paymentMethod": "GIFT",
        "paymentNonceId": "5e600d87-0ba8-47c4-8f39-7e227ebe60da",
        "points": 10,
        "status": "COMPLETED",
        "updatedAt": "2018-05-25T10:03:28.425Z",
        "updatedAtMs": 1527242608425,
        "userName": "scsiva"
    }
]
```

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
### HTTP Endpoint

`GET https://merchant-api.cambi.io/api/v1/recentTransactions`

### URL Parameters
Parameter | Type | Description
--------- | ------- | -----------
merchantId | `string` | If set to true, the result will also include cats.
merchantUserId | `string` | If set to false, the result will include kittens that have already been adopted.
days | `string` | If set to false, the result will include kittens that have already been adopted.

### Response JSON
Parameter | Type | Description
--------- | ------- | -----------
action | `string` | Sample Text 
amount | `decimal` | Sample Text 
cardId | `uuid` | Sample Text 
cardNumber | `string` | Sample Text 
cardType | `string` | Sample Text 
createdAt | `timestamp` | Sample Text 
createdAtMs | `timestamp` | Sample Text 
discountAmount | `decimal` | Sample Text 
discountPoints | `int` | Sample Text 
docType | `string` | Sample Text 
isPromoApplied | `boolean` | Sample Text 
isSplitPayment | `boolean` | Sample Text 
issuedPointsFor | `string` | Sample Text 
itemCount | `int` | Sample Text 
loyaltyLogId | `uuid` | Sample Text 
merchantId | `uuid` | Sample Text 
merchantName | `string` | Sample Text 
merchantStoreId | `uuid` | Sample Text 
merchantStoreName | `string` | Sample Text 
merchantUserId | `uuid` | Sample Text 
merchantUserName | `string` | Sample Text 
mobileNumber | `string` | Sample Text 
paidWith | `string` | Sample Text 
paymentMethod | `string` | Sample Text 
paymentNonceId | `uuid` | Sample Text 
points | `int` | Sample Text 
status | `string` | Sample Text 
updatedAt | `timestamp` | Sample Text 
updatedAtMs | `timestamp` | Sample Text 
userName | `string` | Sample Text 
