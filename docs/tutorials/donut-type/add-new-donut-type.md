---
layout: page
---

# Add New Donut Type

In this tutorial, you'll learn how to add a new type of donut to the Donut Finder API.

### Before You Start 

Before starting this tutorial, ensure you set up your test environment by following the steps outlined in the [Before you start a tutorial](../before-you-start-tutorial.md) section.

---
> Expect this tutorial to take about 10-5 minutes to complete.
---

## Tutorial: Add New Donut Type

To get started, you need to format and send a POST request to add a new type of donut.

> ⚠️ Anyways replace {base_url} with your base URL. For example, if your base URL is `http://localhost:3000`, then the URL should be `http://localhost:3000/donut_store`.

1. **Format the POST request**:

    The POST request requires the new donut type details to be included in the request body. For example, to add a new donut type called "glazed twist", the URL would be `http://localhost:3000/donut_type`, and the request body would contain the details of the new donut type.

2. **Use Postman to add a new donut type**:

    a. Open Postman and create a new request.

    b. Set the request type to `POST`.

    c. Enter the URL: `{base_url}/donut_type`.

    d. In the **Body** tab, select **raw** and set the format to JSON.

    e. Enter the details of the new donut type in JSON format. For example:

    ```json
    {
      "donut_name": "glazed twist"
    }
    ```

    f. Click the **Send** button. You should see a response indicating the new donut type was successfully added.

3. **Use `curl` to add a new donut type**:

    a. Open your terminal.

    b. Run the following `curl` command:

    ```bash
    curl -X POST "{base_url}/donut_type" \
    -H "Content-Type: application/json" \
    -d '{
          "donut_name": "glazed twist"
        }'
    ```

    c. You should see a response indicating the new donut type was successfully added.

## Summary

In this tutorial, you learned how to:

* Format a **POST** request to add a new donut type
* Use Postman to send a **POST** request to add a new donut type
* Use `curl` to send a **POST** request to add a new donut type

---

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Delete a new donut type](delete-a-donut-type.md)
* [Retrieve all donut types](get-a-list-of-donut-types.md)
* [Get details of a specific donut type by name](search-donut-types-by-name.md)
* [Update a donut type](update-a-donut-type.md)
