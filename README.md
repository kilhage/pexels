# Pexels API Client
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/glooby/pexels/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/glooby/pexels/?branch=master)
[![Build Status](https://scrutinizer-ci.com/g/glooby/pexels/badges/build.png?b=master)](https://scrutinizer-ci.com/g/glooby/pexels/build-status/master)
[![Latest Stable Version](https://poser.pugx.org/glooby/pexels/version)](https://packagist.org/packages/glooby/pexels)
[![Total Downloads](https://poser.pugx.org/glooby/pexels/downloads)](https://packagist.org/packages/glooby/pexels)
[![License](https://poser.pugx.org/glooby/pexels/license)](https://packagist.org/packages/glooby/pexels)

## Install

Install the Pexels API Client with Composer.

```json
"require": {
    "glooby/pexels": "~0.1"
},
```

## Usage

Create an instance of the Pexels API Client by passing in your API token as parameter.

```php
$pexels = new \Glooby\Pexels\Client("xxxxx");
```

Perform a search, the response gets returned as an array

```php
$response = $pexels->search('london');
```

Loop trough photos and display them

```php
foreach ($response['photos'] as $photo) {
    echo "<img src='".$photo['src']['small']."'>";
}
```

Example response

```json
{
   "total_results":6,
   "page":1,
   "per_page":15,
   "photos":[  
      {  
         "id":57456,
         "width":4000,
         "height":3000,
         "url":"https://www.pexels.com/photo/brown-rocky-mountain-painting-57456/",
         "photographer":"Pixabay",
         "src":{  
            "original":"https://static.pexels.com/photos/57456/torres-del-paine-mountains-granite-granite-rock-57456.jpeg",
            "large":"https://static.pexels.com/photos/57456/torres-del-paine-mountains-granite-granite-rock-57456-large.jpeg",
            "medium":"https://static.pexels.com/photos/57456/torres-del-paine-mountains-granite-granite-rock-57456-medium.jpeg",
            "small":"https://static.pexels.com/photos/57456/torres-del-paine-mountains-granite-granite-rock-57456-small.jpeg",
            "portrait":"https://static.pexels.com/photos/57456/torres-del-paine-mountains-granite-granite-rock-57456-portrait.jpeg",
            "square":"https://static.pexels.com/photos/57456/torres-del-paine-mountains-granite-granite-rock-57456-square.jpeg",
            "landscape":"https://static.pexels.com/photos/57456/torres-del-paine-mountains-granite-granite-rock-57456-landscape.jpeg",
            "tiny":"https://static.pexels.com/photos/57456/torres-del-paine-mountains-granite-granite-rock-57456-tiny.jpeg"
         }
      }
   ]
}
```

[www.glooby.com](https://www.glooby.com)
[www.glooby.se](https://www.glooby.se)
