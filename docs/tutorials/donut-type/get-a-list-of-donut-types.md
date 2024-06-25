---
layout: page
---

# Get All Donut Types

In this tutorial, you'll learn how to retrieve a list of all available donut types from the Donut Finder API. 

### Before You Start 

Before starting this tutorial, ensure you set up your test environment by following the steps outlined in the [Before you start a tutorial](../before-you-start-tutorial.md) section.

---
> Expect this tutorial to take about 10-5 minutes to complete.
---

## Tutorial: Get All Donut Types

To get started, you need to format and send a GET request to retrieve all donut types.

> ⚠️ Anyways replace {base_url} with your base URL. For example, if your base URL is `http://localhost:3000`, then the URL should be `http://localhost:3000/donut_store`.

1. **Format the GET request**:

    The GET request does not require any additional parameters. Simply use the URL `{base_url}/donut_type` to retrieve all donut types.

2. **Use Postman to get all donut types**:

    a. Open Postman and create a new request.

    b. Set the request type to `GET`.

    c. Enter the URL: `{base_url}/donut_type`.

    d. Click the **Send** button. You should see a response containing the details of all donut types stored in the system in JSON format.

3. **Use `curl` to get all donut types**:

    a. Open your terminal.

    b. Run the following `curl` command:

    ```bash
    curl -X GET "{base_url}/donut_type"
    ```

    c. You should see a response containing the details of all donut types stored in the system in JSON format.

## Summary

In this tutorial, you learned how to:

* Format a **GET** request to retrieve all donut types
* Use Postman to send a **GET** request to retrieve all donut types
* Use `curl` to send a **GET** request to retrieve all donut types

---

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Add a new donut type](add-new-donut-type.md)
* [Retrieve all donut types](get-a-list-of-donut-types.md)
* [Get details of a specific donut type by name](search-donut-types-by-name.md)
* [Update a donut type](update-a-donut-type.md)

