# 関数を変数に格納する

関数は変数に格納することもできます。もちろん `function` キーワードを使った関数宣言で関数を作成できるのですが、次回以降扱うクロージャーや高階関数を使うためには、関数を変数に格納することが必要になります。

## 従来の関数宣言と、変数に関数を格納したときの違い

以下のコードを実行してみてください。

### 関数宣言

```js
sayHello();

function sayHello() {
   console.log("Hello");
}
```

### 変数に関数を格納

```js
sayHello();

const sayHello = function() {
   console.log("Hello");
}
```

関数宣言では問題なく動作しますが、変数に関数を格納した場合は以下のエラーが出力されます。
`ReferenceError: Cannot access 'sayHello' before initialization`

この理由を説明してください。

## 問題

以下の問題はすべて、`function` キーワードを使った関数宣言ではなく、変数に関数を格納する形で関数を作成し、実行して結果を確かめてください。

1. `sayHelloToEveryone` という関数を作りましょう。引数は人の名前が入った配列です。全員1人ずつ、`Hello` を付加した挨拶文をコンソールに表示してください。

   ```js
   const names = ["Makoto", "Kairi", "Ai"];
   sayHelloToEveryone(names);
   // 以下が表示されれば正解
   // "Hello, Makoto"
   // "Hello, Kairi"
   // "Hello, Ai"
   ```

2. `doubleNumbers` という関数を作りましょう。引数は数値型が入った配列です。全ての数値を2倍した配列を返します。

   ```js
   const numbers = [1, 2, 3, 4, 5];
   const result = doubleNumbers(numbers);
   console.log(result); // [2, 4, 6, 8, 10] が出れば正解
   ```

3. `getEvenNumber` という関数を作りましょう。引数は数値型が入った配列です。偶数だけ取り出して新しい配列を返します。

   ```js
   const numbers = [1, 2, 3, 4, 5];
   const result = getEvenNumber(numbers);
   console.log(result); // 2, 4
   ```

4. `averageNumber` という関数を作りましょう。引数は数値型が入った配列です。その配列に入っている数値の平均を返します。

   ```js
   const numbers = [1, 2, 3, 4, 5];
   const result = averageNumber(numbers);
   console.log(result); // 3
   ```

5. `pickStringFromArray` という関数を作りましょう。
   - 第一引数は配列とします。
   - 配列の要素のうち、文字列のものだけを抽出して新しい配列を作成して、その新しい配列を返してください。
   - 第一引数として渡す配列の内容は変更してはいけません。

   ```js
   const testArray = ["Satoshi", 24, true, "Hello"];
   const result = pickStringFromArray(testArray);
   console.log(result); // ["Satoshi", "Hello"]
   console.log(testArray); // ["Satoshi", 24, true, "Hello"]
   ```
