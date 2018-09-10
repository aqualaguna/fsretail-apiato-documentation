---
title: Role and Permissions
permalink: /docs/role-permissions/
---

### Overview

FSretail use role and permission system. this is to prevent unauthorized used on system. for more documentation refer to [this repository](https://github.com/spatie/laravel-permission).

### Permissions

Permission is a consent given by system to user/role to perform some action in system. Fsretail system adopt Bread system from [laravel voyager](https://laravelvoyager.com/) permission system but **not entirely**. the `BREAD` system integrated in fsretail is implemented in any accessable api model. `BREAD` stands for browse, read, edit, add, and delete. example permission will be explained in [Role section](#role).

> Note: Permission is fixed record. it can't be added, updated, or deleted. permission only created in seeder(inside the code).

### Roles <a name="role"></a>

Role are like a group permission given to user.To Access this module you need to login to management console. and go to this page bellow :

![user role]({{ "/img/manual/user-role.png" | prepend: site.baseurl }})

Permission needed: 

1. manage-roles
   * add , edit, delete a role
   * assign permission to role
   * assign a role to user

2. manage-admin-access
   * create admin user

There is 7 default role exist namely: 

1. **Administrator**

    Has All access and can do basically anything in system. **no root access**.

2. **Customer**

    customer is a user that registered via website interface. customer can buy, view transaction and update profile. this role is very limited in any access.

    Permission:

    |Permission name     | Description        |
    |--------------------|--------------------|
    |Delete Comments     |Delete Comments row.|
    |Update Comments     |Update Comments row.|
    |Add Comments        |Insert Comments row.|
    |Delete Reviews      |Delete Reviews row. |
    |Update Reviews      |Update Reviews row. |
    |Add Reviews         |Insert Reviews row. |


3. **Sales**

    sales is a user that manage sales. for example create sales, approve sales, create sales order etc. sales also can create item and many more for detail look table below.

    Permission: 

    | Permission name      | Description                                            |
    |----------------------|--------------------------------------------------------|
    | Access dashboard     | Access the admins dashboard.                           |
    | Browse Users         | Get all Users row.                                     |
    | Browse Attachments   | Get all Attachments row.                               |
    | Read Attachments     | Read 1 (One) Attachments row.                          |
    | Delete Attachments   | Delete Attachments row.                                |
    | Update Attachments   | Update Attachments row.                                |
    | Add Attachments      | Insert Attachments row.                                |
    | Browse Categories    | Get all Categories row.                                |
    | Read Categories      | Read 1 (One) Categories row.                           |
    | Delete Categories    | Delete Categories row.                                 |
    | Update Categories    | Update Categories row.                                 |
    | Add Categories       | Insert Categories row.                                 |
    | Browse Customers     | Get all Customers row.                                 |
    | Read Customers       | Read 1 (One) Customers row.                            |
    | Delete Customers     | Delete Customers row.                                  |
    | Update Customers     | Update Customers row.                                  |
    | Add Customers        | Insert Customers row.                                  |
    | Browse Items         | Get all Items row.                                     |
    | Read Items           | Read 1 (One) Items row.                                |
    | Delete Items         | Delete Items row.                                      |
    | Update Items         | Update Items row.                                      |
    | Add Items            | Insert Items row.                                      |
    | Browse Item Pictures | Get all Item Pictures row.                             |
    | Read Item Pictures   | Read 1 (One) Item Pictures row.                        |
    | Delete Item Pictures | Delete Item Pictures row.                              |
    | Add Item Pictures    | Insert Item Pictures row.                              |
    | Browse Item Details  | Get all Item Details row.                              |
    | Read Item Details    | Read 1 (One) Item Details row.                         |
    | Browse People        | Get all People row.                                    |
    | Read People          | Read 1 (One) People row.                               |
    | Delete People        | Delete People row.                                     |
    | Update People        | Update People row.                                     |
    | Add People           | Insert People row.                                     |
    | Browse Purchases     | Get all Purchases row.                                 |
    | Browse Sales         | Get all Sales row.                                     |
    | Read Sales           | Read 1 (One) Sales row.                                |
    | Delete Sales         | Delete Sales row.                                      |
    | Update Sales         | Update Sales row.                                      |
    | Add Sales            | Insert Sales row.                                      |
    | Approve Sales        | Make Sales Approvement. making sales can't be deleted. |
    | Sent Sales           | Sent Sales Order to customer.                          |
    | Sales Payment        | pay sales invoice received.                            |
    | Browse Suppliers     | Get all Suppliers row.                                 |
    | Browse Taxes         | Get all Taxes row.                                     |
    | Read Taxes           | Read 1 (One) Taxes row.                                |
    | Delete Taxes         | Delete Taxes row.                                      |
    | Update Taxes         | Update Taxes row.                                      |
    | Add Taxes            | Insert Taxes row.                                      |
    | Browse Units         | Get all Units row.                                     |
    | Read Units           | Read 1 (One) Units row.                                |
    | Delete Units         | Delete Units row.                                      |
    | Update Units         | Update Units row.                                      |
    | Add Units            | Insert Units row.                                      |
    | Browse Unit Details  | Get all Unit Details row.                              |
    | Read Unit Details    | Read 1 (One) Unit Details row.                         |
    | Delete Unit Details  | Delete Unit Details row.                               |
    | Update Unit Details  | Update Unit Details row.                               |
    | Add Unit Details     | Insert Unit Details row.                               |
    | Browse Warehouses    | Get all Warehouses row.                                |

4. **Purchaser**

    this role is almost the same as sales the difference this role manage purchase not sales.

    | Permission name      | Description                                                                            |
    |----------------------|----------------------------------------------------------------------------------------|
    | Access Dashboard     | Access the admins dashboard.                                                           |
    | Browse Attachments   | Get all Attachments row.                                                               |
    | Read Attachments     | Read 1 (One) Attachments row.                                                          |
    | Delete Attachments   | Delete Attachments row.                                                                |
    | Update Attachments   | Update Attachments row.                                                                |
    | Add Attachments      | Insert Attachments row.                                                                |
    | Browse Categories    | Get all Categories row.                                                                |
    | Read Categories      | Read 1 (One) Categories row.                                                           |
    | Delete Categories    | Delete Categories row.                                                                 |
    | Update Categories    | Update Categories row.                                                                 |
    | Add Categories       | Insert Categories row.                                                                 |
    | Browse Customers     | Get all Customers row.                                                                 |
    | Read Customers       | Read 1 (One) Customers row.                                                            |
    | Browse Items         | Get all Items row.                                                                     |
    | Read Items           | Read 1 (One) Items row.                                                                |
    | Delete Items         | Delete Items row.                                                                      |
    | Update Items         | Update Items row.                                                                      |
    | Add Items            | Insert Items row.                                                                      |
    | Browse Item Pictures | Get all Item Pictures row.                                                             |
    | Read Item Pictures   | Read 1 (One) Item Pictures row.                                                        |
    | Delete Item Pictures | Delete Item Pictures row.                                                              |
    | Add Item Pictures    | Insert Item Pictures row.                                                              |
    | Browse Item Details  | Get all Item Details row.                                                              |
    | Read Item Details    | Read 1 (One) Item Details row.                                                         |
    | Browse People        | Get all People row.                                                                    |
    | Read People          | Read 1 (One) People row.                                                               |
    | Delete People        | Delete People row.                                                                     |
    | Update People        | Update People row.                                                                     |
    | Add People           | Insert People row.                                                                     |
    | Browse Purchases     | Get all Purchases row.                                                                 |
    | Read Purchases       | Read 1 (One) Purchases row.                                                            |
    | Delete Purchases     | Delete Purchases row.                                                                  |
    | Update Purchases     | Update Purchases row.                                                                  |
    | Add Purchases        | Insert Purchases row.                                                                  |
    | Approve Purchase     | Approve Purchase. approved purchase cannot be deleted. purchase marked with warehouse. |
    | Arrived Purchase     | Mark Purchase as Arrived. making journal and inventory update.                         |
    | Purchase Payment     | Make Payment for Purchase invoice.                                                     |
    | Browse Sales         | Get all Sales row.                                                                     |
    | Read Sales           | Read 1 (One) Sales row.                                                                |
    | Browse Suppliers     | Get all Suppliers row.                                                                 |
    | Read Suppliers       | Read 1 (One) Suppliers row.                                                            |
    | Delete Suppliers     | Delete Suppliers row.                                                                  |
    | Update Suppliers     | Update Suppliers row.                                                                  |
    | Add Suppliers        | Insert Suppliers row.                                                                  |
    | Browse Taxes         | Get all Taxes row.                                                                     |
    | Read Taxes           | Read 1 (One) Taxes row.                                                                |
    | Browse Units         | Get all Units row.                                                                     |
    | Read Units           | Read 1 (One) Units row.                                                                |
    | Delete Units         | Delete Units row.                                                                      |
    | Update Units         | Update Units row.                                                                      |
    | Add Units            | Insert Units row.                                                                      |
    | Browse Unit Details  | Get all Unit Details row.                                                              |
    | Read Unit Details    | Read 1 (One) Unit Details row.                                                         |
    | Delete Unit Details  | Delete Unit Details row.                                                               |
    | Update Unit Details  | Update Unit Details row.                                                               |
    | Add Unit Details     | Insert Unit Details row.                                                               |
    | Browse Warehouses    | Get all Warehouses row.                                                                |
    | Read Warehouses      | Read 1 (One) Warehouses row.                                                           |

5. **Web Manager**

    the purpose of this role is to manage website. for example managing post, editing page, live editor, theme builder etc. for more detail look at the table bellow show complete list of web manager permission.

    | Permission name             | Description                            |
    |-----------------------------|----------------------------------------|
    | Manage Menubar              | Edit Category Menu                     |
    | Manage Category Post        | Edit Category Post                     |
    | Browse Comments             | Get all Comments row.                  |
    | Read Comments               | Read 1 (One) Comments row.             |
    | Delete Comments             | Delete Comments row.                   |
    | Update Comments             | Update Comments row.                   |
    | Add Comments                | Insert Comments row.                   |
    | Browse Pages                | Get all Pages row.                     |
    | Read Pages                  | Read 1 (One) Pages row.                |
    | Delete Pages                | Delete Pages row.                      |
    | Update Pages                | Update Pages row.                      |
    | Add Pages                   | Insert Pages row.                      |
    | Browse Page Blocks          | Get all Page Blocks row.               |
    | Read Page Blocks            | Read 1 (One) Page Blocks row.          |
    | Delete Page Blocks          | Delete Page Blocks row.                |
    | Update Page Blocks          | Update Page Blocks row.                |
    | Add Page Blocks             | Insert Page Blocks row.                |
    | Browse Page Block Templates | Get all Page Block Templates row.      |
    | Read Page Block Templates   | Read 1 (One) Page Block Templates row. |
    | Delete Page Block Templates | Delete Page Block Templates row.       |
    | Update Page Block Templates | Update Page Block Templates row.       |
    | Add Page Block Templates    | Insert Page Block Templates row.       |
    | Browse Posts                | Get all Posts row.                     |
    | Read Posts                  | Read 1 (One) Posts row.                |
    | Delete Posts                | Delete Posts row.                      |
    | Update Posts                | Update Posts row.                      |
    | Add Posts                   | Insert Posts row.                      |
    | Browse Reviews              | Get all Reviews row.                   |
    | Read Reviews                | Read 1 (One) Reviews row.              |
    | Delete Reviews              | Delete Reviews row.                    |
    | Update Reviews              | Update Reviews row.                    |
    | Add Reviews                 | Insert Reviews row.                    |

6. **Accountant**
  
    Accountant is a role that manage journal and balancing incorrect record. Bellow is complete list of accountant Permission. Accountant can also view financial report at the current moment.

    | Permission name          | Description                                                                                        |
    |--------------------------|----------------------------------------------------------------------------------------------------|
    | Access Dashboard         | Access the admins dashboard.                                                                       |
    | Browse Users             | Get all Users row.                                                                                 |
    | Browse Categories        | Get all Categories row.                                                                            |
    | Read Categories          | Read 1 (One) Categories row.                                                                       |
    | Browse Chart Of Accounts | Get all Chart Of Accounts row.                                                                     |
    | Read Chart Of Accounts   | Read 1 (One) Chart Of Accounts row.                                                                |
    | Delete Chart Of Accounts | Delete Chart Of Accounts row.                                                                      |
    | Update Chart Of Accounts | Update Chart Of Accounts row.                                                                      |
    | Add Chart Of Accounts    | Insert Chart Of Accounts row.                                                                      |
    | Browse Customers         | Get all Customers row.                                                                             |
    | Read Customers           | Read 1 (One) Customers row.                                                                        |
    | Browse Items             | Get all Items row.                                                                                 |
    | Read Items               | Read 1 (One) Items row.                                                                            |
    | Browse Item Pictures     | Get all Item Pictures row.                                                                         |
    | Read Item Pictures       | Read 1 (One) Item Pictures row.                                                                    |
    | Browse Item Details      | Get all Item Details row.                                                                          |
    | Read Item Details        | Read 1 (One) Item Details row.                                                                     |
    | Trial Balance            | Take a look at trial balance.                                                                      |
    | Read Financial Statement | Read/Download financial statement such as Balance Sheet, Income Statement, and Cash flow statement |
    | Add Custom Journal       | add Custom Journal. specified for accounting purpose.                                              |
    | Browse People            | Get all People row.                                                                                |
    | Read People              | Read 1 (One) People row.                                                                           |
    | Browse Purchases         | Get all Purchases row.                                                                             |
    | Read Purchases           | Read 1 (One) Purchases row.                                                                        |
    | Browse Sales             | Get all Sales row.                                                                                 |
    | Read Sales               | Read 1 (One) Sales row.                                                                            |
    | Browse Suppliers         | Get all Suppliers row.                                                                             |
    | Read Suppliers           | Read 1 (One) Suppliers row.                                                                        |
    | Browse Taxes             | Get all Taxes row.                                                                                 |
    | Read Taxes               | Read 1 (One) Taxes row.                                                                            |
    | Browse Templates         | Get all Templates row.                                                                             |
    | Read Templates           | Read 1 (One) Templates row.                                                                        |
    | Delete Templates         | Delete Templates row.                                                                              |
    | Update Templates         | Update Templates row.                                                                              |
    | Add Templates            | Insert Templates row.                                                                              |
    | Browse Units             | Get all Units row.                                                                                 |
    | Read Units               | Read 1 (One) Units row.                                                                            |
    | Browse Unit Details      | Get all Unit Details row.                                                                          |
    | Read Unit Details        | Read 1 (One) Unit Details row.                                                                     |
    | Browse Warehouses        | Get all Warehouses row.                                                                            |
    | Read Warehouses          | Read 1 (One) Warehouses row.                                                                       | 

7. **Manager**

    Manager is a role like Administrator except it's lacking critical and technical type permission. manager is like purchaser and sales combined added with permission to manage other user except adminstrator. bellow is complete list of manager role:

    | Permission name          | Description                                                                                        |
    |--------------------------|----------------------------------------------------------------------------------------------------|
    | Manage Roles             | Create, Update, Delete, Get All, Attach/detach permissions to Roles and Get All Permissions.       |
    | Assign Role              | Assign users to Roles.                                                                             |
    | Access Dashboard         | Access the admins dashboard.                                                                       |
    | Browse Users             | Get all Users row.                                                                                 |
    | Read Users               | Read 1 (One) Users row.                                                                            |
    | Delete Users             | Delete Users row.                                                                                  |
    | Update Users             | Update Users row.                                                                                  |
    | Add Users                | Insert Users row.                                                                                  |
    | Add Badge                | Add Badge or Missions.                                                                             |
    | Delete Badge             | delete Badge or Missions.                                                                          |
    | Grant Badge              | grant Badge or Missions.                                                                           |
    | Browse Attachments       | Get all Attachments row.                                                                           |
    | Read Attachments         | Read 1 (One) Attachments row.                                                                      |
    | Delete Attachments       | Delete Attachments row.                                                                            |
    | Update Attachments       | Update Attachments row.                                                                            |
    | Add Attachments          | Insert Attachments row.                                                                            |
    | Browse Categories        | Get all Categories row.                                                                            |
    | Read Categories          | Read 1 (One) Categories row.                                                                       |
    | Delete Categories        | Delete Categories row.                                                                             |
    | Update Categories        | Update Categories row.                                                                             |
    | Add Categories           | Insert Categories row.                                                                             |
    | Browse Chart Of Accounts | Get all Chart Of Accounts row.                                                                     |
    | Read Chart Of Accounts   | Read 1 (One) Chart Of Accounts row.                                                                |
    | Browse Credentials       | Get all Credentials row.                                                                           |
    | Read Credentials         | Read 1 (One) Credentials row.                                                                      |
    | Delete Credentials       | Delete Credentials row.                                                                            |
    | Update Credentials       | Update Credentials row.                                                                            |
    | Add Credentials          | Insert Credentials row.                                                                            |
    | Browse Customers         | Get all Customers row.                                                                             |
    | Read Customers           | Read 1 (One) Customers row.                                                                        |
    | Delete Customers         | Delete Customers row.                                                                              |
    | Update Customers         | Update Customers row.                                                                              |
    | Add Customers            | Insert Customers row.                                                                              |
    | Browse Items             | Get all Items row.                                                                                 |
    | Read Items               | Read 1 (One) Items row.                                                                            |
    | Delete Items             | Delete Items row.                                                                                  |
    | Update Items             | Update Items row.                                                                                  |
    | Add Items                | Insert Items row.                                                                                  |
    | Browse Item Pictures     | Get all Item Pictures row.                                                                         |
    | Read Item Pictures       | Read 1 (One) Item Pictures row.                                                                    |
    | Delete Item Pictures     | Delete Item Pictures row.                                                                          |
    | Update Item Pictures     | Update Item Pictures row.                                                                          |
    | Add Item Pictures        | Insert Item Pictures row.                                                                          |
    | Browse Item Details      | Get all Item Details row.                                                                          |
    | Read Item Details        | Read 1 (One) Item Details row.                                                                     |
    | Trial Balance            | Take a look at trial balance.                                                                      |
    | Read Financial Statement | Read/Download financial statement such as Balance Sheet, Income Statement, and Cash flow statement |
    | Browse People            | Get all People row.                                                                                |
    | Read People              | Read 1 (One) People row.                                                                           |
    | Delete People            | Delete People row.                                                                                 |
    | Update People            | Update People row.                                                                                 |
    | Add People               | Insert People row.                                                                                 |
    | Browse Purchases         | Get all Purchases row.                                                                             |
    | Read Purchases           | Read 1 (One) Purchases row.                                                                        |
    | Delete Purchases         | Delete Purchases row.                                                                              |
    | Update Purchases         | Update Purchases row.                                                                              |
    | Add Purchases            | Insert Purchases row.                                                                              |
    | Approve Purchase         | Approve Purchase. approved purchase cannot be deleted. purchase marked with warehouse.             |
    | Arrived Purchase         | Mark Purchase as Arrived. making journal and inventory update.                                     |
    | Purchase Payment         | Make Payment for Purchase invoice.                                                                 |
    | Browse Sales             | Get all Sales row.                                                                                 |
    | Read Sales               | Read 1 (One) Sales row.                                                                            |
    | Delete Sales             | Delete Sales row.                                                                                  |
    | Update Sales             | Update Sales row.                                                                                  |
    | Add Sales                | Insert Sales row.                                                                                  |
    | Approve Sales            | Make Sales Approvement. making sales can't be deleted.                                             |
    | Sent Sales               | Sent Sales Order to customer.                                                                      |
    | Sales Payment            | pay sales invoice received.                                                                        |
    | Browse Suppliers         | Get all Suppliers row.                                                                             |
    | Read Suppliers           | Read 1 (One) Suppliers row.                                                                        |
    | Delete Suppliers         | Delete Suppliers row.                                                                              |
    | Update Suppliers         | Update Suppliers row.                                                                              |
    | Add Suppliers            | Insert Suppliers row.                                                                              |
    | Browse Taxes             | Get all Taxes row.                                                                                 |
    | Read Taxes               | Read 1 (One) Taxes row.                                                                            |
    | Delete Taxes             | Delete Taxes row.                                                                                  |
    | Update Taxes             | Update Taxes row.                                                                                  |
    | Add Taxes                | Insert Taxes row.                                                                                  |
    | Browse Units             | Get all Units row.                                                                                 |
    | Read Units               | Read 1 (One) Units row.                                                                            |
    | Delete Units             | Delete Units row.                                                                                  |
    | Update Units             | Update Units row.                                                                                  |
    | Add Units                | Insert Units row.                                                                                  |
    | Browse Unit Details      | Get all Unit Details row.                                                                          |
    | Read Unit Details        | Read 1 (One) Unit Details row.                                                                     |
    | Delete Unit Details      | Delete Unit Details row.                                                                           |
    | Update Unit Details      | Update Unit Details row.                                                                           |
    | Add Unit Details         | Insert Unit Details row.                                                                           |
    | Browse Warehouses        | Get all Warehouses row.                                                                            |
    | Read Warehouses          | Read 1 (One) Warehouses row.                                                                       |
    | Update Warehouses        | Update Warehouses row.                                                                             |

> Note: You can create custom role but be cautious for giving permission to role.