# Bookable Products #

The products API allows you to read, update, and delete individual bookable products as well as list all bookable products.

## Bookable Product properties ##

| Attribute               | Type      | Description                                                                                                          |
|-------------------------|-----------|----------------------------------------------------------------------------------------------------------------------|
| `id`                    | integer   | Unique identifier for the product. <i class="label label-info">read-only</i>                                        |
| `name`                  | string    | Product name. |
| `slug`                  | string    | Product slug. |
| `permalink`             | string    | Product URL.  |
| `date_created`          | date-time | The date the product was created, in the site's timezone.  |
| `date_created_gmt`      | date-time | The date the product was created, as GMT.  |
| `date_modified`         | date-time | The date the product was last modified, in the site's timezone.  |
| `date_modified_gmt`     | date-time | The date the product was last modified, as GMT.                             |
| `type`                  | string    | Product type. Options: `simple`, `grouped`, `external` and `variable`. Default is `simple`.                          |
| `status`                | string    | Product status (post status). Options: `draft`, `pending`, `private` and `publish`. Default is `publish`.            |
| `featured`              | boolean   | Featured product. Default is   |
| `catalog_visibility`    | string    | Catalog visibility. Options: `visible`, `catalog`, `search` and `hidden`. Default is `visible`.                      |
| `description`           | string    | Product description.|
| `short_description`     | string    | Product short description.|
| `sku`                   | string    | Unique identifier. |
| `price`                 | string    | Current product price.                                                      |
| `regular_price`         | string    | Product regular price.|
| `sale_price`            | string    | Product sale price. |
| `date_on_sale_from`     | date-time | Start date of sale price, in the site's timezone.                                                                    |
| `date_on_sale_from_gmt` | date-time | Start date of sale price, as GMT.                                                                                    |
| `date_on_sale_to`       | date-time | End date of sale price, in the site's timezone.                                                                      |
| `date_on_sale_to_gmt`   | date-time | End date of sale price, as GMT.                                                                                      |
| `price_html`            | string    | Price formatted in HTML.                                                    |
| `on_sale`               | boolean   | Shows if the product is on sale.                                            |
| `purchasable`           | boolean   | Shows if the product can be bought.                                         |
| `total_sales`           | integer   | Amount of sales.                                                            |
| `virtual`               | boolean   | If the product is virtual. Default is `false`.                                                                       |
| `downloadable`          | boolean   | If the product is downloadable. Default is `false`.                                                                  |
| `downloads`             | array     | List of downloadable files. 
| `download_limit`        | integer   | Number of times downloadable files can be downloaded after purchase. Default is `-1`.                                |
| `download_expiry`       | integer   | Number of days until access to downloadable files expires. Default is `-1`.                                          |
| `external_url`          | string    | Product external URL. Only for external products.                                                                    |
| `button_text`           | string    | Product external button text. Only for external products.                                                            |
| `tax_status`            | string    | Tax status. Options: `taxable`, `shipping` and `none`. Default is `taxable`.                                         |
| `tax_class`             | string    | Tax class.|
| `manage_stock`          | boolean   | Stock management at product level. Default is `false`.                                                               |
| `stock_quantity`        | integer   | Stock quantity. |
| `stock_status`          | string    | Controls the stock status of the product. Options: `instock`, `outofstock`, `onbackorder`. Default is `instock`.     |
| `backorders`            | string    | If managing stock, this controls if backorders are allowed. Options: `no`, `notify` and `yes`. Default is `no`.      |
| `backorders_allowed`    | boolean   | Shows if backorders are allowed.                                            |
| `backordered`           | boolean   | Shows if the product is on backordered.                                     |
| `sold_individually`     | boolean   | Allow one item to be bought in a single order. Default is `false`.                                                   |
| `weight`                | string    | Product weight.|
| `dimensions`            | object    | Product dimensions. |
| `shipping_required`     | boolean   | Shows if the product need to be shipped.                                    |
| `shipping_taxable`      | boolean   | Shows whether or not the product shipping is taxable.                       |
| `shipping_class`        | string    | Shipping class slug.|
| `shipping_class_id`     | integer   | Shipping class ID.                                                          |
| `reviews_allowed`       | boolean   | Allow reviews. Default is `true`.                                                                                    |
| `average_rating`        | string    | Reviews average rating.                                                     |
| `rating_count`          | integer   | Amount of reviews that the product have.                                    |
| `related_ids`           | array     | List of related products IDs.                                               |
| `upsell_ids`            | array     | List of up-sell products IDs.                                                                                        |
| `cross_sell_ids`        | array     | List of cross-sell products IDs.                                                                                     |
| `parent_id`             | integer   | Product parent ID. |
| `purchase_note`         | string    | Optional note to send the customer after purchase. |
| `categories`            | array     | List of categories. |
| `tags`                  | array     | List of tags.    |
| `images`                | array     | List of images.  |
| `attributes`            | array     | List of attributes. |
| `default_attributes`    | array     | Defaults variation attributes. |
| `variations`            | array     | List of variations IDs.                                                     |
| `grouped_products`      | array     | List of grouped products ID.                                                                                         |
| `menu_order`            | integer   | Menu order, used to custom sort products.                                                                            |
| `meta_data`             | array     | Meta data.   |
| `apply_adjacent_buffer` | boolean   | Use adjacent buffering for calculating availability. |
| `availability`          | array     | List of custom availability rules.      |
| `block_cost`            | integer   | Block cost of the bookable product.     |
| `buffer_period`         | integer   | Time(minutes) to apply a buffer between bookings.     |
| `calendar_display_mode` | string    | Calendar display mode on the product page. |
| `cancel_limit_unit`     | string    | The unit type for the cancellation limit. |
| `cancel_limit`          | integer   | The length of the cancellation limit.     |
| `check_start_block_only`| boolean   | Check availability only from the starting block. |
| `cost`                  | integer   | The base cost of the bookable product.     |
| `default_date_availability` | string | Make the bookable product available by default. |
| `display_cost`          | string | String override for the booking display cost. |
| `duration_type`         | string | The product's block duration(fixed or customer-defined). |
| `duration_unit`         | string | The product's block duration unit type(minutes, hours, days). |
| `duration`              | integer | The value of the block duration unit. |
| `enable_range_picker`   | boolean | Enable date range selection on product pages. |
| `first_block_time`      | string | Set a beginning time in which availability is calculated. |
| `has_person_cost_multiplier` | boolean | Multiply booking costs by number of persons. |
| `has_person_qty_multiplier`  | boolean | Treat each person as a booking. |
| `has_person_types`      | boolean | Enable person types for the product. |
| `has_persons`           | boolean | Enable persons for the product. |
| `has_resources`         | boolean | Enable resources for the product. |
| `has_restricted_days`   | string | Days of week are disabled for availability ("1" or "0"). |
| `restricted_days`       | object | Days of the week which are disabled, "0" through "6".|
| `max_duration`          | integer | Maximum number of blocks per booking. |
| `min_duration`          | integer | Minimum number of blocks per booking. |
| `max_persons`           | integer | Maximum number of persons per booking. |
| `min_persons`           | integer | Minimum number of persons per booking. |
| `person_types`          | object | The person types attached to product, linked by ID. |
| `requires_confirmation` | boolean | Require admin confirmation for bookings of this product. |
| `resource_label`        | string | Label shown on product page for resource selection. |
| `resource_base_costs`   | object | The base cost per resource attached to product, linked by ID. |
| `resource_block_costs`  | object | The block cost per resource attached to product, linked by ID.|
| `resource_ids`          | object | The resources attached to product, linked by ID.|
| `resources_assignment`  | object | How resources are chosen, either "automatic" or "customer".|
| `can_be_cancelled`      | boolean | Allow cancellation of bookings. |
| `user_can_cancel`       | boolean | Allow customer cancellation of bookings. |

