# A Babel plugin that automatically add `__debug` variable for debugging and logging

## Install
```
yarn add -D babel-plugin-transform-dbg
```

## .babelrc
```
{
  "presets": ["@babel/env"],
  "plugins": ["@babel/transform-runtime", "babel-plugin-transform-dbg"]
}

```

## Usage

### in Object methods
```
// component.vue
const vm = {
  methods: {
    onSomeEvent () {
      console.log(__debug) // {file:"/absolute/path/to/component.vue",line:3,method:"onSomeEvent"}
    }
  }
}
```

## in function
```
// a.js
function test () {
   console.log(__debug); // {file:"/absolute/path/to/a.js",line:1,method:"test"}
}
test()
```
