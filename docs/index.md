---
layout: page
---

# Donut Finder Service Documentation

The Donut Finder service is designed to help users find their favorite donut types at local donut shops. This documentation provides an overview of the service's functionality and available endpoints.

## Quickstart

To get started with the Donut Finder service, check out our [quickstart guide](api/quickstart.md)

## Tutorials

Learn how to perform common tasks with the Donut Finder service.

#### Donut Store Management

Learn how to manage donut shops using the Donut Finder service.
* [Add a new donut store](tutorials/donut-store/add-new-store.md)
* [Update an existing donut store](tutorials/donut-store/update-a-store.md)
* [Delete a donut store](tutorials/donut-store/delete-store.md)

#### Donut Type Management

Learn how to manage donut types using the Donut Finder service.
* [Add a new donut type](tutorials/donut-type/add-new-donut-type.md)
* [Update an existing donut type](tutorials/donut-type/update-a-donut-type.md)
* [Delete a donut type](tutorials/donut-type/delete-a-donut-type.md)

#### Donut Inventory Management

Learn how to manage donut inventory using the Donut Finder service.
* [Add a new donut to a store's inventory](#)
* [Update a donut in a store's inventory](#)
* [Remove a donut from a store's inventory](#)

## API Reference

Detailed information about the Donut Finder service's resources and endpoints.

* [Donut Shop Endpoints](api/donut-store/index.md)
* [Donut Type Endpoints](api/donut-type/index.md)

## Database Schema
The Donut Finder service uses the following database schema:

```json
{
    "donut_store": [
      {
        "store_name": "Honey Kettle Donut Shop",
        "street_address": "1234 Nectar Ave, Honeyville, CA 91401 ",
        "phone": "(555) 123-1234",
        "id": 1,
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
      },
    ],
    "donut_type": [
        {
            "donut_name": "bear claw",
            "id": 1,
            "donut_stores": [1, 2]
        }
      ]
  }
```

The `donut_store` collection contains information about each donut shop, including its name, address, phone number, and a list of available donut types with their fillings and toppings. The donut_type collection stores details about each donut type, including its name and a list of donut shops that offer it.

## Handling Errors
The Donut Finder service API follows standard HTTP status codes to indicate the outcome of API requests. Here are some common error scenarios and their corresponding HTTP status codes:
* **404 Not Found**: The requested resource could not be found.
* **400 Bad Request**: The request was invalid or cannot be processed.
* **500 Internal Server Error**: An unexpected error occurred on the server.

## Properties Cheat Sheet for Successful Requests
Here is a list of properties that are commonly used in the Donut Finder service API:
* **store_name**: The name of the donut shop.
* **street_address**: The street address of the donut shop.
* **phone**: The phone number of the donut shop.
* **donut_type**: The name of the donut type.
* **variation_filling**: The fillings available for the donut type.
* **variation_topping**: The toppings available for the donut type.

## Example Requests
Here are some example requests to get you started:
* Get a list of all donut shops:

 ```shell
 GET http://localhost:3000/donut_store
 ```

* Get details for a specific donut shop:

 ```shell
 GET http://localhost:3000/donut_store/1
 ```

* Get a list of all donut types:

 ```shell
 GET http://localhost:3000/donut_type
 ```
* Get details for a specific donut type:

 ```shell
 GET http://localhost:3000/donut_type/1
 ```
 
## Conclusion
The Donut Finder service API provides a simple and intuitive way to interact with donut shops and their available donut types. With this documentation, you should be able to get started with the API and begin building your own applications that utilize the Donut Finder service.