### Bookable Product - max_date properties ###

| Attribute | Type    | Description                                              |
|-----------|---------|----------------------------------------------------------|
| `value`   | integer | Value of the maximum date bookings can be made in the future. |
| `unit`    | string  | Unit type("month, day") for maximum future booking date. |

### Bookable Product - min_date properties ###

| Attribute | Type    | Description                                              |
|-----------|---------|----------------------------------------------------------|
| `value`   | integer | Value of the minimum date bookings can be made in the future. |
| `unit`    | string  | Unit type("month, day") for minimum future booking date. |

### Bookable Product - pricing properties ###

| Attribute | Type    | Description                                         |
|-----------|---------|-----------------------------------------------------|
| `type`    | string | The custom pricing rule type.                        |
| `cost`    | string  | Custom block cost.                                  |
| `modifier`| string  | Modifier type for calculating block cost.           |
| `cost`    | string  | Custom base cost.                                   |
| `from`    | string  | Minimum value to apply cost rule.                   |
| `to`      | string  | Maximum value to apply cost rule.                   |
| `base_modifier`| string  | Modifier type for calculating base cost.       |


## Retrieve a bookable product ##

This API lets you retrieve and view a specific bookable product by ID.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/wc-bookings/v1/products/&lt;id&gt;</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/wc-bookings/v1/products/655 \
	-u consumer_key:consumer_secret
