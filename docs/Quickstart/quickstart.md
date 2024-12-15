---
layout: page
---

# Send your first request

Welcome to the Donut Finder API! Get started with the API in minutes.

---

Want to jump straight to the code? Skip the quickstart and dive into the API reference for [Donut store](../Reference/donut-store/index.md) and [Donut type](../Reference/donut-type/index.md) endpoints.

---

## **Overview**
This quickstart guides you through:

* [Part A: Set up your local development environment](#part-a-set-up-your-local-development-environment)
* [Part B: Make your first API request](#part-b-make-your-first-api-request)

It is intended for developers with basic knowledge of:

* RESTful APIs
* JSON format
* HTTP clients like Postman or `curl`


## **Before you start**

*Estimated completion time: 15-20 minutes*

> Before running this quickstart, ensure you download and install the following prerequisites:
>
>    - **Node.js and npm**: [Download here](https://nodejs.org/).
>    - **Git**: [Download here](https://git-scm.com/).
>    - **Postman**: [Download here](https://www.postman.com/downloads/).
>    - **curl**: [Download here](https://curl.se/).


## **Part A: Set up your local development environment**

### **Step 1: Clone the repository**

1. Clone the [Donut Finder API repository](https://github.com/Aviatorscode2/Donut-Finder) to your local machine using Git.
```
git clone https://github.com/Aviatorscode2/Donut-Finder.git
```

2. Navigate to the cloned repository directory:
```
cd Donut-Finder
```

### **Step 2: Start the server**

1. Navigate to the `api` directory:
```
cd api
```

2. Start the server using the following command:
```bash
json-server -w donuts-db.json
```

3. Verify that the server is running by visiting the following endpoints in your browser or HTTP client:
```bash
http://localhost:3000/donut_store
http://localhost:3000/donut_type
```

## **Part B: Make your first API request**

### **Using Postman**

1. **Open Postman**: Install and launch Postman if you haven’t already.

2. **Create a New Request**:
    - Click on "New" and select "Request".
    - Enter a name for the request, e.g., "Add New Donut Store".

3. **Set Up the Request**:
    - Method: `POST`
    - URL: `http://localhost:3000/donut_store`.

4. **Set Headers**:
    - `Key: Content-Type`
    - `Value: application/json`

5. **Add Request Body**:
    - Navigate to the "Body" tab.
    - Choose "raw" and select "JSON."
    - Enter the following JSON data:

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
    - Click "Send"
    - Verify a 201 Created response with the details of the newly added donut store.

### **Using curl**

1. **Open your terminal**: Ensure curl is installed. Verify by running:
    ```bash
    curl --version
    ```

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

3. Check the response:
    - A successful request returns a `201` Created status code with the newly added donut store.

With these steps, you have successfully made your first POST request to the Donut Finder API using both Postman and `curl`. This is a fundamental operation that can be expanded to perform other tasks with the API.

If you don't see the list of donut stores, or receive an error in any step
of the procedure, investigate and correct the error before continuing.
Some common situations that cause errors include:

1. You mistyped a command.
2. You aren't in the correct directory.

---

## **Next Steps**

Now that you’ve completed this quickstart, explore more features of the Donut Finder API:

- [Donut Store API Reference](../Reference/donut-store/index.md)
- [Donut Type API Reference](../Reference/donut-type/index.md)