---
layout: page
---

# Search Donut Store by Name

In this tutorial, you'll learn how to search for a donut store by its name using the Donut Finder API. 

### Before You Start 

Before starting this tutorial, ensure you set up your test environment by following the steps outlined in the [Before you start a tutorial](../before-you-start-tutorial.md) section.

> Expect this tutorial to take about 10-5 minutes to complete.

## Tutorial: Search Donut Store by Name

To get started, you need to format and send a GET request to search for a donut store by its name.

### Use Postman to search for a donut store by name:

  - Open Postman and create a new request.

  - Set the request type to `GET`.

  - Enter the URL: 
    ```
    {base_url}/donut_store?store_name={name}
    ```
  Replace `{store_name}` with the name or partial name of the store you want to search for.

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
        }
      ]
      ```

### Use `curl` to search for a donut store by name:

  - Open your terminal.

  - Run the following `curl` command (replace `{store_name}` with the name or partial name of the store you want to search for):
      ```bash
      curl -X GET "{base_url}/donut_store?name={store_name}"
      ```

  - You should see a response containing the details of the matching donut stores in JSON format, similar to the example shown above.


**Note**: If no donut store name matches the search criteria, the service will return an empty array, indicating that there are no donut stores with the specified name.

## Summary

In this tutorial, you learned how to:

* Format a **GET** request to search for a donut store by name
* Use Postman to send a **GET** request to search for a donut store by name
* Use `curl` to send a **GET** request to search for a donut store by name