```

> JSON response example:

```json
{
    "id": 655,
    "name": "Fitness Photo Shoot",
    "slug": "fitness-photo-shoot",
    "permalink": "https://example.com/product/fitness-photo-shoot/",
    "date_created": "2020-04-09T13:38:30",
    "date_created_gmt": "2020-04-09T13:38:30",
    "date_modified": "2020-04-22T19:04:49",
    "date_modified_gmt": "2020-04-22T19:04:49",
    "type": "booking",
    "status": "publish",
    "featured": false,
    "catalog_visibility": "visible",
    "description": "",
    "short_description": "",
    "sku": "",
    "price": "200",
    "regular_price": "",
    "sale_price": "",
    "date_on_sale_from": null,
    "date_on_sale_from_gmt": null,
    "date_on_sale_to": null,
    "date_on_sale_to_gmt": null,
    "price_html": "From: <span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>200.00</span>",
    "on_sale": false,
    "purchasable": true,
    "total_sales": 4,
    "virtual": true,
    "downloadable": false,
    "downloads": [],
    "download_limit": -1,
    "download_expiry": -1,
    "external_url": "",
    "button_text": "",
    "tax_status": "taxable",
    "tax_class": "",
    "manage_stock": false,
    "stock_quantity": null,
    "stock_status": "instock",
    "backorders": "no",
    "backorders_allowed": false,
    "backordered": false,
    "sold_individually": true,
    "weight": "",
    "dimensions": {
        "length": "",
        "width": "",
        "height": ""
    },
    "shipping_required": false,
    "shipping_taxable": false,
    "shipping_class": "",
    "shipping_class_id": 0,
    "reviews_allowed": true,
    "average_rating": "0.00",
    "rating_count": 0,
    "related_ids": [
        658,
        588,
        523,
        673,
        659
    ],
    "upsell_ids": [],
    "cross_sell_ids": [],
    "parent_id": 0,
    "purchase_note": "",
    "categories": [
        {
            "id": 15,
            "name": "Uncategorized",
            "slug": "uncategorized"
        }
    ],
    "tags": [],
    "images": [],
    "attributes": [],
    "default_attributes": [],
    "variations": [],
    "grouped_products": [],
    "menu_order": 0,
    "meta_data": [
        {
            "id": 18087,
            "key": "_wc_booking_base_cost",
            "value": "0"
        },
        {
            "id": 18117,
            "key": "_wc_booking_resouce_label",
            "value": ""
        },
        {
            "id": 18134,
            "key": "_product_addons",
            "value": []
        },
        {
            "id": 18135,
            "key": "_product_addons_exclude_global",
            "value": "0"
        },
        {
            "id": 18895,
            "key": "_nyp",
            "value": "no"
        },
        {
            "id": 18896,
            "key": "_suggested_price",
            "value": ""
        },
        {
            "id": 18897,
            "key": "_min_price",
            "value": ""
        },
        {
            "id": 18898,
            "key": "_hide_nyp_minimum",
            "value": "no"
        },
        {
            "id": 18899,
            "key": "_maximum_price",
            "value": ""
        },
        {
            "id": 18900,
            "key": "_wcopc",
            "value": "no"
        }
    ],
    "apply_adjacent_buffer": false,
    "availability": [],
    "block_cost": 0,
    "buffer_period": 30,
    "calendar_display_mode": "always_visible",
    "cancel_limit_unit": "month",
    "cancel_limit": 1,
    "check_start_block_only": false,
    "cost": 200,
    "default_date_availability": "non-available",
    "display_cost": "",
    "duration_type": "fixed",
    "duration_unit": "minute",
    "duration": 90,
    "enable_range_picker": false,
    "first_block_time": "",
    "has_person_cost_multiplier": false,
    "has_person_qty_multiplier": false,
    "has_person_types": false,
    "has_persons": true,
    "has_resources": true,
    "has_restricted_days": "",
    "max_date": {
        "value": 6,
        "unit": "month"
    },
    "max_date_value": 6,
    "max_date_unit": "month",
    "max_duration": 1,
    "max_persons": 2,
    "min_date": {
        "value": 0,
        "unit": "month"
    },
    "min_date_value": 0,
    "min_date_unit": "month",
    "min_duration": 1,
    "min_persons": 1,
    "person_types": [],
    "pricing": [
        {
            "type": "persons",
            "cost": "",
            "modifier": "",
            "base_cost": "60",
            "base_modifier": "",
            "from": "2",
            "to": "2"
        }
    ],
    "qty": 1,
    "requires_confirmation": false,
    "resource_label": "Shoot Location",
    "resource_base_costs": {
        "656": "",
        "657": "50"
    },
    "resource_block_costs": {
        "656": "",
        "657": ""
    },
    "resource_ids": [
        656,
        657
    ],
    "resources_assignment": "customer",
    "restricted_days": {
        "0": "0",
        "6": "6"
    },
    "can_be_cancelled": false,
    "user_can_cancel": false,
    "_links": {
        "self": [
            {
                "href": "https://example.com/wp-json/wc-bookings/v1/products/655"
            }
        ],
        "collection": [
            {
                "href": "https://example.com/wp-json/wc-bookings/v1/products"
            }
        ]
    }
}
```

## List all bookable products ##

This API helps you to view all published bookable products.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/wc-bookings/v1/products</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/wc-bookings/v1/products \
	-u consumer_key:consumer_secret
```

> JSON response example:

