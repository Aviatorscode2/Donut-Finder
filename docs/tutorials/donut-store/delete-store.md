---
layout: page
---

# Delete a Donut Store

## Overview

In this tutorial, you'll learn how to delete a donut store from the Donut Finder API. This tutorial is intended for developers who need to manage the list of donut stores by removing stores that are no longer relevant. It assumes you have basic knowledge of:

* RESTful APIs
* JSON format
* Tools like Postman or `curl`

By the end of this tutorial, you'll be able to:

* Understand how to format a DELETE request to remove a donut store
* Use Postman to delete a donut store
* Use `curl` to delete a donut store

## Background

The Donut Finder API allows users to manage and access information about various donut stores and their inventories. Deleting a donut store can be necessary for maintaining an up-to-date list of available stores. This tutorial will guide you through the process of making a DELETE request to remove a store from the database using the Donut Finder API.

## Before You Start 

Before starting this tutorial, install Postman and json-server. Then, sync the To-Do service to your GitHub repository so that you can clone it to your desktop. For a complete set of steps, see [Before you start a tutorial](../before-you-start-tutorial.md).


## Delete a Donut Store

To get started, you need to format and send a DELETE request to remove a donut store by its ID.

> ⚠️ Anyways replace {base_url} with your base URL. For example, if your base URL is `http://localhost:3000`, then the URL should be `http://localhost:3000/donut_store`.

1. **Format the DELETE request**:

    The DELETE request requires the store ID to be included in the URL. For example, to delete the store with ID 1, the URL would be `http://localhost:3000/donut_store/1`.

2. **Use Postman to delete a donut store**:

    a. Open Postman and create a new request.

    b. Set the request type to `DELETE`.

    c. Enter the URL: `http://localhost:3000/donut_store/{id}` (replace `{id}` with the actual store ID you want to delete).

    d. Click the "Send" button. You should see a response indicating the success of the request, such as a status code `200 OK` or `204 No Content`.

3. **Use `curl` to delete a donut store**:

    a. Open your terminal.

    b. Run the following `curl` command (replace `{id}` with the actual store ID you want to delete):

    ```bash
    curl -X DELETE http://localhost:3000/donut_store/{id}
    ```

    c. You should see a response indicating the success of the request, such as a status code `200 OK` or `204 No Content`.

## Summary

In this tutorial, you learned how to:

* Format a DELETE request to remove a donut store
* Use Postman to send a DELETE request to remove a donut store
* Use `curl` to send a DELETE request to remove a donut store

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Add a new store](link-to-tutorial)
* [Retrieve all donut stores](link-to-tutorial)
* [Get details of a specific donut store](link-to-tutorial)
