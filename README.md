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

Source: [codeburst.io](https://codeburst.io/use-es2015-object-rest-operator-to-omit-properties-38a3ecffe90)
