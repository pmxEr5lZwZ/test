# Write Route

```

/*
 * v1.1.5
 */
//CRM - Customer
Route::get(MODULE_ADMIN_NAME.'/'.MODULE_CRM_NAME.'/'.MENU_SLUG_CRM_CUSTOMER, 'Admin\Crm\CustomerController@index')->middleware('can:view,App\AdminGroup');
Route::get(MODULE_ADMIN_NAME.'/'.MODULE_CRM_NAME.'/'.MENU_SLUG_CRM_CUSTOMER.'/create', 'Admin\Crm\CustomerController@create')->middleware('can:create,App\AdminGroup');
Route::post(MODULE_ADMIN_NAME.'/'.MODULE_CRM_NAME.'/'.MENU_SLUG_CRM_CUSTOMER, 'Admin\Crm\CustomerController@store')->middleware('can:create,App\AdminGroup');
Route::get(MODULE_ADMIN_NAME.'/'.MODULE_CRM_NAME.'/'.MENU_SLUG_CRM_CUSTOMER.'/{customer}/edit', 'Admin\Crm\CustomerController@edit')->middleware('can:update,App\AdminGroup');
Route::put(MODULE_ADMIN_NAME.'/'.MODULE_CRM_NAME.'/'.MENU_SLUG_CRM_CUSTOMER.'/{customer}', 'Admin\Crm\CustomerController@update')->middleware('can:update,App\AdminGroup');
Route::delete(MODULE_ADMIN_NAME.'/'.MODULE_CRM_NAME.'/'.MENU_SLUG_CRM_CUSTOMER.'/{customer}', 'Admin\Crm\CustomerController@destroy')->middleware('can:delete,App\AdminGroup');
```



