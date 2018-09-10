---
title: Folder Structure
permalink: /docs/theme-folder-structure/
---

## Overview

This Folder purpose is for storing `.blade.php` file. this is the core of the theme. this folder is placed in `app\Containers\Page\UI\WEB\Views\theme\{theme-name}`.

The `{theme-name}` must be exactly the same as selected theme name (eg. metronome).

below is folder structure :

* {theme name}
  * [layouts]({{ "/docs/theme-folder-layouts" | prepend: site.baseurl }})
    * [default.blade.php]({{ "/docs/theme-folder-layouts#default" | prepend: site.baseurl }})
    * [blank.blade.php]({{ "/docs/theme-folder-layouts#blank" | prepend: site.baseurl }})
    * ...
  * [modules]({{ "/docs/theme-folder-modules" | prepend: site.baseurl }})
    * [auth]({{ "/docs/theme-folder-modules#auth" | prepend: site.baseurl }})
      * [account.blade.php]({{ "/docs/theme-folder-modules#authaccount" | prepend: site.baseurl }})
      * [login.blade.php]({{ "/docs/theme-folder-modules#authlogin" | prepend: site.baseurl }})
      * [register.blade.php]({{ "/docs/theme-folder-modules#authregister" | prepend: site.baseurl }})
    * [blog]({{ "/docs/theme-folder-modules#blog" | prepend: site.baseurl }})
      * [partials]({{ "/docs/theme-folder-partials" | prepend: site.baseurl }})
        * ...
      * [blog-all.blade.php]({{ "/docs/theme-folder-modules#blogall" | prepend: site.baseurl }})
      * [blog-single.blade.php]({{ "/docs/theme-folder-modules#blogsingle" | prepend: site.baseurl }})
    * [cart]({{ "/docs/theme-folder-modules#cart" | prepend: site.baseurl }})
      * [cart-all.blade.php]({{ "/docs/theme-folder-modules#cartall" | prepend: site.baseurl }})
    * [pages]({{ "/docs/theme-folder-modules#pages" | prepend: site.baseurl }})
      * [default.blade.php]({{ "/docs/theme-folder-modules#pages" | prepend: site.baseurl }})
    * [product]({{ "/docs/theme-folder-modules#product" | prepend: site.baseurl }})
      * [partials]({{ "/docs/theme-folder-partials" | prepend: site.baseurl }})
        * ...
      * [product-all.blade.php]({{ "/docs/theme-folder-modules#productall" | prepend: site.baseurl }})
      * [product-single.blade.php]({{ "/docs/theme-folder-modules#productsingle" | prepend: site.baseurl }})
    * [transaction]({{ "/docs/theme-folder-modules#transaction" | prepend: site.baseurl }})
      * [transactional-all.blade.php]({{ "/docs/theme-folder-modules#transaction" | prepend: site.baseurl }})
  * [partials]({{ "/docs/theme-folder-partials" | prepend: site.baseurl }})
    * ...