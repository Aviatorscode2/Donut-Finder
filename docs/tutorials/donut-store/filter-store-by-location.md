---
layout: page
---

# Filter Store by Location

In this tutorial, you'll learn how to filter donut stores by their location using the Donut Finder API.

## Before You Start 

Before starting this tutorial, ensure you set up your test environment by following the steps outlined in the [installation guide](../../Quickstart/installation.md).

> Expect this tutorial to take about 10-5 minutes to complete.

## Tutorial: Filter Store by Location

To get started, you need to format and send a GET request to filter donut stores by their location.

### Use Postman to filter donut stores by location:

  - Open Postman and create a new request.

  - Set the request type to `GET`.

  - Enter the URL: 
      ```
      {base_url}/donut_store?street_address={location}
      ```
    Replace `{location}` with the location you want to filter by, e.g., "CA".

  - Click the **Send** button. You should see a response containing the details of the matching donut stores in JSON format. For example:

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

### Use `curl` to filter donut stores by location:

  - Open your terminal.

  - Run the following `curl` command (replace `{location}` with the location you want to filter by, e.g., "CA"):

      ```bash
      curl -X GET "{base_url}/donut_store?street_address={location}"
      ```

  - You should see a response containing the details of the matching donut stores in JSON format, similar to the Postman example above.

**Note**: If no donut store name matches the search criteria, the service will return an empty array, indicating that there are no donut stores with the specified name.

## Summary

In this tutorial, you learned how to:

* Format a **GET** request to filter donut stores by location
* Use Postman to send a **GET** request to filter donut stores by location
* Use `curl` to send a **GET** request to filter donut stores by location