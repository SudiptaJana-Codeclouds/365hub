## Project Outline

365Hub is a brilliant approach to manage products using a single UI.
Currently using this platform users can manage products, create and edit
them to the different channels. This platform will act as a hub for all
365 instances like steelriver, alternascript, valley food storage, and
others.

## Getting Started

### Prerequisite

-   Need XAMPP or any apache php based development environment

-   Need node js 14.x or upper version

### **Installation instructions**

1.  At first you need to clone the git repository from GitHub, so youneed to login to the GitHub portal and get the clone URL.
    > ![](media/image3.png){width="6.5in" height="2.736111111111111in"}\
    > git clone git@github.com:365holdings/365hub.git

2.  Then go to your project app directory and clone the site using the below command.
    > git clone git@github.com:365holdings/365hub.git

3.  Copy .env.example to new file .env using below command
    > cp .env.example .env

4.  Update the .env file with required information as per your configuration. Eg db connection details, smtp settings
    > details and domain

5.  Then install external Laravel packages using below command
    > composer install

6.  Generate a unique key for the project using below command\
    > php artisan key:generate

7.  Migrate database and table using this command\
    > php artisan migrate

8.  Install node packages using this command\
    > npm install

9.  Run build version of the project using below command\
    > npm run build

10. Hit the URL on the browser

## **Project Scope/Modules**

### **Users**

Users can log in and view their dashboard. They will get an invitation
through mail by administration. After they receive their invitation they
can register to the platform After login they can edit their profile
settings. They can take different actions based on their roles like
create/edit products, create companies/channels and many more. Also they
can reset their password if they forget them.

![](media/image1.png){width="6.5in" height="2.125in"}

While inviting a user admin can set their role as well will populate as
a dropdown.

![](media/image2.png){width="6.5in" height="2.4444444444444446in"}

### **Roles**

Every user has a particular role. Every role will have many actions and
permissions. Admin can edit permission for every role. Admin can
create/edit roles through their dashboard.

Admin/role based user will set the permission for each role by toggling
the switch on edit role page.

![](media/image7.png){width="6.5in" height="3.263888888888889in"}

### **Permissions**

System will have some permissions. Admin can view the lists of
permissions. From their account. Every permission has a self explanatory
role. Like create-product has the role to create products. Some
permissions are limited to modify like create permission or update
permissions. Those permissions will not shown on edit role page. THose
mostly are predefined permissions.

##### **Company/Channels**

Users can create/edit companies and channels also they
activate/deactivate them if they have that permissions. Every company
(steelriver, alternascript) has their particular channels like fulfil,
sticky. These companies will automatically populate on product creation
pages. Users can choose the company to which they want to import the
product.

![](media/image8.png){width="6.5in" height="2.0555555555555554in"}

##### **Products**

Users can create/edit products through this system. Users can choose in
which channels they want to import the product. They can import more
than one channel in one go. Also users can have the option to create
bulk products through CSV import.

For now this instances are active

