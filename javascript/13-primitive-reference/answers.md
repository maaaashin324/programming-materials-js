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
   const person2 = { ...person1 };

   person1.age += 1;
   ```

   もしくは以下でも良いです。

   ```js
   const person1 = { name: "Satoshi", age: 31 };
   const person2 = {};
   for (const key in person1) {
      person2[key] = person1[key];
   }

   person1.age += 1;
   ```

2. `numbers1` という配列の内容を `numbers2` という変数に複製します。その後、`numbers1` 配列から最後の要素を取り出してください。このとき、`numbers2` の配列は変更されないようにしてください。

   ```js
   const numbers1 = [1, 2, 3, 4, 5];

   const numbers2 = [...numbers1];
   numbers1.pop();
   ```

   もしくは以下でも良いです。

   ```js
   const numbers1 = [1, 2, 3, 4, 5];
   const numbers = [];

   for (const element of numbers1) {
      numbers2.push(element);
   }

   numbers1.pop();
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

   ```js
   function changeAge(personObj) {
      personObj.age += 1;
      return personObj;
   }
   ```

   もちろん `for-in-loop` を使ってオブジェクトを複製しても良いです。

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

   ```js
   function changeAge2(personObj) {
      const result = { ...personObj };
      result.age += 1;
      return result;
   }
   ```

   もちろん `for-of-loop` を使って配列を複製しても良いです。

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

   ```js
   function retrieveEvenNumber(arrayOfNumbers) {
      const result = [];

      for (const element of arrayOfNumbers) {
         if (element % === 0) {
            result.push(element);
         }
      }

      return result;
   }
   ```

   この答えでは最初に新しい配列を `result` という変数に格納し、その後その新しい配列に必要な要素を追加しています。このようにして、引数の配列に直接変更をすることを避けることもできます。
