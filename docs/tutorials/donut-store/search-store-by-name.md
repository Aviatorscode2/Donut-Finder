---
layout: page
---

# Search Donut Store by Name

## Overview

In this tutorial, you'll learn how to search for a donut store by its name using the Donut Finder API. This tutorial is intended for developers who need to access information about specific donut stores based on their names. It assumes you have basic knowledge of:

* RESTful APIs
* JSON format
* Tools like Postman or `curl`

By the end of this tutorial, you'll be able to:

* Understand how to format a GET request to search for a donut store by name
* Use Postman to search for a donut store by name
* Use `curl` to search for a donut store by name

## Background

The Donut Finder API allows users to manage and access information about various donut stores and their inventories. Searching for a donut store by its name is a common operation that enables users to find stores quickly based on partial or full name matches. This tutorial will guide you through the process of making a GET request to search for a donut store by name using the Donut Finder API.

---
> Expect this tutorial to take about 10-5 minutes to complete.
---

## Before You Start 

Before starting this tutorial, install Postman and json-server. Then, sync the To-Do service to your GitHub repository so that you can clone it to your desktop. For a complete set of steps, see [Before you start a tutorial](../before-you-start-tutorial.md).

## Search Donut Store by Name

To get started, you need to format and send a GET request to search for a donut store by its name.

> ⚠️ Anyways replace {base_url} with your base URL. For example, if your base URL is `http://localhost:3000`, then the URL should be `http://localhost:3000/donut_store`.

1. **Format the GET request**:

    The GET request requires the store name to be included as a query parameter in the URL. For example, to search for stores with the name "Honey", the URL would be `http://localhost:3000/donut_store?name=Honey`.

2. **Use Postman to search for a donut store by name**:

    a. Open Postman and create a new request.

    b. Set the request type to `GET`.

    c. Enter the URL: `{base_url}/donut_store?name={name}` (replace `{name}` with the name or partial name of the store you want to search for).

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
    ]
    ```

3. **Use `curl` to search for a donut store by name**:

    a. Open your terminal.

    b. Run the following `curl` command (replace `{name}` with the name or partial name of the store you want to search for):

    ```bash
    curl -X GET "{base_url}/donut_store?name={name}"
    ```

    c. You should see a response containing the details of the matching donut stores in JSON format, similar to the example shown above.


**Note**: If no donut store name matches the search criteria, the service will return an empty array ([]), indicating that there are no donut stores with the specified name.

## Summary

In this tutorial, you learned how to:

* Format a GET request to search for a donut store by name
* Use Postman to send a GET request to search for a donut store by name
* Use `curl` to send a GET request to search for a donut store by name

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Add a new store](add-new-store.md)
* [Retrieve all donut stores](get-list-of-donut-stores.md)
* [Get details of a specific donut store by ID](get-donut-store-by-id.md)
* [Delete a donut store](delete-store.md)
