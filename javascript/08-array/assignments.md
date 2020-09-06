# 配列を使おう

## 配列の宣言と追加

1. `fruits` という配列を宣言して、`apple`, `orange`, `peach` を要素として入れましょう。
2. `weather` という配列を宣言して、`sunny`, `cloudy`, `rainy` を要素として入れましょう。

## 配列の要素へのアクセス

1. 以下の配列のうち、`2` をコンソールに表示するようにコードを書いてください。

   ```js
   const numbers = [1, 2, 3, 4, 5];
   console.log(???);
   ```

2. 以下の配列のうち、`tea` をコンソールに表示するようにコードを書いてください。

   ```js
   const beverage = ["coffee", "water", "tea"];
   console.log(???)
   ```

## 配列の要素の更新

1. 以下の配列のうち、`2` を `10` に更新して、配列全体をコンソールに表示してください。

   ```js
   const numbers = [1, 2, 3, 4, 5];
   // 配列を更新してから
   console.log(numbers);
   ```

2. 以下の配列のうち、`coffee` を `juice` に更新して、配列全体をコンソールに表示してください。

   ```js
   const beverage = ["coffee", "water", "tea"];
   // 配列を更新してから
   console.log(beverage);
   ```

## 配列のメソッド

以下の配列があるとします。

```js
const numbers = [1, 2, 3, 4, 5];
```

1. 上記の配列から最後の要素を抜き出して、変数に格納し、その変数と要素を抜き出した後の配列の中身をコンソールに表示してください。
2. 1の続きで、最初の要素を抜き出して、変数に格納し、その変数と要素を抜き出した後の配列の中身をコンソールに表示してください。
3. 2の続きで、配列の最後の要素として `10` を追加し、配列の中身をコンソールに表示してください。
4. 3の続きで、配列の最初の要素として `0` を追加し、配列の中身をコンソールに表示してください。
5. 上記の配列の要素と、以下の配列の要素を組み合わせた配列を作成し、変数に格納し、その変数をコンソールに表示してください。

   ```js
   const numbers2 = [6, 7, 8];
   ```

## 配列を使う関数の作成

1. `calculateLength` という関数を作成しましょう。
   - 引数は配列が与えられるとします。
   - その引数の配列の長さを返してください。

   ```js
   const numbers = [1, 2, 3, 4, 5];
   const result = calculateLength(numbers);
   console.log(result); // 5 が出れば正解
   ```

2. `retrieveLastOne` という関数を作成しましょう。
   - 引数は配列が与えられるとします。
   - その引数の配列の最後の要素を返してください。
   - 元の配列の内容を変更してはいけません。

   ```js
   const fruits = ["orange", "apple", "peach"]
   const result = retrieveLastOne(fruits);
   console.log(result); //  "peach" が出れば正解
   ```

3. `retrieveOneElement` という関数を作成しましょう。
   - 第一引数は配列、第二引数は数値型とします。
   - 第二引数を配列のインデックスとして、指定された要素を返してください。
   - もし指定されたインデックスが存在しなければ、`The index doesn't exist.` という文字列を返してください。

   ```js
   const numbers = [1, 2, 3, 4, 5];
   const result = retrieveOneElement(numbers, 3);
   console.log(result); // 4 が出れば正解。3 が出たら不正解。

   const result2 = retrieveOneElement(numbers, 10);
   console.log(result); // "The index doesn't exist." が出れば正解。
   ```
