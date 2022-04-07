## Overview

This website shows how GitHub page look likes and how it works.

A GitHub Page is a simple static website building with html, javascript and css.

## Authentication

> ### **_You can securely access your account's resources by authenticating to Coca-Cola, using different credentials depending on where you authenticate._**

To keep your account secure, you must authenticate before you can access certain resources on Coca-Cola. When you authenticate to Coca-Cola, you supply or confirm credentials that are unique to you to prove that you are exactly who you declare to be.

You can access your resources in Coca-Cola in a variety of ways: in the browser, via Coca-Cola authenticator or another authenticator application, with the API, or via the command line. Each way of accessing Coca-Cola supports different modes of authentication.

Username and password with two-factor authentication
Personal access token
SSH key

## List of RESTful APIs

See how to use our APIs to integrate third-party solutions to a single platform for all experiences.

### Order Create API

**_GET_** **_https://{accountName}.{environment}.com.br/api/catalog_system/pvt/products/GetProductAndSkuIds_**

Retrieves the IDs of all products and SKUs from a specific category by its category ID.

#### Query params:

| Attribute  | Type    | Description                                                                        |
| ---------- | ------- | ---------------------------------------------------------------------------------- |
| categoryId | integer | Replace this variable with the category ID that you need retrieves Product and SKU |
| \_from     | integer | Insert the number that will start the request result                               |
| \_to       | integer | Insert the number that will end the request result                                 |

#### Response object has the following properties:

| Attribute | Type   | Description                                                                                                       |
| --------- | ------ | ----------------------------------------------------------------------------------------------------------------- |
| data      | object | Object compose by Product IDs and SKU IDs, where the parent ID is from Products and the SKU IDs are the Child IDs |

#### Response body example:

```json
{
  "data": {
    "3": [5],
    "8": [310118453, 310118459, 310118463],
    "2": [3, 310118450, 310118451, 4, 8],
    "9": [
      310118454, 310118455, 310118456, 310118457, 310118458, 310118460,
      310118461, 310118462, 310118464
    ],
    "12": [310118490],
    "6": [],
    "7": [310118452],
    "1": [1, 123456, 310118449, 310118489, 7, 2],
    "5": [310118465],
    "4": [310118448],
    "10": [],
    "11": []
  },
  "range": {
    "total": 12,
    "from": 1,
    "to": 20
  }
}
```
