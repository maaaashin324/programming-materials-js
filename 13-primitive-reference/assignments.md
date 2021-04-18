# primitive-reference

## プリミティブな値とオブジェクトのちがい

### プリミティブ

```js
let x = 5;
let y = x;

console.log(x);
console.log(y);

x += 1;

console.log(x);
console.log(y);
```

`x` に1を足した後、当然 `x` は値が変化しますが、`y` は変化していないことを自分でもコードを実行して確かめてください。

### オブジェクト

```js
const person1 = { name: "Satoshi", age: 31 };
const person2 = person1;

console.log(person1);
console.log(person2);

person1.age += 1;

console.log(person1);
console.log(person2);
```

`person1` の `age` というプロパティに1を足した後、`person1` の `age` も `person2` の `age` も同じ値に変化していることを、自分でもコードを実行して確かめてください。

また同じ事象は配列でも起こります。

```js
const numbers1 = [1, 2, 3, 4, 5];
const numbers2 = numbers1;

console.log(numbers1);
console.log(numbers2);

numbers1.pop();

console.log(numbers1);
console.log(numbers2);
```

`numbers1` から `pop` メソッドを使って最後の要素を取り除いた後、`numbers1` からも `numbers2` からも `5` が取り除かれていることを、自分でもコードを実行して確かめてください。

## オブジェクトや配列の複製

1. `person1` オブジェクトの内容を `person2` という変数に複製します。その後、`person1` オブジェクトの `age` プロパティに1を足してください。このとき、`person2` のオブジェクトは変更されないようにしてください。

   ```js
   const person1 = { name: "Satoshi", age: 31 };
   ```

2. `numbers1` という配列の内容を `numbers2` という変数に複製します。その後、`numbers1` 配列から最後の要素を取り出してください。このとき、`numbers2` の配列は変更されないようにしてください。

   ```js
   const numbers1 = [1, 2, 3, 4, 5];
   ```

## オブジェクトの性質を利用した関数

1. `changeAge` という関数を作ります。
   - 第一引数はオブジェクトとします。
   - 第一引数のオブジェクトは `age` というプロパティを持っていることとします。この `age` というプロパティに1を足してください。
   - 第一引数のオブジェクトを直接変更してください。

   ```js
   const person1 = { name: "Satoshi", age: 31 };
   const result = changeAge(person1);
   console.log(result); // { name: "Satoshi", age: 32 }
   console.log(person1); // { name: "Satoshi", age: 32 }
   ```

2. `changeAge2` という関数を作ります。
   - 第一引数はオブジェクトとします。
   - 第一引数のオブジェクトは `age` というプロパティを持っていることとします。この `age` というプロパティに1を足してください。
   - 第一引数のオブジェクトを直接変更しないでください。

   ```js
   const person1 = { name: "Satoshi", age: 31 };
   const result = changeAge2(person1);
   console.log(result); // { name: "Satoshi", age: 32 }
   console.log(person1); // { name: "Satoshi", age: 31 }
   ```

3. `retrieveEvenNumber` という関数を作ります。
   - 第一引数は要素が全て数値型となっている配列とします。
   - 第一引数の配列から、偶数の値だけを抜き出した配列を返してください。
   - 第一引数の配列を直接変更しないでください。

   ```js
   const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
   const result = retrieveEvenNumber(numbers);

   console.log(result); // [2, 4, 6, 8, 10]
   console.log(numbers); // [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
   ```
