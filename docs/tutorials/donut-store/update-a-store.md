---
layout: page
---

# Update a Donut Store

In this tutorial, you'll learn how to update the details of an existing donut store using the Donut Finder API.

### Before You Start 

Before starting this tutorial, ensure you set up your test environment by following the steps outlined in the [Before you start a tutorial](../before-you-start-tutorial.md) section.

---
> Expect this tutorial to take about 10-5 minutes to complete.
---

## Tutorial: Update a Donut Store

To get started, you need to format and send a PUT request to update the details of an existing donut store.

> ⚠️ Anyways replace {base_url} with your base URL. For example, if your base URL is `http://localhost:3000`, then the URL should be `http://localhost:3000/donut_store`.

1. **Format the PUT request**:

    The PUT request requires the store's ID to be included in the URL and the updated details to be included in the request body. For example, to update the store with ID 1, the URL would be `{base_url}/donut_store/1`.

2. **Use Postman to update a donut store**:

    a. Open Postman and create a new request.

    b. Set the request type to `PUT`.

    c. Enter the URL: `{base_url}/donut_store/{id}` (replace `{id}` with the `ID` of the store you want to update).

    d. In the "Body" tab, select "raw" and set the format to JSON.

    e. Enter the updated store details in JSON format. For example:

    ```json
    {
      "store_name": "Honey Kettle Donut Shop",
      "street_address": "1234 Nectar Ave, Honeyville, CA 91401",
      "phone": "(555) 123-1234"
    }
    ```

    f. Click the **Send** button. You should see a response indicating the store was successfully updated.

3. **Use `curl` to update a donut store**:

    a. Open your terminal.

    b. Run the following `curl` command (replace `{id}` with the ID of the store you want to update, and include the updated store details in JSON format):

    ```bash
    curl -X PUT "{base_url}/donut_store/{id}" \
    -H "Content-Type: application/json" \
    -d '{
          "store_name": "Honey Kettle Donut Shop",
          "street_address": "1234 Nectar Ave, Honeyville, CA 91401",
          "phone": "(555) 123-1234"
        }'
    ```

    c. You should see a response indicating the store was successfully updated.

## Summary

In this tutorial, you learned how to:

* Format a **PUT** request to update a donut store
* Use Postman to send a **PUT** request to update a donut store
* Use `curl` to send a **PUT** request to update a donut store

---

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Search donut store by name](search-store-by-name.md)
* [Get details of a specific donut store by ID](get-donut-store-by-id.md)
* [update donut store details](update-a-store.md)
* [Delete a donut store](delete-store.md)
