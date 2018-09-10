---
title: Modules Auth Folder
permalink: /docs/theme-folder-auth/
---

### Overview

this folder holding for Authentication purpose such as: 
* Login
* User Profile
* Register
* Forgot Password
* Reset Password

---
#### Account Blade <a name="authaccount"></a>

this blade reponsible for showing user profile , user activity, and  user favorite. filename: `account.blade.php`.

Variable Injected : 

* Auth Facade

##### Feature Available :

###### 1. Update Profile

> use Action point to `route('patch_user_profile', ['id' => Auth::user()->id])` with method `post`.
> Note: do not forget to addd `csrf_field()` and `method_field('PATCH')`

  |Param                  | type   | description          | Access                                 |
  | --------------------- | -------| -------------------- |----------------------------------------|
  | name                  | string |User Name             | Auth::user()->Name                     |
  | phone_number          | string |Phone Number          | Auth::user()->customer->phone_number   |
  | gender                | string |['male', 'female']    | Auth::user()->gender                   |
  | address               | string |                      | Auth::user()->customer->address        |
  | administrative        | string |                      | Auth::user()->customer->administrative |
  | city                  | string |                      | Auth::user()->customer->city           |
  | password              | string |                      |                                        |
  | password_confirmation | string |same as password      |                                        |

###### 2. User Behavior <a name="behavior"></a>

>this will get What user behavior. behavior defined as:
>  * like
>  * dislike
>  * favorite
>  * follow
>  * upvote
>  * downvote
>  * subscribe.

  ```html
   @foreach (Auth::user()->behavior()->latest()->get() as $behavior)
      {% raw %}<tr>
        <td>
           {{ $behavior->created_at->diffForHumans() }} 
        </td>
        <td>
          {{ $behavior->behavior }}
        </td>
        <td>
          {{ $behavior->obj_type }}
        </td>
      </tr>{% endraw %}
    @endforeach
  ```
###### 3. Favorite Only

  ```html
  @foreach (Auth::user()->favorites()->latest()->get() as $favorite)
      {% raw %}<td>
        <a href="{{$favorite->obj->url()}}">
          {{ $behavior->obj->name }}
        </a>
        <button class="btn btn-link">
          <i class="fas fa-heart"></i>
        </button>
      </td>
      <td>
        {{ $behavior->obj->intro }}
      </td>{% endraw %}
    </tr>
  @endforeach
  
  ```
###### 4. Add or Delete User Behavior
  This will be always return `200 OK` even there is error.

  Add Behavior
  ```shell
  GET /user/{behavior}/{classname}/{id}
  ```

  Delete Behavior
  ```shell
  DELETE /user/{behavior}/{classname}/{id}
  ```

|Param| Description|
|------|-----------|
|behavior|enum:upvote, downvote, like, dislike, favorite, follow, subsribe|
| classname| enum:item, comment, review|
|id   |id referenced from classname|

---

#### Login Blade <a name="authlogin"></a>

this blade reponsible for showing user login page. filename: `login.blade.php`.

##### Feature Available :

###### 1. Login

Url:
```
POST /customer/login
```

Param: 

|Param|Type | Description|
|------|-----------|------------------|
|email|string|required, type:email|
|password|string|required|
|rememberme|boolean|optional, default: false|

###### 2. Login Using Social Authentication

Url:

```
GET /auth/{provider}
```

Param:

|Param|Type| Description|
|-----|-----|--------|
|provider|Enum| in:facebook,google,twitter|


###### 3. Logout

Url:
```
GET /logout
```

###### 4. Forgot Password

Url:
```
// not yet implemented
```
###### 5. Reset Password

Url:
```
// not yet implemented
```

---
#### Register Blade <a name="authlogin"></a>

This blade responsible for registering new User. filename: `register.blade.php`.

Feature Register:

Url:
```
POST /customer/register
```

Param:

|Param| Type| Description|
|-----|----|-----|
|name|string|required|
|email|string|required|
|password|string|required,confirmed|
|password_confirmation|string||

---