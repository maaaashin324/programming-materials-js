# 関数の宿題

## 関数の宣言

1. `sayHello` という関数を作ってください。
   - 引数はなし
   - `"Hello"` という文字列を `return` する

```js
function sayHello() {
  return "Hello";
}
```

2. `showYourName` という関数を作ってください。
   - 引数は `name`
   - `Your name is Masa` というような文字列を `return` する

```js
function showYourName(name) {
  return "Your name is " + name;
}
```

3. `showNumber` という関数を作ってください。
   - 引数は `number`
   - コンソールに引数の `number` を表示する

```js
function showNumber(number) {
  console.log(number);
}
```

4. `sayThankYou` という関数を作ってください。
   - 引数はなし
   - コンソールに引数の `Thank you` を表示する

```js
function sayThankYou() {
  console.log("Thank you");
}
```

## 関数の実行

宣言した4つの関数を実行します。

1. `sayHello` 関数を実行します。RunJs の右側のペインに `Hello` が出たら正解。

```js
sayHello();
```

2. あなたの名前を文字列として引数に渡して、`showYourName` 関数を実行します。RunJs の右側のペインに `Your name is あなたの名前` が出たら正解。

```js
showYourName("Masa");
```

3. 数字を何でも良いので引数に渡して、`showNumber` 関数を実行します。RunJs の右側のペインに引数の数字が出たら正解。

```js
showNumber(32);
```

4. `sayThankYou` 関数を実行します。RunJs の右側のペインに `Thank you` が出たら正解。

```js
sayThankYou();
```

**さて、1番と4番のちがいは何なのでしょう？**
