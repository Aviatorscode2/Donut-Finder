---
layout: page
---

# Update a Donut Type

## Overview

In this tutorial, you'll learn how to update the details of a donut type in the Donut Finder API. This tutorial is intended for developers who need to modify the information associated with an existing donut type. It assumes you have basic knowledge of:

* RESTful APIs
* JSON format
* Tools like Postman or `curl`

By the end of this tutorial, you'll be able to:

* Understand how to format a PUT request to update a donut type
* Use Postman to update a donut type
* Use `curl` to update a donut type

## Background

The Donut Finder API allows users to manage and access information about various donut types. Updating a donut type is necessary when there are changes to its details, such as the name or variations. This tutorial will guide you through the process of making a PUT request to update a donut type using the Donut Finder API.

---
> Expect this tutorial to take about 10-5 minutes to complete.
---

## Before You Start 

Before starting this tutorial, install Postman and json-server. Then, sync the To-Do service to your GitHub repository so that you can clone it to your desktop. For a complete set of steps, see [Before you start a tutorial](../before-you-start-tutorial.md).

## Update a Donut Type

To get started, you need to format and send a PUT request to update a donut type.

> ⚠️ Anyways replace {base_url} with your base URL. For example, if your base URL is `http://localhost:3000`, then the URL should be `http://localhost:3000/donut_store`.

1. **Format the PUT request**:

    The PUT request requires the ID of the donut type to be included in the URL, along with the updated details in the request body. For example, to update the donut type with ID 1, the URL would be `http://localhost:3000/donut_type/1`, and the request body would contain the updated details.

2. **Use Postman to update a donut type**:

    a. Open Postman and create a new request.

    b. Set the request type to `PUT`.

    c. Enter the URL: `{base_url}/donut_type/{id}` (replace `{id}` with the ID of the donut type you want to update).

    d. In the "Body" tab, select "raw" and set the format to JSON.

    e. Enter the updated details of the donut type in JSON format. For example:

    ```json
    {
      "donut_name": "new_donut_name",
      "donut_stores": [2, 3]
    }
    ```

    f. Click the "Send" button. You should see a response indicating the donut type was successfully updated.

3. **Use `curl` to update a donut type**:

    a. Open your terminal.

    b. Run the following `curl` command (replace `{id}` with the ID of the donut type you want to update):

    ```bash
    curl -X PUT "{base_url}/donut_type/{id}" \
    -H "Content-Type: application/json" \
    -d '{
          "donut_name": "pepperoni",
          "donut_stores": [2, 3]
        }'
    ```

    c. You should see a response indicating the donut type was successfully updated.

## Summary

In this tutorial, you learned how to:

* Format a PUT request to update a donut type
* Use Postman to send a PUT request to update a donut type
* Use `curl` to send a PUT request to update a donut type

## Next Steps

Consider completing some other common tasks using the Donut Finder API:

* [Delete a new donut type](delete-a-donut-type.md)
* [Retrieve all donut types](get-a-list-of-donut-types.md)
* [Get details of a specific donut type by name](search-donut-types-by-name.md)
* [Update a donut type](update-a-donut-type.md)
