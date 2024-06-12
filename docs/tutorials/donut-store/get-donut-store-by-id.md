---
layout: page
---

# Get Donut Store by ID

## Overview

In this tutorial, you'll learn how to retrieve the details of a specific donut store by its ID using the Donut Finder API. This tutorial is intended for developers who need to access detailed information about a particular donut store. It assumes you have basic knowledge of:

* RESTful APIs
* JSON format
* Tools like Postman or `curl`

By the end of this tutorial, you'll be able to:

* Understand how to format a GET request to retrieve a specific donut store by ID
* Use Postman to retrieve a donut store by ID
* Use `curl` to retrieve a donut store by ID

## Background

The Donut Finder API allows users to manage and access information about various donut stores and their inventories. Retrieving the details of a specific donut store by its ID is a common operation that enables users to view detailed information about a particular store. This tutorial will guide you through the process of making a GET request to retrieve a donut store by its ID using the Donut Finder API.

---
> Expect this tutorial to take about 10-5 minutes to complete.
---

## Before You Start 

Before starting this tutorial, install Postman and json-server. Then, sync the To-Do service to your GitHub repository so that you can clone it to your desktop. For a complete set of steps, see [Before you start a tutorial](../before-you-start-tutorial.md).

## Get Donut Store by ID

To get started, you need to format and send a GET request to retrieve a donut store by its ID.

> ⚠️ Anyways replace {base_url} with your base URL. For example, if your base URL is `http://localhost:3000`, then the URL should be `http://localhost:3000/donut_store`.

1. **Format the GET request**:

    The GET request requires the store ID to be included in the URL. For example, to get the store with ID 1, the URL would be `{base_url}/donut_store/1`.

2. **Use Postman to get a donut store by ID**:

    a. Open Postman and create a new request.

    b. Set the request type to `GET`.

    c. Enter the URL: `{base_url}/donut_store/{id}` (replace `{id}` with the actual store ID you want to retrieve).

    d. Click the "Send" button. You should see a response containing the details of the specified donut store in JSON format. For example:

    ```json
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
        {
          "donut_type": "cruller",
          "variation_filling": "none",
          "variation_topping": "chocolate, glazed, maple, pink"
        },
        // More donuts...
      ]
    }
    ```

3. **Use `curl` to get a donut store by ID**:

    a. Open your terminal.

    b. Run the following `curl` command (replace `{id}` with the actual store ID you want to retrieve):

    ```bash
    curl -X GET {base_url}/donut_store/{id}
    ```

    c. You should see a response containing the details of the specified donut store in JSON format, similar to the example shown above.

## Summary

In this tutorial, you learned how to:

* Format a GET request to retrieve a specific donut store by ID
* Use Postman to send a GET request to retrieve a donut store by ID
* Use `curl` to send a GET request to retrieve a donut store by ID

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Add a new store](link-to-tutorial)
* [Retrieve all donut stores](link-to-tutorial)
* [Update the inventory of a donut store](link-to-tutorial)
* [Delete a donut store](link-to-tutorial)