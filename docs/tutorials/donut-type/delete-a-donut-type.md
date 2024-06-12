---
layout: page
---

# Delete a Donut Type

## Overview

In this tutorial, you'll learn how to delete a donut type from the Donut Finder API. This tutorial is intended for developers who need to remove existing donut types from the system. It assumes you have basic knowledge of:

* RESTful APIs
* JSON format
* Tools like Postman or `curl`

By the end of this tutorial, you'll be able to:

* Understand how to format a DELETE request to remove a donut type
* Use Postman to delete a donut type
* Use `curl` to delete a donut type

## Background

The Donut Finder API allows users to manage and access information about various donut stores and their inventories. Deleting donut types is necessary when certain types of donuts are no longer available. This tutorial will guide you through the process of making a DELETE request to remove a donut type using the Donut Finder API.

## Before You Start 

Before you start the tutorial, you should:

* Have a basic understanding of RESTful APIs and JSON format
* Have Postman installed, or know how to use `curl`
* Ensure your local development environment is set up and the Donut Finder API server is running on `http://localhost:3000`

## Delete a Donut Type

To get started, you need to format and send a DELETE request to remove a donut type.

1. **Format the DELETE request**:

    The DELETE request requires the ID of the donut type to be included in the URL. For example, to delete the donut type with ID 1, the URL would be `http://localhost:3000/donut_type/1`.

2. **Use Postman to delete a donut type**:

    a. Open Postman and create a new request.

    b. Set the request type to `DELETE`.

    c. Enter the URL: `http://localhost:3000/donut_type/{id}` (replace `{id}` with the ID of the donut type you want to delete).

    d. Click the "Send" button. You should see a response indicating the donut type was successfully deleted.

3. **Use `curl` to delete a donut type**:

    a. Open your terminal.

    b. Run the following `curl` command (replace `{id}` with the ID of the donut type you want to delete):

    ```bash
    curl -X DELETE "http://localhost:3000/donut_type/{id}"
    ```

    c. You should see a response indicating the donut type was successfully deleted.

## Summary

In this tutorial, you learned how to:

* Format a DELETE request to remove a donut type
* Use Postman to send a DELETE request to remove a donut type
* Use `curl` to send a DELETE request to remove a donut type

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Add a new store](link-to-tutorial)
* [Retrieve all donut stores](link-to-tutorial)
* [Get details of a specific donut store](link-to-tutorial)
* [Delete a donut store](link-to-tutorial)
