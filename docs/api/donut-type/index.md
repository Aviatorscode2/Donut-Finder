## Donut Type API Reference

Table of Content
## Overview

The Donut Type API provides endpoints to interact with donut type data in the Donut Finder service. It allows you to retrieve information about donut types, as well as create, update, and delete donut type records.

The Donut Type API follows a REST architecture. You can access the API’s resources via HTTP requests, and responses are given in JSON format.

## Base URL

The API reference docs refer to a `{base_url}` when they refer to the URL of a resource. The `{base_url}` value depends on the installation of the service.

When running a local test, the `{base_url}` is generally `http://localhost:3000`.

```shell
{base_url}/donut_type
```

## Version

The current API version is 1.0.

## Events

The Donut Type API supports the following events: `donut_type added`, `donut_type updated`, and `donut_type deleted`.

### Get a list of all donut type

Retrieves a list of all donut type.

#### Endpoint

```shell
GET {base_url}/donut_type
```

#### Request example

```shell
curl -X GET http://localhost:3000/donut_type
```

#### Response example

```json
[
    {
        "donut_name": "bear claw",
        "id": "1",
        "donut_stores": [
            1,
            2
        ]
    },
    {
        "donut_name": "cruller",
        "id": "2",
        "donut_stores": [
            1,
            3
        ]
    },
    {
        "donut_name": "donut holes",
        "id": "3",
        "donut_stores": [
            1,
            2,
            3
        ]
    },
    {
        "donut_name": "jelly",
        "id": "4",
        "donut_stores": [
            1,
            3
        ]
    }
]
```

### Get details for a specific donut type

Retrieves details for a donut type specified by the `id` parameter, if it exists.

#### Endpoint

```shell
GET {base_url}/donut_type/{id}
```

#### Path parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The record ID of the donut type to return |

#### Request example

```shell
curl -X GET http://localhost:3000/donut_type/1
```

#### Response example

```json
{
    "donut_name": "bear claw",
    "id": "1",
    "donut_stores": [
        1,
        2
    ]
}
```

## Response schema



* `GET /donut_store` - Get a list of all donut shops
* `GET /donut_store/{id}` - Get details for a specific donut shop
* `POST /donut_store` - Add a new donut shop
* `PUT /donut_store/{id}` - Update an existing donut shop
* `DELETE /donut_store/{id}` - Delete a donut shop