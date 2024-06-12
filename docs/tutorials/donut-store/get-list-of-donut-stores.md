---
layout: page
---

# Get All Donut Stores

## Overview

In this tutorial, you'll learn how to retrieve a list of all donut stores from the Donut Finder API. This tutorial is intended for developers who want to access and display information about all available donut stores. It assumes you have basic knowledge of:

* RESTful APIs
* JSON format
* Tools like Postman or `curl`

By the end of this tutorial, you'll be able to:

* Understand how to format a GET request to retrieve all donut stores
* Use Postman to retrieve all donut stores
* Use `curl` to retrieve all donut stores

## Background

The Donut Finder API allows users to manage and access information about various donut stores and their inventories. Retrieving a list of all donut stores is a common operation that enables users to view and interact with the available stores. This tutorial will guide you through the process of making a GET request to retrieve all donut stores using the Donut Finder API.

---
> Expect this tutorial to take about 5 minutes to complete.
---

## Before You Start 

Before starting this tutorial, install Postman and json-server. Then, sync the To-Do service to your GitHub repository so that you can clone it to your desktop. For a complete set of steps, see [Before you start a tutorial](../before-you-start-tutorial.md).

## Get All Donut Stores

To get started, you need to format and send a GET request to retrieve all donut stores.

> ⚠️ Anyways replace {base_url} with your base URL. For example, if your base URL is `http://localhost:3000`, then the URL should be `http://localhost:3000/donut_store`.

1. **Format the GET request**:

    The GET request does not require a body, only the correct endpoint URL.

2. **Use Postman to get all donut stores**:

    a. Open Postman and create a new request.

    b. Set the request type to `GET`.

    c. Enter the URL: `{base_url}/donut_store`.

    d. Click the "Send" button. You should see a response containing a list of all donut stores in JSON format. For example:

    ```json
    [
      {
        "store_name": "Honey Kettle Donut Shop",
        "street_address": "1234 Nectar Ave, Honeyville, CA 91401",
        "phone": "(555) 123-1234",
        "id": 1,
        "donut inventory": [
          {
            "donut_type": "bear claw",
            "variation_filling": "almond paste, raspberry, chocolate, vanilla cream",
            "variation_topping": "chocolate, powdered sugar"
          },
          // More donuts...
        ]
      },
      {
        "store_name": "Michaelangelo's Morsels",
        "street_address": "222 Yum Drive, Chocolate, CA 91403",
        "phone": "(555) 222-2212",
        "id": 2,
        "donut inventory": [
          {
            "donut_type": "bear claw",
            "variation_filling": "none",
            "variation_topping": "chocolate, glazed, maple, pink"
          },
          // More donuts...
        ]
      },
      // More stores...
    ]
    ```

3. **Use `curl` to get all donut stores**:

    a. Open your terminal.

    b. Run the following `curl` command:

    ```bash
    curl -X GET {base_url}/donut_store
    ```

    c. You should see a response containing a list of all donut stores in JSON format, similar to the example shown above.

## Summary

In this tutorial, you learned how to:

* Format a GET request to retrieve all donut stores
* Use Postman to send a GET request to retrieve all donut stores
* Use `curl` to send a GET request to retrieve all donut stores

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Add a new store](add-new-store.md)
* [Get details of a specific donut store](get-donut-store-by-id.md)
* [Update the inventory of a donut store](update-a-store.md)
