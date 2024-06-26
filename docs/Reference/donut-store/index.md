# Donut Store API Reference

## Overview

The Donut Store API provides endpoints to interact with donut shop data in the Donut Finder service. It allows you to retrieve information about donut shops, as well as create, update, and delete donut shop records.

The Donut Store API follows a REST architecture. You can access the API’s resources via HTTP requests, and responses are given in JSON format.

## Base URL

The API reference docs refer to a `{base_url}` when they refer to the URL of a resource. The `{base_url}` value depends on the installation of the service.

When running a local test, the `{base_url}` is generally `http://localhost:3000`.

```shell
{base_url}/donut_store
```

## Version

The current API version is 1.0.

## Events

The Donut Store API supports the following events: `donut_store added`, `donut_store updated`,`donut_store deleted`, etc.

### Get a list of all donut store

Retrieves a list of all donut store.

#### Endpoint

```shell
GET {base_url}/donut_store
```

#### Request example

```shell
curl -X GET http://localhost:3000/donut_store
```

#### Response example 

```json
[
    {
        "store_name": "Honey Kettle Donut Shop",
        "street_address": "1234 Nectar Ave, Honeyville, CA 91401 ",
        "phone": "(555) 123-1234",
        "id": "1",
        "donut inventory": [
            {
                "donut_type": "bear claw",
                "variation_filling": "almond paste, raspberry, chocolate, vanilla cream",
                "variation_topping": "chocolate, powdered sugar"
            },
            {
                "donut_type": "cruller",
                "variation_filling": "none",
                "variation_topping": "chocolate, glazed, maple, pink"
            }
        ]
    },
    {
        "store_name": "Michaelangelo's Morsels",
        "street_address": "222 Yum Drive, Chocolate, CA 91403",
        "phone": "(555) 222-2212",
        "id": "2",
        "donut inventory": [
            {
                "donut_type": "bear claw",
                "variation_filling": "none",
                "variation_topping": "chocolate, glazed, maple, pink"
            },
            {
                "donut_type": "donut holes",
                "variation_filling": "none",
                "variation_topping": "chocolate, glazed"
            }
        ]
    }
]
```

### Get details for a specific donut store

Retrieves details for a donut shop specified by the `id` parameter, if it exists.

#### Endpoint

```shell
GET {base_url}/donut_store/{id}
```

#### Path parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The record ID of the donut store to return |

#### Request example

```shell
curl -X GET http://localhost:3000/donut_store/1
```

#### Response example

```json
{
    "store_name": "Honey Kettle Donut Shop",
    "street_address": "1234 Nectar Ave, Honeyville, CA 91401 ",
    "phone": "(555) 123-1234",
    "id": "1",
    "donut inventory": [
        {
            "donut_type": "bear claw",
            "variation_filling": "almond paste, raspberry, chocolate, vanilla cream",
            "variation_topping": "chocolate, powdered sugar"
        },
        {
            "donut_type": "cruller",
            "variation_filling": "none",
            "variation_topping": "chocolate, glazed, maple, pink"
        },
        {
            "donut_type": "donut holes",
            "variation_filling": "none",
            "variation_topping": "chocolate, glazed"
        },
        {
            "donut_type": "jelly",
            "variation_filling": "lemon, cherry, raspberry, vanilla cream",
            "variation_topping": "glazed, powdered sugar"
        }
    ]
}
```

### Add a new donut store

Adds a new donut shop to the donut store collection.

#### Endpoint

```shell
POST {base_url}/donut_store
```

#### Request headers



#### Request body

In the request body, specify a JSON representation of the `donut_store` object. The following table lists the properties that are required when you add a new donut store. 

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `store_name` | string | The name of the donut store |
| `street_address` | string | The street address of the donut store |
| `phone` | string | The phone number of the donut shop |
| `donut inventory` | array | An array of donut items in the donut store's inventory |

#### Request example 

```bash
curl -X POST http://localhost:3000/donut_store \ 
    -H "Content-Type: application/json" \
    -d '{
        "store_name": "Honey Kettle Donut Shop",
        "street_address": "1234 Nectar Ave, Honeyville, CA 91401 ",
        "phone": "(555) 123-1234",
        "donut inventory": [
            {
                "donut_type": "bear claw",
                "variation_filling": "almond paste, raspberry, chocolate, vanilla cream",
                "variation_topping": "chocolate, powdered sugar"
            }
        ]
        }
```

```bash
curl -X POST -H "Content-Type: application/json"
     -d  '{
        "store_name": "Honey Kettle Donut Shop",
        "street_address": "1234 Nectar Ave, Honeyville, CA 91401 ",
        "phone": "(555) 123-1234",
        "donut inventory": [
            {
                "donut_type": "bear claw",
                "variation_filling": "almond paste, raspberry, chocolate, vanilla cream",
                "variation_topping": "chocolate, powdered sugar"
            }
        ]
        }'
     http://localhost:3000/donut_store
```

#### Response example

```json
{
     "store_name": "Honey Kettle Donut Shop",
        "street_address": "1234 Nectar Ave, Honeyville, CA 91401 ",
        "phone": "(555) 123-1234",
        "donut inventory": [
            {
                "donut_type": "bear claw",
                "variation_filling": "almond paste, raspberry, chocolate, vanilla cream",
                "variation_topping": "chocolate, powdered sugar"
            }
        ]
}
```

### Update an existing donut store

Updates an existing donut shop in the donut store collection.

#### Endpoint

```shell
PUT {base_url}/donut_store/{id}
```

#### Path parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The record ID of the donut store to update |

#### Request headers

### Delete a donut store

Deletes a donut shop from the donut store collection.

#### Endpoint

```shell
DELETE {base_url}/donut_store/{id}
```

#### Path parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The record ID of the donut store to delete |

#### Request example

```shell
curl -X DELETE http://localhost:3000/donut_store/1
```

#### Request headers

None

#### Request body

None

#### Return body

None

### Error responses

The following table lists the possible error responses.




## Response schema
