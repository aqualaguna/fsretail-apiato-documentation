---
title: Theme Builder 
permalink: /docs/theme-builder/
---

### Overview

Theme builder is used for making or editing change for live editor page.

Minimum Requirement for using Theme Builder: 

* html, css, javascript basic
* Front End Developer
* [Understand how component is structured](https://github.com/givanz/VvvebJs/wiki/Components)
* [Basic Blade Template knowledge](https://laravel.com/docs/5.6/blade)


To Access this page you must has:
* Role `admin` or `web_manager`
* Permission `browse_page_block_templates`


Url to access
```
https://yourdomainname.com/theme-builder
```

Bellow is how look like for theme builder

![Theme Builder]({{ "/img/theme-builder.png" | prepend: site.baseurl }})

### Block Maker

Block Maker is a feature to make a block with html template. Live editor itself is taken from [this repository](https://github.com/givanz/VvvebJs). so the documentation for component and behavior is almost the same.

Bellow is how it's look like :

![Block Maker]({{ "/img/block-maker.png" | prepend: site.baseurl }})

Rule :
* every block must have attribute `data-id` with value `$blockId`. this is for updating block. if ever live editor does not update the real site this likely the cause.

    Correct Example :

    ```html
  <div class="card" data-id="$blockId">
    <div class="card-title">
      Hello
    </div>
    <div class="card-body">
      World!!
    </div>
  </div>
    ```


#### Shortcut Must know

1. Showing border of container and block

    Hold Shift key for about 1.5 sec and it will bordered with blue for container and orange for block.
    > note: unbordered block inside container mean its a block but can't update even in live editor is changed. this is due to attribute `data-id` does not exists in root block.

#### Javascript Must Know Rule

1. dont ever use anonymous function when defining an option for a block template.

    Wrong Example of options :
    ```javascript
    image: 'icons/container.svg',
    beforeInit: () => {
      console.log(this.properties[0]) // this is refered to window global object
    }
    ```

    Correct Example of options :
    ```javascript
    image: 'icons/container.svg',
    beforeInit: function() {
      console.log(this.properties[0]) // this is refered to current object
    }
    ```