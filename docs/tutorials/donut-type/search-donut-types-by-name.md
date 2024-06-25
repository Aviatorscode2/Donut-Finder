---
layout: page
---

# Search Donut Type by Name


In this tutorial, you'll learn how to search for a specific donut type by its name in the Donut Finder API.

### Before You Start 

Before starting this tutorial, ensure you set up your test environment by following the steps outlined in the [Before you start a tutorial](../before-you-start-tutorial.md) section.

---
> Expect this tutorial to take about 10-5 minutes to complete.
---

## Search Donut Type by Name

To get started, you need to format and send a GET request to search for a donut type by name.

> ⚠️ Anyways replace {base_url} with your base URL. For example, if your base URL is `http://localhost:3000`, then the URL should be `http://localhost:3000/donut_store`.

1. **Format the GET request**:

    The GET request requires the donut type name to be included as a query parameter in the URL. For example, to search for a donut type named "glazed twist", the URL would be `{base_url}/donut_type?donut_name=glazed%20twist`.

2. **Use Postman to search for a donut type by name**:

    a. Open Postman and create a new request.

    b. Set the request type to `GET`.

    c. Enter the URL: `{base_url}/donut_type?donut_name={donut_name}` (replace `{donut_name}` with the name of the donut type you want to search for).

    d. Click the "Send" button. You should see a response containing the details of the matching donut type in JSON format.

3. **Use `curl` to search for a donut type by name**:

    a. Open your terminal.

    b. Run the following `curl` command (replace `{donut_name}` with the name of the donut type you want to search for):

    ```bash
    curl -X GET "{base_url}/donut_type?donut_name={donut_name}"
    ```

    c. You should see a response containing the details of the matching donut type in JSON format.

**Note**: If no donut store name matches the search criteria, the service will return an empty array ([]), indicating that there are no donut stores with the specified name.

## Summary

In this tutorial, you learned how to:

* Format a GET request to search for a donut type by name
* Use Postman to send a GET request to search for a donut type by name
* Use `curl` to send a GET request to search for a donut type by name

---

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Add a new donut type](add-new-donut-type.md)
* [Retrieve all donut types](get-a-list-of-donut-types.md)
* [Get details of a specific donut type by name](search-donut-types-by-name.md)
* [Update a donut type](update-a-donut-type.md)
