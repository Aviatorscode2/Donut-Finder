---
layout: page
---

# Filter Store by Location

## Overview

In this tutorial, you'll learn how to filter donut stores by their location using the Donut Finder API. This tutorial is intended for developers who need to access information about donut stores based on their geographic location. It assumes you have basic knowledge of:

* RESTful APIs
* JSON format
* Tools like Postman or `curl`

By the end of this tutorial, you'll be able to:

* Understand how to format a GET request to filter donut stores by location
* Use Postman to filter donut stores by location
* Use `curl` to filter donut stores by location

## Background

The Donut Finder API allows users to manage and access information about various donut stores and their inventories. Filtering stores by location is a common operation that enables users to find stores within a specific geographic area. This tutorial will guide you through the process of making a GET request to filter donut stores by location using the Donut Finder API.

---
> Expect this tutorial to take about 10-5 minutes to complete.
---

## Before You Start 

Before starting this tutorial, install Postman and json-server. Then, sync the To-Do service to your GitHub repository so that you can clone it to your desktop. For a complete set of steps, see [Before you start a tutorial](../before-you-start-tutorial.md).

## Filter Store by Location

> ⚠️ Anyways replace {base_url} with your base URL. For example, if your base URL is `http://localhost:3000`, then the URL should be `http://localhost:3000/donut_store`.

To get started, you need to format and send a GET request to filter donut stores by their location.

1. **Format the GET request**:

    The GET request requires the location to be included as a query parameter in the URL. For example, to filter stores in "CA", the URL would be `{base_url}/donut_store?location=CA`.

2. **Use Postman to filter donut stores by location**:

    a. Open Postman and create a new request.

    b. Set the request type to `GET`.

    c. Enter the URL: `{base_url}/donut_store?street_address={location}` (replace `{location}` with the location you want to filter by, e.g., "CA").

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
          {
            "donut_type": "donut holes",
            "variation_filling": "none",
            "variation_topping": "chocolate, glazed"
          }
        ]
      }
    ]
    ```

3. **Use `curl` to filter donut stores by location**:

    a. Open your terminal.

    b. Run the following `curl` command (replace `{location}` with the location you want to filter by, e.g., "CA"):

    ```bash
    curl -X GET "{base_url}/donut_store?street_address={location}"
    ```

    c. You should see a response containing the details of the matching donut stores in JSON format, similar to the example shown above.

## Summary

In this tutorial, you learned how to:

* Format a GET request to filter donut stores by location
* Use Postman to send a GET request to filter donut stores by location
* Use `curl` to send a GET request to filter donut stores by location

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Search donut store by name](search-store-by-name.md)
* [Get details of a specific donut store by ID](get-donut-store-by-id.md)
* [update donut store details](update-a-store.md)
* [Delete a donut store](delete-store.md)
