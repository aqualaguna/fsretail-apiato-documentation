---
title: Dashboard
permalink: /docs/access-dashboard/
---

### Overview

There is 3 kind of dashboard exists in fsretail system.

list of dashboard : 

1. Customer Dashboard

    created from `account.blade.php` in theme folder. this dashboard only accessable if the user has **customer** role. this dashboard is the most simple one it's feature is only for updating user profile and look what activity 

    ![User Dashboard]({{ "/img/user-profile.png" | prepend: site.baseurl }})

    How to Access: 
    ```
    https://yourdomainname.com/customer/profile
    ```

    > Note: image above only example every theme has very different view for each theme. so when accessing this dashboard maybe not exactly the same as picture above.

2. Web Manager Dashboard
  
    this dashboard created for user that has `web_manager` or `admin` role. mainly used for managing site and set setting for site. this dashboard is like CMS (content management system) but more simple than wordpress.

    ![User Dashboard]({{ "/img/web-manager-dashboard.png" | prepend: site.baseurl }})
    How to Access: 
    ```
    https://yourdomainname.com/login
    ```

3. Management Dashboard
  
    this dashboard is created for any user. in case he/she does not have permission `access-dashboard`, that user may not even see the menu it will be auto logout. this is the most complex dashboard in fsretail system. not only for accepting sales, but also purchasing, looking at financial statement etc.

    this dashboard will later be explained in [User Manual Guide]({{ "/docs/manual-intro" | prepend: site.baseurl }}) in detail.

    ![User Dashboard]({{ "/img/console-dashboard.png" | prepend: site.baseurl }})
    
    How to Access: 
    ```
    https://yourdomainname.com/console
    ```
