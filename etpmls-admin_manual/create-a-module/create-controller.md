# Create Controller

## 1.First, you need create a controller

* If your controller is only used in the backstage, you need to follow the format below.

```
php artisan make:controller Crm/Admin/CustomerController
```

## 2.Inheritance controller

If your controller does not inherit the controller that are common to the module, you will need to create the controller manually.

Create Base Controller

```
php artisan make:controller Crm/Admin/Controller
```

Edit Base Controller

> app/Http/Controllers/Crm/Admin/Controller.php

```
<?php

namespace App\Http\Controllers\Crm\Admin;

use Illuminate\Http\Request;
use App\Http\Controllers\Admin\Controller as BaseController;

class Controller extends BaseController
{
    //
}
```

Inheritance base controller

> app/Http/Controllers/Crm/Admin/CustomerController.php

```
<?php

namespace App\Http\Controllers\Crm\Admin;

use Illuminate\Http\Request;
use App\Http\Controllers\Crm\Admin\Controller;

class CustomerController extends Controller
{
    //
}
```

### 



