# Parameters for successful requests

This section highlights the required and optional parameters for the operations of the Donut Finder service.

To get a successful response from the following operations, you must specify at least the `required` properties listed under each task. 

## Donut Store Endpoints

### Add a New Donut Store

| Property         | Type   | Description                                                         |
|------------------|--------|---------------------------------------------------------------------|
| store_name       | String | Required. The name of the donut store.                              |
| street_address   | String | Required. The street address of the donut store.                    |
| phone            | String | Required. The phone number of the donut store.                      |
| id               | Number | Optional. The unique identifier for the donut store.                |
| donut_inventory  | Array  | Optional. A list of donut types available at the store.             |

### Find donut store by id

| Property         | Type   | Description                                                         |
|------------------|--------|---------------------------------------------------------------------|
| id               | Number | Required. The unique identifier of the store.                       |

### Find donut store by name

| Property         | Type   | Description                                                         |
|------------------|--------|---------------------------------------------------------------------|
| store_name       | String | Required. The name of the donut store.                              |

### Find donut store by location

| Property         | Type   | Description                                                         |
|------------------|--------|---------------------------------------------------------------------|
| street_address   | String | Required. The street address of the donut store.                       |


### Delete a donut store by id

| Property         | Type   | Description                                                         |
|------------------|--------|---------------------------------------------------------------------|
| id               | Number | Required. The unique identifier of the store.                       |

### Update a donut store

| Property         | Type   | Description                                                         |
|------------------|--------|---------------------------------------------------------------------|
| id               | Number | Required. The unique identifier of the store.                       |
| store_name       | String | Optional. The name of the donut store.                              |
| street_address   | String | Optional. The street address of the donut store.                    |
| phone            | String | Optional. The phone number of the donut store.                      |
| donut_inventory  | Array  | Optional. A list of donut types available at the store.             |


## Donut Type Endpoints

### Add a new donut type

| Property         | Type   | Description                                                         |
|------------------|--------|---------------------------------------------------------------------|
| donut_name       | String | Required. The name of the donut type.                               |
| id               | Number | Optional. The unique identifier for the donut store.                |
| donut_stores	   | Array  | Optional. A list of store IDs where this donut type is available.   |

### Find donut type by ID

| Property         | Type   | Description                                                         |
|------------------|--------|---------------------------------------------------------------------|
| id               | Number | Required. The unique identifier of the store.                       |

### Find donut type by name

| Property         | Type   | Description                                                         |
|------------------|--------|---------------------------------------------------------------------|
| donut_name       | String | Required. The name of the donut type.                               |


### Delete a donut type

| Property         | Type   | Description                                                         |
|------------------|--------|---------------------------------------------------------------------|
| id               | Number | Required. The unique identifier of the donut type.                  |

### Update a donut type

| Property         | Type   | Description                                                         |
|------------------|--------|---------------------------------------------------------------------|
| id               | Number | Required. The unique identifier of the donut type.                  |
| donut_name       | String | Required. The name of the donut type.                               |
| donut_stores	   | Array  | Optional. A list of store IDs where this donut type is available.   |