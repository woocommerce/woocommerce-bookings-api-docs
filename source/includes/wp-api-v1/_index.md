# Index #

By default, the API provides information about all available endpoints on the site. Authentication is not required to access the API index.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/wc-bookings/v1</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/wc-bookings/v1
```

> JSON response example:

```json
{
    "namespace": "wc-bookings/v1",
    "routes": {
        "/wc-bookings/v1": {
            "namespace": "wc-bookings/v1",
            "methods": [
                "GET"
            ],
            "endpoints": [
                {
                    "methods": [
                        "GET"
                    ],
                    "args": {
                        "namespace": {
                            "required": false,
                            "default": "wc-bookings/v1"
                        },
                        "context": {
                            "required": false,
                            "default": "view"
                        }
                    }
                }
            ],
            "_links": {
                "self": "https://example.com/wp-json/wc-bookings/v1"
            }
        },
        "/wc-bookings/v1/products": {
            "namespace": "wc-bookings/v1",
            "methods": [
                "GET",
                "POST"
            ],
            "endpoints": [
                {
                    "methods": [
                        "GET"
                    ],
                    "args": {
                        "context": {
                            "required": false,
                            "default": "view",
                            "enum": [
                                "view",
                                "edit"
                            ],
                            "description": "Scope under which the request is made; determines fields present in response.",
                            "type": "string"
                        },
                        "page": {
                            "required": false,
                            "default": 1,
                            "description": "Current page of the collection.",
                            "type": "integer"
                        },
                        "per_page": {
                            "required": false,
                            "default": 10,
                            "description": "Maximum number of items to be returned in result set.",
                            "type": "integer"
                        },
                        "search": {
                            "required": false,
                            "description": "Limit results to those matching a string.",
                            "type": "string"
                        },
                        "after": {
                            "required": false,
                            "description": "Limit response to resources published after a given ISO8601 compliant date.",
                            "type": "string"
                        },
                        "before": {
                            "required": false,
                            "description": "Limit response to resources published before a given ISO8601 compliant date.",
                            "type": "string"
                        },
                        "exclude": {
                            "required": false,
                            "default": [],
                            "description": "Ensure result set excludes specific IDs.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        },
                        "include": {
                            "required": false,
                            "default": [],
                            "description": "Limit result set to specific ids.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        },
                        "offset": {
                            "required": false,
                            "description": "Offset the result set by a specific number of items.",
                            "type": "integer"
                        },
                        "order": {
                            "required": false,
                            "default": "desc",
                            "enum": [
                                "asc",
                                "desc"
                            ],
                            "description": "Order sort attribute ascending or descending.",
                            "type": "string"
                        },
                        "orderby": {
                            "required": false,
                            "default": "date",
                            "enum": [
                                "date",
                                "id",
                                "include",
                                "title",
                                "slug",
                                "menu_order",
                                "price",
                                "popularity",
                                "rating"
                            ],
                            "description": "Sort collection by object attribute.",
                            "type": "string"
                        },
                        "parent": {
                            "required": false,
                            "default": [],
                            "description": "Limit result set to those of particular parent IDs.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        },
                        "parent_exclude": {
                            "required": false,
                            "default": [],
                            "description": "Limit result set to all items except those of a particular parent ID.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        },
                        "slug": {
                            "required": false,
                            "description": "Limit result set to products with a specific slug.",
                            "type": "string"
                        },
                        "status": {
                            "required": false,
                            "default": "publish",
                            "enum": [
                                "any",
                                "future",
                                "draft",
                                "pending",
                                "private",
                                "publish"
                            ],
                            "description": "Limit result set to products assigned a specific status.",
                            "type": "string"
                        },
                        "type": {
                            "required": false,
                            "default": "booking",
                            "enum": [
                                "booking"
                            ],
                            "description": "Limit result set to products assigned a specific type.",
                            "type": "string"
                        },
                        "sku": {
                            "required": false,
                            "description": "Limit result set to products with specific SKU(s). Use commas to separate.",
                            "type": "string"
                        },
                        "featured": {
                            "required": false,
                            "description": "Limit result set to featured products.",
                            "type": "boolean"
                        },
                        "category": {
                            "required": false,
                            "description": "Limit result set to products assigned a specific category ID.",
                            "type": "string"
                        },
                        "tag": {
                            "required": false,
                            "description": "Limit result set to products assigned a specific tag ID.",
                            "type": "string"
                        },
                        "shipping_class": {
                            "required": false,
                            "description": "Limit result set to products assigned a specific shipping class ID.",
                            "type": "string"
                        },
                        "attribute": {
                            "required": false,
                            "description": "Limit result set to products with a specific attribute. Use the taxonomy name/attribute slug.",
                            "type": "string"
                        },
                        "attribute_term": {
                            "required": false,
                            "description": "Limit result set to products with a specific attribute term ID (required an assigned attribute).",
                            "type": "string"
                        },
                        "tax_class": {
                            "required": false,
                            "enum": [
                                "standard",
                                "reduced-rate",
                                "zero-rate"
                            ],
                            "description": "Limit result set to products with a specific tax class.",
                            "type": "string"
                        },
                        "on_sale": {
                            "required": false,
                            "description": "Limit result set to products on sale.",
                            "type": "boolean"
                        },
                        "min_price": {
                            "required": false,
                            "description": "Limit result set to products based on a minimum price.",
                            "type": "string"
                        },
                        "max_price": {
                            "required": false,
                            "description": "Limit result set to products based on a maximum price.",
                            "type": "string"
                        },
                        "stock_status": {
                            "required": false,
                            "enum": [
                                "instock",
                                "outofstock",
                                "onbackorder"
                            ],
                            "description": "Limit result set to products with specified stock status.",
                            "type": "string"
                        },
                        "resource": {
                            "required": false,
                            "description": "Limit result set to products assigned a specific resource ID.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        }
                    }
                },
                {
                    "methods": [
                        "POST"
                    ],
                    "args": {
                        "name": {
                            "required": false,
                            "description": "Product name.",
                            "type": "string"
                        },
                        "slug": {
                            "required": false,
                            "description": "Product slug.",
                            "type": "string"
                        },
                        "date_created": {
                            "required": false,
                            "description": "The date the product was created, in the site's timezone.",
                            "type": "date-time"
                        },
                        "date_created_gmt": {
                            "required": false,
                            "description": "The date the product was created, as GMT.",
                            "type": "date-time"
                        },
                        "type": {
                            "required": false,
                            "default": "simple",
                            "enum": [
                                "simple",
                                "grouped",
                                "external",
                                "variable"
                            ],
                            "description": "Product type.",
                            "type": "string"
                        },
                        "status": {
                            "required": false,
                            "default": "publish",
                            "enum": [
                                "draft",
                                "pending",
                                "private",
                                "publish",
                                "future"
                            ],
                            "description": "Product status (post status).",
                            "type": "string"
                        },
                        "featured": {
                            "required": false,
                            "default": false,
                            "description": "Featured product.",
                            "type": "boolean"
                        },
                        "catalog_visibility": {
                            "required": false,
                            "default": "visible",
                            "enum": [
                                "visible",
                                "catalog",
                                "search",
                                "hidden"
                            ],
                            "description": "Catalog visibility.",
                            "type": "string"
                        },
                        "description": {
                            "required": false,
                            "description": "Product description.",
                            "type": "string"
                        },
                        "short_description": {
                            "required": false,
                            "description": "Product short description.",
                            "type": "string"
                        },
                        "sku": {
                            "required": false,
                            "description": "Unique identifier.",
                            "type": "string"
                        },
                        "regular_price": {
                            "required": false,
                            "description": "Product regular price.",
                            "type": "string"
                        },
                        "sale_price": {
                            "required": false,
                            "description": "Product sale price.",
                            "type": "string"
                        },
                        "date_on_sale_from": {
                            "required": false,
                            "description": "Start date of sale price, in the site's timezone.",
                            "type": "date-time"
                        },
                        "date_on_sale_from_gmt": {
                            "required": false,
                            "description": "Start date of sale price, as GMT.",
                            "type": "date-time"
                        },
                        "date_on_sale_to": {
                            "required": false,
                            "description": "End date of sale price, in the site's timezone.",
                            "type": "date-time"
                        },
                        "date_on_sale_to_gmt": {
                            "required": false,
                            "description": "End date of sale price, in the site's timezone.",
                            "type": "date-time"
                        },
                        "virtual": {
                            "required": false,
                            "default": false,
                            "description": "If the product is virtual.",
                            "type": "boolean"
                        },
                        "downloadable": {
                            "required": false,
                            "default": false,
                            "description": "If the product is downloadable.",
                            "type": "boolean"
                        },
                        "downloads": {
                            "required": false,
                            "description": "List of downloadable files.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "File ID.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "File name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "file": {
                                        "description": "File URL.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "download_limit": {
                            "required": false,
                            "default": -1,
                            "description": "Number of times downloadable files can be downloaded after purchase.",
                            "type": "integer"
                        },
                        "download_expiry": {
                            "required": false,
                            "default": -1,
                            "description": "Number of days until access to downloadable files expires.",
                            "type": "integer"
                        },
                        "external_url": {
                            "required": false,
                            "description": "Product external URL. Only for external products.",
                            "type": "string"
                        },
                        "button_text": {
                            "required": false,
                            "description": "Product external button text. Only for external products.",
                            "type": "string"
                        },
                        "tax_status": {
                            "required": false,
                            "default": "taxable",
                            "enum": [
                                "taxable",
                                "shipping",
                                "none"
                            ],
                            "description": "Tax status.",
                            "type": "string"
                        },
                        "tax_class": {
                            "required": false,
                            "description": "Tax class.",
                            "type": "string"
                        },
                        "manage_stock": {
                            "required": false,
                            "default": false,
                            "description": "Stock management at product level.",
                            "type": "boolean"
                        },
                        "stock_quantity": {
                            "required": false,
                            "description": "Stock quantity.",
                            "type": "integer"
                        },
                        "stock_status": {
                            "required": false,
                            "default": "instock",
                            "enum": [
                                "instock",
                                "outofstock",
                                "onbackorder"
                            ],
                            "description": "Controls the stock status of the product.",
                            "type": "string"
                        },
                        "backorders": {
                            "required": false,
                            "default": "no",
                            "enum": [
                                "no",
                                "notify",
                                "yes"
                            ],
                            "description": "If managing stock, this controls if backorders are allowed.",
                            "type": "string"
                        },
                        "sold_individually": {
                            "required": false,
                            "default": false,
                            "description": "Allow one item to be bought in a single order.",
                            "type": "boolean"
                        },
                        "weight": {
                            "required": false,
                            "description": "Product weight (oz).",
                            "type": "string"
                        },
                        "dimensions": {
                            "required": false,
                            "description": "Product dimensions.",
                            "type": "object"
                        },
                        "shipping_class": {
                            "required": false,
                            "description": "Shipping class slug.",
                            "type": "string"
                        },
                        "reviews_allowed": {
                            "required": false,
                            "default": true,
                            "description": "Allow reviews.",
                            "type": "boolean"
                        },
                        "upsell_ids": {
                            "required": false,
                            "description": "List of up-sell products IDs.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        },
                        "cross_sell_ids": {
                            "required": false,
                            "description": "List of cross-sell products IDs.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        },
                        "parent_id": {
                            "required": false,
                            "description": "Product parent ID.",
                            "type": "integer"
                        },
                        "purchase_note": {
                            "required": false,
                            "description": "Optional note to send the customer after purchase.",
                            "type": "string"
                        },
                        "categories": {
                            "required": false,
                            "description": "List of categories.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Category ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "Category name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "slug": {
                                        "description": "Category slug.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    }
                                }
                            }
                        },
                        "tags": {
                            "required": false,
                            "description": "List of tags.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Tag ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "Tag name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "slug": {
                                        "description": "Tag slug.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    }
                                }
                            }
                        },
                        "images": {
                            "required": false,
                            "description": "List of images.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Image ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "date_created": {
                                        "description": "The date the image was created, in the site's timezone.",
                                        "type": "date-time",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "date_created_gmt": {
                                        "description": "The date the image was created, as GMT.",
                                        "type": "date-time",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "date_modified": {
                                        "description": "The date the image was last modified, in the site's timezone.",
                                        "type": "date-time",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "date_modified_gmt": {
                                        "description": "The date the image was last modified, as GMT.",
                                        "type": "date-time",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "src": {
                                        "description": "Image URL.",
                                        "type": "string",
                                        "format": "uri",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "Image name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "alt": {
                                        "description": "Image alternative text.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "attributes": {
                            "required": false,
                            "description": "List of attributes.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Attribute ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "Attribute name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "position": {
                                        "description": "Attribute position.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "visible": {
                                        "description": "Define if the attribute is visible on the \"Additional information\" tab in the product's page.",
                                        "type": "boolean",
                                        "default": false,
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "variation": {
                                        "description": "Define if the attribute can be used as variation.",
                                        "type": "boolean",
                                        "default": false,
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "options": {
                                        "description": "List of available term names of the attribute.",
                                        "type": "array",
                                        "items": {
                                            "type": "string"
                                        },
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "default_attributes": {
                            "required": false,
                            "description": "Defaults variation attributes.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Attribute ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "Attribute name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "option": {
                                        "description": "Selected attribute term name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "menu_order": {
                            "required": false,
                            "description": "Menu order, used to custom sort products.",
                            "type": "integer"
                        },
                        "meta_data": {
                            "required": false,
                            "description": "Meta data.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Meta ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "key": {
                                        "description": "Meta key.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "value": {
                                        "description": "Meta value.",
                                        "type": "mixed",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "apply_adjacent_buffer": {
                            "required": false,
                            "description": "Apply adjacent buffers.",
                            "type": "boolean"
                        },
                        "availability": {
                            "required": false,
                            "description": "Availability rules defined on product level.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "type": {
                                        "description": "Availability type.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "from": {
                                        "description": "Starting month/day/week inclusive.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "to": {
                                        "description": "Ending month/day/week inclusive.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "from_date": {
                                        "description": "Starting day if 'from' is a time.,",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "to_date": {
                                        "description": "Ending day if 'to' is a time.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "bookable": {
                                        "description": "Rule marks things as bookable or not, 'yes' or 'no'.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "priority": {
                                        "description": "Priority of rule.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "block_cost": {
                            "required": false,
                            "description": "Base cost of each block.",
                            "type": "number"
                        },
                        "buffer_period": {
                            "required": false,
                            "description": "Required buffer Period between bookings.",
                            "type": "integer"
                        },
                        "calendar_display_mode": {
                            "required": false,
                            "enum": [
                                "",
                                "always_visible"
                            ],
                            "description": "How the calendar will display on the product page. Valid values are 'always_visible' or ''.",
                            "type": "string"
                        },
                        "cancel_limit_unit": {
                            "required": false,
                            "enum": [
                                "month",
                                "day",
                                "hour",
                                "minute"
                            ],
                            "description": "The unit limit is defined in. Valid values are 'month', 'day', 'hour', and 'minute'.",
                            "type": "string"
                        },
                        "cancel_limit": {
                            "required": false,
                            "description": "How many limit units in advance users are allowed to cancel bookings.",
                            "type": "integer"
                        },
                        "check_start_block_only": {
                            "required": false,
                            "description": "If true only the first block in checked for availability.",
                            "type": "boolean"
                        },
                        "cost": {
                            "required": false,
                            "description": "Product cost.",
                            "type": "number"
                        },
                        "default_date_availability": {
                            "required": false,
                            "enum": [
                                "",
                                "available"
                            ],
                            "description": "If 'available' product is bookable unless made unbookable by availability rules.",
                            "type": "string"
                        },
                        "display_cost": {
                            "required": false,
                            "description": "Product cost displayed.",
                            "type": "string"
                        },
                        "duration_type": {
                            "required": false,
                            "enum": [
                                "customer",
                                "fixed"
                            ],
                            "description": "How duration is defined.",
                            "type": "string"
                        },
                        "duration_unit": {
                            "required": false,
                            "enum": [
                                "month",
                                "day",
                                "hour",
                                "minute"
                            ],
                            "description": "Unit duration is defined in.",
                            "type": "string"
                        },
                        "duration": {
                            "required": false,
                            "description": "Size in duration units of each block.",
                            "type": "integer"
                        },
                        "enable_range_picker": {
                            "required": false,
                            "description": "Customer can pick a range of days on calendar.",
                            "type": "boolean"
                        },
                        "first_block_time": {
                            "required": false,
                            "description": "Time of day first block starts.",
                            "type": "string"
                        },
                        "has_person_cost_multiplier": {
                            "required": false,
                            "description": "Will multiply cost by number of persons.",
                            "type": "boolean"
                        },
                        "has_person_qty_multiplier": {
                            "required": false,
                            "description": "Each person counts as a booking.",
                            "type": "boolean"
                        },
                        "has_person_types": {
                            "required": false,
                            "description": "Product has different types of persons.",
                            "type": "boolean"
                        },
                        "has_persons": {
                            "required": false,
                            "description": "Product has persons defined.",
                            "type": "boolean"
                        },
                        "has_resources": {
                            "required": false,
                            "description": "Product has resources defined.",
                            "type": "boolean"
                        },
                        "has_restricted_days": {
                            "required": false,
                            "description": "Product has restricted days.",
                            "type": "boolean"
                        },
                        "max_date": {
                            "required": false,
                            "description": "Max date value combined with max date unit.",
                            "type": "string"
                        },
                        "max_date_value": {
                            "required": false,
                            "description": "Max amount af max_date_units into the future a block is bookable.",
                            "type": "integer"
                        },
                        "max_date_unit": {
                            "required": false,
                            "enum": [
                                "month",
                                "day",
                                "hour",
                                "week"
                            ],
                            "description": "Units for max_date_value.",
                            "type": "string"
                        },
                        "min_date": {
                            "required": false,
                            "description": "Min date value combined with min date unit.",
                            "type": "string"
                        },
                        "min_date_value": {
                            "required": false,
                            "description": "Min amount af min_date_units into the future a block is bookable.",
                            "type": "integer"
                        },
                        "min_date_unit": {
                            "required": false,
                            "enum": [
                                "month",
                                "day",
                                "hour",
                                "week"
                            ],
                            "description": "Units for min_date_value.",
                            "type": "string"
                        },
                        "max_duration": {
                            "required": false,
                            "description": "Max duration of units a booking can be.",
                            "type": "integer"
                        },
                        "min_duration": {
                            "required": false,
                            "description": "Min duration of units a booking can be.",
                            "type": "integer"
                        },
                        "max_persons": {
                            "required": false,
                            "description": "Max persons which can be booked per booking.",
                            "type": "integer"
                        },
                        "min_persons": {
                            "required": false,
                            "description": "Min persons which can be booked per booking.",
                            "type": "integer"
                        },
                        "pricing": {
                            "required": false,
                            "description": "Pricing rules.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "type": {
                                        "description": "Date range type.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "from": {
                                        "description": "Starting month/day/week inclusive.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "to": {
                                        "description": "Ending month/day/week inclusive.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "from_date": {
                                        "description": "Starting day if 'from' is a time.,",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "to_date": {
                                        "description": "Ending day if 'to' is a time.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "modifier": {
                                        "description": "How the block cost should be modified.",
                                        "type": "string",
                                        "enum": [
                                            "+",
                                            "minus",
                                            "times",
                                            "divide",
                                            "equals"
                                        ],
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "cost": {
                                        "description": "Block cost.",
                                        "type": "number",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "base_modifier": {
                                        "description": "How the base cost should be modified.",
                                        "type": "string",
                                        "enum": [
                                            "+",
                                            "minus",
                                            "times",
                                            "divide",
                                            "equals"
                                        ],
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "base_cost": {
                                        "description": "Base cost.",
                                        "type": "number",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "priority": {
                                        "description": "Priority of rule.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "qty": {
                            "required": false,
                            "description": "Max bookings per block.",
                            "type": "integer"
                        },
                        "requires_confirmation": {
                            "required": false,
                            "description": "Booking require confirmation.",
                            "type": "boolean"
                        },
                        "restricted_days": {
                            "required": false,
                            "description": "Days days of week bookings cannot start. Array of numeric day indexes with 0 being Sunday.",
                            "type": "array",
                            "items": {
                                "type": "integer",
                                "enum": [
                                    0,
                                    1,
                                    2,
                                    3,
                                    4,
                                    5,
                                    6
                                ]
                            }
                        },
                        "can_be_cancelled": {
                            "required": false,
                            "description": "Booking can be cancelled by customer.",
                            "type": "boolean"
                        }
                    }
                }
            ],
            "_links": {
                "self": "https://example.com/wp-json/wc-bookings/v1/products"
            }
        },
        "/wc-bookings/v1/products/(?P<id>[\\d]+)": {
            "namespace": "wc-bookings/v1",
            "methods": [
                "GET",
                "POST",
                "PUT",
                "PATCH",
                "DELETE"
            ],
            "endpoints": [
                {
                    "methods": [
                        "GET"
                    ],
                    "args": {
                        "id": {
                            "required": false,
                            "description": "Unique identifier for the resource.",
                            "type": "integer"
                        },
                        "context": {
                            "required": false,
                            "default": "view",
                            "enum": [
                                "view",
                                "edit"
                            ],
                            "description": "Scope under which the request is made; determines fields present in response.",
                            "type": "string"
                        }
                    }
                },
                {
                    "methods": [
                        "POST",
                        "PUT",
                        "PATCH"
                    ],
                    "args": {
                        "id": {
                            "required": false,
                            "description": "Unique identifier for the resource.",
                            "type": "integer"
                        },
                        "name": {
                            "required": false,
                            "description": "Product name.",
                            "type": "string"
                        },
                        "slug": {
                            "required": false,
                            "description": "Product slug.",
                            "type": "string"
                        },
                        "date_created": {
                            "required": false,
                            "description": "The date the product was created, in the site's timezone.",
                            "type": "date-time"
                        },
                        "date_created_gmt": {
                            "required": false,
                            "description": "The date the product was created, as GMT.",
                            "type": "date-time"
                        },
                        "type": {
                            "required": false,
                            "enum": [
                                "simple",
                                "grouped",
                                "external",
                                "variable"
                            ],
                            "description": "Product type.",
                            "type": "string"
                        },
                        "status": {
                            "required": false,
                            "enum": [
                                "draft",
                                "pending",
                                "private",
                                "publish",
                                "future"
                            ],
                            "description": "Product status (post status).",
                            "type": "string"
                        },
                        "featured": {
                            "required": false,
                            "description": "Featured product.",
                            "type": "boolean"
                        },
                        "catalog_visibility": {
                            "required": false,
                            "enum": [
                                "visible",
                                "catalog",
                                "search",
                                "hidden"
                            ],
                            "description": "Catalog visibility.",
                            "type": "string"
                        },
                        "description": {
                            "required": false,
                            "description": "Product description.",
                            "type": "string"
                        },
                        "short_description": {
                            "required": false,
                            "description": "Product short description.",
                            "type": "string"
                        },
                        "sku": {
                            "required": false,
                            "description": "Unique identifier.",
                            "type": "string"
                        },
                        "regular_price": {
                            "required": false,
                            "description": "Product regular price.",
                            "type": "string"
                        },
                        "sale_price": {
                            "required": false,
                            "description": "Product sale price.",
                            "type": "string"
                        },
                        "date_on_sale_from": {
                            "required": false,
                            "description": "Start date of sale price, in the site's timezone.",
                            "type": "date-time"
                        },
                        "date_on_sale_from_gmt": {
                            "required": false,
                            "description": "Start date of sale price, as GMT.",
                            "type": "date-time"
                        },
                        "date_on_sale_to": {
                            "required": false,
                            "description": "End date of sale price, in the site's timezone.",
                            "type": "date-time"
                        },
                        "date_on_sale_to_gmt": {
                            "required": false,
                            "description": "End date of sale price, in the site's timezone.",
                            "type": "date-time"
                        },
                        "virtual": {
                            "required": false,
                            "description": "If the product is virtual.",
                            "type": "boolean"
                        },
                        "downloadable": {
                            "required": false,
                            "description": "If the product is downloadable.",
                            "type": "boolean"
                        },
                        "downloads": {
                            "required": false,
                            "description": "List of downloadable files.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "File ID.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "File name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "file": {
                                        "description": "File URL.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "download_limit": {
                            "required": false,
                            "description": "Number of times downloadable files can be downloaded after purchase.",
                            "type": "integer"
                        },
                        "download_expiry": {
                            "required": false,
                            "description": "Number of days until access to downloadable files expires.",
                            "type": "integer"
                        },
                        "external_url": {
                            "required": false,
                            "description": "Product external URL. Only for external products.",
                            "type": "string"
                        },
                        "button_text": {
                            "required": false,
                            "description": "Product external button text. Only for external products.",
                            "type": "string"
                        },
                        "tax_status": {
                            "required": false,
                            "enum": [
                                "taxable",
                                "shipping",
                                "none"
                            ],
                            "description": "Tax status.",
                            "type": "string"
                        },
                        "tax_class": {
                            "required": false,
                            "description": "Tax class.",
                            "type": "string"
                        },
                        "manage_stock": {
                            "required": false,
                            "description": "Stock management at product level.",
                            "type": "boolean"
                        },
                        "stock_quantity": {
                            "required": false,
                            "description": "Stock quantity.",
                            "type": "integer"
                        },
                        "stock_status": {
                            "required": false,
                            "enum": [
                                "instock",
                                "outofstock",
                                "onbackorder"
                            ],
                            "description": "Controls the stock status of the product.",
                            "type": "string"
                        },
                        "backorders": {
                            "required": false,
                            "enum": [
                                "no",
                                "notify",
                                "yes"
                            ],
                            "description": "If managing stock, this controls if backorders are allowed.",
                            "type": "string"
                        },
                        "sold_individually": {
                            "required": false,
                            "description": "Allow one item to be bought in a single order.",
                            "type": "boolean"
                        },
                        "weight": {
                            "required": false,
                            "description": "Product weight (oz).",
                            "type": "string"
                        },
                        "dimensions": {
                            "required": false,
                            "description": "Product dimensions.",
                            "type": "object"
                        },
                        "shipping_class": {
                            "required": false,
                            "description": "Shipping class slug.",
                            "type": "string"
                        },
                        "reviews_allowed": {
                            "required": false,
                            "description": "Allow reviews.",
                            "type": "boolean"
                        },
                        "upsell_ids": {
                            "required": false,
                            "description": "List of up-sell products IDs.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        },
                        "cross_sell_ids": {
                            "required": false,
                            "description": "List of cross-sell products IDs.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        },
                        "parent_id": {
                            "required": false,
                            "description": "Product parent ID.",
                            "type": "integer"
                        },
                        "purchase_note": {
                            "required": false,
                            "description": "Optional note to send the customer after purchase.",
                            "type": "string"
                        },
                        "categories": {
                            "required": false,
                            "description": "List of categories.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Category ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "Category name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "slug": {
                                        "description": "Category slug.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    }
                                }
                            }
                        },
                        "tags": {
                            "required": false,
                            "description": "List of tags.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Tag ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "Tag name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "slug": {
                                        "description": "Tag slug.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    }
                                }
                            }
                        },
                        "images": {
                            "required": false,
                            "description": "List of images.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Image ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "date_created": {
                                        "description": "The date the image was created, in the site's timezone.",
                                        "type": "date-time",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "date_created_gmt": {
                                        "description": "The date the image was created, as GMT.",
                                        "type": "date-time",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "date_modified": {
                                        "description": "The date the image was last modified, in the site's timezone.",
                                        "type": "date-time",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "date_modified_gmt": {
                                        "description": "The date the image was last modified, as GMT.",
                                        "type": "date-time",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "src": {
                                        "description": "Image URL.",
                                        "type": "string",
                                        "format": "uri",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "Image name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "alt": {
                                        "description": "Image alternative text.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "attributes": {
                            "required": false,
                            "description": "List of attributes.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Attribute ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "Attribute name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "position": {
                                        "description": "Attribute position.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "visible": {
                                        "description": "Define if the attribute is visible on the \"Additional information\" tab in the product's page.",
                                        "type": "boolean",
                                        "default": false,
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "variation": {
                                        "description": "Define if the attribute can be used as variation.",
                                        "type": "boolean",
                                        "default": false,
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "options": {
                                        "description": "List of available term names of the attribute.",
                                        "type": "array",
                                        "items": {
                                            "type": "string"
                                        },
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "default_attributes": {
                            "required": false,
                            "description": "Defaults variation attributes.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Attribute ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "Attribute name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "option": {
                                        "description": "Selected attribute term name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "menu_order": {
                            "required": false,
                            "description": "Menu order, used to custom sort products.",
                            "type": "integer"
                        },
                        "meta_data": {
                            "required": false,
                            "description": "Meta data.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Meta ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "key": {
                                        "description": "Meta key.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "value": {
                                        "description": "Meta value.",
                                        "type": "mixed",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "apply_adjacent_buffer": {
                            "required": false,
                            "description": "Apply adjacent buffers.",
                            "type": "boolean"
                        },
                        "availability": {
                            "required": false,
                            "description": "Availability rules defined on product level.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "type": {
                                        "description": "Availability type.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "from": {
                                        "description": "Starting month/day/week inclusive.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "to": {
                                        "description": "Ending month/day/week inclusive.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "from_date": {
                                        "description": "Starting day if 'from' is a time.,",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "to_date": {
                                        "description": "Ending day if 'to' is a time.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "bookable": {
                                        "description": "Rule marks things as bookable or not, 'yes' or 'no'.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "priority": {
                                        "description": "Priority of rule.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "block_cost": {
                            "required": false,
                            "description": "Base cost of each block.",
                            "type": "number"
                        },
                        "buffer_period": {
                            "required": false,
                            "description": "Required buffer Period between bookings.",
                            "type": "integer"
                        },
                        "calendar_display_mode": {
                            "required": false,
                            "enum": [
                                "",
                                "always_visible"
                            ],
                            "description": "How the calendar will display on the product page. Valid values are 'always_visible' or ''.",
                            "type": "string"
                        },
                        "cancel_limit_unit": {
                            "required": false,
                            "enum": [
                                "month",
                                "day",
                                "hour",
                                "minute"
                            ],
                            "description": "The unit limit is defined in. Valid values are 'month', 'day', 'hour', and 'minute'.",
                            "type": "string"
                        },
                        "cancel_limit": {
                            "required": false,
                            "description": "How many limit units in advance users are allowed to cancel bookings.",
                            "type": "integer"
                        },
                        "check_start_block_only": {
                            "required": false,
                            "description": "If true only the first block in checked for availability.",
                            "type": "boolean"
                        },
                        "cost": {
                            "required": false,
                            "description": "Product cost.",
                            "type": "number"
                        },
                        "default_date_availability": {
                            "required": false,
                            "enum": [
                                "",
                                "available"
                            ],
                            "description": "If 'available' product is bookable unless made unbookable by availability rules.",
                            "type": "string"
                        },
                        "display_cost": {
                            "required": false,
                            "description": "Product cost displayed.",
                            "type": "string"
                        },
                        "duration_type": {
                            "required": false,
                            "enum": [
                                "customer",
                                "fixed"
                            ],
                            "description": "How duration is defined.",
                            "type": "string"
                        },
                        "duration_unit": {
                            "required": false,
                            "enum": [
                                "month",
                                "day",
                                "hour",
                                "minute"
                            ],
                            "description": "Unit duration is defined in.",
                            "type": "string"
                        },
                        "duration": {
                            "required": false,
                            "description": "Size in duration units of each block.",
                            "type": "integer"
                        },
                        "enable_range_picker": {
                            "required": false,
                            "description": "Customer can pick a range of days on calendar.",
                            "type": "boolean"
                        },
                        "first_block_time": {
                            "required": false,
                            "description": "Time of day first block starts.",
                            "type": "string"
                        },
                        "has_person_cost_multiplier": {
                            "required": false,
                            "description": "Will multiply cost by number of persons.",
                            "type": "boolean"
                        },
                        "has_person_qty_multiplier": {
                            "required": false,
                            "description": "Each person counts as a booking.",
                            "type": "boolean"
                        },
                        "has_person_types": {
                            "required": false,
                            "description": "Product has different types of persons.",
                            "type": "boolean"
                        },
                        "has_persons": {
                            "required": false,
                            "description": "Product has persons defined.",
                            "type": "boolean"
                        },
                        "has_resources": {
                            "required": false,
                            "description": "Product has resources defined.",
                            "type": "boolean"
                        },
                        "has_restricted_days": {
                            "required": false,
                            "description": "Product has restricted days.",
                            "type": "boolean"
                        },
                        "max_date": {
                            "required": false,
                            "description": "Max date value combined with max date unit.",
                            "type": "string"
                        },
                        "max_date_value": {
                            "required": false,
                            "description": "Max amount af max_date_units into the future a block is bookable.",
                            "type": "integer"
                        },
                        "max_date_unit": {
                            "required": false,
                            "enum": [
                                "month",
                                "day",
                                "hour",
                                "week"
                            ],
                            "description": "Units for max_date_value.",
                            "type": "string"
                        },
                        "min_date": {
                            "required": false,
                            "description": "Min date value combined with min date unit.",
                            "type": "string"
                        },
                        "min_date_value": {
                            "required": false,
                            "description": "Min amount af min_date_units into the future a block is bookable.",
                            "type": "integer"
                        },
                        "min_date_unit": {
                            "required": false,
                            "enum": [
                                "month",
                                "day",
                                "hour",
                                "week"
                            ],
                            "description": "Units for min_date_value.",
                            "type": "string"
                        },
                        "max_duration": {
                            "required": false,
                            "description": "Max duration of units a booking can be.",
                            "type": "integer"
                        },
                        "min_duration": {
                            "required": false,
                            "description": "Min duration of units a booking can be.",
                            "type": "integer"
                        },
                        "max_persons": {
                            "required": false,
                            "description": "Max persons which can be booked per booking.",
                            "type": "integer"
                        },
                        "min_persons": {
                            "required": false,
                            "description": "Min persons which can be booked per booking.",
                            "type": "integer"
                        },
                        "pricing": {
                            "required": false,
                            "description": "Pricing rules.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "type": {
                                        "description": "Date range type.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "from": {
                                        "description": "Starting month/day/week inclusive.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "to": {
                                        "description": "Ending month/day/week inclusive.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "from_date": {
                                        "description": "Starting day if 'from' is a time.,",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "to_date": {
                                        "description": "Ending day if 'to' is a time.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "modifier": {
                                        "description": "How the block cost should be modified.",
                                        "type": "string",
                                        "enum": [
                                            "+",
                                            "minus",
                                            "times",
                                            "divide",
                                            "equals"
                                        ],
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "cost": {
                                        "description": "Block cost.",
                                        "type": "number",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "base_modifier": {
                                        "description": "How the base cost should be modified.",
                                        "type": "string",
                                        "enum": [
                                            "+",
                                            "minus",
                                            "times",
                                            "divide",
                                            "equals"
                                        ],
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "base_cost": {
                                        "description": "Base cost.",
                                        "type": "number",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "priority": {
                                        "description": "Priority of rule.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "qty": {
                            "required": false,
                            "description": "Max bookings per block.",
                            "type": "integer"
                        },
                        "requires_confirmation": {
                            "required": false,
                            "description": "Booking require confirmation.",
                            "type": "boolean"
                        },
                        "restricted_days": {
                            "required": false,
                            "description": "Days days of week bookings cannot start. Array of numeric day indexes with 0 being Sunday.",
                            "type": "array",
                            "items": {
                                "type": "integer",
                                "enum": [
                                    0,
                                    1,
                                    2,
                                    3,
                                    4,
                                    5,
                                    6
                                ]
                            }
                        },
                        "can_be_cancelled": {
                            "required": false,
                            "description": "Booking can be cancelled by customer.",
                            "type": "boolean"
                        }
                    }
                },
                {
                    "methods": [
                        "DELETE"
                    ],
                    "args": {
                        "id": {
                            "required": false,
                            "description": "Unique identifier for the resource.",
                            "type": "integer"
                        },
                        "force": {
                            "required": false,
                            "default": false,
                            "description": "Whether to bypass trash and force deletion.",
                            "type": "boolean"
                        }
                    }
                }
            ]
        },
        "/wc-bookings/v1/products/batch": {
            "namespace": "wc-bookings/v1",
            "methods": [
                "POST",
                "PUT",
                "PATCH"
            ],
            "endpoints": [
                {
                    "methods": [
                        "POST",
                        "PUT",
                        "PATCH"
                    ],
                    "args": {
                        "name": {
                            "required": false,
                            "description": "Product name.",
                            "type": "string"
                        },
                        "slug": {
                            "required": false,
                            "description": "Product slug.",
                            "type": "string"
                        },
                        "date_created": {
                            "required": false,
                            "description": "The date the product was created, in the site's timezone.",
                            "type": "date-time"
                        },
                        "date_created_gmt": {
                            "required": false,
                            "description": "The date the product was created, as GMT.",
                            "type": "date-time"
                        },
                        "type": {
                            "required": false,
                            "enum": [
                                "simple",
                                "grouped",
                                "external",
                                "variable"
                            ],
                            "description": "Product type.",
                            "type": "string"
                        },
                        "status": {
                            "required": false,
                            "enum": [
                                "draft",
                                "pending",
                                "private",
                                "publish",
                                "future"
                            ],
                            "description": "Product status (post status).",
                            "type": "string"
                        },
                        "featured": {
                            "required": false,
                            "description": "Featured product.",
                            "type": "boolean"
                        },
                        "catalog_visibility": {
                            "required": false,
                            "enum": [
                                "visible",
                                "catalog",
                                "search",
                                "hidden"
                            ],
                            "description": "Catalog visibility.",
                            "type": "string"
                        },
                        "description": {
                            "required": false,
                            "description": "Product description.",
                            "type": "string"
                        },
                        "short_description": {
                            "required": false,
                            "description": "Product short description.",
                            "type": "string"
                        },
                        "sku": {
                            "required": false,
                            "description": "Unique identifier.",
                            "type": "string"
                        },
                        "regular_price": {
                            "required": false,
                            "description": "Product regular price.",
                            "type": "string"
                        },
                        "sale_price": {
                            "required": false,
                            "description": "Product sale price.",
                            "type": "string"
                        },
                        "date_on_sale_from": {
                            "required": false,
                            "description": "Start date of sale price, in the site's timezone.",
                            "type": "date-time"
                        },
                        "date_on_sale_from_gmt": {
                            "required": false,
                            "description": "Start date of sale price, as GMT.",
                            "type": "date-time"
                        },
                        "date_on_sale_to": {
                            "required": false,
                            "description": "End date of sale price, in the site's timezone.",
                            "type": "date-time"
                        },
                        "date_on_sale_to_gmt": {
                            "required": false,
                            "description": "End date of sale price, in the site's timezone.",
                            "type": "date-time"
                        },
                        "virtual": {
                            "required": false,
                            "description": "If the product is virtual.",
                            "type": "boolean"
                        },
                        "downloadable": {
                            "required": false,
                            "description": "If the product is downloadable.",
                            "type": "boolean"
                        },
                        "downloads": {
                            "required": false,
                            "description": "List of downloadable files.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "File ID.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "File name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "file": {
                                        "description": "File URL.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "download_limit": {
                            "required": false,
                            "description": "Number of times downloadable files can be downloaded after purchase.",
                            "type": "integer"
                        },
                        "download_expiry": {
                            "required": false,
                            "description": "Number of days until access to downloadable files expires.",
                            "type": "integer"
                        },
                        "external_url": {
                            "required": false,
                            "description": "Product external URL. Only for external products.",
                            "type": "string"
                        },
                        "button_text": {
                            "required": false,
                            "description": "Product external button text. Only for external products.",
                            "type": "string"
                        },
                        "tax_status": {
                            "required": false,
                            "enum": [
                                "taxable",
                                "shipping",
                                "none"
                            ],
                            "description": "Tax status.",
                            "type": "string"
                        },
                        "tax_class": {
                            "required": false,
                            "description": "Tax class.",
                            "type": "string"
                        },
                        "manage_stock": {
                            "required": false,
                            "description": "Stock management at product level.",
                            "type": "boolean"
                        },
                        "stock_quantity": {
                            "required": false,
                            "description": "Stock quantity.",
                            "type": "integer"
                        },
                        "stock_status": {
                            "required": false,
                            "enum": [
                                "instock",
                                "outofstock",
                                "onbackorder"
                            ],
                            "description": "Controls the stock status of the product.",
                            "type": "string"
                        },
                        "backorders": {
                            "required": false,
                            "enum": [
                                "no",
                                "notify",
                                "yes"
                            ],
                            "description": "If managing stock, this controls if backorders are allowed.",
                            "type": "string"
                        },
                        "sold_individually": {
                            "required": false,
                            "description": "Allow one item to be bought in a single order.",
                            "type": "boolean"
                        },
                        "weight": {
                            "required": false,
                            "description": "Product weight (oz).",
                            "type": "string"
                        },
                        "dimensions": {
                            "required": false,
                            "description": "Product dimensions.",
                            "type": "object"
                        },
                        "shipping_class": {
                            "required": false,
                            "description": "Shipping class slug.",
                            "type": "string"
                        },
                        "reviews_allowed": {
                            "required": false,
                            "description": "Allow reviews.",
                            "type": "boolean"
                        },
                        "upsell_ids": {
                            "required": false,
                            "description": "List of up-sell products IDs.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        },
                        "cross_sell_ids": {
                            "required": false,
                            "description": "List of cross-sell products IDs.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        },
                        "parent_id": {
                            "required": false,
                            "description": "Product parent ID.",
                            "type": "integer"
                        },
                        "purchase_note": {
                            "required": false,
                            "description": "Optional note to send the customer after purchase.",
                            "type": "string"
                        },
                        "categories": {
                            "required": false,
                            "description": "List of categories.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Category ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "Category name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "slug": {
                                        "description": "Category slug.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    }
                                }
                            }
                        },
                        "tags": {
                            "required": false,
                            "description": "List of tags.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Tag ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "Tag name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "slug": {
                                        "description": "Tag slug.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    }
                                }
                            }
                        },
                        "images": {
                            "required": false,
                            "description": "List of images.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Image ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "date_created": {
                                        "description": "The date the image was created, in the site's timezone.",
                                        "type": "date-time",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "date_created_gmt": {
                                        "description": "The date the image was created, as GMT.",
                                        "type": "date-time",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "date_modified": {
                                        "description": "The date the image was last modified, in the site's timezone.",
                                        "type": "date-time",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "date_modified_gmt": {
                                        "description": "The date the image was last modified, as GMT.",
                                        "type": "date-time",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "src": {
                                        "description": "Image URL.",
                                        "type": "string",
                                        "format": "uri",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "Image name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "alt": {
                                        "description": "Image alternative text.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "attributes": {
                            "required": false,
                            "description": "List of attributes.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Attribute ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "Attribute name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "position": {
                                        "description": "Attribute position.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "visible": {
                                        "description": "Define if the attribute is visible on the \"Additional information\" tab in the product's page.",
                                        "type": "boolean",
                                        "default": false,
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "variation": {
                                        "description": "Define if the attribute can be used as variation.",
                                        "type": "boolean",
                                        "default": false,
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "options": {
                                        "description": "List of available term names of the attribute.",
                                        "type": "array",
                                        "items": {
                                            "type": "string"
                                        },
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "default_attributes": {
                            "required": false,
                            "description": "Defaults variation attributes.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Attribute ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "name": {
                                        "description": "Attribute name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "option": {
                                        "description": "Selected attribute term name.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "menu_order": {
                            "required": false,
                            "description": "Menu order, used to custom sort products.",
                            "type": "integer"
                        },
                        "meta_data": {
                            "required": false,
                            "description": "Meta data.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "id": {
                                        "description": "Meta ID.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ],
                                        "readonly": true
                                    },
                                    "key": {
                                        "description": "Meta key.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "value": {
                                        "description": "Meta value.",
                                        "type": "mixed",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "apply_adjacent_buffer": {
                            "required": false,
                            "description": "Apply adjacent buffers.",
                            "type": "boolean"
                        },
                        "availability": {
                            "required": false,
                            "description": "Availability rules defined on product level.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "type": {
                                        "description": "Availability type.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "from": {
                                        "description": "Starting month/day/week inclusive.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "to": {
                                        "description": "Ending month/day/week inclusive.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "from_date": {
                                        "description": "Starting day if 'from' is a time.,",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "to_date": {
                                        "description": "Ending day if 'to' is a time.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "bookable": {
                                        "description": "Rule marks things as bookable or not, 'yes' or 'no'.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "priority": {
                                        "description": "Priority of rule.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "block_cost": {
                            "required": false,
                            "description": "Base cost of each block.",
                            "type": "number"
                        },
                        "buffer_period": {
                            "required": false,
                            "description": "Required buffer Period between bookings.",
                            "type": "integer"
                        },
                        "calendar_display_mode": {
                            "required": false,
                            "enum": [
                                "",
                                "always_visible"
                            ],
                            "description": "How the calendar will display on the product page. Valid values are 'always_visible' or ''.",
                            "type": "string"
                        },
                        "cancel_limit_unit": {
                            "required": false,
                            "enum": [
                                "month",
                                "day",
                                "hour",
                                "minute"
                            ],
                            "description": "The unit limit is defined in. Valid values are 'month', 'day', 'hour', and 'minute'.",
                            "type": "string"
                        },
                        "cancel_limit": {
                            "required": false,
                            "description": "How many limit units in advance users are allowed to cancel bookings.",
                            "type": "integer"
                        },
                        "check_start_block_only": {
                            "required": false,
                            "description": "If true only the first block in checked for availability.",
                            "type": "boolean"
                        },
                        "cost": {
                            "required": false,
                            "description": "Product cost.",
                            "type": "number"
                        },
                        "default_date_availability": {
                            "required": false,
                            "enum": [
                                "",
                                "available"
                            ],
                            "description": "If 'available' product is bookable unless made unbookable by availability rules.",
                            "type": "string"
                        },
                        "display_cost": {
                            "required": false,
                            "description": "Product cost displayed.",
                            "type": "string"
                        },
                        "duration_type": {
                            "required": false,
                            "enum": [
                                "customer",
                                "fixed"
                            ],
                            "description": "How duration is defined.",
                            "type": "string"
                        },
                        "duration_unit": {
                            "required": false,
                            "enum": [
                                "month",
                                "day",
                                "hour",
                                "minute"
                            ],
                            "description": "Unit duration is defined in.",
                            "type": "string"
                        },
                        "duration": {
                            "required": false,
                            "description": "Size in duration units of each block.",
                            "type": "integer"
                        },
                        "enable_range_picker": {
                            "required": false,
                            "description": "Customer can pick a range of days on calendar.",
                            "type": "boolean"
                        },
                        "first_block_time": {
                            "required": false,
                            "description": "Time of day first block starts.",
                            "type": "string"
                        },
                        "has_person_cost_multiplier": {
                            "required": false,
                            "description": "Will multiply cost by number of persons.",
                            "type": "boolean"
                        },
                        "has_person_qty_multiplier": {
                            "required": false,
                            "description": "Each person counts as a booking.",
                            "type": "boolean"
                        },
                        "has_person_types": {
                            "required": false,
                            "description": "Product has different types of persons.",
                            "type": "boolean"
                        },
                        "has_persons": {
                            "required": false,
                            "description": "Product has persons defined.",
                            "type": "boolean"
                        },
                        "has_resources": {
                            "required": false,
                            "description": "Product has resources defined.",
                            "type": "boolean"
                        },
                        "has_restricted_days": {
                            "required": false,
                            "description": "Product has restricted days.",
                            "type": "boolean"
                        },
                        "max_date": {
                            "required": false,
                            "description": "Max date value combined with max date unit.",
                            "type": "string"
                        },
                        "max_date_value": {
                            "required": false,
                            "description": "Max amount af max_date_units into the future a block is bookable.",
                            "type": "integer"
                        },
                        "max_date_unit": {
                            "required": false,
                            "enum": [
                                "month",
                                "day",
                                "hour",
                                "week"
                            ],
                            "description": "Units for max_date_value.",
                            "type": "string"
                        },
                        "min_date": {
                            "required": false,
                            "description": "Min date value combined with min date unit.",
                            "type": "string"
                        },
                        "min_date_value": {
                            "required": false,
                            "description": "Min amount af min_date_units into the future a block is bookable.",
                            "type": "integer"
                        },
                        "min_date_unit": {
                            "required": false,
                            "enum": [
                                "month",
                                "day",
                                "hour",
                                "week"
                            ],
                            "description": "Units for min_date_value.",
                            "type": "string"
                        },
                        "max_duration": {
                            "required": false,
                            "description": "Max duration of units a booking can be.",
                            "type": "integer"
                        },
                        "min_duration": {
                            "required": false,
                            "description": "Min duration of units a booking can be.",
                            "type": "integer"
                        },
                        "max_persons": {
                            "required": false,
                            "description": "Max persons which can be booked per booking.",
                            "type": "integer"
                        },
                        "min_persons": {
                            "required": false,
                            "description": "Min persons which can be booked per booking.",
                            "type": "integer"
                        },
                        "pricing": {
                            "required": false,
                            "description": "Pricing rules.",
                            "type": "array",
                            "items": {
                                "type": "object",
                                "properties": {
                                    "type": {
                                        "description": "Date range type.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "from": {
                                        "description": "Starting month/day/week inclusive.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "to": {
                                        "description": "Ending month/day/week inclusive.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "from_date": {
                                        "description": "Starting day if 'from' is a time.,",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "to_date": {
                                        "description": "Ending day if 'to' is a time.",
                                        "type": "string",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "modifier": {
                                        "description": "How the block cost should be modified.",
                                        "type": "string",
                                        "enum": [
                                            "+",
                                            "minus",
                                            "times",
                                            "divide",
                                            "equals"
                                        ],
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "cost": {
                                        "description": "Block cost.",
                                        "type": "number",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "base_modifier": {
                                        "description": "How the base cost should be modified.",
                                        "type": "string",
                                        "enum": [
                                            "+",
                                            "minus",
                                            "times",
                                            "divide",
                                            "equals"
                                        ],
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "base_cost": {
                                        "description": "Base cost.",
                                        "type": "number",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    },
                                    "priority": {
                                        "description": "Priority of rule.",
                                        "type": "integer",
                                        "context": [
                                            "view",
                                            "edit"
                                        ]
                                    }
                                }
                            }
                        },
                        "qty": {
                            "required": false,
                            "description": "Max bookings per block.",
                            "type": "integer"
                        },
                        "requires_confirmation": {
                            "required": false,
                            "description": "Booking require confirmation.",
                            "type": "boolean"
                        },
                        "restricted_days": {
                            "required": false,
                            "description": "Days days of week bookings cannot start. Array of numeric day indexes with 0 being Sunday.",
                            "type": "array",
                            "items": {
                                "type": "integer",
                                "enum": [
                                    0,
                                    1,
                                    2,
                                    3,
                                    4,
                                    5,
                                    6
                                ]
                            }
                        },
                        "can_be_cancelled": {
                            "required": false,
                            "description": "Booking can be cancelled by customer.",
                            "type": "boolean"
                        }
                    }
                }
            ],
            "_links": {
                "self": "https://example.com/wp-json/wc-bookings/v1/products/batch"
            }
        },
        "/wc-bookings/v1/products/categories": {
            "namespace": "wc-bookings/v1",
            "methods": [
                "GET",
                "POST"
            ],
            "endpoints": [
                {
                    "methods": [
                        "GET"
                    ],
                    "args": {
                        "context": {
                            "required": false,
                            "default": "view",
                            "enum": [
                                "view",
                                "edit"
                            ],
                            "description": "Scope under which the request is made; determines fields present in response.",
                            "type": "string"
                        },
                        "page": {
                            "required": false,
                            "default": 1,
                            "description": "Current page of the collection.",
                            "type": "integer"
                        },
                        "per_page": {
                            "required": false,
                            "default": 10,
                            "description": "Maximum number of items to be returned in result set.",
                            "type": "integer"
                        },
                        "search": {
                            "required": false,
                            "description": "Limit results to those matching a string.",
                            "type": "string"
                        },
                        "exclude": {
                            "required": false,
                            "default": [],
                            "description": "Ensure result set excludes specific IDs.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        },
                        "include": {
                            "required": false,
                            "default": [],
                            "description": "Limit result set to specific ids.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        },
                        "order": {
                            "required": false,
                            "default": "asc",
                            "enum": [
                                "asc",
                                "desc"
                            ],
                            "description": "Order sort attribute ascending or descending.",
                            "type": "string"
                        },
                        "orderby": {
                            "required": false,
                            "default": "name",
                            "enum": [
                                "id",
                                "include",
                                "name",
                                "slug",
                                "term_group",
                                "description",
                                "count"
                            ],
                            "description": "Sort collection by resource attribute.",
                            "type": "string"
                        },
                        "hide_empty": {
                            "required": false,
                            "default": false,
                            "description": "Whether to hide resources not assigned to any products.",
                            "type": "boolean"
                        },
                        "parent": {
                            "required": false,
                            "description": "Limit result set to resources assigned to a specific parent.",
                            "type": "integer"
                        },
                        "product": {
                            "required": false,
                            "description": "Limit result set to resources assigned to a specific product.",
                            "type": "integer"
                        },
                        "slug": {
                            "required": false,
                            "description": "Limit result set to resources with a specific slug.",
                            "type": "string"
                        }
                    }
                },
                {
                    "methods": [
                        "POST"
                    ],
                    "args": {
                        "name": {
                            "required": true,
                            "description": "Name for the resource.",
                            "type": "string"
                        },
                        "slug": {
                            "required": false,
                            "description": "An alphanumeric identifier for the resource unique to its type.",
                            "type": "string"
                        },
                        "parent": {
                            "required": false,
                            "description": "The ID for the parent of the resource.",
                            "type": "integer"
                        },
                        "description": {
                            "required": false,
                            "description": "HTML description of the resource.",
                            "type": "string"
                        },
                        "display": {
                            "required": false,
                            "default": "default",
                            "enum": [
                                "default",
                                "products",
                                "subcategories",
                                "both"
                            ],
                            "description": "Category archive display type.",
                            "type": "string"
                        },
                        "image": {
                            "required": false,
                            "description": "Image data.",
                            "type": "object"
                        },
                        "menu_order": {
                            "required": false,
                            "description": "Menu order, used to custom sort the resource.",
                            "type": "integer"
                        }
                    }
                }
            ],
            "_links": {
                "self": "https://example.com/wp-json/wc-bookings/v1/products/categories"
            }
        },
        "/wc-bookings/v1/products/categories/(?P<id>[\\d]+)": {
            "namespace": "wc-bookings/v1",
            "methods": [
                "GET",
                "POST",
                "PUT",
                "PATCH",
                "DELETE"
            ],
            "endpoints": [
                {
                    "methods": [
                        "GET"
                    ],
                    "args": {
                        "id": {
                            "required": false,
                            "description": "Unique identifier for the resource.",
                            "type": "integer"
                        },
                        "context": {
                            "required": false,
                            "default": "view",
                            "enum": [
                                "view",
                                "edit"
                            ],
                            "description": "Scope under which the request is made; determines fields present in response.",
                            "type": "string"
                        }
                    }
                },
                {
                    "methods": [
                        "POST",
                        "PUT",
                        "PATCH"
                    ],
                    "args": {
                        "id": {
                            "required": false,
                            "description": "Unique identifier for the resource.",
                            "type": "integer"
                        },
                        "name": {
                            "required": false,
                            "description": "Category name.",
                            "type": "string"
                        },
                        "slug": {
                            "required": false,
                            "description": "An alphanumeric identifier for the resource unique to its type.",
                            "type": "string"
                        },
                        "parent": {
                            "required": false,
                            "description": "The ID for the parent of the resource.",
                            "type": "integer"
                        },
                        "description": {
                            "required": false,
                            "description": "HTML description of the resource.",
                            "type": "string"
                        },
                        "display": {
                            "required": false,
                            "enum": [
                                "default",
                                "products",
                                "subcategories",
                                "both"
                            ],
                            "description": "Category archive display type.",
                            "type": "string"
                        },
                        "image": {
                            "required": false,
                            "description": "Image data.",
                            "type": "object"
                        },
                        "menu_order": {
                            "required": false,
                            "description": "Menu order, used to custom sort the resource.",
                            "type": "integer"
                        }
                    }
                },
                {
                    "methods": [
                        "DELETE"
                    ],
                    "args": {
                        "id": {
                            "required": false,
                            "description": "Unique identifier for the resource.",
                            "type": "integer"
                        },
                        "force": {
                            "required": false,
                            "default": false,
                            "description": "Required to be true, as resource does not support trashing.",
                            "type": "boolean"
                        }
                    }
                }
            ]
        },
        "/wc-bookings/v1/products/categories/batch": {
            "namespace": "wc-bookings/v1",
            "methods": [
                "POST",
                "PUT",
                "PATCH"
            ],
            "endpoints": [
                {
                    "methods": [
                        "POST",
                        "PUT",
                        "PATCH"
                    ],
                    "args": {
                        "name": {
                            "required": false,
                            "description": "Category name.",
                            "type": "string"
                        },
                        "slug": {
                            "required": false,
                            "description": "An alphanumeric identifier for the resource unique to its type.",
                            "type": "string"
                        },
                        "parent": {
                            "required": false,
                            "description": "The ID for the parent of the resource.",
                            "type": "integer"
                        },
                        "description": {
                            "required": false,
                            "description": "HTML description of the resource.",
                            "type": "string"
                        },
                        "display": {
                            "required": false,
                            "enum": [
                                "default",
                                "products",
                                "subcategories",
                                "both"
                            ],
                            "description": "Category archive display type.",
                            "type": "string"
                        },
                        "image": {
                            "required": false,
                            "description": "Image data.",
                            "type": "object"
                        },
                        "menu_order": {
                            "required": false,
                            "description": "Menu order, used to custom sort the resource.",
                            "type": "integer"
                        }
                    }
                }
            ],
            "_links": {
                "self": "https://example.com/wp-json/wc-bookings/v1/products/categories/batch"
            }
        },
        "/wc-bookings/v1/resources": {
            "namespace": "wc-bookings/v1",
            "methods": [
                "GET",
                "POST"
            ],
            "endpoints": [
                {
                    "methods": [
                        "GET"
                    ],
                    "args": {
                        "context": {
                            "required": false,
                            "default": "view",
                            "enum": [
                                "view"
                            ],
                            "description": "Scope under which the request is made; determines fields present in response.",
                            "type": "string"
                        },
                        "page": {
                            "required": false,
                            "default": 1,
                            "description": "Current page of the collection.",
                            "type": "integer"
                        },
                        "per_page": {
                            "required": false,
                            "default": 10,
                            "description": "Maximum number of items to be returned in result set.",
                            "type": "integer"
                        },
                        "search": {
                            "required": false,
                            "description": "Limit results to those matching a string.",
                            "type": "string"
                        },
                        "after": {
                            "required": false,
                            "description": "Limit response to resources published after a given ISO8601 compliant date.",
                            "type": "string"
                        },
                        "before": {
                            "required": false,
                            "description": "Limit response to resources published before a given ISO8601 compliant date.",
                            "type": "string"
                        },
                        "exclude": {
                            "required": false,
                            "default": [],
                            "description": "Ensure result set excludes specific IDs.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        },
                        "include": {
                            "required": false,
                            "default": [],
                            "description": "Limit result set to specific ids.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        },
                        "offset": {
                            "required": false,
                            "description": "Offset the result set by a specific number of items.",
                            "type": "integer"
                        },
                        "order": {
                            "required": false,
                            "default": "desc",
                            "enum": [
                                "asc",
                                "desc"
                            ],
                            "description": "Order sort attribute ascending or descending.",
                            "type": "string"
                        },
                        "orderby": {
                            "required": false,
                            "default": "date",
                            "enum": [
                                "date",
                                "id",
                                "include",
                                "title",
                                "slug"
                            ],
                            "description": "Sort collection by object attribute.",
                            "type": "string"
                        }
                    }
                },
                {
                    "methods": [
                        "POST"
                    ],
                    "args": {
                        "availability": {
                            "required": false,
                            "type": {
                                "description": "Availability date/time range type string.",
                                "type": "string",
                                "readonly": true,
                                "context": [
                                    "view"
                                ]
                            }
                        }
                    }
                }
            ],
            "_links": {
                "self": "https://example.com/wp-json/wc-bookings/v1/resources"
            }
        },
        "/wc-bookings/v1/resources/(?P<id>[\\d]+)": {
            "namespace": "wc-bookings/v1",
            "methods": [
                "GET",
                "POST",
                "PUT",
                "PATCH",
                "DELETE"
            ],
            "endpoints": [
                {
                    "methods": [
                        "GET"
                    ],
                    "args": {
                        "id": {
                            "required": false,
                            "description": "Unique identifier for the resource.",
                            "type": "integer"
                        },
                        "context": {
                            "required": false,
                            "default": "view",
                            "enum": [
                                "view"
                            ],
                            "description": "Scope under which the request is made; determines fields present in response.",
                            "type": "string"
                        }
                    }
                },
                {
                    "methods": [
                        "POST",
                        "PUT",
                        "PATCH"
                    ],
                    "args": {
                        "id": {
                            "required": false,
                            "description": "Unique identifier for the resource.",
                            "type": "integer"
                        },
                        "availability": {
                            "required": false,
                            "type": {
                                "description": "Availability date/time range type string.",
                                "type": "string",
                                "readonly": true,
                                "context": [
                                    "view"
                                ]
                            }
                        }
                    }
                },
                {
                    "methods": [
                        "DELETE"
                    ],
                    "args": {
                        "id": {
                            "required": false,
                            "description": "Unique identifier for the resource.",
                            "type": "integer"
                        },
                        "force": {
                            "required": false,
                            "default": false,
                            "description": "Whether to bypass trash and force deletion.",
                            "type": "boolean"
                        }
                    }
                }
            ]
        },
        "/wc-bookings/v1/resources/batch": {
            "namespace": "wc-bookings/v1",
            "methods": [
                "POST",
                "PUT",
                "PATCH"
            ],
            "endpoints": [
                {
                    "methods": [
                        "POST",
                        "PUT",
                        "PATCH"
                    ],
                    "args": {
                        "availability": {
                            "required": false,
                            "type": {
                                "description": "Availability date/time range type string.",
                                "type": "string",
                                "readonly": true,
                                "context": [
                                    "view"
                                ]
                            }
                        }
                    }
                }
            ],
            "_links": {
                "self": "https://example.com/wp-json/wc-bookings/v1/resources/batch"
            }
        },
        "/wc-bookings/v1/bookings": {
            "namespace": "wc-bookings/v1",
            "methods": [
                "GET",
                "POST"
            ],
            "endpoints": [
                {
                    "methods": [
                        "GET"
                    ],
                    "args": {
                        "context": {
                            "required": false,
                            "default": "view",
                            "description": "Scope under which the request is made; determines fields present in response.",
                            "type": "string"
                        },
                        "page": {
                            "required": false,
                            "default": 1,
                            "description": "Current page of the collection.",
                            "type": "integer"
                        },
                        "per_page": {
                            "required": false,
                            "default": 10,
                            "description": "Maximum number of items to be returned in result set.",
                            "type": "integer"
                        },
                        "search": {
                            "required": false,
                            "description": "Limit results to those matching a string.",
                            "type": "string"
                        },
                        "after": {
                            "required": false,
                            "description": "Limit response to resources published after a given ISO8601 compliant date.",
                            "type": "string"
                        },
                        "before": {
                            "required": false,
                            "description": "Limit response to resources published before a given ISO8601 compliant date.",
                            "type": "string"
                        },
                        "exclude": {
                            "required": false,
                            "default": [],
                            "description": "Ensure result set excludes specific IDs.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        },
                        "include": {
                            "required": false,
                            "default": [],
                            "description": "Limit result set to specific ids.",
                            "type": "array",
                            "items": {
                                "type": "integer"
                            }
                        },
                        "offset": {
                            "required": false,
                            "description": "Offset the result set by a specific number of items.",
                            "type": "integer"
                        },
                        "order": {
                            "required": false,
                            "default": "desc",
                            "enum": [
                                "asc",
                                "desc"
                            ],
                            "description": "Order sort attribute ascending or descending.",
                            "type": "string"
                        },
                        "orderby": {
                            "required": false,
                            "default": "date",
                            "enum": [
                                "date",
                                "id",
                                "include",
                                "title",
                                "slug"
                            ],
                            "description": "Sort collection by object attribute.",
                            "type": "string"
                        }
                    }
                },
                {
                    "methods": [
                        "POST"
                    ],
                    "args": []
                }
            ],
            "_links": {
                "self": "https://example.com/wp-json/wc-bookings/v1/bookings"
            }
        },
        "/wc-bookings/v1/bookings/(?P<id>[\\d]+)": {
            "namespace": "wc-bookings/v1",
            "methods": [
                "GET",
                "POST",
                "PUT",
                "PATCH",
                "DELETE"
            ],
            "endpoints": [
                {
                    "methods": [
                        "GET"
                    ],
                    "args": {
                        "id": {
                            "required": false,
                            "description": "Unique identifier for the resource.",
                            "type": "integer"
                        },
                        "context": {
                            "required": false,
                            "default": "view",
                            "description": "Scope under which the request is made; determines fields present in response.",
                            "type": "string"
                        }
                    }
                },
                {
                    "methods": [
                        "POST",
                        "PUT",
                        "PATCH"
                    ],
                    "args": {
                        "id": {
                            "required": false,
                            "description": "Unique identifier for the resource.",
                            "type": "integer"
                        }
                    }
                },
                {
                    "methods": [
                        "DELETE"
                    ],
                    "args": {
                        "id": {
                            "required": false,
                            "description": "Unique identifier for the resource.",
                            "type": "integer"
                        },
                        "force": {
                            "required": false,
                            "default": false,
                            "description": "Whether to bypass trash and force deletion.",
                            "type": "boolean"
                        }
                    }
                }
            ]
        },
        "/wc-bookings/v1/bookings/batch": {
            "namespace": "wc-bookings/v1",
            "methods": [
                "POST",
                "PUT",
                "PATCH"
            ],
            "endpoints": [
                {
                    "methods": [
                        "POST",
                        "PUT",
                        "PATCH"
                    ],
                    "args": []
                }
            ],
            "_links": {
                "self": "https://example.com/wp-json/wc-bookings/v1/bookings/batch"
            }
        },
        "/wc-bookings/v1/products/slots": {
            "namespace": "wc-bookings/v1",
            "methods": [
                "GET"
            ],
            "endpoints": [
                {
                    "methods": [
                        "GET"
                    ],
                    "args": []
                }
            ],
            "_links": {
                "self": "https://example.com/wp-json/wc-bookings/v1/products/slots"
            }
        }
    },
    "_links": {
        "up": [
            {
                "href": "https://example.com/wp-json/"
            }
        ]
    }
}