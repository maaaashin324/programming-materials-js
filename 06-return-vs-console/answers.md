# return vs console.log

## return と console の比較

1. `sayHello` という関数を作成します。関数を実行し、アウトプットを変数に入れて、その変数の中身をコンソールに表示してください。何が表示されますか？
   - 引数はなし
   - `"Hello"` という文字列を `return` する

```js
function sayHello() {
  return "Hello";
}

const result = sayHello();
console.log(result); // Hello が表示されたら正解！
```

2. `showYourName` という関数を作成します。関数を実行し、アウトプットを変数に入れて、その変数の中身をコンソールに表示してください。何が表示されますか？
   - 引数は `name`
   - `Your name is Masa` というような文字列を `return` する

```js
function showYourName(name) {
  return "Your name is " + name;
}

const result = showYourName("Masa");
console.log(result); // Your name is Masa が表示されたら正解！
```

3. `showNumber` という関数を作成します。関数を実行し、アウトプットを変数に入れて、その変数の中身をコンソールに表示してください。何が表示されますか？
   - 引数は `number`
   - コンソールに引数の `number` を表示する

```js
function showNumber(number) {
  console.log(number);
}

const result = showNumber(32);
console.log(result);
```

  2行が表示されたら正解！
     1. 32
     2. `undefined`

4. `sayThankYou` という関数を作成します。関数を実行し、アウトプットを変数に入れて、その変数の中身をコンソールに表示してください。何が表示されますか？
   - 引数はなし
   - コンソールに引数の `Thank you` を表示する

```js
function sayThankYou() {
  console.log("Thank you");
}

const result = sayThankYou();
console.log(result);
```

  2行が表示されたら正解！
     1. `Thank you`
     2. `undefined`
