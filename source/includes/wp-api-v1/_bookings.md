# Bookings #

The Bookings API allows you to create, read, and delete individual bookings as well as list multiple bookings.

## Booking properties ##

| Attribute              | Type      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`id`| integer | Unique identifier for the resource. <i class="label label-info">read-only</i>|
| `all_day`          | boolean   | A boolean describing if the booking is for an entire day. <i class="label label-info">read-only</i> |
| `cost`             | string    | Total booking cost. <i class="label label-info">read-only</i> |
| `customer_id`      | integer   | ID of customer that purchased the booking. <i class="label label-info">read-only</i>                                                                     |
| `date_created`     | integer    | Timestamp of the time the booking was created. <i class="label label-info">read-only</i> |
| `date_modified`    | integer    | Timestamp of the time the booking was last updated. <i class="label label-info">read-only</i> |
| `end`              | integer    | Timestamp of the end time of the booking. <i class="label label-info">read-only</i> |
| `google_calendar_event_id` | string | A unique ID of a synced booking event to Google Calendar. <i class="label label-info">read-only</i> |
| `order_id`         | integer | The order ID linked to the booking. <i class="label label-info">read-only</i> |
| `order_item_id`    | integer | The unique order line item ID of the booking. <i class="label label-info">read-only</i> |
| `parent_id`        | integer | The unique item ID of the parent post. <i class="label label-info">read-only</i> |
| `person_counts`    | array | The number of persons by person type within the booking. <i class="label label-info">read-only</i> |
| `product_id`       | integer | The unique product ID linked to the booking. <i class="label label-info">read-only</i> |
| `resource_id`      | integer | The unique resource ID linked to the booking. <i class="label label-info">read-only</i> |
| `start`             | integer    | Timestamp of the start time of the booking. <i class="label label-info">read-only</i> |
| `status`            | string    | The current status of the booking. <i class="label label-info">read-only</i> |
| `local_timezone`    | string    | The local timezone used when the booking was purchased. <i class="label label-info">read-only</i> |

## Create a booking ##

This API helps you to create a new booking.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-post">POST</i>
		<h6>/wp-json/wc-bookings/v1/bookings/</h6>
	</div>
</div>

> Example of creating a new booking:

```shell
curl -X POST https://example.com/wp-json/wc-bookings/v1/bookings/ \
	-u consumer_key:consumer_secret \
    -H "Content-Type: application/json" \
    -d '{
    "all_day": false,
    "cost": "300",
    "customer_id": 1,
    "date_created": 1587634157,
    "date_modified": 1587647729,
    "end": 1588534200,
    "order_item_id": 573,
    "parent_id": 0,
    "person_counts": [
        1
    ],
    "product_id": 655,
    "resource_id": 656,
    "start": 1588528800,
    "status": "publish",
    "local_timezone": "Europe/Berlin"
}'
```

> JSON response example:

```json
{
    "id": 688,
    "all_day": false,
    "cost": "0",
    "customer_id": 0,
    "date_created": 1587666559,
    "date_modified": 1587666559,
    "end": false,
    "google_calendar_event_id": "0",
    "order_id": 0,
    "order_item_id": 0,
    "parent_id": 0,
    "person_counts": [],
    "product_id": 0,
    "resource_id": 0,
    "start": false,
    "status": "unpaid",
    "local_timezone": "",
    "_links": {
        "self": [
            {
                "href": "https://example.com/wp-json/wc-bookings/v1/bookings/688"
            }
        ],
        "collection": [
            {
                "href": "https://example.com/wp-json/wc-bookings/v1/bookings"
            }
        ]
    }
}
```

## Retrieve a booking ##

This API helps you to view an existing booking.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-post">GET</i>
		<h6>/wp-json/wc-bookings/v1/bookings/&lt;id&gt;</h6>
	</div>
</div>

> Example of viewing a specific booking:

```shell
curl https://example.com/wp-json/wc-bookings/v1/bookings/678 \
	-u consumer_key:consumer_secret \
```

> JSON response example:

