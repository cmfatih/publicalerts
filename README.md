## Public Alerts
[![NPM][npm-image]][npm-url] [![Build Status][travis-image]][travis-url]

[publicalerts](http://github.com/cmfatih/publicalerts) is a Node.js module for 
obtaining emergency messages about hurricanes, storm warnings and earthquakes.  

### Installation

For latest release
```
npm install publicalerts
```

For HEAD
```
git clone https://github.com/cmfatih/publicalerts.git
```

### Usage

#### Test
```
npm test
```

#### Examples

```javascript
var publicalerts = require('publicalerts');

// Options:
// query:    any keyword to search
// location: location filter for search

publicalerts.search({location: 'texas'}, function(err, result) {
  if(err) console.log(err);

  console.log(JSON.stringify(result, null, 2));
});
/*
[
  [
    null,
    "-8092547155034825075",
    "6938810711701504273",
    "Severe Thunderstorm Warning",
    [
      "extreme_thunderstorm",
      "thunderstorm",
      "wind_storm",
      "met"
    ],
    "Southeast Texas",
    1,
    "${event} in ${location}",
    [
      null,
      30.606945322920698,
      -94.03319269248593
    ],
    "National Weather Service",
    0,
    [
      "The National Weather Service in Lake Charles has issued a Severe Thunderstorm..."
    ],
    "Active for next 16 minutes",
    "updated 21 minutes ago",
    "en-US",
    "//www.gstatic.com/images/icons/onebox/publicalerts_storm-24.png",
    "http://alerts.weather.gov/cap/wwacapget.php?x=TX12515A187758.SevereThunderstormWarning.12515A18956CTX.LCHSVRLCH.bd68b6b41660907dbc6b4e3104c71a90",
    "http://www.google.org/publicalerts/alert?aid=8fb17f3d180d1e8d",
    "More info",
    null,
    0.87,
    null,
    null,
    null,
    null,
    null,
    null,
    "Severe Thunderstorm Warning in Southeast Texas",
    [
      [
        null,
        [
          null,
          30.479999999999976,
          -94.14
        ],
        [
          null,
          30.700000000000024,
          -93.91
        ]
      ]
    ]
  ]
]
*/
```

### Notes

* It uses `www.google.org/publicalerts/`

### Changelog

For all notable changes see [CHANGELOG.md](https://github.com/cmfatih/publicalerts/blob/master/CHANGELOG.md)

### License

Licensed under The MIT License (MIT)  
For the full copyright and license information, please view the LICENSE.txt file.

[npm-url]: http://npmjs.org/package/publicalerts
[npm-image]: https://badge.fury.io/js/publicalerts.png

[travis-url]: https://travis-ci.org/cmfatih/publicalerts
[travis-image]: https://travis-ci.org/cmfatih/publicalerts.svg?branch=master