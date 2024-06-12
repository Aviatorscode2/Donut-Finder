---
layout: page
---

# Before you  start a tutorial

These are the steps you must do before you can run
the tutorials for the **Donut Finder Service**.

*Expect this preparation to take about 20 minutes to complete.*

## Preparing for the tutorials

### To complete the tutorials in this section, you need the following:

* A [GitHub account](https://github.com)
* A development system (PC, Mac, or Linux) running a current or
long-term support (LTS version of the operating system).
* The following software on your development system:
    * [Git](https://docs.github.com/en/get-started/quickstart/set-up-git) (for the command line)
    * [GitHub Desktop](https://desktop.github.com) (optional)
    * A fork of the [Donut Finder repo](https://github.com/Aviatorscode2/Donut-Finder)
    * A current/LTS version of [node.js](https://nodejs.org/en/)
    * A current version of [json-server](https://www.npmjs.com/package/json-server)
    * A current copy of the database file. You can get this by syncing your fork.
    * The [Postman desktop app](https://www.postman.com/downloads/). Because you run the **Donut Finder service** on your development system with an `http://localhost` hostname, the web-version of Postman can't perform the exercises.

## Test your development system

To test your development system, follow these steps:

1. Create and checkout a test branch of your fork of the To-Do-service repo. Your `GitHub repo workspace` is the directory that contains your fork of the `donut finder` repo.

    ```shell
    cd <your GitHub repo workspace>
    cd donut-finder
    cd api
    json-server -w donuts-db.json
    ```

    If your development system is installed correctly, you should see
    the service start and display the URL of the service: `http://localhost:3000`.

2. Make a test call to the service.

    ```shell
    curl http://localhost:3000/donut-store
    ```

3. If the service is running correctly, you should see a list of donut stores from the service, such as in this example.

    ```js
    [
        {
            "store_name": "Honey Kettle Donut Shop",
            "street_address": "1234 Nectar Ave, Honeyville, CA 91401 ",
            "phone": "(555) 123-1234",
            "id": "1",
            "donut inventory": [
                {
                    "donut_type": "bear claw",
                    "variation_filling": "almond paste, raspberry, chocolate, vanilla cream",
                    "variation_topping": "chocolate, powdered sugar"
                },
                {
                "donut_type": "cruller",
                "variation_filling": "none",
                "variation_topping": "chocolate, glazed, maple, pink"
            }
            ]
        },
        ...
    ```

If you don't see the list of donut stores, or receive an error in any step
of the procedure, investigate and correct the error before continuing.
Some common situations that cause errors include:

1. You mistyped a command.
2. You aren't in the correct directory.
3. A required software component didn't install correctly.
4. A required software component isn't up to date.

If you see the list of donut stores from the service, you're ready to do
the tutorials.