```json
[
    {
        "id": 680,
        "name": "Personal Trainer Session",
        "slug": "personal-trainer-session",
        "permalink": "https://example.com/product/personal-trainer-session/",
        "date_created": "2020-04-23T10:12:27",
        "date_created_gmt": "2020-04-23T10:12:27",
        "date_modified": "2020-04-23T10:13:20",
        "date_modified_gmt": "2020-04-23T10:13:20",
        "type": "booking",
        "status": "publish",
        "featured": false,
        "catalog_visibility": "visible",
        "description": "",
        "short_description": "",
        "sku": "",
        "price": "100",
        "regular_price": "",
        "sale_price": "",
        "date_on_sale_from": null,
        "date_on_sale_from_gmt": null,
        "date_on_sale_to": null,
        "date_on_sale_to_gmt": null,
        "price_html": "From: <span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>100.00</span>",
        "on_sale": false,
        "purchasable": true,
        "total_sales": 0,
        "virtual": true,
        "downloadable": false,
        "downloads": [],
        "download_limit": -1,
        "download_expiry": -1,
        "external_url": "",
        "button_text": "",
        "tax_status": "taxable",
        "tax_class": "",
        "manage_stock": false,
        "stock_quantity": null,
        "stock_status": "instock",
        "backorders": "no",
        "backorders_allowed": false,
        "backordered": false,
        "sold_individually": true,
        "weight": "",
        "dimensions": {
            "length": "",
            "width": "",
            "height": ""
        },
        "shipping_required": false,
        "shipping_taxable": false,
        "shipping_class": "",
        "shipping_class_id": 0,
        "reviews_allowed": true,
        "average_rating": "0.00",
        "rating_count": 0,
        "related_ids": [
            659,
            663,
            655,
            673,
            523
        ],
        "upsell_ids": [],
        "cross_sell_ids": [],
        "parent_id": 0,
        "purchase_note": "",
        "categories": [
            {
                "id": 15,
                "name": "Uncategorized",
                "slug": "uncategorized"
            }
        ],
        "tags": [],
        "images": [],
        "attributes": [],
        "default_attributes": [],
        "variations": [],
        "grouped_products": [],
        "menu_order": 0,
        "meta_data": [
            {
                "id": 19191,
                "key": "_wc_booking_base_cost",
                "value": "0"
            },
            {
                "id": 19192,
                "key": "_wc_booking_resouce_label",
                "value": ""
            },
            {
                "id": 19193,
                "key": "_product_addons",
                "value": []
            },
            {
                "id": 19194,
                "key": "_product_addons_exclude_global",
                "value": "0"
            },
            {
                "id": 19195,
                "key": "_nyp",
                "value": "no"
            },
            {
                "id": 19196,
                "key": "_suggested_price",
                "value": ""
            },
            {
                "id": 19197,
                "key": "_min_price",
                "value": ""
            },
            {
                "id": 19198,
                "key": "_hide_nyp_minimum",
                "value": "no"
            },
            {
                "id": 19199,
                "key": "_maximum_price",
                "value": ""
            },
            {
                "id": 19200,
                "key": "_wcopc",
                "value": "no"
            }
        ],
        "apply_adjacent_buffer": false,
        "availability": [],
        "block_cost": 0,
        "buffer_period": 30,
        "calendar_display_mode": "always_visible",
        "cancel_limit_unit": "month",
        "cancel_limit": 1,
        "check_start_block_only": false,
        "cost": 100,
        "default_date_availability": "non-available",
        "display_cost": "",
        "duration_type": "fixed",
        "duration_unit": "minute",
        "duration": 90,
        "enable_range_picker": false,
        "first_block_time": "",
        "has_person_cost_multiplier": false,
        "has_person_qty_multiplier": false,
        "has_person_types": false,
        "has_persons": true,
        "has_resources": true,
        "has_restricted_days": "",
        "max_date": {
            "value": 6,
            "unit": "month"
        },
        "max_date_value": 6,
        "max_date_unit": "month",
        "max_duration": 1,
        "max_persons": 2,
        "min_date": {
            "value": 0,
            "unit": "month"
        },
        "min_date_value": 0,
        "min_date_unit": "month",
        "min_duration": 1,
        "min_persons": 1,
        "person_types": [],
        "pricing": [
            {
                "type": "persons",
                "cost": "",
                "modifier": "",
                "base_cost": "60",
                "base_modifier": "",
                "from": "2",
                "to": "2"
            }
        ],
        "qty": 1,
        "requires_confirmation": false,
        "resource_label": "Training Location",
        "resource_base_costs": {
            "656": "",
            "657": "50"
        },
        "resource_block_costs": {
            "656": "",
            "657": ""
        },
        "resource_ids": [
            656,
            657
        ],
        "resources_assignment": "customer",
        "restricted_days": {
            "0": "0",
            "6": "6"
        },
        "can_be_cancelled": false,
        "user_can_cancel": false,
        "_links": {
            "self": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/products/680"
                }
            ],
            "collection": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/products"
                }
            ]
        }
    },
    {
        "id": 655,
        "name": "Fitness Photo Shoot",
        "slug": "fitness-photo-shoot",
        "permalink": "https://example.com/product/fitness-photo-shoot/",
        "date_created": "2020-04-09T13:38:30",
        "date_created_gmt": "2020-04-09T13:38:30",
        "date_modified": "2020-04-22T19:04:49",
        "date_modified_gmt": "2020-04-22T19:04:49",
        "type": "booking",
        "status": "publish",
        "featured": false,
        "catalog_visibility": "visible",
        "description": "",
        "short_description": "",
        "sku": "",
        "price": "200",
        "regular_price": "",
        "sale_price": "",
        "date_on_sale_from": null,
        "date_on_sale_from_gmt": null,
        "date_on_sale_to": null,
        "date_on_sale_to_gmt": null,
        "price_html": "From: <span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>200.00</span>",
        "on_sale": false,
        "purchasable": true,
        "total_sales": 4,
        "virtual": true,
        "downloadable": false,
        "downloads": [],
        "download_limit": -1,
        "download_expiry": -1,
        "external_url": "",
        "button_text": "",
        "tax_status": "taxable",
        "tax_class": "",
        "manage_stock": false,
        "stock_quantity": null,
        "stock_status": "instock",
        "backorders": "no",
        "backorders_allowed": false,
        "backordered": false,
        "sold_individually": true,
        "weight": "",
        "dimensions": {
            "length": "",
            "width": "",
            "height": ""
        },
        "shipping_required": false,
        "shipping_taxable": false,
        "shipping_class": "",
        "shipping_class_id": 0,
        "reviews_allowed": true,
        "average_rating": "0.00",
        "rating_count": 0,
        "related_ids": [
            510,
            522,
            523,
            663,
            673
        ],
        "upsell_ids": [],
        "cross_sell_ids": [],
        "parent_id": 0,
        "purchase_note": "",
        "categories": [
            {
                "id": 15,
                "name": "Uncategorized",
                "slug": "uncategorized"
            }
        ],
        "tags": [],
        "images": [],
        "attributes": [],
        "default_attributes": [],
        "variations": [],
        "grouped_products": [],
        "menu_order": 0,
        "meta_data": [
            {
                "id": 18087,
                "key": "_wc_booking_base_cost",
                "value": "0"
            },
            {
                "id": 18117,
                "key": "_wc_booking_resouce_label",
                "value": ""
            },
            {
                "id": 18134,
                "key": "_product_addons",
                "value": []
            },
            {
                "id": 18135,
                "key": "_product_addons_exclude_global",
                "value": "0"
            },
            {
                "id": 18895,
                "key": "_nyp",
                "value": "no"
            },
            {
                "id": 18896,
                "key": "_suggested_price",
                "value": ""
            },
            {
                "id": 18897,
                "key": "_min_price",
                "value": ""
            },
            {
                "id": 18898,
                "key": "_hide_nyp_minimum",
                "value": "no"
            },
            {
                "id": 18899,
                "key": "_maximum_price",
                "value": ""
            },
            {
                "id": 18900,
                "key": "_wcopc",
                "value": "no"
            }
        ],
        "apply_adjacent_buffer": false,
        "availability": [],
        "block_cost": 0,
        "buffer_period": 30,
        "calendar_display_mode": "always_visible",
        "cancel_limit_unit": "month",
        "cancel_limit": 1,
        "check_start_block_only": false,
        "cost": 200,
        "default_date_availability": "non-available",
        "display_cost": "",
        "duration_type": "fixed",
        "duration_unit": "minute",
        "duration": 90,
        "enable_range_picker": false,
        "first_block_time": "",
        "has_person_cost_multiplier": false,
        "has_person_qty_multiplier": false,
        "has_person_types": false,
        "has_persons": true,
        "has_resources": true,
        "has_restricted_days": "",
        "max_date": {
            "value": 6,
            "unit": "month"
        },
        "max_date_value": 6,
        "max_date_unit": "month",
        "max_duration": 1,
        "max_persons": 2,
        "min_date": {
            "value": 0,
            "unit": "month"
        },
        "min_date_value": 0,
        "min_date_unit": "month",
        "min_duration": 1,
        "min_persons": 1,
        "person_types": [],
        "pricing": [
            {
                "type": "persons",
                "cost": "",
                "modifier": "",
                "base_cost": "60",
                "base_modifier": "",
                "from": "2",
                "to": "2"
            }
        ],
        "qty": 1,
        "requires_confirmation": false,
        "resource_label": "Shoot Location",
        "resource_base_costs": {
            "656": "",
            "657": "50"
        },
        "resource_block_costs": {
            "656": "",
            "657": ""
        },
        "resource_ids": [
            656,
            657
        ],
        "resources_assignment": "customer",
        "restricted_days": {
            "0": "0",
            "6": "6"
        },
        "can_be_cancelled": false,
        "user_can_cancel": false,
        "_links": {
            "self": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/products/655"
                }
            ],
            "collection": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/products"
                }
            ]
        }
    }
]
```
#### Available parameters ####

