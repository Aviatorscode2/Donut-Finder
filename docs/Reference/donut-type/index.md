# Donut Type API Reference

The Donut Type API provides endpoints to interact with donut type data in the Donut Finder service. You can retrieve information about donut types, as well as create, update, and delete donut type records.

The Donut Type API follows a REST architecture. You can access the API’s resources via HTTP requests, and responses are given in JSON format.

## Base URL

```shell
{base_url}/donut_type
```

## **Version**

The current API version is 1.0.

## **Endpoints**

### **Retrieve All Donut Types**

Returns a list of all available donut types, including their IDs and associated store IDs. Note: The number of records returned is not limited, but pagination options are not currently supported by this endpoint.

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
        "id": 1,
        "donut_stores": [1, 2]
    },
    {
        "donut_name": "cruller",
        "id": 2,
        "donut_stores": [1, 3]
    }
]
```

### **Retrieve a Donut Type by ID**

Fetches details of a specific donut type using its unique `id`.


#### Endpoint

```shell
GET {base_url}/donut_type/{id}
```

#### Path parameters

| Parameter name | Type | Required | Description |
| ---------------|------|----------|------------|
| `id` | number | required | The unique ID of the donut type. |

#### Request example

```shell
curl -X GET http://localhost:3000/donut_type/1
```

#### Response example

```json
{
    "donut_name": "bear claw",
    "id": 1,
    "donut_stores": [1, 2]
}
```

### **Create a New Donut Type**

Adds a new donut type to the database.

#### Endpoint

```shell
POST {base_url}/donut_type
```


#### Request body

In the request body, specify a JSON representation of the `donut_type` object. The following table lists the properties that are required when you add a new donut type.

| Field | Type | Required | Description |
| ------|-------|------|------------|
| `donut_name` | string | required | The name of the new donut type. |
| `donut_stores` | array | required | List of store IDs where it is available. |

#### Request example 

```bash
curl -X POST 'http://donutfinder.net/api/donut-type' \
    -H 'Content-Type: application/json' \
    -d '{
        "donut_name": "glazed",
        "donut_stores": [1, 3]
    }'
```

#### Response example

```json
{
    "donut_name": "glazed",
    "id": 5,
    "donut_stores": [1, 3]
}
```

### **Update a Donut Type**

Updates details of an existing donut type.

#### Endpoint

```shell
PUT {base_url}/donut_type/{id}
```

#### Path parameters

| Parameter name | Type | Required | Description |
| ---------------|------|----------|------------|
| `id` | number | required | The unique ID of the donut type. |

#### Request body

| Field | Type | Required | Description |
| ------|--------|------|------------|
| `donut_name` | string | optional | The updated name of the type. |
| `donut_stores` | array | optional | The updated address. 

#### Request example
```bash
curl -X PUT 'http://donutfinder.net/api/donut-type/1' \
    -H 'Content-Type: application/json' \
    -d '{
        "donut_name": "chocolate bear claw",
        "donut_stores": [1, 2, 4]
    }'
```

#### Response example

```json
{
    "donut_name": "chocolate bear claw",
    "id": 1,
    "donut_stores": [1, 2, 4]
}
```

### Delete a Donut Type

Deletes a donut type by its unique ID. If the specified ID does not exist, no action is taken, and an error message is returned in the response.

#### Endpoint

```shell
DELETE {base_url}/donut_type/{id}
```

#### Path parameters

| Parameter name | Type | Required | Description |
| ---------------| ------|---------|-------------|
| `id` | number | required | The unique ID of the donut type. |

#### Request example

```shell
curl -X DELETE http://localhost:3000/donut_type/1
```

#### Response example
```json
{
    "message": "Donut type deleted successfully."
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


For further assistance, contact our [support team](mailto:support@donuttype.com).