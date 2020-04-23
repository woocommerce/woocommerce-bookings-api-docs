# Resources #

The resources API allows you to view all or individual Bookings resources.

## Resource properties ##

| Attribute                     | Type      | Description                                                                                                                          |
| ----------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                          | integer   | Unique identifier for the resource. <i class="label label-info">read-only</i>                                                          |
| `availability`                | array     | Array of availability rules. <i class="label label-info">read-only<i>                                                           |
| `base_cost`                   | integer   | The base cost of the resource. <i class="label label-info">read-only</i>                                                          |
| `block_cost`                  | integer   | The block cost of the resource. <i class="label label-info">read-only</i>                                                          |
| `name`                        | string    | The given name for the resource. <i class="label label-info">read-only</i>                                                          |
| `parent_id`                   | integer   | The parent post id. <i class="label label-info">read-only</i>  |
| `qty`                         | integer   | The available quantity of resource. <i class="label label-info">read-only</i>  |
| `sort_order`                  | integer    | Determines the sort order. <i class="label label-info">read-only</i> |

### Resource - availability properties ###

| Attribute | Type    | Description                                        |
| --------- | ------- | -------------------------------------------------- |
| `type`    | string  | Type of availability rule.                         |
| `bookable`| string  | Whether the product is bookable or not("yes/no").  |
| `priority`| integer | Priority value of availability rule.               |
| `from`    | string  | Start time of the availability rule.               |
| `to`      | string  | End time of availability rule.                     |

## Retrieve a resource ##

This API lets you retrieve and view a specific resource by ID.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/wc-bookings/v1/resources/&lt;id&gt;</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/wc-bookings/v1/resources/99 \
	-u consumer_key:consumer_secret
```

> JSON response example:

```json
{
    "id": 99,
    "availability": [
        {
            "type": "time:6",
            "bookable": "yes",
            "priority": 10,
            "from": "12:00",
            "to": "20:00"
        },
        {
            "type": "time:7",
            "bookable": "yes",
            "priority": 10,
            "from": "12:00",
            "to": "20:00"
        },
        {
            "type": "custom",
            "bookable": "no",
            "priority": 9,
            "from": "2019-05-18",
            "to": "2019-05-18"
        },
        {
            "type": "custom",
            "bookable": "no",
            "priority": 9,
            "from": "2019-05-25",
            "to": "2019-05-25"
        }
    ],
    "base_cost": 10,
    "block_cost": 10,
    "name": "Gym of Your Choice",
    "parent_id": 0,
    "qty": "1",
    "sort_order": 0,
    "_links": {
        "self": [
            {
                "href": "https://example.com/wp-json/wc-bookings/v1/resources/99"
            }
        ],
        "collection": [
            {
                "href": "https://example.com/wp-json/wc-bookings/v1/resources"
            }
        ]
    }
}
```

#### Available parameters ####

| Parameter  | Type    | Description                                                                                                                  |
| ---------- | ------- | ---------------------------------------------------------------------------------------------------------------------------- |
| `id`  | integer  | The post ID of a specific resource. | 

## List all resources ##

This API helps you to list all the resources that have been created.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/wc-bookings/v1/resources</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/wc-bookings/v1/resources \
	-u consumer_key:consumer_secret
```

> JSON response example:

```json
[
    {
        "id": 99,
        "availability": [
            {
                "type": "time:6",
                "bookable": "yes",
                "priority": 10,
                "from": "12:00",
                "to": "20:00"
            },
            {
                "type": "time:7",
                "bookable": "yes",
                "priority": 10,
                "from": "12:00",
                "to": "20:00"
            },
            {
                "type": "custom",
                "bookable": "no",
                "priority": 9,
                "from": "2019-05-18",
                "to": "2019-05-18"
            },
            {
                "type": "custom",
                "bookable": "no",
                "priority": 9,
                "from": "2019-05-25",
                "to": "2019-05-25"
            }
        ],
        "base_cost": 0,
        "block_cost": 0,
        "name": "The Second Best Gym, San Jose",
        "parent_id": 0,
        "qty": "1",
        "sort_order": 0,
        "_links": {
            "self": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/resources/657"
                }
            ],
            "collection": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/resources"
                }
            ]
        }
    },
    {
        "id": 98,
        "availability": [
            {
                "type": "time:6",
                "bookable": "yes",
                "priority": 10,
                "from": "18:00",
                "to": "22:00"
            },
            {
                "type": "time:7",
                "bookable": "yes",
                "priority": 10,
                "from": "18:00",
                "to": "22:00"
            }
        ],
        "base_cost": 0,
        "block_cost": 0,
        "name": "The Best Gym, Los Angeles",
        "parent_id": 0,
        "qty": "1",
        "sort_order": 0,
        "_links": {
            "self": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/resources/656"
                }
            ],
            "collection": [
                {
                    "href": "https://example.com/wp-json/wc-bookings/v1/resources"
                }
            ]
        }
    }
]
```