| Parameter        | Type    | Description                                                                                                                             |
|------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `resource`       | integer  | Resource ID attached to a bookable product.            |
| `page`           | integer | Current page of the collection. Default is `1`.                                                                                         |
| `per_page`       | integer | Maximum number of items to be returned in result set. Default is `10`.                                                                  |
| `search`         | string  | Limit results to those matching a string.                                                                                               |
| `after`          | string  | Limit response to resources published after a given ISO8601 compliant date.                                                             |
| `before`         | string  | Limit response to resources published before a given ISO8601 compliant date.                                                            |
| `exclude`        | array   | Ensure result set excludes specific IDs.                                                                                                |
| `include`        | array   | Limit result set to specific ids.                                                                                                       |
| `offset`         | integer | Offset the result set by a specific number of items.                                                                                    |
| `order`          | string  | Order sort attribute ascending or descending. Options: `asc` and `desc`. Default is `desc`.                                             |
| `orderby`        | string  | Sort collection by object attribute. Options: `date`, `id`, `include`, `title` and `slug`. Default is `date`.                           |
| `parent`         | array   | Limit result set to those of particular parent IDs.                                                                                     |
| `parent_exclude` | array   | Limit result set to all items except those of a particular parent ID.                                                                   |
| `slug`           | string  | Limit result set to products with a specific slug.                                                                                      |
| `status`         | string  | Limit result set to products assigned a specific status. Options: `any`, `draft`, `pending`, `private` and `publish`. Default is `any`. |
| `type`           | string  | Limit result set to products assigned a specific type. Options: `simple`, `grouped`, `external` and `variable`.                         |
| `sku`            | string  | Limit result set to products with a specific SKU.                                                                                       |
| `featured`       | boolean | Limit result set to featured products.                                                                                                  |
| `category`       | string  | Limit result set to products assigned a specific category ID.                                                                           |
| `tag`            | string  | Limit result set to products assigned a specific tag ID.                                                                                |
| `shipping_class` | string  | Limit result set to products assigned a specific shipping class ID.                                                                     |
| `attribute`      | string  | Limit result set to products with a specific attribute.                                                                                 |
| `attribute_term` | string  | Limit result set to products with a specific attribute term ID (required an assigned attribute).                                        |
| `tax_class`      | string  | Limit result set to products with a specific tax class. Default options: `standard`, `reduced-rate` and `zero-rate`.                    |
| `on_sale`        | boolean | Limit result set to products on sale.                                                                                                   |
| `min_price`      | string  | Limit result set to products based on a minimum price.                                                                                  |
| `max_price`      | string  | Limit result set to products based on a maximum price.                                                                                  |
| `stock_status`   | string  | Limit result set to products with specified stock status. Options: `instock`, `outofstock` and `onbackorder`.                           |


