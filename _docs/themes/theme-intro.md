---
title: Introduction 
permalink: /docs/theme-intro/
---

### Overview (Developer use only)

Theme is a style how website page is presented. Unlike other site builder FSretail Theme simplified how web manager operate website. Every structure of Container, Block and Page is stored in database (not as a file). Changing theme of finished website may break the website. because each block of defined in old theme is different for new theme. It is recommended to clear all block to start all over when Changing theme occur.

the Rule of choosing a theme name:
1. One word (eg. metronome)
2. Alpha lowercase only (a-z)
3. Short (optional but prefered)

NameSpace for `@include` syntax:

```php
  @include('page::theme.{theme-name}.{whatever-file-you-need}')
```

This is the topic we will explain in next page :


| Topic           | Description                               |
|-----------------|-------------------------------------------|
|[Intro to Block Maker]({{ "/docs/theme-folder-asset" | prepend: site.baseurl }})| What is block maker and how to use it? |
|[Asset Folder]({{ "/docs/theme-folder-asset" | prepend: site.baseurl }})| Where do I Save asset such as image, css and js file ?|
| [Folder Structure]({{ "/docs/theme-folder-structure" | prepend: site.baseurl }})| Explain How Theme is stored and what extensions used|
|[Folder Layouts]({{ "/docs/theme-folder-layouts" | prepend: site.baseurl }})|What is Layout? and how it is displayed?|
|[Folder Modules]({{ "/docs/theme-folder-modules" | prepend: site.baseurl }})|explanation what modules folder used for|
|[Folder Partials]({{ "/docs/theme-folder-partials" | prepend: site.baseurl }})|explanation what every partials folder used for|
