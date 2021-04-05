---
title: "Wordpress child theme"
date: 2021-04-04T23:56:54+08:00
draft: false
tags: ["wordpress","snippets"]
---
# Child Theme 

### functions.php

```php
<?php
function add_assets(){
  wp_enqueue_style("mystyle",get_stylesheet_uri());
  wp_enqueue_style("bootstrap_css", get_stylesheet_directory_uri()."/bootstrap.min.css");
  wp_enqueue_script("bootstrap_js", get_stylesheet_directory_uri()."/bootstrap.min.js");
}

add_action("wp_enqueue_scripts","add_assets");
>
```

### style.css

```css
/*
Theme Name: CyberBuf
Template: blankslate
/*
*{margin:0;padding:0;box-sizing:border-box}
```