-   Steel River (Company)

    -   SR Fulfil (365sandbox)

    -   SR Sticky.io (limelight)

    -   SR Shopify (nicki's diapers sandbox)

###### **Create Product Fields Specification - **

**Product Title** **(required)** - Title of the product

**Product SKU (required)** - SKU of the product

**Fulfil.io Product Template (required for Fulfil) -** Product template
is a field in which template the product will create on Fulfil. This
field is required if the variant option is unchecked. It will hide and
won't be required once the variant option is checked. The product
templates will automatically fetch from fulfil and populate on dropdown
if a fulfil instance is checked.

**Sticky.io Product Category (required for sticky) -** Product sticky
category is a field in which the category under the product will be
created on Fulfil. The product sticky category will automatically fetch
from fulfil and populate on dropdown if a fulfil instance is checked.

**Max Sticky.io Product Quantity (required for sticky/shopify) -** This
field is max quantity for sticky and quantity for shopify.

**Product Price (required) -** The product price (numerical input).

**Product Cost (required) -** The product cost (numerical input).

**Product Cost Price Method** - This field is a dropdown of value
average and fixed.

**Product Description (required) -** The **p**roduct description.

**Media** (applicable for fulfil/shopify) - This field is a file
dropzone to set the media of the product.

**Product status -** This field is a file dropzone to set the media of
the product.

**Product Salable on fulfil** (applicable for fulfil) - This field is a
checkbox to set the product will be saleable or not

**Product Purchasable on fulfil** (applicable for fulfil) - This field
is a checkbox to set the product will be purchasable or not

**Product Scan Required on fulfil** (applicable for fulfil) - This field
is a checkbox to set the product will be scan required or not

**Product Publish to Shopify** (applicable for fulfil) - This field is a
checkbox to set the product will be scan required or not

**Shopify ADD ON / OTO** (applicable for shopify) - This is a checkbox
to select whether the ADD ON/OTO product will create or not. If this is
checked then respective input will open to set the price for ADD ON/OTO

![](media/image4.png){width="6.5in" height="1.0in"}

**Suppliers** (applicable for fulfil) - This field is a dropdown of
suppliers that automatically fetch and populate from fulfil. It will set
the supplier for a product.

**HS CODE** (applicable for fulfil) - This field will set the hs code
for a product on fulfil.

**Vendor Lead Time** (applicable for fulfil) - This field will set the
vendor lead time for a product on fulfil.

**Country Of Origin** (applicable for fulfil) - This field will set the
Country of origin for a product on fulfil. This is a dropdown of
countries.

**GS1** (applicable for none) - This field is text input that will be
stored on the database.

**Product Shopify Type** (applicable for shopify) - This field will set
the type for a product on shopify.

**Product Shopify Vendor** (applicable for shopify) - This field will
set the vendor for a product on shopify.

**Tag** (applicable for shopify) - This field will set the tag for a
product on shopify. This is a dropdown of existing tags that will fetch
from the database or you can create another tag on the go.

**Digital Or Physical** (applicable for shopify, sticky, fulfil) - This
field will set the product digital or physical. If this check then
Product shipping digital url text input will open.

![](media/image5.png){width="6.5in" height="1.0694444444444444in"}

**Product shipping digital url (required if product is digital)**
(applicable for all) - To set the digital url for the product.

**Shippable** (applicable for shopify) - This field will set the product
shippable or not.

**Product Weight/Weight Uom/Width/Height/Length/Dimension Uom**
(applicable for all) **-** This will set product Weight/Weight
Uom/Width/Height/Length/Dimension Uom.These fields only applicable if
the product is physical.

**Variants** (applicable for shopify/fulfil) - This field will set the
product if the product has variants or not.

![](media/image6.png){width="6.5in" height="2.4166666666666665in"}

Users can set 3 options between size, color, material, style, title and
their respective values. You can also remove variants also if not
needed.Users also preview variants and set their SKU and price
respectively. These inputs will create variant products on shopify and
fulfil.

> ![](media/image9.png){width="6.5in" height="3.263888888888889in"}

#### 

#### 


#### **API Documentation**

The following APIs belong to the Laravel routing. They are used throughout the system.

##### **Sign Up**

This API used for signing up into the system

**POST**  **api/sign-up**

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| name | Required | Name of the user |
| emali | Required |Should be a valid email | Should be a unique email | Email of the user |
| password | Required | Password of the user |
| confirm\_password | Required | Should be same as password | Password confirmation |

**Response**

```json
{
    "success" : "Register successful"
}
```

##### **Login**

This API used for login into the system

**POST**  **api/login**

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| name | Required | Name of the user |
| emali | Required |Should be a valid email | Email of the user |

**Response**

```json
{
    "auth_token": "125|SUHBRtB3nDq0xfkZF0yLAE5dmv9UkfzMekCCwfn2",
    "token_type": "Bearer",
    "message": "login successful",
    "user": {
        "id": 24,
        "name": "Sd",
        "email": "sudipta.jana@codeclouds.in",
        "email_verified_at": null,
        "deleted_at": null,
        "last_login_at": "2021-07-09T13:52:04.000000Z",
        "last_login_ip": "127.0.0.1",
        "is_active": true,
        "created_at": "30 Jun, 2021",
        "updated_at": "2021-07-09T13:52:04.000000Z",
        "role": {
            "id": 2,
            "name": "sub admin",
            "description": null,
            "deleted_at": null,
            "created_at": "2021-05-31T15:11:11.000000Z",
            "updated_at": "2021-05-31T15:18:13.000000Z",
            "pivot": {
                "user_id": 24,
                "role_id": 2
            }
        },
        "permissions": [
            {
                "id": 26,
                "name": "read product",
                "slug": "read-product",
                "model": "product",
                "description": "Can read product",
                "content": {
                    "name": "Products",
                    "type": "View"
                },
                "active": true,
                "created_at": "2021-06-03T08:32:50.000000Z",
                "updated_at": "2021-06-21T12:33:27.000000Z",
                "pivot": {
                    "role_id": 2,
                    "permission_id": 26
                }
            }
        ],
        "last_login_at_diff_for_human": "2 weeks ago"
    }
}
```

##### **Forget Password**

**GET**  **api/forget-password**

This API is used to reset user password

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| emali | Required |Should be a valid email | Email of the user |

##### **Company**

**GET**  **api/admin/company**

This API is used to fetch the lists of companies

**Response**

```json
{
    "data": [
        {
            "id": 1,
            "name": "Steel River",
            "description": "description",
            "is_active": true,
            "created_at": "02/25/2021",
            "updated_at": "2021-04-23T09:11:28.000000Z",
            "channels": [
                {
                    "id": 1,
                    "company_id": 1,
                    "name": "SR Fulfil",
                    "description": null,
                    "credential": {
                        "url": "https://365-holdings-sandbox.fulfil.io/api/v2/model/",
                        "x_api_key": "a026a119032241aba46e757bed20814c",
                        "product_url": "https://365-holdings-sandbox.fulfil.io/client/#/model/product.product/"
                    },
                    "type": "fulfil",
                    "is_active": true,
                    "created_at": "02/25/2021",
                    "updated_at": "2021-05-24T11:24:02.000000Z"
                }
            ]
        },
        {
            "id": 2,
            "name": "Nicki’s Diapers",
            "description": null,
            "is_active": true,
            "created_at": "02/25/2021",
            "updated_at": "2021-04-05T12:35:15.000000Z",
            "channels": [
                {
                    "id": 4,
                    "company_id": 2,
                    "name": "ND Fulfil",
                    "description": null,
                    "credential": null,
                    "type": null,
                    "is_active": true,
                    "created_at": "02/25/2021",
                    "updated_at": "2021-02-25T08:54:45.000000Z"
                }
            ]
        }
    ]
}
```

**POST**  **api/admin/company**

This API is used to create new company

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| name | Required | Name of the company |

**Response**

```json
{
    "status": "success",
    "data": {
        "name": "New Company",
        "updated_at": "2021-07-23T14:57:53.000000Z",
        "created_at": "07/23/2021",
        "id": 9
    }
}
```

**PUT**  **api/admin/company/{id}**

This API is used to update existing company

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| name | Required | Name of the company |

**Response**

```json
{
    "status": "success",
    "data": {
        "name": "New Company",
        "updated_at": "2021-07-23T14:57:53.000000Z",
        "created_at": "07/23/2021",
        "id": 9
    }
}
```

**PUT**  **api/admin/company/status/update/{id}**

This API is used to update status of company (active or inactive)

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| is\_active | Optional | Status of the channel (default active) |

**Response**

```json
{
    "status": "success",
    "data": {
        "name": "New Company",
        "updated_at": "2021-07-23T14:57:53.000000Z",
        "created_at": "07/23/2021",
        "id": 9
    }
}
```

##### **Channel**

**GET**  **api/admin/channel**

This API is used to fetch the lists of channels

**Response**

```json
{
    "data": [
        {
            "id": 1,
            "company_id": 1,
            "name": "SR Fulfil",
            "description": null,
            "credential": {
                "url": "https://365-holdings-sandbox.fulfil.io/api/v2/model/",
                "x_api_key": "a026a119032241aba46e757bed20814c",
                "product_url": "https://365-holdings-sandbox.fulfil.io/client/#/model/product.product/"
            },
            "type": "fulfil",
            "is_active": true,
            "created_at": "02/25/2021",
            "updated_at": "2021-05-24T11:24:02.000000Z",
            "company": {
                "id": 1,
                "name": "Steel River",
                "description": "description",
                "is_active": true,
                "created_at": "02/25/2021",
                "updated_at": "2021-04-23T09:11:28.000000Z"
            },
            "instance_options": []
        },
        {
            "id": 2,
            "company_id": 1,
            "name": "SR Sticky.io/LL",
            "description": null,
            "credential": {
                "url": "https://sos.limelightcrm.com/api/",
                "username": "api-sos-live",
                "password": "s7SVBrnswPAmsV",
                "product_url": "https://sos.limelightcrm.com/admin/products/products.php?product_id="
            },
            "type": "sticky",
            "is_active": true,
            "created_at": "02/25/2021",
            "updated_at": "2021-05-24T11:25:08.000000Z",
            "company": {
                "id": 1,
                "name": "Steel River",
                "description": "description",
                "is_active": true,
                "created_at": "02/25/2021",
                "updated_at": "2021-04-23T09:11:28.000000Z"
            },
            "instance_options": []
        }
    ]
}
```

**POST**  **api/admin/channel**

This API is used to create new channel

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| name | Required | Name of the channel |
| type | Required | value should be between fulfil, sticky, shopify | Type of the channel |
| instance\_options | Optional | Instances options for the channel, like API url, API key etc |

**Response**

```json
{
    "status": "success",
    "data": {
        "name": "New Channel",
        "type": "sticky",
        "company_id": "1",
        "credential": null,
        "updated_at": "2021-07-26T07:22:17.000000Z",
        "created_at": "07/26/2021",
        "id": 29
    }
}
```

**PUT**  **api/admin/channel/{id}**

This API is used to update existing channel

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| name | Required | Name of the channel |
| type | Required | value should be between fulfil, sticky, shopify | Type of the channel |
| instance\_options | Optional | Instances options for the channel, like API url, API key etc |

**Response**

```json
{
    "status": "success",
    "data": true
}
```

**PUT**  **api/admin/channel/status/update/{id}**

This API is used to update status of channel (active or inactive)

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| is\_active | Optional | Status of the channel (default active) |

**Response**

```json
{
    "status": "success",
    "data": true
}
```

##### **User**

**GET**  **api/admin/user**

This API is used to fetch the lists of users

**Response**

```json
{
    "data": [
        {
            "id": 24,
            "name": "Sd",
            "email": "sudipta.jana@codeclouds.in",
            "email_verified_at": null,
            "deleted_at": null,
            "last_login_at": "2021-07-23T14:51:50.000000Z",
            "last_login_ip": "127.0.0.1",
            "is_active": true,
            "created_at": "30 Jun, 2021",
            "updated_at": "2021-07-23T14:51:50.000000Z",
            "role": {
                "id": 2,
                "name": "sub admin",
                "description": null,
                "deleted_at": null,
                "created_at": "2021-05-31T15:11:11.000000Z",
                "updated_at": "2021-05-31T15:18:13.000000Z",
                "pivot": {
                    "user_id": 24,
                    "role_id": 2
                }
            },
            "permissions": [
                {
                    "id": 26,
                    "name": "read product",
                    "slug": "read-product",
                    "model": "product",
                    "description": "Can read product",
                    "content": {
                        "name": "Products",
                        "type": "View"
                    },
                    "active": true,
                    "created_at": "2021-06-03T08:32:50.000000Z",
                    "updated_at": "2021-06-21T12:33:27.000000Z",
                    "pivot": {
                        "role_id": 2,
                        "permission_id": 26
                    }
                }
            ],
            "last_login_at_diff_for_human": "2 days ago"
        }
    ]
}
```

**PUT**  **api/admin/user/{id}**

This API is used to update existing user

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| name | Required | Name of the user |
| email | Required |Should be a valid email | Should be a unique email | Email of the user |
| role\_id | Required | Role of the user |

**Response**

```json
{
    "success": true,
    "message": "User updated"
}
```

**PUT**  **api/admin/user/status/update/{id}**

This API is used to update status of user (active or inactive)

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| is\_active | Optional | Status of the user (default active) |

**Response**

```json
{
    "success": true,
    "message": "Status updated"
}
```

**GET**  **api/admin/auth-user**

This API is used to fetch the authorized user

**PUT**  **api/admin/profile/update**

This API is used to update authorized user&#39;s data

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| name | Required | Name of the user |
| email | Required |Should be a valid email | Should be a unique email | Email of the user |

**Response**

```json
{
    "success": true,
    "message": "Profile updated"
}
```

##### **Role**

**GET**  **api/admin/role**

This API is used to fetch the lists of roles

**Response**

```json
{
    "data": [
        {
            "id": 1,
            "name": "admin",
            "description": null,
            "deleted_at": null,
            "created_at": "25 Feb, 2021",
            "updated_at": "2021-02-25T09:02:21.000000Z",
            "total_users_count": 2,
            "permissions": [
                {
                    "id": 4,
                    "name": "delete user",
                    "slug": "delete-user",
                    "model": "user",
                    "description": "Can delete user",
                    "content": {
                        "name": "Users",
                        "type": "Delete"
                    },
                    "active": false,
                    "created_at": "2021-06-03T08:32:50.000000Z",
                    "updated_at": "2021-06-21T12:33:27.000000Z",
                    "pivot": {
                        "role_id": 1,
                        "permission_id": 4
                    }
                }
            ]
        },
        {
            "id": 2,
            "name": "sub admin",
            "description": null,
            "deleted_at": null,
            "created_at": "31 May, 2021",
            "updated_at": "2021-05-31T15:18:13.000000Z",
            "total_users_count": 3,
            "permissions": [
                {
                    "id": 26,
                    "name": "read product",
                    "slug": "read-product",
                    "model": "product",
                    "description": "Can read product",
                    "content": {
                        "name": "Products",
                        "type": "View"
                    },
                    "active": true,
                    "created_at": "2021-06-03T08:32:50.000000Z",
                    "updated_at": "2021-06-21T12:33:27.000000Z",
                    "pivot": {
                        "role_id": 2,
                        "permission_id": 26
                    }
                }
            ]
        }
    ]
}
```

**POST**  **api/admin/role**

This API is used to create new role

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| name | Required | Name of the role |

**Response**

```json
{
    "status": "success",
    "message": "Role is created"
}
```

**PUT**  **api/admin/role/{id}**

This API is used to update existing role

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| name | Required | Name of the role |

**Response**

```json
{
    "status": "success",
    "message": "Permission update"
}
```

##### **Permission**

**GET**  **api/admin/permission**

This API is used to fetch the lists of permissions

**Response**

```json
{
    "data": [
        {
            "id": 1,
            "name": "create user",
            "slug": "create-user",
            "model": "user",
            "description": "Can create user",
            "content": {
                "name": "Users",
                "type": "Create"
            },
            "active": true,
            "created_at": "03 Jun, 2021",
            "updated_at": "2021-06-21T12:33:27.000000Z"
        },
        {
            "id": 2,
            "name": "read user",
            "slug": "read-user",
            "model": "user",
            "description": "Can read user",
            "content": {
                "name": "Users",
                "type": "View"
            },
            "active": true,
            "created_at": "03 Jun, 2021",
            "updated_at": "2021-06-21T12:33:27.000000Z"
        }
    ]
}
```

**PUT**  **api/admin/role/permission/update/{id}**

This API is used to update permissions of a particular role

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| role\_id | Required | Role id of the user |
| permission\_id | Required | Permission id of the user |

**Response**

```json
{
    "status": "success",
    "message": "Permission update"
}
```

##### **Product**

**GET**  **api/admin/product**

This API is used to fetch the lists of products

**Response**

```json
{
    "data": [
        {
            "id": 347,
            "company_id": 1,
            "channel_id": 2,
            "channels": [
                {
                    "id": 2,
                    "company_id": 1,
                    "name": "SR Sticky.io/LL",
                    "description": null,
                    "credential": {
                        "url": "https://sos.limelightcrm.com/api/",
                        "username": "api-sos-live",
                        "password": "s7SVBrnswPAmsV",
                        "product_url": "https://sos.limelightcrm.com/admin/products/products.php?product_id="
                    },
                    "type": "sticky",
                    "is_active": true,
                    "created_at": "02/25/2021",
                    "updated_at": "2021-05-24T11:25:08.000000Z"
                }
            ],
            "title": "OTO: Product fulfil media test 0321",
            "price": 10,
            "cost": 10,
            "cost_price_method": "average",
            "description": "kjdasdbmn",
            "status": 3,
            "is_publish": true,
            "sku": "DEVTEST3379",
            "quantity": 10,
            "template": null,
            "sale_uom": null,
            "purchasable": true,
            "scan_required": true,
            "salable": true,
            "sticky_category_id": 13,
            "is_shippable": true,
            "shipping_digital_url": null,
            "type": null,
            "vendor": null,
            "tags": [],
            "is_digital": false,
            "weight": null,
            "weight_uom": null,
            "width": null,
            "height": null,
            "length": null,
            "dimensions_uom": null,
            "flavor": null,
            "supplement_type": null,
            "pills_per_bottle": null,
            "print": null,
            "suppliers": [],
            "hs_code": null,
            "vendor_lead_time": null,
            "country_id": null,
            "handle": null,
            "gs1": null,
            "has_variants": false,
            "variant_options": [],
            "variant_option_preview": [],
            "instance_response": {
                "status": "pending",
                "data": null,
                "payload": {
                    "product_name": "OTO: Product fulfil media test 0321",
                    "product_sku": "DEVTEST3379",
                    "product_price": "10",
                    "product_description": "kjdasdbmn",
                    "product_max_quantity": "10",
                    "shippable": true,
                    "shipping_weight": null,
                    "weight_unit_id": null,
                    "category_id": 13,
                    "events": [
                        "Order Refund"
                    ]
                }
            },
            "update_response": null,
            "created_at": "07/01/2021",
            "updated_at": "2021-07-01T14:18:53.000000Z",
            "channel": {
                "id": 2,
                "company_id": 1,
                "name": "SR Sticky.io/LL",
                "description": null,
                "credential": {
                    "url": "https://sos.limelightcrm.com/api/",
                    "username": "api-sos-live",
                    "password": "s7SVBrnswPAmsV",
                    "product_url": "https://sos.limelightcrm.com/admin/products/products.php?product_id="
                },
                "type": "sticky",
                "is_active": true,
                "created_at": "02/25/2021",
                "updated_at": "2021-05-24T11:25:08.000000Z"
            },
            "companies": {
                "id": 1,
                "name": "Steel River",
                "description": "description",
                "is_active": true,
                "created_at": "02/25/2021",
                "updated_at": "2021-04-23T09:11:28.000000Z"
            },
            "country": null,
            "child_products": null,
            "instance_status": "pending",
            "instance_id": null,
            "instance_product_url": "https://sos.limelightcrm.com/admin/products/products.php?product_id="
        },
        {
            "id": 346,
            "company_id": 1,
            "channel_id": 2,
            "channels": [
                {
                    "id": 2,
                    "company_id": 1,
                    "name": "SR Sticky.io/LL",
                    "description": null,
                    "credential": {
                        "url": "https://sos.limelightcrm.com/api/",
                        "username": "api-sos-live",
                        "password": "s7SVBrnswPAmsV",
                        "product_url": "https://sos.limelightcrm.com/admin/products/products.php?product_id="
                    },
                    "type": "sticky",
                    "is_active": true,
                    "created_at": "02/25/2021",
                    "updated_at": "2021-05-24T11:25:08.000000Z"
                }
            ],
            "title": "OTO: Product fulfil media test 0321",
            "price": 10,
            "cost": 10,
            "cost_price_method": "average",
            "description": "kjdasdbmn",
            "status": 3,
            "is_publish": true,
            "sku": "DEVTEST3379",
            "quantity": 10,
            "template": null,
            "sale_uom": null,
            "purchasable": true,
            "scan_required": true,
            "salable": true,
            "sticky_category_id": 12,
            "is_shippable": true,
            "shipping_digital_url": null,
            "type": null,
            "vendor": null,
            "tags": [],
            "is_digital": false,
            "weight": null,
            "weight_uom": null,
            "width": null,
            "height": null,
            "length": null,
            "dimensions_uom": null,
            "flavor": null,
            "supplement_type": null,
            "pills_per_bottle": null,
            "print": null,
            "suppliers": [],
            "hs_code": null,
            "vendor_lead_time": null,
            "country_id": null,
            "handle": null,
            "gs1": null,
            "has_variants": false,
            "variant_options": [],
            "variant_option_preview": [],
            "instance_response": {
                "status": "pending",
                "data": null,
                "payload": {
                    "product_name": "OTO: Product fulfil media test 0321",
                    "product_sku": "DEVTEST3379",
                    "product_price": "10",
                    "product_description": "kjdasdbmn",
                    "product_max_quantity": "10",
                    "shippable": true,
                    "shipping_weight": null,
                    "weight_unit_id": null,
                    "category_id": 12,
                    "events": [
                        "Order Refund"
                    ]
                }
            },
            "update_response": null,
            "created_at": "07/01/2021",
            "updated_at": "2021-07-01T14:18:53.000000Z",
            "channel": {
                "id": 2,
                "company_id": 1,
                "name": "SR Sticky.io/LL",
                "description": null,
                "credential": {
                    "url": "https://sos.limelightcrm.com/api/",
                    "username": "api-sos-live",
                    "password": "s7SVBrnswPAmsV",
                    "product_url": "https://sos.limelightcrm.com/admin/products/products.php?product_id="
                },
                "type": "sticky",
                "is_active": true,
                "created_at": "02/25/2021",
                "updated_at": "2021-05-24T11:25:08.000000Z"
            },
            "companies": {
                "id": 1,
                "name": "Steel River",
                "description": "description",
                "is_active": true,
                "created_at": "02/25/2021",
                "updated_at": "2021-04-23T09:11:28.000000Z"
            },
            "country": null,
            "child_products": null,
            "instance_status": "pending",
            "instance_id": null,
            "instance_product_url": "https://sos.limelightcrm.com/admin/products/products.php?product_id="
        }
    ]
}
```

**POST**  **api/admin/product**

This API is used to create new product

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| title | Required | Title of the product |
| sku | Required | SKU of the product |
| description | Required | Description of the product |
| price | Required | Price of the product |
| cost | Required | Cost of the product |
| quantity | Required for sticky and shopify | Max quantity for sticky, quantity for shopify |
| template | Required for fulfil | Optional if product has variant | Fulfil product template |
| salable | Optional (Fulfil) | Is the product salable or not (default 1 = yes) |
| scan\_required | Optional (Fulfil) | Is the product scan required or not (default 1 = yes) |
| purchasable | Optional (Fulfil) | Is the product purchasable or not (default 1 = yes) |
| vendor | Optional (Fulfil) | Vendor/brand of the product |
| hs\_code | Optional (Fulfil) | Hs Code for the product |
| vendor\_lead\_time | Optional (Fulfil) | Vendor lead time of the product |
| country | Optional (Fulfil) | Country or origin of the product |
| weight | Optional | Weight of the product |
| weight\_uom | Optional | Weight uom of the product |
| height | Optional | Height of the product |
| width | Optional | Width of the product |
| length | Optional | Length of the product |
| dimensions\_uom | Optional | Dimension uom of the product |
| shippable | Optional | Is the product shippable or not (default 1 = yes) |
| sticky\_category\_id | Required for sticky | Sticky category of the product |
| is\_digital | Optional for sticky | Is the product digital or not (default 0 = no) |
| shipping\_digital\_url | Optional for sticky | Digital url of the product |
| type | Optional for shopify | Type of the product |
| vendor | Optional for shopify | Vendor of the product |
| tags | Optional for shopify | Tags of the product (value separated by comma) |
| is\_publish | Optional for shopify | Status of the product (value can be either active or draft, default value active) |
| variant\_options | Optional for shopify | Variant options of the product for shopify and fulfil |
| image | Optional for shopify and fulfil | Image of product (Image url or base64 encode image data) |

**Response**

```json
{
    "status": "success",
    "message": "Product created”
}
```

**PUT**  **api/admin/product/{id}**

This API is used to update existing channel

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| title | Required | Title of the product |
| sku | Required | SKU of the product |
| description | Required | Description of the product |
| price | Required | Price of the product |
| cost | Required | Cost of the product |
| quantity | Required for sticky and shopify | Max quantity for sticky, quantity for shopify |
| template | Required for fulfil | Optional if product has variant | Fulfil product template |
| salable | Optional (Fulfil) | Is the product salable or not (default 1 = yes) |
| scan\_required | Optional (Fulfil) | Is the product scan required or not (default 1 = yes) |
| purchasable | Optional (Fulfil) | Is the product purchasable or not (default 1 = yes) |
| vendor | Optional (Fulfil) | Vendor/brand of the product |
| hs\_code | Optional (Fulfil) | Hs Code for the product |
| vendor\_lead\_time | Optional (Fulfil) | Vendor lead time of the product |
| country | Optional (Fulfil) | Country or origin of the product |
| weight | Optional | Weight of the product |
| weight\_uom | Optional | Weight uom of the product |
| height | Optional | Height of the product |
| width | Optional | Width of the product |
| length | Optional | Length of the product |
| dimensions\_uom | Optional | Dimension uom of the product |
| shippable | Optional | Is the product shippable or not (default 1 = yes) |
| sticky\_category\_id | Required for sticky | Sticky category of the product |
| is\_digital | Optional for sticky | Is the product digital or not (default 0 = no) |
| shipping\_digital\_url | Optional for sticky | Digital url of the product |
| type | Optional for shopify | Type of the product |
| vendor | Optional for shopify | Vendor of the product |
| tags | Optional for shopify | Tags of the product (value separated by comma) |
| is\_publish | Optional for shopify | Status of the product (value can be either active or draft, default value active) |
| variant\_options | Optional for shopify | Variant options of the product for shopify and fulfil |
| image | Optional for shopify and fulfil | Image of product (Image url or base64 encode image data) |

**Response**

```json
{
    "status": "success",
    "message": "Product update"
}
```

**PUT**  **api/admin/product/bulk/upload**

This API is used to create bulk product using CSV file

**Request Parameter**

| **Parameter** | **Validation** | **Description** |
| --- | --- | --- |
| csv\_file | Required | CSV file includes list of products |

**GET**  **api/admin/product/template/{channel\_id}**

This API is used to fetch all fulfil template list from fulfill

**GET**  **api/admin/product/fulfil\_category/{channel\_id}**

This API is used to fetch all fulfil category list from fulfill

**GET**  **api/admin/product/fulfil\_product\_supplier/{channel\_id}**

This API is used to fetch all fulfil product supplier list from fulfill

**GET**  **api/admin/product/sticky\_category/{channel\_id}**

This API is used to fetch all sticky category list from sticky

**GET**  **api/country**

This API is used to fetch list of country from fulfil

#### **3rd Party API documentation**

These APIs below are used from 3rd party crm like in Fulfil, Shopify and Sticky. These API are used to perform many different actions throughout the system like create product, update product etc.

##### **Fulfil**

**GET**  **/model/product.template**

This API is used to retrieve all Product Templates from Fulfi.

Location: app\Instances\Fulfil.php Method: getProductTemplate

**GET**  **/model/product.category**

This API is used to retrieve all Product Categories from Fulfi.

Location: app\Instances\Fulfil.php Method: getProductCategory

**POST**  **/model/product.product**

This API is used to create a new product for Fulfil.

Location: app\Instances\Fulfil.php Method: insertProductToFulfil

**PUT**  **/model/product.product/{product\_id}/add\_media**

This API is used to upload media to a product on Fulfil.

Location: app\Instances\Fulfil.php Method: uploadMedia

**PUT**  **/model/product.product/{product\_id}**

This API is used to update information of a product on Fulfil.

Location: app\Instances\Fulfil.php Method: updateProductToFulfil

**PUT**  **/model/country.country/search**

This API is used to fetch a country by country code on Fulfil.

Location: app\Instances\Fulfil.php Method: getCountryIdOnFulfil

**PUT**  **/model/party.party?per\_page=500&amp;is\_supplier=true**

This API is used to fetch a list of product suppliers from Fulfil.

Location: app\Instances\Fulfil.php Method: getProductSupplier

**POST**  **/model/purchase.product\_supplier**

This API is used to create a new product supplier to Fulfil.

Location: app\Instances\Fulfil.php Method: setProductSuppliers

**POST**  **/model/product.template**

This API is used to create a product template to Fulfil.

Location: app\Instances\Fulfil.php Method: createProductTemplate

##### **Sticky**

**GET**  **/v2/categories**

This API is used to retrieve all Product Categories from sticky.

Location: app\Instances\Sticky.php Method: getStickyProductCategories

**POST**  **/v1/product\_create**

This API is used to create a new product for sticky.

Location: app\Instances\Sticky.php Method: insertProductToSticky

**POST**  **/v1/product\_update**

This API is used to update information of a product on Sticky.

Location: app\Instances\Sticky.php Method: updateProductToSticky

##### **Shopify**

**GET**  **/products/{id}.json?fields=handle**

This API is used to retrieve all Product handles from Shopify.

Location: app\Instances\Shopify.php Method: getProductHandle

**POST**  **/products.json**

This API is used to create a new product for Shopify.

Location: app\Instances\Shopify.php Method: insertProductToShopify

**POST**  **/products/{id}.json**

This API is used to update information of a product on Shopify.

Location: app\Instances\Shopify.php Method: updateProductToShopify

#### **Citation information**

In this project we used laravel as back end and vue as frontend technology. In this project we also use fulfil, sticky, shopify crm and their APIs. We are using Laravel sanctum for Single Page Application.

This below vue packages are used in this project

Vuex - [https://vuex.vuejs.org/](https://vuex.vuejs.org/)

Vue-router - [https://router.vuejs.org/installation.html](https://router.vuejs.org/installation.html)

Vue-multiselect - [https://vue-multiselect.js.org/#sub-getting-started](https://vue-multiselect.js.org/#sub-getting-started)

Vue-progressbar - [https://www.npmjs.com/package/vue-progressbar](https://www.npmjs.com/package/vue-progressbar)

Vue-route-middleware - [https://www.npmjs.com/package/vue-route-middleware](https://www.npmjs.com/package/vue-route-middleware)

Vue2-dropzone - [https://www.npmjs.com/package/vue2-dropzone](https://www.npmjs.com/package/vue2-dropzone)

Vuelidate - [https://vuelidate.js.org/#getting-started](https://vuelidate.js.org/#getting-started)

##### References

[https://laravel.com/docs/8.x](https://laravel.com/docs/8.x)

[https://vuejs.org/v2/guide/](https://vuejs.org/v2/guide/)

[https://laravel.com/docs/8.x/sanctum#introduction](https://laravel.com/docs/8.x/sanctum#introduction)

[https://developer-prod.sticky.io/](https://developer-prod.sticky.io/)

[https://developers.fulfil.io/](https://developers.fulfil.io/)

#### **Contributors**

Contributor of this project are CodeClouds team ([team@codeclouds.biz](mailto:team@codeclouds.biz))