## Update a bookable product##

This API helps you to update an existing bookable product.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-post">PUT</i>
		<h6>/wp-json/wc-bookings/v1/products/&lt;id&gt;</h6>
	</div>
</div>

> Example of updating an existing booking:

```shell
curl -X PUT https://example.com/wp-json/wc-bookings/v1/products/684 \
	-u consumer_key:consumer_secret \
    -d '{
    "name": "Fitness Video Shoot",
    "cost": 50,
    "featured": true,
    "requires_confirmation": true
    }'
```

> JSON response example:

```json
{
    "id": 684,
    "name": "Fitness Video Shoot",
    "slug": "product-2",
    "permalink": "https://example.com/product/product-2/",
    "date_created": "2020-04-23T13:38:43",
    "date_created_gmt": "2020-04-23T13:38:43",
    "date_modified": "2020-04-23T13:43:58",
    "date_modified_gmt": "2020-04-23T13:43:58",
    "type": "booking",
    "status": "publish",
    "featured": true,
    "catalog_visibility": "visible",
    "description": "",
    "short_description": "",
    "sku": "",
    "price": "50",
    "regular_price": "",
    "sale_price": "",
    "date_on_sale_from": null,
    "date_on_sale_from_gmt": null,
    "date_on_sale_to": null,
    "date_on_sale_to_gmt": null,
    "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>50.00</span>",
    "on_sale": false,
    "purchasable": true,
    "total_sales": 0,
    "virtual": false,
    "downloadable": false,
    "downloads": [],
    "download_limit": -1,
    "download_expiry": -1,
    "external_url": "",
    "button_text": "",
    "tax_status": "taxable",
    "tax_class": "",
    "manage_stock": false,
    "stock_quantity": null,
    "stock_status": "instock",
    "backorders": "no",
    "backorders_allowed": false,
    "backordered": false,
    "sold_individually": true,
    "weight": "",
    "dimensions": {
        "length": "",
        "width": "",
        "height": ""
    },
    "shipping_required": true,
    "shipping_taxable": true,
    "shipping_class": "",
    "shipping_class_id": 0,
    "reviews_allowed": true,
    "average_rating": "0",
    "rating_count": 0,
    "related_ids": [
        663,
        523,
        680,
        655,
        510
    ],
    "upsell_ids": [],
    "cross_sell_ids": [],
    "parent_id": 0,
    "purchase_note": "",
    "categories": [
        {
            "id": 15,
            "name": "Uncategorized",
            "slug": "uncategorized"
        }
    ],
    "tags": [],
    "images": [],
    "attributes": [],
    "default_attributes": [],
    "variations": [],
    "grouped_products": [],
    "menu_order": 0,
    "meta_data": [],
    "apply_adjacent_buffer": false,
    "availability": [],
    "block_cost": 0,
    "buffer_period": 0,
    "calendar_display_mode": "always_visible",
    "cancel_limit_unit": "month",
    "cancel_limit": 1,
    "check_start_block_only": false,
    "cost": 50,
    "default_date_availability": "",
    "display_cost": "",
    "duration_type": "fixed",
    "duration_unit": "day",
    "duration": 1,
    "enable_range_picker": false,
    "first_block_time": "",
    "has_person_cost_multiplier": false,
    "has_person_qty_multiplier": false,
    "has_person_types": false,
    "has_persons": false,
    "has_resources": false,
    "has_restricted_days": "",
    "max_date_value": 12,
    "max_date_unit": "month",
    "max_duration": 1,
    "max_persons": 1,
    "min_date_value": 0,
    "min_date_unit": "day",
    "min_duration": 1,
    "min_persons": 1,
    "person_types": [],
    "pricing": [],
    "qty": 1,
    "requires_confirmation": true,
    "resource_label": "",
    "resource_base_costs": [],
    "resource_block_costs": [],
    "resource_ids": [],
    "resources_assignment": "",
    "restricted_days": "",
    "can_be_cancelled": false,
    "user_can_cancel": false,
    "_links": {
        "self": [
            {
                "href": "https://example.com/wp-json/wc-bookings/v1/products/684"
            }
        ],
        "collection": [
            {
                "href": "https://example.com/wp-json/wc-bookings/v1/products"
            }
        ]
    }
}
```


