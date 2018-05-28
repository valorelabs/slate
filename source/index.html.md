---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell: cURL

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Merchant Tablet API!

## Environment
## Authentication
## HTTP Status Code
## Error Code


# Authentication

## Login

> Definition

```
**POST** https://merchant-api.cambi.io/api/v2/authenticate
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
    "permissions": [
        "11",
        "21",
        "31",
        "41",
        "42",
        "43",
        "51",
        "52",
        "53",
        "61",
        "62",
        "63",
        "71",
        "501",
        "401",
        "402",
        "403",
        "201",
        "202",
        "203",
        "301",
        "302",
        "303",
        "101",
        "102",
        "103",
        "104",
        "105",
        "userManagementPage"
    ],
    "authTokenExpiryAtMs": 1527554765941,
    "isSuccess": true,
    "message": "Logged in successfully"
}
```

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
### HTTP Request

`POST https://merchant-api.cambi.io/api/v2/authenticate`

### Request JSON
Parameter | Type | Description
--------- | ------- | -----------
userName | `string` | If set to true, the result will also include cats.
password | `string` | If set to false, the result will include kittens that have already been adopted.

### Response JSON
Parameter | Type | Description
--------- | ------- | -----------
userName | `string` | If set to true, the result will also include cats.
password | `string` | If set to false, the result will include kittens that have already been adopted.

## Logout

> Definition

```
POST https://merchant-api.cambi.io/api/v1/logout
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

}
```

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
### HTTP Endpoint

`POST https://merchant-api.cambi.io/api/v1/logout`

### Request JSON
Parameter | Type | Description
--------- | ------- | -----------
userName | `string` | If set to true, the result will also include cats.
password | `string` | If set to false, the result will include kittens that have already been adopted.

### Response JSON
Parameter | Type | Description
--------- | ------- | -----------
userName | `string` | If set to true, the result will also include cats.
password | `string` | If set to false, the result will include kittens that have already been adopted.

# Transactions
## Recent Transactions

> Definition

```
GET https://merchant-api.cambi.io/api/v1/recentTransactions
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
    "message": "Logged in successfully"
}
```

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
### HTTP Endpoint

`GET https://merchant-api.cambi.io/api/v1/recentTransactions`

### Request Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
merchantId | `string` | If set to true, the result will also include cats.
merchantUserId | `string` | If set to false, the result will include kittens that have already been adopted.
days | String | If set to false, the result will include kittens that have already been adopted.

### Response JSON
Parameter | Type | Description
--------- | ------- | -----------
userName | `string` | If set to true, the result will also include cats.
password | `string` | If set to false, the result will include kittens that have already been adopted.