---
title: Modules Cart Folder
permalink: /docs/theme-folder-cart/
---

### Overview

This Folder hold cart modules blade.

---
#### Cart All Blade <a name="cartall"></a>

this blade reponsible for rendering Items Cart. for online shop.
there is a setting called `ecommerce` for checking if user available to pay.
filename: `cart-all.blade.php`
Injected variable:
1. $carts = Collection of Cart Model

Helper carts :
```php
$cart->user() // get user model
$cart->item() // get Product model
$cart->unit() // get Unit model
$cart->isValid() // check if cart row if there is item in stock
$cart->getPrice() // get Price
Auth::user()->cartsTotal() // get Total for carts
```

Feature:
1. Checkout = just visit `/checkout`

---

### Pages Folder <a name="pages"></a>

This Folder is responsible to how the page is rendered.
this folder only contains 1 file namely `default.blade.php`
> Note: Do Not change any line in this code just copy paste it.

content of default.blade.php :
```html
@extends('page::theme.personal.layouts.default')
{% raw %}@section('title')
  {{ $page->title }}
@endsection

@section('meta_description')
  {{ $page->meta_description }}
@endsection
{% endraw %}
@section('content')
    {!! $page->body !!}
@endsection

```

### Product Folder <a name="product"></a>

this folder is holding 2 file namely `product-all.blade.php` and `product-single.blade.php`. this for rendering product that being sell.

#### Product All Blade <a name="productall"></a>

This blade is for rendering all product that exists in database.this route can be applied with [Query Parameter](http://docs.apiato.io/features/query-parameters/). 
filename: `product-all.blade.php`

Injected Variable:
1. $items = collection of all item all pagination method is available
2. $toprated = get 5 top rated item.

Item Helper pagination:
```php
$items->count()
$items->currentPage()
$items->firstItem()
$items->hasMorePages()
$items->lastItem()
$items->lastPage() (Not available when using simplePaginate)
$items->nextPageUrl()
$items->perPage()
$items->previousPageUrl()
$items->total() (Not available when using simplePaginate)
$items->url($page)
```
#### Product Single Blade <a name="productsingle"></a>

This blade is responsible for rendering single product.

filename: `product-single.blade.php`

Product Single Url:
```
GET /products/{id}/{unit_id}/{slug}
```
Param: 
|Param|Type|Description|
|---|----|----|
|id|integer unsigned|required, exists in items table|
|unit_id|integer unsingned| required, exists in units table|
|slug|string|optional but prefered due to SEO|

Injected Variable:
1. $item = Selected Item Model
2. $unit = Selected Unit Model

Item Helper
```
$item->pictures // get pictures
$item->pictures[0]->url // get url thumb image
$item->pictures[0]->url_original // get url original image
$item->reviews // get all review
$item->related() // default 4 item get related item by category
$item->getPrice(Unit $unit) // get price by Unit
$item->units // get All Unit
$item->category // get Category
$item->details // get Current Stock
```
Feature :
1. [favorite](#behavior)
2. [upvote](#behavior)
3. [downvote](#behavior)

---
