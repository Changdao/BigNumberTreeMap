
# BigNumberTreeMap.js
This is based on treemap-js. This package extended it to support BigNumber in JavaScript;
The following is copied from it.

A binary tree based map (aka dictionary) data type for Javascript, keeping keys sorted at all times. Provides `O(log n)` average case performance for inserting, retrieving and removing values.

## Installation
Works with Node.js(treemap.js support Browser, but this package not yet).

### Node
Install via `npm install bignumbertreemap-js`. Then access the TreeMap like this:

```javascript
const TreeMap = require("bignumbertreemap-js");
```

### Browser
Not support yet(0.5.3);

## Usage
```javascript
const BigNumber = require('bignumber.js');
var map = new TreeMap();

map.set(BigNumber(11.13));

map.set("my first key", "hello");    // keys can be strings, numbers or booleans. Values can be any data type
map.set("second key", [ 1, 3, 4 ]);
map.get("my first key");    // returns "hello"

map.set("my first key", 2342);
map.get("my first key");    // returns 2342

map.getLength();    //  returns 2

map.getMinKey();    // returns "my first key"
map.getMaxKey();    // returns "second key"

map.each(function (value, key) {
    // do something...
});

map.remove("my first key");
map.getLength();    // returns 1

map.getTree();    // returns the backing tree object
```
