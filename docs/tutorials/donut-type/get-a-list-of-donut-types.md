---
layout: page
---

# Get All Donut Types

## Overview

In this tutorial, you'll learn how to retrieve a list of all available donut types from the Donut Finder API. This tutorial is intended for developers who need to fetch the complete list of donut types stored in the system. It assumes you have basic knowledge of:

* RESTful APIs
* JSON format
* Tools like Postman or `curl`

By the end of this tutorial, you'll be able to:

* Understand how to format a GET request to retrieve all donut types
* Use Postman to get all donut types
* Use `curl` to get all donut types

## Background

The Donut Finder API allows users to manage and access information about various donut stores and their inventories. Retrieving all donut types is useful when displaying a list of available donut options to users. This tutorial will guide you through the process of making a GET request to retrieve all donut types using the Donut Finder API.

---
> Expect this tutorial to take about 5 minutes to complete.
---

## Before You Start 

Before starting this tutorial, install Postman and json-server. Then, sync the To-Do service to your GitHub repository so that you can clone it to your desktop. For a complete set of steps, see [Before you start a tutorial](../before-you-start-tutorial.md).

## Get All Donut Types

To get started, you need to format and send a GET request to retrieve all donut types.

> ⚠️ Anyways replace {base_url} with your base URL. For example, if your base URL is `http://localhost:3000`, then the URL should be `http://localhost:3000/donut_store`.

1. **Format the GET request**:

    The GET request does not require any additional parameters. Simply use the URL `{base_url}/donut_type` to retrieve all donut types.

2. **Use Postman to get all donut types**:

    a. Open Postman and create a new request.

    b. Set the request type to `GET`.

    c. Enter the URL: `{base_url}/donut_type`.

    d. Click the "Send" button. You should see a response containing the details of all donut types stored in the system in JSON format.

3. **Use `curl` to get all donut types**:

    a. Open your terminal.

    b. Run the following `curl` command:

    ```bash
    curl -X GET "{base_url}/donut_type"
    ```

    c. You should see a response containing the details of all donut types stored in the system in JSON format.

## Summary

In this tutorial, you learned how to:

* Format a GET request to retrieve all donut types
* Use Postman to send a GET request to retrieve all donut types
* Use `curl` to send a GET request to retrieve all donut types

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Add a new donut type](add-new-donut-type.md)
* [Retrieve all donut types](get-a-list-of-donut-types.md)
* [Get details of a specific donut type by name](search-donut-types-by-name.md)
* [Update a donut type](update-a-donut-type.md)

