---
layout: page
---

# Home

The Donut Finder service is designed to help users find their favorite donut types at local donut shops. This documentation provides an overview of the service's functionality and available endpoints. The Donut Finder service has two endpoints: the donut store endpoint and the donut type endpoint. 

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