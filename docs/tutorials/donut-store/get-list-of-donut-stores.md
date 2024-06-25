---
layout: page
---

# Get All Donut Stores

In this tutorial, you'll learn how to retrieve a list of all donut stores from the Donut Finder API.

### Before You Start 

Before starting this tutorial, ensure you set up your test environment by following the steps outlined in the [Before you start a tutorial](../before-you-start-tutorial.md) section.

---
> Expect this tutorial to take about 5 minutes to complete.
---

## Tutorial: Get All Donut Stores

To get started, you need to format and send a GET request to retrieve all donut stores.

> ⚠️ Anyways replace {base_url} with your base URL. For example, if your base URL is `http://localhost:3000`, then the URL should be `http://localhost:3000/donut_store`.

1. **Format the GET request**:

    The GET request does not require a body, only the correct endpoint URL.

2. **Use Postman to get all donut stores**:

    a. Open Postman and create a new request.

    b. Set the request type to `GET`.

    c. Enter the URL: `{base_url}/donut_store`.

    d. Click the **Send** button. You should see a response containing a list of all donut stores in JSON format. For example:

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

* Format a **GET** request to retrieve all donut stores
* Use Postman to send a **GET** request to retrieve all donut stores
* Use `curl` to send a **GET** request to retrieve all donut stores

---

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Add a new store](add-new-store.md)
* [Get details of a specific donut store](get-donut-store-by-id.md)
* [Update the inventory of a donut store](update-a-store.md)
