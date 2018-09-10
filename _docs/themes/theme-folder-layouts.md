---
title: Layouts Folder
permalink: /docs/theme-folder-layouts/
---

### Overview

Layout Folder is a folder that hold file that explain how to load website template.
Most of layout file only load absolutely must have in every page in web like header, footer, navigation, and importing css and js file.

there is currently 2 required file in this folder namely `default.blade.php` and `blank.blade.php`.

Rule :
* must yield content `@yield('content')`
* layout `<body>` tag must contain `<div id="main"> <span></span></div>`

> Note: span empty element used for drag and drop if this element didn't exist it will impossible to drag and drop.
> 

#### Default Blade <a name="default"></a>

default blade is a blade of a front end always use. this file must have header and footer. used for rendering page.

Example of default.blade.php :

```php
<!DOCTYPE html>
<html lang="en">
  @include('page::theme.porto.partials.head')
  <body>
    <div class="body">
      @include('page::theme.porto.partials.header')
      <div role="main" class="main">
        @yield('header-block')
        @include('page::theme.porto.partials.errors')
        @yield('content')
        <span></span>
      </div>
      @include('page::theme.porto.partials.footer')
    </div>
    @include('page::theme.porto.partials.script')
  </body>
</html>
```

#### Default Blade <a name="blank"></a>

This file is same as default blade except it does not have header or footer. this file is used for [block maker]({{ "/docs/theme-block-maker" | prepend: site.baseurl }}).

Example of blank.blade.php :

```php
<!DOCTYPE html>
<html lang="en">
  @include('page::theme.porto.partials.head')
  <body>
    <div class="body">
      <div role="main" class="main">
        @yield('content')
      </div>
    </div>
    @include('page::theme.porto.partials.script')
  </body>
</html>
```
