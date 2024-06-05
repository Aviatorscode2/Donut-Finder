---
layout: page
---

# Developer quickstart

## Get up and running with the Donut Finder API

The Donut Finder API provides a simple interface for developers to access and manage information about donut stores and their offerings. This API enables users to retrieve detailed information about donut stores, the types of donuts they offer, and the variations available for each donut type. With the Donut Finder API, you can seamlessly integrate donut data into your applications, making it easier for donut enthusiasts to find their favorite treats.

---

Want to jump straight to the code?
Skip the quickstart and dive into the API reference for [Donut store](donut-store/index.md) and [Donut type](donut-type/index.md) endpoints.

---

This quickstart is designed to help get your local development environment setup and send your first API request. If you are an experienced developer or want to just dive into using the Donut Finder API, the API reference of the Donut API are a great place to start. Throughout this quickstart, you will learn:

* How to set up your local development environment
* How to send your first API request

If you run into any challenges or have questions getting started, please contact our [support team](https://donut.com/support).

### Step 1: Set up your local development environment

Before you start using the Donut Finder API, set up your development environment. Follow these simple steps to get started:

1. **Install Necessary Tools**: Ensure you have a system with Windows, Linux, or iOS. Install Postman or curl for making API requests.
2. **Start Server**: `cd` into the `api` directory and start the server
```bash
json-server -w donuts-db.json
```
3. **Base URL**: For local testing, use `http://localhost:3000` as your {base_url}.

### Step 2: Send your first API request

In this section, we'll show you how to make a POST request to the Donut Finder API to add a new donut store. We'll cover how to do this using both Postman and `curl`.

#### Using Postman

1. **Open Postman**: If you haven't already installed Postman, download and install it from the [Postman website](https://www.postman.com/downloads/).

2. **Create a New Request**:
    - Click on the "New" button and select "Request".
    - Name your request (e.g., "Add New Donut Store") and save it to a collection.

3. **Set Up the Request**:
    - Set the request type to `POST`.
    - Enter the URL: `http://localhost:3000/donut_store`.

4. **Set Headers**:
    - Add a header with `Key: Content-Type` and `Value: application/json`.

5. **Add Request Body**:
    - Select the "Body" tab.
    - Choose "raw" and set the format to "JSON".
    - Enter the JSON data for the new donut store. For example:

    ```json
    {
        "store_name": "Glazed and Confused Donut Shop",
        "street_address": "5678 Sugar Lane, Sweetville, CA 91405",
        "phone": "(555) 456-7890",
        "id": 4,
        "donut inventory": [
            {
                "donut_type": "glazed",
                "variation_filling": "none",
                "variation_topping": "glazed, chocolate"
            }
        ]
    }
    ```

6. **Send the Request**:
    - Click the "Send" button.
    - You should see a response indicating the success of the request, such as a status code `201 Created` and the details of the newly added donut store.

#### Using curl

1. **Open Your Terminal**: Make sure you have `curl` installed. You can check by running `curl --version`.

2. **Run the curl Command**:
    - Use the following command to make a POST request to add a new donut store:

    ```bash
    curl -X POST http://localhost:3000/donut_store \
    -H "Content-Type: application/json" \
    -d '{
        "store_name": "Glazed and Confused Donut Shop",
        "street_address": "5678 Sugar Lane, Sweetville, CA 91405",
        "phone": "(555) 456-7890",
        "id": 4,
        "donut inventory": [
            {
                "donut_type": "glazed",
                "variation_filling": "none",
                "variation_topping": "glazed, chocolate"
            }
        ]
    }'
    ```

    - After running the command, you should see a response indicating the success of the request, such as a status code `201 Created` and the details of the newly added donut store.

With these steps, you have successfully made your first POST request to the Donut Finder API using both Postman and `curl`. This is a fundamental operation that can be expanded to perform other tasks with the API.

---

### What’s Next?

Explore more features and tutorials:

- **Add a New Donut Store**: [Enroll a User](../tutorials/donut-store/add-new-store.md)
- **Update a Donut Store**: [Update a Donut Store](../tutorials/donut-store/update-a-store.md)
- **Delete a Donut Store**: [Delete a Donut Store](../tutorials/donut-store/delete-store.md)
- **Get a Donut Store**: [Get a Donut Store](../tutorials/get-a-donut-store.md)
- **Get a List of Donut Stores**: [Get a List of Donut Stores](../tutorials/donut-store/get-a-list-of-donut-stores.md)
- **Get a List of Donut Types**: [Get a List of Donut Types](../tutorials/donut-type/get-a-list-of-donut-types.md)

---

### Additional Resources

- **[Overview](../index.md)**: Comprehensive guides and examples to help you integrate our API.
- **API Reference**: In-depth technical details and endpoint specifications.
  - [Donut Store Resource](../api/donut-store/index.md)
  - [Donut Type Resource](../api/donut-type/index.md)
