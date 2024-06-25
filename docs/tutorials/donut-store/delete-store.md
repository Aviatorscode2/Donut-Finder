---
layout: page
---

# Delete a Donut Store

In this tutorial, you'll learn how to delete a donut store from the Donut Finder API.


### Before You Start 

Before starting this tutorial, ensure you set up your test environment by following the steps outlined in the [Before you start a tutorial](../before-you-start-tutorial.md) section.

---
> Expect this tutorial to take about 5 minutes to complete.
---

## Tutorial: Delete a Donut Store

To get started, you need to format and send a DELETE request to remove a donut store by its ID.

> ⚠️ Anyways replace {base_url} with your base URL. For example, if your base URL is `http://localhost:3000`, then the URL should be `http://localhost:3000/donut_store`.

1. **Format the DELETE request**:

    The DELETE request requires the store ID to be included in the URL. For example, to delete the store with ID 1, the URL would be `{base_url}/donut_store/1`.

2. **Use Postman to delete a donut store**:

    a. Open Postman and create a new request.

    b. Set the request type to `DELETE`.

    c. Enter the URL: `{base_url}/donut_store/{id}` (replace `{id}` with the actual `store ID` you want to delete).

    d. Click the **Send** button. You should see a response indicating the success of the request, such as a status code `200 OK` or `204 No Content`.

3. **Use `curl` to delete a donut store**:

    a. Open your terminal.

    b. Run the following `curl` command (replace `{id}` with the actual `store ID` you want to delete):

    ```bash
    curl -X DELETE {base_url}/donut_store/{id}
    ```

    c. You should see a response indicating the success of the request, such as a status code `200 OK` or `204 No Content`.

## Summary

In this tutorial, you learned how to:

* Format a **DELETE** request to remove a donut store
* Use Postman to send a **DELETE** request to remove a donut store
* Use `curl` to send a **DELETE** request to remove a donut store

---

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Search donut store by name](search-store-by-name.md)
* [Get details of a specific donut store by ID](get-donut-store-by-id.md)
* [update donut store details](update-a-store.md)
* [Get donut store by location](filter-store-by-location.md)