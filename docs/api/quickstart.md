---
layout: page
---

# Quick Start Guide

The Donut Finder API provides a simple interface for developers to access and manage information about donut stores and their offerings. This API enables users to retrieve detailed information about donut stores, the types of donuts they offer, and the variations available for each donut type. With the Donut Finder API, you can seamlessly integrate donut data into your applications, making it easier for donut enthusiasts to find their favorite treats.

---

Want to jump straight to the code?
Skip the quickstart and dive into the API reference for [Donut store](donut-store/index.md) and [Donut type](donut-type/index.md) endpoints.

---

This quickstart is designed to help get your local development environment setup and send your first API request. If you are an experienced developer or want to just dive into using the Donut Finder API, the API reference of the Donut API are a great place to start. Throughout this quickstart, you will learn:

* [How to set up your local development environment](#part-a-set-up-your-local-development-environment)
* [How to send your first API request](#part-b-send-your-first-api-request)
* How to make request using [Postman](#using-postman) and [ `curl` ](#using-curl)

It is intended for developers. It assumes that you have basic knowledge of: 
    - Familiarity with RESTful APIs.
    - Basic understanding of JSON format.
    - Experience with tools like Postman or `curl` for making HTTP requests.

If you run into any challenges or have questions getting started, please contact our [support team](https://donut.com/support).

## Before you start

*Estimated completion time: 15-20 minutes*

> Before running this quickstart, ensure you have completed the following prerequisites:
>
> 1. **Installed Software**:
>    - **Node.js and npm**: Ensure you have Node.js and npm installed. You can download them from the [official Node.js website](https://nodejs.org/).
>    - **Git**: Ensure you have Git installed. You can download it from the [official Git website](https://git-scm.com/).
>    - **Postman**: If you prefer using a graphical interface for making HTTP requests, download and install Postman from the [Postman website](https://www.postman.com/downloads/).
>    - **curl**: If you prefer using the command line for making HTTP requests, install curl from the [curl website](https://curl.se/).


### Part A: Set up your local development environment

    - Clone the [Donut Finder API repository](https://github.com/Aviatorscode2/Donut-Finder) to your local machine using Git.
    - Navigate to the cloned repository directory and open it using a code editor of your choice.
    - **Start Server**: `cd` into the `api` directory and start the server
    
    ```bash
    json-server -w donuts-db.json
    ```

    If your development system is installed correctly, you should see the service start and running on the following endpoints
    
    ```bash
    http://localhost:3000/donut_store
    http://localhost:3000/donut_type
    ```
    with `localhost` being the {server_url} of your development system.

By ensuring you meet these prerequisites, you'll be well-prepared to follow along with the quickstart guide and make the most out of the Donut Finder API.

### Part B: Send your first API request

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

## What’s Next?

Now that you've completed this quickstart, try these to learn more about Donut API features through these tutorials:

- **Add a New Donut Store**: [Enroll a User](../tutorials/donut-store/add-new-store.md)
- **Update a Donut Store**: [Update a Donut Store](../tutorials/donut-store/update-a-store.md)
- **Delete a Donut Store**: [Delete a Donut Store](../tutorials/donut-store/delete-store.md)
- **Get a Donut Store**: [Get a Donut Store](../tutorials/get-a-donut-store.md)
- **Get a List of Donut Stores**: [Get a List of Donut Stores](../tutorials/donut-store/get-a-list-of-donut-stores.md)
- **Get a List of Donut Types**: [Get a List of Donut Types](../tutorials/donut-type/get-a-list-of-donut-types.md)