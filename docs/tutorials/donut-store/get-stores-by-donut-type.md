# Get Stores by Donut Type

## Overview

In this tutorial, you'll learn how to retrieve a list of donut stores that carry a specific type of donut using the Donut Finder API. This tutorial is intended for developers who need to filter stores based on their donut inventory. It assumes you have basic knowledge of:

* RESTful APIs
* JSON format
* Tools like Postman or `curl`

By the end of this tutorial, you'll be able to:

* Understand how to format a GET request to retrieve stores by donut type
* Use Postman to get stores by donut type
* Use `curl` to get stores by donut type

## Background

The Donut Finder API allows users to manage and access information about various donut stores and their inventories. Retrieving stores by donut type is a common operation that enables users to find stores that carry their favorite donuts. This tutorial will guide you through the process of making a GET request to retrieve stores by donut type using the Donut Finder API.

---
> Expect this tutorial to take about 10 minutes to complete.
---

## Before You Start 

Before starting this tutorial, install Postman and json-server. Then, sync the To-Do service to your GitHub repository so that you can clone it to your desktop. For a complete set of steps, see [Before you start a tutorial](../before-you-start-tutorial.md).

## Get Stores by Donut Type

To get started, you need to format and send a GET request to retrieve the stores that carry a specific type of donut.

> ⚠️ Anyways replace {base_url} with your base URL. For example, if your base URL is `http://localhost:3000`, then the URL should be `http://localhost:3000/donut_store`.

1. **Format the GET request**:

    The GET request requires the donut type to be included as a query parameter in the URL. For example, to retrieve stores that carry "cruller" donuts, the URL would be `{base_url}/donut_store?donut_type=cruller`.

2. **Use Postman to get stores by donut type**:

    a. Open Postman and create a new request.

    b. Set the request type to `GET`.

    c. Enter the URL: `{base_url}/donut_store?donut_type={donut_type}` (replace `{donut_type}` with the type of donut you want to filter by, e.g., "cruller").

    d. Click the "Send" button. You should see a response containing the details of the matching donut stores in JSON format. For example:

    ```json
    [
      {
        "store_name": "Honey Kettle Donut Shop",
        "street_address": "1234 Nectar Ave, Honeyville, CA 91401",
        "phone": "(555) 123-1234",
        "id": 1,
        "donut inventory": [
          {
            "donut_type": "cruller",
            "variation_filling": "none",
            "variation_topping": "chocolate, glazed, maple, pink"
          },
          // More donuts...
        ]
      },
      {
        "store_name": "Betsy's Best Donuts",
        "street_address": "998 Flavor Street, Cordial, CA 91403",
        "phone": "(555) 181-1181",
        "id": 3,
        "donut inventory": [
          {
            "donut_type": "cruller",
            "variation_filling": "none",
            "variation_topping": "chocolate, glazed, maple, pink"
          },
          // More donuts...
        ]
      }
    ]
    ```

3. **Use `curl` to get stores by donut type**:

    a. Open your terminal.

    b. Run the following `curl` command (replace `{donut_type}` with the type of donut you want to filter by, e.g., "cruller"):

    ```bash
    curl -X GET "{base_url}/donut_store?donut_type={donut_type}"
    ```

    c. You should see a response containing the details of the matching donut stores in JSON format, similar to the example shown above.

## Summary

In this tutorial, you learned how to:

* Format a GET request to retrieve stores by donut type
* Use Postman to send a GET request to retrieve stores by donut type
* Use `curl` to send a GET request to retrieve stores by donut type

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Add a new store](add-new-store.md)
* [Retrieve all donut stores](get-list-of-donut-stores.md)
* [Get details of a specific donut store by ID](get-donut-store-by-id.md)
* [Delete a donut store](delete-store.md)