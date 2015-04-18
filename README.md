# flowRight

Function composition from right to left.

# Install

```bash
npm install flowright
```

```bash
bower install flowright
```

# Usage

```javascript
var flowRight = require('flowright');

function square(n) {
  return n * n;
}

function add(/* args */) {
  var result = 0, i = arguments.length;
  while(i--) result += arguments[i];
  return result;
}

var addSquare = flowRight(square, add);

console.log(addSquare(1, 2)); // 9
console.log(addSquare(1, 2, 3)); // 36
console.log((addSquare(2)); // 4
```

# License

MIT
