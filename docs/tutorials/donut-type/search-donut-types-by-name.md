---
layout: page
---

# How to Search for Donut Type by Name

In this tutorial, you'll learn how to search donut stores by their location using the Donut Finder API.

### Before You Start 

Before starting this tutorial, ensure you set up your test environment by following the steps outlined in the [installation guide](../../Quickstart/installation.md).

> Expect this tutorial to take about 5-3 minutes to complete.

## Search Donut Type by Name


### Use Postman to search for a donut type by name:

- Open Postman and create a new request.

- Set the request type to `GET`.

- Enter the URL: 
    ```
    {base_url}/donut_type?donut_name={donut_name}
    ```
    Replace `{donut_name}` with the name of the donut type you want to search for.

- Click the "Send" button. You should see a response containing the details of the matching donut type in JSON format.

### Use `curl` to search for a donut type by name:

- Open your terminal.

- Run the following `curl` command (replace `{donut_name}` with the name of the donut type you want to search for):

    ```bash
    curl -X GET "{base_url}/donut_type?donut_name={donut_name}"
    ```

- You should see a response containing the details of the matching donut type in JSON format.

**Note**: If no donut store name matches the search criteria, the service will return an empty array, indicating that there are no donut stores with the specified name.

## Summary

In this tutorial, you learned how to:

* Format a GET request to search for a donut type by name
* Use Postman to send a GET request to search for a donut type by name
* Use `curl` to send a GET request to search for a donut type by name