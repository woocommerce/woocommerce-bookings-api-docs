# Booking Slots #

The Booking Slots API allows you to query booking product slots.

## Booking Slot properties ##

| Attribute            | Type      | Description                                                                                                |
|----------------------|-----------|------------------------------------------------------------------------------------------------------------|
| `product_id`         | integer   | Unique identifier for the product linked to the booking slot. <i class="label label-info">read-only</i>                              |
| `date`               | date-time | The date-time of the booking slot. <i class="label label-info">read-only</i>       |
| `duration`           | integer   | The duration of the booking slot. <i class="label label-info">read-only</i>|
| `available`          | integer   | Availability of the booking slot(1 or 0).<i class="label label-info">read-only</i> |
| `booked`             | integer   | Booking slot is already booked(1 or 0).<i class="label label-info">read-only</i> |

## List all booking product slots ##

This API helps you to view booking product slots via query arguments.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/wc-bookings/v1/products/slots</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/wc-bookings/v1/products/slots?min_date=2020-04-20&max_date=2020-05-01&product_ids=655 \
	-u consumer_key:consumer_secret
```

> JSON response example:

```json
{
    "records": [
        {
            "date": "2020-04-25T12:00",
            "duration": 90,
            "available": 1,
            "booked": 0,
            "product_id": 655
        },
        {
            "date": "2020-04-25T14:00",
            "duration": 90,
            "available": 1,
            "booked": 0,
            "product_id": 655
        },
        {
            "date": "2020-04-25T16:00",
            "duration": 90,
            "available": 1,
            "booked": 0,
            "product_id": 655
        },
        {
            "date": "2020-04-25T18:00",
            "duration": 90,
            "available": 0,
            "booked": 1,
            "product_id": 655
        },
        {
            "date": "2020-04-25T18:00",
            "duration": 90,
            "available": 1,
            "booked": 0,
            "product_id": 655
        },
        {
            "date": "2020-04-25T20:00",
            "duration": 90,
            "available": 0,
            "booked": 1,
            "product_id": 655
        },
        {
            "date": "2020-04-26T12:00",
            "duration": 90,
            "available": 1,
            "booked": 0,
            "product_id": 655
        },
        {
            "date": "2020-04-26T14:00",
            "duration": 90,
            "available": 1,
            "booked": 0,
            "product_id": 655
        },
        {
            "date": "2020-04-26T16:00",
            "duration": 90,
            "available": 1,
            "booked": 0,
            "product_id": 655
        },
        {
            "date": "2020-04-26T18:00",
            "duration": 90,
            "available": 1,
            "booked": 0,
            "product_id": 655
        }
    ],
    "count": 12
}
```

#### Available parameters ####

| Parameter  | Type    | Description                                                                                                                                                                                 |
| ---------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
                                                               |
| `min_date`     | string  | Set a minimum start date for booking slots retrieval.   |
| `max_date`     | string  | Set a max start date for booking slots retrieval.       <i class="label label-info">mandatory</i> |
| `product_ids`  | integer  | Comma-separated list of product ids to search.         |
| `resource_ids` | integer  | Comma-separated list of resource ids to search.        |
| `page`         | integer | Current page of the collection. Default is `1`.         |
| `per_page`     | integer | Maximum number of items to be returned in result set. Default is `10`.   |
| `search`       | string  | Limit results to those matching a string.               |
| `offset`       | integer | Offset the result set by a specific number of items.    |
| `order`        | string  | Order sort attribute ascending or descending. Options: `asc` and `desc`. Default is `asc`.  |

