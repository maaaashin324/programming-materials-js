# スコープ

## スコープとは何かを確認

どのスコープにある変数かによって、コードがその変数にアクセスできる / できないを実体験してください。

1. この関数を実行すると `Hello Satoshi` はコンソールに表示されますか？されませんか？

表示されますね。

```js
const name = "Satoshi";

function sayHello() {
   console.log("Hello " + name);
}

sayHello();
```

2. あいさつをするのは `Satoshi` に対してですか？ `Bob` に対してですか？

`Bob` に対してです。一番身近なスコープから、その変数があるかどうかを探しに行きます。ところで、スコープの内外で同じ変数名を使うのはバッドプラクティスです。

```js
const name = "Satoshi";

function sayHello(name) {
   console.log("Hello " + name);
}
sayHello("Bob");
```

3. 表示されるのは `31` でしょうか？ `32` でしょうか？

`32` です。2番と同じ理由ですね。

```js
const age = 31;

function sayMyAge() {
   const age = 32;
   console.log("My age is " + age);
}
sayMyAge();
```

4. `permitted` はコンソールに2回表示できるでしょうか？

1回しか表示できません。`if` のスコープの中で `permitted` という変数が宣言されているので、`if` の外からは参照できないのです。

```js
const age = 32;
if (age > 20) {
   const permitted = true;
   console.log(permitted);
}

console.log(permitted);
```

5. `i` はコンソールに表示できるでしょうか？

`i` はできません。`i` は for-loop の中で宣言されているので、for-loop の外側からは参照できないのです。

```js
for (let i = 0; i < 10; i += 1) {
   console.log("count up");
}

console.log(i);
```
