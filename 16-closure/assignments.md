# クロージャ

## クロージャを使った問題

1. `createCountUp` という関数を作成してください。
   - 引数にカウントアップする際に初期値を数値として設定します。
   - アウトプットとして関数を返します。
     - この関数の引数はありません。
     - この関数は実行するたびに `createCountUp` の引数から1ずつカウントアップしてコンソールに表示します。

   ```js
   const countUp = createCountUp(1);
   countUp(); // コンソールに 1 が表示される
   countUp(); // コンソールに 2 が表示される
   countUp(); // コンソールに 3 が表示される
   countUp(); // コンソールに 4 が表示される
   countUp(); // コンソールに 5 が表示される
   ```

2. `createAdd` という関数を作成してください。
   - 第一引数は数値型とします。
   - アウトプットとして関数を返します。
     - この関数も第一引数は数値型とします。
     - この関数は `createAdd` の引数とこの関数の引数の足し算の結果（和）を返します。

   ```js
   const add = createAdd(10);
   const result = add(10);
   console.log(result); // 20

   const result2 = add(100);
   console.log(result2); // 110
   ```

3. `createConcatenateString` という関数を作成してください。
   - 第一引数は文字列型とします。
   - アウトプットとして関数を返します。
     - この関数も引数は文字列型とします。
     - この関数は `createConcatenateString` の引数とこの引数の文字列を結合したものを返します。
     - ただし、その間には半角スペースを入れてください。

   ```js
   const concatenateString = createConcatenateString("Hello");
   const result = concatenateString("Satoshi");
   console.log(result); // Hello Satoshi

   const concatenateString = createConcatenateString("Hello");
   const result2 = concatenateString("Bob");
   console.log(result2); // Hello Bob
   ```
