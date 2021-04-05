---
title: "Wordpress custom api"
date: 2021-04-04T23:56:54+08:00
draft: false
tags: ["wordpress","snippets"]
---
# Custom Api Endpoint

### 自定义 rest api

在wp-content =>themes => 使用中的主题 =>functions.php 中 加入相关的代码

```php
function hello( $data ) {
  return array(array("hello"=>"asfd","world"=>"dsfadsf"));
}

add_action( 'rest_api_init', function () {
  register_rest_route( 'iaa', '/news', array(
    'methods' => 'GET',
    'callback' => 'hello',
  ) );
} );
```

就可以访问 /wp-json/iaa/news