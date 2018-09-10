---
title: Journal Template
permalink: /docs/accounting-template/
---

### Overview

Based on accounting principle every journal entry must be balanced. so debit must equal to credit. doing this will make sure the system statisfy accounting equation :

> Asset = Liability + Equity

Journal Template is an concept to make journal entry error less, and to avoid imbalance.

Example of Journal Template: 

```php
name: "Initial Capital (Cash)",
detail : [
   {
     class: "Equity",
     type: "Equity",
     name: "Owner A Funds Introduced",
     description: "Funds contributed by the owner",
     fill: "Credit"
   },
   {
     class: "Assets",
     type: "Current Asset",
     name: "Cash",
     description: "Checking account balance, currency, coins, checks received from customer but not yet deposited.",
     fill: "Debit"
   }
]

```
the example above showing there a template named `Initial Capital(Cash)`. if this template is called to create journal. it will credit the `Owner A Funds Introduced` account and debit the `Cash` account.

the concept is simple it's just add overhead when creating a journal. while it seems it inefficient in long run it will be useful for filtering and auditing.

> **Warning** : Creating a wrong template mean making wrong journal entry. Make sure journal template is correct.

> **Warning** : Updating template often will make journal entry hard to read. it is not recommended to update the template unless the detail is incorrect.

> **Note** : above is only illustration not the real structure

### Creating New Template Journal

