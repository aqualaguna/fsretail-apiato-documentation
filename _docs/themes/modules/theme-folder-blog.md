---
title: Modules Blog Folder
permalink: /docs/theme-folder-blog/
---

### Overview <a name="blog"></a>

Blog is a feature from fsretail CMS. for showing there recent activity in site. and also this for publishing news for website.

there is a setting named `blog`. if this setting set to false then blog will not load instead it show 404 not found.

#### Blog All Blade <a name="blogall"></a>

This blade is responsible for showing all of post available from latest post. this route can be applied with [Query Parameter](http://docs.apiato.io/features/query-parameters/). there is addition in query parameter custom query for filtering based on category:

Example :
```
https://test.com/blog-posts?category_ids=1,2,3
```
filename: `blog-all.blade.php`

Injected Variable :
1. $posts = collection of Post
2. $populars = collection of Post that has most view
3. $recents = collection of Post that has recently published
4. $categories = collection of Category of type post

Post Helper pagination:
```php
$posts->count()
$posts->currentPage()
$posts->firstItem()
$posts->hasMorePages()
$posts->lastItem()
$posts->lastPage() (Not available when using simplePaginate)
$posts->nextPageUrl()
$posts->perPage()
$posts->previousPageUrl()
$posts->total() (Not available when using simplePaginate)
$posts->url($page)
```

#### Blog Single Blade <a name="blogsingle"></a>

This blade is responsible for showing 1 post. there is comment and like also in here.
for applying like([User Behavior](#behavior)) comment must be implemented first.
for this blade there is setting named `comment` if it disabled dont render comment.

how to check if comment available
```
(boolean)setting('comment')
```

filename: `blog-single.blade.php`

variable Injected :
1. $post = Single Model of Post
2. $populars = collection of Post that has most view
3. $recents = collection of Post that has recently published
4. $categories = collection of Category of type post

Post Helper:
```php
$post->prev()  // get previous post
$post->next()  // get next post
$post->comments // get this post comment
```

Url for posting a comment:
```
POST /comments/post/{post-id}
```
Param :

|Param|Type|Description|
|---|---|---|
|id | integer unsigned| required, exists in posts table|
|content|text||

----