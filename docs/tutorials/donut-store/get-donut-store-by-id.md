---
layout: page
---

# Get Donut Store by ID

## Overview

In this tutorial, you'll learn how to retrieve the details of a specific donut store by its ID using the Donut Finder API.

### Before You Start 

Before starting this tutorial, ensure you set up your test environment by following the steps outlined in the [Before you start a tutorial](../before-you-start-tutorial.md) section.

---
> Expect this tutorial to take about 10-5 minutes to complete.
---

## Tutorial: Get Donut Store by ID

To get started, you need to format and send a GET request to retrieve a donut store by its ID.

> ⚠️ Anyways replace {base_url} with your base URL. For example, if your base URL is `http://localhost:3000`, then the URL should be `http://localhost:3000/donut_store`.

1. **Format the GET request**:

    The GET request requires the store ID to be included in the URL. For example, to get the store with `ID` of 1, the URL would be `{base_url}/donut_store/1`.

2. **Use Postman to get a donut store by ID**:

    a. Open Postman and create a new request.

    b. Set the request type to `GET`.

    c. Enter the URL: `{base_url}/donut_store/{id}` (replace `{id}` with the actual `store ID` you want to retrieve).

    d. Click the **Send** button. You should see a response containing the details of the specified donut store in JSON format. For example:

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

**Note**: If no donut store name matches the search criteria, the service will return an empty array ([]), indicating that there are no donut stores with the specified name.

## Summary

In this tutorial, you learned how to:

* Format a **GET** request to retrieve a specific donut store by ID
* Use Postman to send a **GET** request to retrieve a donut store by ID
* Use `curl` to send a **GET** request to retrieve a donut store by ID

---

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Add a new store](add-new-store.md)
* [Get details of a specific donut store](get-donut-store-by-id.md)
* [Update the inventory of a donut store](update-a-store.md)
* [Delete a donut store](delete-store.md)