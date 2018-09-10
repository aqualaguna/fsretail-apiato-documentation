---
title: Modules Folder
permalink: /docs/theme-folder-modules/
---

### Overview

Folder Modules is where blade for Auth, Cart, Blog, Product, and Transaction show to user.
this kind of blade is kind of static and required (must not missing). if missing it would make critical error. and some of the function not properly used.

there is 6 folder namely:
* [auth]({{ "/docs/theme-folder-auth" | prepend: site.baseurl }})
* [blog]({{ "/docs/theme-folder-blog" | prepend: site.baseurl }})
* [cart]({{ "/docs/theme-folder-cart" | prepend: site.baseurl }})
* [product]({{ "/docs/theme-folder-product" | prepend: site.baseurl }})
* [transaction]({{ "/docs/theme-folder-transaction" | prepend: site.baseurl }})

---
## **Helper Function**

Helper function is used for easing access to certain resources in server.
list of helper : 
1. setting

setting is an helper to get setting variable in this environment. if not found return `null`. this helper always return string.

```php
  {% raw %}{{ setting('{enter key here}')}}
  {{ setting('theme')}}{% endraw %}
```

2. menus

menus is a helper that getting menus on header of the page. for Example Home, Blog, Product, and About us. this helper always return Collection. this usually paired with `[toTree()](#toTree)` function created custom (not available in general laravel application).

``` php
@foreach(menus()->toTree() as $menu)
  // do something
@endforeach
```

3. imageUrl 

this helper only extension of `url('/storage/' + $path)`. Only accept String.

4. humanInteger

this helper convert `12324` to `12.3 K` just make integer readable. only accept Number.

5. avatar

this helper accept string parameter which contains email.
if database has avatar return it if not return to gravatar search with email.
```html
  {% raw %}{{ avatar('test@gmail.com') }}{% endraw %}
```

## Collection Custom Function 

list of currently created function to ease use of blade.

### toTree <a name="toTree"></a>

this function help convert collection to tree structure.
this function accept 3 parameter : `root = null`, `idKey= 'id'`, and `parentKey = 'parent_id'`. this function can be used without parameter. make sure collection has 'id' which identified itself and 'parent_id' key to indentify parent.
``` php
@foreach(menus()->toTree() as $menu)
  // do something
@endforeach
```
