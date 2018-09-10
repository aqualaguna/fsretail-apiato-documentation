---
title: Modules Transaction Folder
permalink: /docs/theme-folder-transaction/
---

### Transaction Folder

Transaction is a modules for showing transaction happen from currently logged in User.

there is only 1 file for showing sales transaction from logged in user.

filename: `transaction-all.blade.php`

There is only
Injected Variable:
1. $sales = sales transaction for current user.

Feature: 
1. Pay 
  Url:
  ```
  GET /checkout?sales_id={sales-id}
  ```
  Param
  |Param|Type|Description|
  |---|---|---|
  |sales_id| integer unsigned| optional, exists in sales table|
