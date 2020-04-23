# Product categories #

The product categories API allows you to list all categories which have published bookable products.

## Product category properties ##

| Attribute     | Type    | Description                                                                                                      |
|---------------|---------|------------------------------------------------------------------------------------------------------------------|
| `id`          | integer | Unique identifier for the category. <i class="label label-info">read-only</i> |
| `name`        | string  | Category name. <i class="label label-info">read-only</i>  |
| `slug`        | string  | An alphanumeric identifier for the category unique to its type.<i class="label label-info">read-only</i>|
| `parent`      | integer | The ID for the parent of the category. <i class="label label-info">read-only</i>|
| `description` | string  | HTML description of the category. <i class="label label-info">read-only</i> |
| `display`     | string  | Category archive display type. Options: `default`, `products`, `subcategories` and `both`. Default is `default`. <i class="label label-info">read-only</i> |
| `image`       | object  | Image data.       <i class="label label-info">read-only</i>             |
| `menu_order`  | integer | Menu order, used to custom sort the category. <i class="label label-info">read-only</i>  |
| `count`       | integer | Number of published products for the resource. <i class="label label-info">read-only</i> |

## List all product categories ##

This API lets you retrieve all product categories which have bookable products.

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/wc-bookings/v1/products/categories</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/wc-bookings/v1/products/categories \
	-u consumer_key:consumer_secret
```

> JSON response example:

```json
[
    {
        "id": 45,
        "name": "Bookings",
        "slug": "bookings",
        "parent": 0,
        "description": "",
        "display": "default",
        "image": null,
        "menu_order": 0,
        "count": 1,
        "_links": {
            "self": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/products/categories/45"
                }
            ],
            "collection": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/products/categories"
                }
            ]
        }
    },
    {
        "id": 15,
        "name": "Uncategorized",
        "slug": "uncategorized",
        "parent": 0,
        "description": "",
        "display": "default",
        "image": null,
        "menu_order": 0,
        "count": 13,
        "_links": {
            "self": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/products/categories/15"
                }
            ],
            "collection": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/products/categories"
                }
            ]
        }
    }
]
```

#### Available parameters ####

| Parameter    | Type    | Description                                                                                                                                  |
|--------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `context`    | string  | Scope under which the request is made; determines fields present in response. Options: `view` and `edit`. Default is `view`.                                                                                                        |
| `page`       | integer | Current page of the collection. Default is `1`.                                                |
| `per_page`   | integer | Maximum number of items to be returned in result set. Default is `10`.                         |
| `search`     | string  | Limit results to those matching a string.                                                      |
| `exclude`    | array   | Ensure result set excludes specific ids.                                                       |
| `include`    | array   | Limit result set to specific ids.                                                              |
| `order`      | string  | Order sort attribute ascending or descending. Options: `asc` and `desc`. Default is `asc`.     |
| `orderby`    | string  | Sort collection by resource attribute. Options: `id`, `include`, `name`, `slug`, `term_group`, `description` and `count`. Default is `name`.                                                                             |
| `hide_empty` | boolean | Whether to hide resources not assigned to any products. Default is `false`.                    |
| `parent`     | integer | Limit result set to resources assigned to a specific parent.                                   |
| `product`    | integer | Limit result set to resources assigned to a specific product.                                  |
| `slug`       | string  | Limit result set to resources with a specific slug.                                            |
