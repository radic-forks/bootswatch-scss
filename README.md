Bootswatch-Sass
==========
<!-- test commit -->
Bootswatch-sass is a version of the [bootswatch](https://github.com/thomaspark/bootswatch) themes packaged as scss and made for use as a bower component.

Usage
-----

#### Features

- <sub>Namespaced config (like laravel 4: `Config::get('vendor/package::config.item')`)</sub>
- Namespaced publishing (like laravel 4: `config/packages/VENDOR/PACKAGE/config.php`)
- Or use the standard Laravel 5 way:     Compatible with laravel 5 default configs. Adding the package will not invalidate your current setup. 
- Persistent configuration. Save changes to a **`mirroring` `file` or `database`**.
- `Config::getLoader()->set('iam/awesome::my.config.key', 'A changed value')` saves it to a **mirroring** `file` or `db`
- 
- Supports **PHP**, **YAML** and soon also **XML** configuration files.

<sub><sup>combining the two tags</sup></sub>


<div style="font-size: 9px">sfsdfsdf
</div>
Add it to your bower_components directory by executing

    bower install bootswatch-scss

To use a theme in a Sass file, add the following:

    @import "bootstrap-sass-official/assets/stylesheets/bootstrap/variables";
    @import "bootswatch-scss/readable/variables";
    @import "bootstrap-sass-official/assets/stylesheets/bootstrap/bootstrap";
    @import "bootswatch-scss/readable/bootswatch";

It seems you have to shuffle the variables import around to make it load correctly. Some variable files will require that the theme-specific `variables.scss` be imported *before* the Bootstrap equivalent. For example:

    @import "bootswatch-scss/flatly/variables";
    @import "bootstrap-sass-official/assets/stylesheets/bootstrap/variables";
    @import "bootstrap-sass-official/assets/stylesheets/bootstrap/bootstrap";
    @import "bootswatch-scss/flatly/bootswatch";

See `global/build.scss` for a working example.

Copyright/License
-----

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
