---
title: "WordPress register menu"
date: 2021-04-04T23:56:54+08:00
draft: false
tags: ["wordpress","snippets"]
---
# Register Menu in WordPress


### 注册菜单
```php
function custom_menus() {
 register_nav_menus(
  array(
   'primary' => 'Primary menu',
   'secondary' => 'Secondary menu',
   'tertiary' => 'Tertiary menu'
  )
 );
}

add_action( 'init', 'custom_menus' );
```

### 在前端使用菜单

```php
wp_nav_menu(
 array(
  'theme_location' => 'primary',
  'container' => false,
 )
);

wp_nav_menu(
 array(
  'menu' => 'primary',
  'container' => false,
 )
);
```