```json
{
    "id": 678,
    "all_day": false,
    "cost": "200",
    "customer_id": 1,
    "date_created": 1587634157,
    "date_modified": 1587634168,
    "end": 1588534200,
    "google_calendar_event_id": "0",
    "order_id": 679,
    "order_item_id": 573,
    "parent_id": 0,
    "person_counts": [
        1
    ],
    "product_id": 655,
    "resource_id": 656,
    "start": 1588528800,
    "status": "paid",
    "local_timezone": "Europe/Berlin",
    "_links": {
        "self": [
            {
                "href": "https://example.com/wp-json/wc-bookings/v1/bookings/678"
            }
        ],
        "collection": [
            {
                "href": "https://example.com/wp-json/wc-bookings/v1/bookings"
            }
        ]
    }
}
```

## List all bookings ##

This API lets you retrieve and view all bookings made on the site.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/wc-bookings/v1/bookings/</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/wc-bookings/v1/bookings/ \
	-u consumer_key:consumer_secret
```

> JSON response example:

```json
[
    {
        "id": 678,
        "all_day": false,
        "cost": "200",
        "customer_id": 1,
        "date_created": 1587634157,
        "date_modified": 1587634168,
        "end": 1588534200,
        "google_calendar_event_id": "0",
        "order_id": 679,
        "order_item_id": 573,
        "parent_id": 0,
        "person_counts": [
            1
        ],
        "product_id": 655,
        "resource_id": 656,
        "start": 1588528800,
        "status": "paid",
        "local_timezone": "Europe/Berlin",
        "_links": {
            "self": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/bookings/678"
                }
            ],
            "collection": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/bookings"
                }
            ]
        }
    },
    {
        "id": 677,
        "all_day": false,
        "cost": "200",
        "customer_id": 1,
        "date_created": 1587634151,
        "date_modified": 1587634167,
        "end": 1588455000,
        "google_calendar_event_id": "0",
        "order_id": 679,
        "order_item_id": 572,
        "parent_id": 0,
        "person_counts": [
            1
        ],
        "product_id": 655,
        "resource_id": 656,
        "start": 1588449600,
        "status": "paid",
        "local_timezone": "Europe/Berlin",
        "_links": {
            "self": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/bookings/677"
                }
            ],
            "collection": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/bookings"
                }
            ]
        }
    },
    {
        "id": 676,
        "all_day": false,
        "cost": "200",
        "customer_id": 1,
        "date_created": 1587634146,
        "date_modified": 1587634167,
        "end": 1587936600,
        "google_calendar_event_id": "0",
        "order_id": 679,
        "order_item_id": 571,
        "parent_id": 0,
        "person_counts": [
            1
        ],
        "product_id": 655,
        "resource_id": 656,
        "start": 1587931200,
        "status": "paid",
        "local_timezone": "Europe/Berlin",
        "_links": {
            "self": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/bookings/676"
                }
            ],
            "collection": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/bookings"
                }
            ]
        }
    }
]
```


## Delete a booking ##

This API helps you to delete an existing booking, changing the booking's status to "trash".

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-post">DELETE</i>
		<h6>/wp-json/wc-bookings/v1/bookings/&lt;id&gt;</h6>
	</div>
</div>

> Example of deleting a specific booking:

```shell
curl -X DELETE https://example.com/wp-json/wc-bookings/v1/bookings/678?force=true \
	-u consumer_key:consumer_secret \
```

> JSON response example:

```json
{
    "id": 678,
    "all_day": false,
    "cost": "200",
    "customer_id": 1,
    "date_created": 1587634157,
    "date_modified": 1587647316,
    "end": 1588534200,
    "google_calendar_event_id": "0",
    "order_id": 679,
    "order_item_id": 573,
    "parent_id": 0,
    "person_counts": [
        1
    ],
    "product_id": 655,
    "resource_id": 656,
    "start": 1588528800,
    "status": "trash",
    "local_timezone": "Europe/Berlin",
    "_links": {
        "self": [
            {
                "href": "https://example.com/wp-json/wc-bookings/v1/bookings/678"
            }
        ],
        "collection": [
            {
                "href": "https://example.com/wp-json/wc-bookings/v1/bookings"
            }
        ]
    }
}
```
#### Available parameters ####

| Parameter  | Type    | Description                                                                                                                  |
| ---------- | ------- | ---------------------------------------------------------------------------------------------------------------------------- |
| `force`  | string  | Use true to permanently delete the product. Default is false. | 