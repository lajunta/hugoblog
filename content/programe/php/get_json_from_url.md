---
title: "Get Json From Url"
date: 2021-04-09T11:55:26+08:00
draft: false
---

```php
<?php
// set location
$address = "Brooklyn+NY+USA";

//set map api url
$url = "http://maps.google.com/maps/api/geocode/json?address=$address";

//call api
$json = file_get_contents($url);
$json = json_decode($json);
$lat = $json->results[0]->geometry->location->lat;
$lng = $json->results[0]->geometry->location->lng;
echo "Latitude: " . $lat . ", Longitude: " . $lng;

// output
// Latitude: 40.6781784, Longitude: -73.9441579
?>
```