## Ark Ideas - Front End Coding Skills Challenge

The Ark Ideas front end coding challenge is designed to allow us to evaluate your front-end coding skill level, as well as your overall approach to the project.
 
A successful completion of the challenge will incorporate all of the functionality outlined below.
  
For additional clarification a [video demo](Register.mp4) of a working version of the solved challenge is included. 



#### Products
Products are defined in the *products.json* file. Each product contains:

* **id** - A unique identifier for the product
* **name** - The name of the product
* **sku** - The sku / upc of the product
* **price** - The price of the product
* **product_type** - The type of product
* **esns** - The esns of the product (only on certain products), will be an array of strings

```
{
    "id": "70",
    "name": "Apple iPhone 4/4s Intact Case, Blue & Gray",
    "sku": "819907010391",
    "price": "30.00",
    "product_type": "Cases"
}, 
{
    "id": "370",
    "name": "LG G2 Titanium",
    "sku": "LGLS980ABB",
    "price": "120.00",
    "product_type": "Boost Phones",
    "esns": [
        "676213872138318181",
        "676213872138318182",
        "676213872138318183",
        "676213872138318184"
    ]
},   
```  

#### Search / Filtering

**Searching**

The search box has 3 search options:
1. Search by Name - this should search on the product name (name)
1. Search By Sku - this is should on the product SKU (sku)
1. Search by ESN - this should search on the associated esns of the product (esns)

**Filtering**

The product filter box, filters out products by 'product_type'

#### Adding products to the sale

Products can be added to the sale by clicking them in the left hand side products list. Once added the Sub Total and Total should auto-update with the price of the newly added product. 

To the left of the product is the quantity box. This should default to 1. This can be changed by the user to indicate multiple qty of the same product on the sale. When changed the Sub Total and total should auto-update with the new total price of the product. 

To the right of the product is the product price. This should default to the value of the product provided. This can be changed by the user to an updated price of a value grater than or equal to 0. When changed the Sub Total and total should auto-update with the new total price of the product. 


#### Discounts

Discounts are provided in the *discounts.json* file. Each discount contains:

* **id** - A unique identifier for the discount
* **name** - The name of the discount
* **type** - The apply type of the discount (*percentage* or *flat*)
* **value** - The value of the discount

```
{
    "id": 1,
    "name": "5% Discount",
    "type": "percentage",
    "value": 5
}
```

When a discount is chosen, the Discount and Total of the sale should auto-update with the corresponding computed value of the selected discount. 


#### Taxes

Taxes are provided in the *taxes.json* file. Each tax contains:

* **id** - A unique identifier for the discount
* **name** - The name of the discount
* **rate** - The rate of tax

```
{
    "id": 1,
    "name": "5% Sales Tax",
    "rate": 5
},
```

When a tax rate is chosen, the Taxes and Total of the sale should auto-update with the corresponding computed value of the selected tax. **Sales tax is computed on the subtotal and not the discounted amount.**
