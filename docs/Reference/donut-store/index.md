# Donut Store API Reference
The Donut Store API provides endpoints to interact with donut shop data in the Donut Finder service. This API allows you to retrieve information about donut shops, as well as create, update, and delete donut shop records.

## **Base URL**

```
{base_url}/donut_store
```

## **Version**

The current API version is 1.0.

## **Endpoints**

### **Retrieve All Donut Stores**

Returns a list of all donut stores and their inventory details.

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

### **Retrieve a Donut Store by ID**

Fetches details of a specific donut store by its unique `id`.

#### Endpoint

```shell
GET {base_url}/donut_store/{id}
```

#### Path parameters
| Parameter name   | Type   | Required    | Description                                                         |
|------------------|--------|-------------|---------------------------------------------------------------------|
| `id`             | number | required    | The unique ID of the donut store.                                   |


#### Request example

```shell
curl -X GET http://localhost:3000/donut_store/1
```

#### Response example

```json
{
  "store_name": "Honey Kettle Donut Shop",
  "street_address": "1234 Nectar Ave, Honeyville, CA 91401",
  "phone": "(555) 123-1234",
  "id": 1,
  "donut_inventory": [
    {
      "donut_type": "bear claw",
      "variation_filling": "almond paste, raspberry, chocolate, vanilla cream",
      "variation_topping": "chocolate, powdered sugar"
    }
  ]
}
```

### **Create a New Donut Store**

Adds a new donut store to the database.

#### Endpoint

```shell
POST {base_url}/donut_store
```


#### Request body

In the request body, specify a JSON representation of the `donut_store` object. The following table lists the properties that are required when you add a new donut store. 

| Field | Type | Required | Description |
|-------|-------|-------|-------------|
| `store_name` | string | required | The name of the donut store. |
| `street_address` | string | required | The street address of the donut store. |
| `phone` | string | required | The store’s contact phone number. |
| `donut inventory` | array | required | A list of donuts available.|

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

#### Response example

```json
{
  "id": 4,
  "message": "Donut store created successfully."
}
```

### **Update a Donut Store**

Updates details of an existing donut store.

#### Endpoint

```shell
PUT {base_url}/donut_store/{id}
```

#### Path parameters

| Parameter name | Type | Required | Description |
| ---------------|-------|--------|------------|
| `id` | number | required | The unique ID of the donut store. |

#### Request body

| Field | Type | Required | Description |
| ------|--------|---------| ------------|
| `store_name` | string | optional | The updated name of the store. |
| `street_address` | string | optional | The updated address. |
| `phone` | string | optional | The updated phone number. |
| `donut inventory` | array | optional | The updated inventory details.|

#### Request example
```bash
curl -X PUT 'http://donutfinder.api/v1/donut_store/1' \
    -H 'Content-Type: application/json' \
    -d '{
    "store_name": "Honey Kettle Donut House",
    "phone": "(555) 123-4321"
    }'
```

#### Response example

```json
{
    "id": 1,
    "message": "Donut store updated successfully."
}
```

### Delete a Donut Store

Deletes a donut store by its unique ID.

#### Endpoint

```shell
DELETE {base_url}/donut_store/{id}
```

#### Path parameters

| Parameter name | Type | Required | Description |
| --------------|-------|----------|-------------|
| `id` | number | required | The unique ID of the donut store. |

#### Request example

```shell
curl -X DELETE http://localhost:3000/donut_store/1
```

#### Response example
```json
{
    "message": "Donut store deleted successfully."
}
```

### Error responses

The API uses standard HTTP status codes to indicate the success or failure of a request.

| Status code | Description |
| ----------- | ----------- |
| 200 | Success |
| 201 | Resource created successfully |
| 400 | Bad request (e.g., missing required fields) |
| 404 | Resource not found |
| 500 | Internal server error |



For further assistance, contact our [support team](mailto:support@donutstore.com).
