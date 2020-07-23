# JS Basics

### Objects

Removing values from an object in a non-destructive manner:

``` js
const myObject = {
  a: 1,
  b: 2,
  c: 3
};
const { a, ...noA } = myObject;
console.log(noA); // => { b: 2, c: 3 }
```

_Source: [codeburst.io](https://codeburst.io/use-es2015-object-rest-operator-to-omit-properties-38a3ecffe90)_

### Mixed

Get select keys and values from either an object or an array:

``` js
function getSome (original, desired) {
  const cleaned = (original && typeof original === 'object' && original.constructor === Array) ? Object.assign({}, ...original) : original

  return desired.reduce((obj, key) => ({ ...obj, [key]: cleaned[key] }), {})
}
```
