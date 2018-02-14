# Introduction

Welcome to the WMS API! You can use our API to access WMS API endpoints, which can get information on various `products`, `vendors`, `users`, `request_orders`, `purchase_orders`, etc in our database. 

<!-- We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right. -->

<!-- This example API documentation page was created with [Slate](https://github.com/tripit/slate). Feel free to edit it and use it as a base for your own API's documentation. -->

# Authentication

> To authorize, use this code:

```bash
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

> Make sure to replace `meowmeowmeow` with your API key.

Will be updated!

<!-- Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://domain/developers). -->

<!-- Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following: -->

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

# Products

## Get All Products

```bash
curl "http://domain/api/products"
  # -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
    "jsonapi": {
        "version": "1.0"
    },
    "data": [
        {
            "id": 56,
            "type": "products",
            "attributes": {
                "name": "test",
                "min": 1,
                "max": 10,
                "barcode": "7777777",
                "price": "2.000",
                "description": "5",
                "panjang": "4.000",
                "lebar": "5.000",
                "tinggi": "6.000",
                "berat": "7.000",
                "conversion": null,
                "fk_categories": null,
                "fk_satuan": null,
                "fk_statuses": null,
                "fk_satuanJual": null,
                "fk_satuanBeli": null,
                "createdAt": "2018-01-21T00:00:00.000Z",
                "updatedAt": "2018-02-02T00:00:00.000Z"
            },
            "relationships": {
                "vendors": {
                    "data": [
                        {
                            "type": "vendors",
                            "id": 1
                        }
                    ]
                },
                "vendor_items": {
                    "data": [
                        {
                            "type": "vendor_items",
                            "id": 4
                        }
                    ]
                }
            }
        },
        {
            "id": 57,
            "type": "products",
            "attributes": {
                "name": "Teh Pucuk 350ml",
                "min": 123,
                "max": 7777,
                "barcode": "7777777",
                "price": "2.000",
                "description": "5",
                "panjang": "4.000",
                "lebar": "5.000",
                "tinggi": "6.000",
                "berat": "7.000",
                "conversion": null,
                "fk_categories": 2,
                "fk_satuan": 2,
                "fk_statuses": 2,
                "fk_satuanJual": 2,
                "fk_satuanBeli": 2,
                "createdAt": "2018-01-21T00:00:00.000Z",
                "updatedAt": "2018-02-03T13:52:24.000Z"
            },
            "relationships": {
                "vendors": {
                    "data": [
                        {
                            "type": "vendors",
                            "id": 1
                        },
                        {
                            "type": "vendors",
                            "id": 2
                        },
                        {
                            "type": "vendors",
                            "id": 3
                        }
                    ]
                },
                "vendor_items": {
                    "data": [
                        {
                            "type": "vendor_items",
                            "id": 1
                        },
                        {
                            "type": "vendor_items",
                            "id": 2
                        },
                        {
                            "type": "vendor_items",
                            "id": 3
                        }
                    ]
                },
                "categories": {
                    "data": [
                        {
                            "type": "categories",
                            "id": 2
                        }
                    ]
                },
                "satuan": {
                    "data": [
                        {
                            "type": "satuan",
                            "id": 2
                        }
                    ]
                },
                "statuses": {
                    "data": [
                        {
                            "type": "statuses",
                            "id": 2
                        }
                    ]
                },
                "satuanJual": {
                    "data": [
                        {
                            "type": "satuanJual",
                            "id": 2
                        }
                    ]
                },
                "satuanBeli": {
                    "data": [
                        {
                            "type": "satuanBeli",
                            "id": 2
                        }
                    ]
                }
            }
        },
    ],
    "included": [
        {
            "id": 4,
            "type": "vendor_items",
            "attributes": {
                "fk_vendors": 1,
                "fk_products": 56,
                "tax": null,
                "price": "77777.000",
                "level": 1,
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 1,
            "type": "vendor_items",
            "attributes": {
                "fk_vendors": 1,
                "fk_products": 57,
                "tax": null,
                "price": "10000.000",
                "level": 1,
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 2,
            "type": "vendor_items",
            "attributes": {
                "fk_vendors": 2,
                "fk_products": 57,
                "tax": null,
                "price": "15000.500",
                "level": 2,
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 3,
            "type": "vendor_items",
            "attributes": {
                "fk_vendors": 3,
                "fk_products": 57,
                "tax": null,
                "price": "18000.000",
                "level": 2,
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 1,
            "type": "vendors",
            "attributes": {
                "name": "Vendor Pertama",
                "address": null,
                "telephone": null,
                "fax": null,
                "email": null,
                "website": null,
                "salesPerson": null,
                "attention": null,
                "contactPerson": null,
                "paymentTerms": null,
                "status": null,
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 2,
            "type": "vendors",
            "attributes": {
                "name": "Edbert",
                "address": "Cibubur",
                "telephone": "1",
                "fax": "2",
                "email": "3",
                "website": "4",
                "salesPerson": 5,
                "attention": 6,
                "contactPerson": 7,
                "paymentTerms": null,
                "status": 8,
                "createdAt": "2018-01-22T00:00:00.000Z",
                "updatedAt": "2018-01-22T00:00:00.000Z"
            }
        },
        {
            "id": 3,
            "type": "vendors",
            "attributes": {
                "name": "Test Ganti Nama",
                "address": "Depok",
                "telephone": "021",
                "fax": "021",
                "email": "kareem.lukitomo@gmail.com",
                "website": "google.com",
                "salesPerson": 1,
                "attention": 1,
                "contactPerson": 1,
                "paymentTerms": null,
                "status": 1,
                "createdAt": "2018-01-22T00:00:00.000Z",
                "updatedAt": "2018-01-22T00:00:00.000Z"
            }
        },
        {
            "id": 2,
            "type": "categories",
            "attributes": {
                "name": "minuman siap saji",
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 2,
            "type": "satuan",
            "attributes": {
                "name": "krat",
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 2,
            "type": "statuses",
            "attributes": {
                "name": "available",
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 2,
            "type": "satuanJual",
            "attributes": {
                "name": "gram",
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 2,
            "type": "satuanBeli",
            "attributes": {
                "name": "gram",
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 6,
            "type": "vendors",
            "attributes": {
                "name": "John Doe",
                "address": "Jakarta",
                "telephone": "120931023",
                "fax": "123123",
                "email": "jogn",
                "website": "doe",
                "salesPerson": null,
                "attention": null,
                "contactPerson": null,
                "paymentTerms": null,
                "status": 1,
                "createdAt": "2018-01-25T00:00:00.000Z",
                "updatedAt": "2018-01-25T00:00:00.000Z"
            }
        },
        {
            "id": 1,
            "type": "categories",
            "attributes": {
                "name": "minuman mentah",
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 2,
            "type": "satuan",
            "attributes": {
                "name": "krat",
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 2,
            "type": "statuses",
            "attributes": {
                "name": "available",
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 2,
            "type": "satuanJual",
            "attributes": {
                "name": "gram",
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 1,
            "type": "satuanBeli",
            "attributes": {
                "name": "kilogram",
                "createdAt": null,
                "updatedAt": null
            }
        }
    ]
}
```

This endpoint retrieves all products.

### HTTP Request

`GET http://domain/api/products`

<!-- ### Query Parameters -->
<!--  -->
<!-- Parameter | Default | Description -->
<!-- --------- | ------- | ----------- -->
<!-- include_cats | false | If set to true, the result will also include cats. -->
<!-- available | true | If set to false, the result will include kittens that have already been adopted. -->

<!-- <aside class="success"> -->
<!-- Remember — a happy kitten is an authenticated kitten! -->
<!-- </aside> -->

## Get a Specific Product

```bash
curl "http://domain/api/products/:id"
  # -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
    "jsonapi": {
        "version": "1.0"
    },
    "data": [
        {
            "id": 56,
            "type": "products",
            "attributes": {
                "name": "Teh Pucuk 600ml",
                "min": 1,
                "max": 10,
                "barcode": "7777777",
                "price": "2.000",
                "description": "5",
                "panjang": "4.000",
                "lebar": "5.000",
                "tinggi": "6.000",
                "berat": "7.000",
                "conversion": null,
                "fk_categories": 2,
                "fk_satuan": null,
                "fk_statuses": null,
                "fk_satuanJual": null,
                "fk_satuanBeli": null,
                "createdAt": "2018-01-21T00:00:00.000Z",
                "updatedAt": "2018-02-02T00:00:00.000Z"
            },
            "relationships": {
                "vendors": {
                    "data": [
                        {
                            "type": "vendors",
                            "id": 1
                        }
                    ]
                },
                "vendor_items": {
                    "data": [
                        {
                            "type": "vendor_items",
                            "id": 4
                        }
                    ]
                },
                "categories": {
                    "data": [
                        {
                            "type": "categories",
                            "id": 2
                        }
                    ]
                }
            }
        }
    ],
    "included": [
        {
            "id": 4,
            "type": "vendor_items",
            "attributes": {
                "fk_vendors": 1,
                "fk_products": 56,
                "tax": null,
                "price": "77777.000",
                "level": 1,
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 1,
            "type": "vendors",
            "attributes": {
                "name": "Vendor Pertama",
                "address": null,
                "telephone": null,
                "fax": null,
                "email": null,
                "website": null,
                "salesPerson": null,
                "attention": null,
                "contactPerson": null,
                "paymentTerms": null,
                "status": null,
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 2,
            "type": "categories",
            "attributes": {
                "name": "minuman siap saji",
                "createdAt": null,
                "updatedAt": null
            }
        }
    ]
}

```

This endpoint retrieves a specific kitten.

<!-- <aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside> -->

### HTTP Request

`GET http://domain/products/:id`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the `products` to retrieve

# Vendors

## Get All Vendors

```bash
curl "http://domain/api/vendors"
  # -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
    "jsonapi": {
        "version": "1.0"
    },
    "data": [
        {
            "id": 1,
            "type": "vendors",
            "attributes": {
                "name": "Vendor Pertama",
                "address": null,
                "telephone": null,
                "fax": null,
                "email": null,
                "website": null,
                "salesPerson": null,
                "attention": null,
                "contactPerson": null,
                "paymentTerms": null,
                "status": null,
                "createdAt": null,
                "updatedAt": null
            },
            "relationships": {
                "products": {
                    "data": [
                        {
                            "type": "products",
                            "id": 56
                        },
                        {
                            "type": "products",
                            "id": 57
                        }
                    ]
                },
                "vendor_items": {
                    "data": [
                        {
                            "type": "vendor_items",
                            "id": 1
                        },
                        {
                            "type": "vendor_items",
                            "id": 4
                        }
                    ]
                }
            }
        },
        {
            "id": 2,
            "type": "vendors",
            "attributes": {
                "name": "Edbert",
                "address": "Cibubur",
                "telephone": "1",
                "fax": "2",
                "email": "3",
                "website": "4",
                "salesPerson": 5,
                "attention": 6,
                "contactPerson": 7,
                "paymentTerms": null,
                "status": 8,
                "createdAt": "2018-01-22T00:00:00.000Z",
                "updatedAt": "2018-01-22T00:00:00.000Z"
            },
            "relationships": {
                "products": {
                    "data": [
                        {
                            "type": "products",
                            "id": 57
                        }
                    ]
                },
                "vendor_items": {
                    "data": [
                        {
                            "type": "vendor_items",
                            "id": 2
                        }
                    ]
                }
            }
        },
    ],
    "included": [
        {
            "id": 1,
            "type": "vendor_items",
            "attributes": {
                "fk_vendors": 1,
                "fk_products": 57,
                "tax": null,
                "price": "10000.000",
                "level": 1,
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 4,
            "type": "vendor_items",
            "attributes": {
                "fk_vendors": 1,
                "fk_products": 56,
                "tax": null,
                "price": "77777.000",
                "level": 1,
                "createdAt": null,
                "updatedAt": null
            }
        },
        {
            "id": 56,
            "type": "products",
            "attributes": {
                "name": "Teh Pucuk 600ml",
                "min": 1,
                "max": 10,
                "barcode": "7777777",
                "price": "2.000",
                "description": "5",
                "panjang": "4.000",
                "lebar": "5.000",
                "tinggi": "6.000",
                "berat": "7.000",
                "conversion": null,
                "fk_categories": 2,
                "fk_satuan": null,
                "fk_statuses": null,
                "fk_satuanJual": null,
                "fk_satuanBeli": null,
                "createdAt": "2018-01-21T00:00:00.000Z",
                "updatedAt": "2018-02-02T00:00:00.000Z"
            }
        },
        {
            "id": 57,
            "type": "products",
            "attributes": {
                "name": "Teh Pucuk 350ml",
                "min": 123,
                "max": 7777,
                "barcode": "7777777",
                "price": "2.000",
                "description": "5",
                "panjang": "4.000",
                "lebar": "5.000",
                "tinggi": "6.000",
                "berat": "7.000",
                "conversion": null,
                "fk_categories": 2,
                "fk_satuan": 2,
                "fk_statuses": 2,
                "fk_satuanJual": 2,
                "fk_satuanBeli": 2,
                "createdAt": "2018-01-21T00:00:00.000Z",
                "updatedAt": "2018-02-03T13:52:24.000Z"
            }
        },
        {
            "id": 2,
            "type": "vendor_items",
            "attributes": {
                "fk_vendors": 2,
                "fk_products": 57,
                "tax": null,
                "price": "15000.500",
                "level": 2,
                "createdAt": null,
                "updatedAt": null
            }
        },
    ]
}
```

This endpoint retrieves all vendors.

### HTTP Request

`GET http://domain/api/vendors`

<!-- ### Query Parameters -->
<!--  -->
<!-- Parameter | Default | Description -->
<!-- --------- | ------- | ----------- -->
<!-- include_cats | false | If set to true, the result will also include cats. -->
<!-- available | true | If set to false, the result will include kittens that have already been adopted. -->

<!-- <aside class="success"> -->
<!-- Remember — a happy kitten is an authenticated kitten! -->
<!-- </aside> -->
