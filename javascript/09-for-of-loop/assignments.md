# for-of-loop

## for-of-loop の使い方

1. 以下の配列の要素を1つずつ for-of-loop で取り出して、コンソールに表示してください。

   ```js
   const numbers = [1, 2, 3, 4, 5];
   // 以下のように1つずつ取り出せれば正解
   // 1
   // 2
   // 3
   // 4
   // 5
   ```

## 問題

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
