# Create Menu

Menu can be displayed in the background. If you want to create a menu, you need to follow some rules in menu create page.

> Slug

If your menu contains submenus, please leave the slug field blank.

Naming rules: **admin/{ModuleName}/slug**

_For example: admin/crm/customer_

> Module

Please choose Admin module.

_Because your module is displayed in the background, you need to choose Admin module instead of the your module name._

* ## Define Menu Slug

After you create the menu, you need to define menu slug constant. The definition here is for writing a routing file.

> config/application/constant.php

```
/*
 * Menu Slug Setting v1.1.5
 */
//CRM
define('MENU_SLUG_CRM_CUSTOMER', 'crm/customer');
```



