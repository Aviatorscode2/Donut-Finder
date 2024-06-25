---
layout: page
---

# Add a new store

In this tutorial, you'll learn how to add a new store to the Donut Finder API.

### Before You Start

Before starting this tutorial, ensure you set up your test environment by following the steps outlined in the [Before you start a tutorial](../before-you-start-tutorial.md) section.

---

> Expect this tutorial to take about 15 minutes to complete.

---

## Tutorial: Add a New Store

To get started, you need to format and send a **POST** request to add a new store.

> ⚠️ Anyways replace {base_url} with your base URL. For example, if your base URL is `http://localhost:3000`, then the URL should be `http://localhost:3000/donut_store`.

1. **Format the POST request**:

    The body of the POST request should contain the details of the new store in JSON format. For example:

    ```json
    {
        "store_name": "Glazed and Confused Donut Shop",
        "street_address": "5678 Sugar Lane, Sweetville, CA 91405",
        "phone": "(555) 456-7890",
        "id": 4,
        "donut inventory": [
            {
                "donut_type": "glazed",
                "variation_filling": "none",
                "variation_topping": "glazed, chocolate"
            }
        ]
    }
    ```

2. **Use Postman to add a new store**:

    a. Open Postman and create a new request.

    b. Set the request type to `POST`.

    c. Enter the URL: `{base_url}/donut_store`.

    d. Add a header with `Key: Content-Type` and `Value: application/json`.

    e. In the **Body** tab, choose **raw** and set the format to **JSON**. Enter the JSON data for the new store.

    f. Click the **Send** button. You should see a response indicating the success of the request, such as a status code `201 Created` and the details of the newly added store.

3. **Use `curl` to add a new store**:

    a. Open your terminal.

    b. Run the following `curl` command:

    ```bash
    curl -X POST {base_url}/donut_store \
    -H "Content-Type: application/json" \
    -d '{
        "store_name": "Glazed and Confused Donut Shop",
        "street_address": "5678 Sugar Lane, Sweetville, CA 91405",
        "phone": "(555) 456-7890",
        "id": 4,
        "donut inventory": [
            {
                "donut_type": "glazed",
                "variation_filling": "none",
                "variation_topping": "glazed, chocolate"
            }
        ]
    }'
    ```

    c. You should see a response indicating the success of the request, such as a status code `201 Created` and the details of the newly added store.

## Summary

In this tutorial, you learned how to:

* Format a **POST** request to add a new store
* Use Postman to send a **POST** request to add a new store
* Use `curl` to send a **POST** request to add a new store

---

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Get all donut stores](get-list-of-donut-stores.md)
* [Get details of a specific donut store](get-donut-store-by-id.md)
* [Update the inventory of a donut store](update-a-store.md)
