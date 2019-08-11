# Upgrading To 1.1.4 From 1.1.3

> Run make:seeder

```
php artisan make:seeder FieldCheckboxesTableSeeder
```

> database/seeds/FieldCheckboxesTableSeeder.php

```
<?php

use Illuminate\Database\Seeder;
use Illuminate\Support\Facades\DB;

class FieldCheckboxesTableSeeder extends Seeder
{
    /**
     * Run the database seeds.
     *
     * @return void
     */
    public function run()
    {
        //
        $field_checkboxes = array (
            0 =>
                array (
                    'id' => 1,
                    'field_id' => 20,
                    'name' => 'is_main',
                    'title' => '',
                    'value' => '1',
                    'sort' => 100,
                    'checked' => 1,
                ),
        );

        DB::table('field_checkboxes')->insert($field_checkboxes);
    }
}
```

> database/seeds/DatabaseSeeder.php

```
<?php

use Illuminate\Database\Seeder;

class DatabaseSeeder extends Seeder
{
    /**
     * Run the database seeds.
     *
     * @return void
     */

    //        file_put_contents('abc.php', var_export($a,true));

    public function run()
    {
        // $this->call(UsersTableSeeder::class);
        $this->call(AdminAuthoritiesTableSeeder::class);
        $this->call(AdminAuthorityGroupTableSeeder::class);
        $this->call(AdminGroupsTableSeeder::class);
        $this->call(AdminUsersTableSeeder::class);
        $this->call(ConfigsTableSeeder::class);
        $this->call(FieldCheckboxesTableSeeder::class);
        $this->call(FieldRadiosTableSeeder::class);
        $this->call(FieldSelectsTableSeeder::class);
        $this->call(FieldsTableSeeder::class);
        $this->call(MenusTableSeeder::class);
    }
}
```

> Run db:seed

```
php artisan db:seed --class=FieldCheckboxesTableSeeder
```