#### Available parameters ####

| Parameter        | Type    | Description                                                                                                                             |
|------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `resource_ids`   | array  | Resource IDs attached to a bookable product.            |
| `parent`         | array   | Set parent post ID.    |
| `slug`           | string  | Set bookable product slug.     |
| `status`         | string  | Change status of bookable product. Options: `any`, `draft`, `pending`, `private` and `publish`. Default is `any`.                       |
| `featured`       | boolean | Set bookable product as a featured product.      |
| `categories`     | array   | Set the categories assigned to the bookable product.     |
| `tags`           | array   | Set the tags assigned to the bookable product.          |
| `tax_class`      | string  | Set tax class assigned to the bookable product. Default options: `standard`, `reduced-rate` and `zero-rate`.                    |
| `on_sale`        | boolean | Set bookable product on sale.              |
| `stock_status`   | string  | Set product stock status. Options: `instock`, `outofstock` and `onbackorder`.     |
| `apply_adjacent_buffer` | boolean   | Use adjacent buffering for calculating availability. |
| `availability`          | array     | List of custom availability rules.      |
| `block_cost`            | integer   | Block cost of the bookable product.     |
| `buffer_period`         | integer   | Time(minutes) to apply a buffer between bookings.     |
| `calendar_display_mode` | string    | Calendar display mode on the product page. |
| `cancel_limit_unit`     | string    | The unit type for the cancellation limit. |
| `cancel_limit`          | integer   | The length of the cancellation limit.     |
| `check_start_block_only`| boolean   | Check availability only from the starting block. |
| `cost`                  | integer   | The base cost of the bookable product.     |
| `default_date_availability` | string | Make the bookable product available by default. |
| `display_cost`          | string | String override for the booking display cost. |
| `duration_type`         | string | The product's block duration(fixed or customer-defined). |
| `duration_unit`         | string | The product's block duration unit type(minutes, hours, days). |
| `duration`              | integer | The value of the block duration unit. |
| `enable_range_picker`   | boolean | Enable date range selection on product pages. |
| `first_block_time`      | string | Set a beginning time in which availability is calculated. |
| `has_person_cost_multiplier` | boolean | Multiply booking costs by number of persons. |
| `has_person_qty_multiplier`  | boolean | Treat each person as a booking. |
| `has_person_types`      | boolean | Enable person types for the product. |
| `has_persons`           | boolean | Enable persons for the product. |
| `has_resources`         | boolean | Enable resources for the product. |
| `has_restricted_days`   | string | Days of week are disabled for availability ("1" or "0"). |
| `restricted_days`       | object | Days of the week which are disabled, "0" through "6".|
| `max_duration`          | integer | Maximum number of blocks per booking. |
| `min_duration`          | integer | Minimum number of blocks per booking. |
| `max_persons`           | integer | Maximum number of persons per booking. |
| `min_persons`           | integer | Minimum number of persons per booking. |
| `person_types`          | object | The person types attached to product, linked by ID. |
| `requires_confirmation` | boolean | Require admin confirmation for bookings of this product. |
| `resource_label`        | string | Label shown on product page for resource selection. |
| `resource_base_costs`   | object | The base cost per resource attached to product, linked by ID. |
| `resource_block_costs`  | object | The block cost per resource attached to product, linked by ID.|
| `resource_ids`          | object | The resources attached to product, linked by ID.|
| `resources_assignment`  | object | How resources are chosen, either "automatic" or "customer".|
| `can_be_cancelled`      | boolean | Allow cancellation of bookings. |
| `user_can_cancel`       | boolean | Allow customer cancellation of bookings. |


