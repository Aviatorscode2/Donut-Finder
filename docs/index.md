---
layout: page
---

# Introduction

The Donut Finder API allows developers to search for donut stores, retrieve detailed information about donuts, and perform related operations with ease. This documentation provides a complete reference to help you get started quickly and use the API effectively. The API follows a REST architecture. You can access the API’s resources via HTTP requests, and responses are given in JSON format.

![Alt text](images/logo.png)

<div class="grid-container">
  <div class="grid-item">
    <h3>Quickstart</h3>
    <p>Get started quickly with our API.</p>
    <a href="Quickstart/installation.md" class="button">Learn More</a>
  </div>
  <div class="grid-item">
    <h3>Reference</h3>
    <p>Dive into detailed API documentation.</p>
    <a href="Reference/donut-store/index.md" class="button">View Reference</a>
  </div>
  <div class="grid-item">
    <h3>Tutorial</h3>
    <p>Learn how to use the API with step-by-step guides.</p>
    <a href="Tutorial/donut-store/index.md" class="button">Start Tutorial</a>
  </div>
  <div class="grid-item">
    <h3>Changelog</h3>
    <p>View the latest updates and changes to the API.</p>
    <a href="Changelog/changelog.md" class="button">View Changelog</a>
  </div>
</div>

## Quickstart

To get started with the Donut Finder service, check out our [quickstart guide](Quickstart/quickstart.md)

## Tutorials

Learn how to perform common tasks with the Donut Finder service.

#### Donut Store Management

Learn how to manage donut shops using the Donut Finder service.

* [Get a list of all donut stores](tutorials/donut-store/get-list-of-donut-stores.md)
* [Add a new donut store](tutorials/donut-store/add-new-store.md)
* [Update an existing donut store](tutorials/donut-store/update-a-store.md)
* [Delete a donut store](tutorials/donut-store/delete-store.md)

#### Donut Type Management

Learn how to manage donut types using the Donut Finder service.

* [Get a list of donut types](tutorials/donut-type/get-a-list-of-donut-types.md)
* [Add a new donut type](tutorials/donut-type/add-new-donut-type.md)
* [Update an existing donut type](tutorials/donut-type/update-a-donut-type.md)
* [Delete a donut type](tutorials/donut-type/delete-a-donut-type.md)
* [Get details of a specific donut type by name](tutorials/donut-type/search-donut-types-by-name.md)

## API Reference

The `donut_store` endpoint contains information about each donut shop, including its name, address, phone number, and a list of available donut types with their fillings and toppings. The `donut_type` endpoint contains information about each donut type, including its name and a list of donut shops that offer it.


The API reference docs refer to a `{base_url}` when they refer to the URL of a resource. The `{base_url}` value depends on the installation of the service. When running a local test, the `{base_url}` is generally `http://localhost:3000`.

* [Donut Shop Endpoints](Reference/donut-type/index.md)
* [Donut Type Endpoints](Reference/donut-type/index.md)

## Contact Us

If you have any questions or need further assistance, please contact us at support@donutfinder.com.