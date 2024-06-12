---
layout: page
---

# Search Donut Type by Name

## Overview

In this tutorial, you'll learn how to search for a specific donut type by its name in the Donut Finder API. This tutorial is intended for developers who need to find a particular donut type based on its name. It assumes you have basic knowledge of:

* RESTful APIs
* JSON format
* Tools like Postman or `curl`

By the end of this tutorial, you'll be able to:

* Understand how to format a GET request to search for a donut type by name
* Use Postman to search for a donut type by name
* Use `curl` to search for a donut type by name

## Background

The Donut Finder API allows users to manage and access information about various donut types. Searching for a donut type by name is useful when users want to find a specific donut type among the available options. This tutorial will guide you through the process of making a GET request to search for a donut type by name using the Donut Finder API.

---
> Expect this tutorial to take about 10-5 minutes to complete.
---

## Before You Start 

Before starting this tutorial, install Postman and json-server. Then, sync the To-Do service to your GitHub repository so that you can clone it to your desktop. For a complete set of steps, see [Before you start a tutorial](../before-you-start-tutorial.md).

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

## Summary

In this tutorial, you learned how to:

* Format a GET request to search for a donut type by name
* Use Postman to send a GET request to search for a donut type by name
* Use `curl` to send a GET request to search for a donut type by name

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Add a new donut type](add-new-donut-type.md)
* [Retrieve all donut types](get-a-list-of-donut-types.md)
* [Get details of a specific donut type by name](search-donut-types-by-name.md)
* [Update a donut type](update-a-donut-type.md)