## Delete a bookable product ##

This API helps you to delete an existing bookable product, changing the post status to "trash".

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-post">DELETE</i>
		<h6>/wp-json/wc-bookings/v1/bookings/products/&lt;id&gt;</h6>
	</div>
</div>

> Example of deleting a specific booking:

```shell
curl -X DELETE https://example.com/wp-json/wc-bookings/v1/bookings/products/678 \
	-u consumer_key:consumer_secret \
```

> JSON response example:

```json
{
    "id": 684,
    "name": "Fitness Video Shoot",
    "slug": "product-2",
    "permalink": "https://example.com/product/product-2/",
    "date_created": "2020-04-23T13:38:43",
    "date_created_gmt": "2020-04-23T13:38:43",
    "date_modified": "2020-04-23T13:49:55",
    "date_modified_gmt": "2020-04-23T13:49:55",
    "type": "booking",
    "status": "publish",
    "featured": true,
    "catalog_visibility": "visible",
    "description": "",
    "short_description": "",
    "sku": "",
    "price": "50",
    "regular_price": "",
    "sale_price": "",
    "date_on_sale_from": null,
    "date_on_sale_from_gmt": null,
    "date_on_sale_to": null,
    "date_on_sale_to_gmt": null,
    "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>50.00</span>",
    "on_sale": false,
    "purchasable": true,
    "total_sales": 0,
    "virtual": false,
    "downloadable": false,
    "downloads": [],
    "download_limit": -1,
    "download_expiry": -1,
    "external_url": "",
    "button_text": "",
    "tax_status": "taxable",
    "tax_class": "",
    "manage_stock": false,
    "stock_quantity": null,
    "stock_status": "instock",
    "backorders": "no",
    "backorders_allowed": false,
    "backordered": false,
    "sold_individually": true,
    "weight": "",
    "dimensions": {
        "length": "",
        "width": "",
        "height": ""
    },
    "shipping_required": true,
    "shipping_taxable": true,
    "shipping_class": "",
    "shipping_class_id": 0,
    "reviews_allowed": true,
    "average_rating": "0",
    "rating_count": 0,
    "related_ids": [
        522,
        510,
        663,
        659,
        680
    ],
    "upsell_ids": [],
    "cross_sell_ids": [],
    "parent_id": 0,
    "purchase_note": "",
    "categories": [
        {
            "id": 15,
            "name": "Uncategorized",
            "slug": "uncategorized"
        }
    ],
    "tags": [],
    "images": [],
    "attributes": [],
    "default_attributes": [],
    "variations": [],
    "grouped_products": [],
    "menu_order": 0,
    "meta_data": [],
    "apply_adjacent_buffer": false,
    "availability": [],
    "block_cost": 0,
    "buffer_period": 0,
    "calendar_display_mode": "always_visible",
    "cancel_limit_unit": "month",
    "cancel_limit": 1,
    "check_start_block_only": false,
    "cost": 50,
    "default_date_availability": "",
    "display_cost": "",
    "duration_type": "fixed",
    "duration_unit": "day",
    "duration": 1,
    "enable_range_picker": false,
    "first_block_time": "",
    "has_person_cost_multiplier": false,
    "has_person_qty_multiplier": false,
    "has_person_types": false,
    "has_persons": false,
    "has_resources": false,
    "has_restricted_days": "",
    "max_date_value": 12,
    "max_date_unit": "month",
    "max_duration": 1,
    "max_persons": 1,
    "min_date_value": 0,
    "min_date_unit": "day",
    "min_duration": 1,
    "min_persons": 1,
    "person_types": [],
    "pricing": [],
    "qty": 1,
    "requires_confirmation": true,
    "resource_label": "",
    "resource_base_costs": [],
    "resource_block_costs": [],
    "resource_ids": [],
    "resources_assignment": "",
    "restricted_days": "",
    "can_be_cancelled": false,
    "user_can_cancel": false,
    "_links": {
        "self": [
            {
                "href": "https://example.com/wp-json/wc-bookings/v1/products/684"
            }
        ],
        "collection": [
            {
                "href": "https://example.com/wp-json/wc-bookings/v1/products"
            }
        ]
    }
}
```