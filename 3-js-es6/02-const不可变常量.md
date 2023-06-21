# Const

`const`声明一个只读的常量。一旦声明，常量的值就不能改变, 且必须立即初始化，不能留到以后赋值

```js
const PI = 3.1415;
PI // 3.1415

PI = 3;
// TypeError: Assignment to constant variable.

const foo;
// SyntaxError: Missing initializer in const declaration
```

- `const`的作用域与let命令相同：只在声明所在的块级作用域内有效
```js
if (true) {
  const MAX = 5;
}

MAX // Uncaught ReferenceError: MAX is not defined
```

- `const`命令声明的常量也是不存在提升
```js
if (true) {
  console.log(MAX); // ReferenceError
  const MAX = 5;
}
```

- `const`声明的常量，也与`let`一样不可重复声明
```js
var message = "Hello!";
let age = 25;

// 以下两行都会报错
const message = "Goodbye!";
const age = 30;
```




