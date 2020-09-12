# Higher order functions - 高階関数

## 高階関数を使った問題

1. `sayHelloToEveryone` という関数を作りましょう。引数は人の名前が入った配列です。全員1人ずつ、`Hello` を付加した挨拶文をコンソールに表示してください。ただし、高階関数を使ってください。

   ```js
   const names = ["Makoto", "Kairi", "Ai"];
   sayHelloToEveryone(names);
   // 以下が表示されれば正解
   // "Hello, Makoto"
   // "Hello, Kairi"
   // "Hello, Ai"
   ```

   ```js
   function sayHelloToEveryone(arrayOfNames) {
      arrayOfNames.forEach(function(eachName) {
         console.log("Hello, " + eachName);
      });
   }
   ```

   アロー関数を使っても良いです。

   ```js
   function sayHelloToEveryone(arrayOfNames) {
      arrayOfNames.forEach(eachName => {
         console.log("Hello, " + eachName);
      });
   }
   ```

2. `doubleNumbers` という関数を作りましょう。引数は数値型が入った配列です。全ての数値を2倍した配列を返します。ただし、高階関数を使ってください。

   ```js
   const numbers = [1, 2, 3, 4, 5];
   const result = doubleNumbers(numbers);
   console.log(result); // [2, 4, 6, 8, 10] が出れば正解
   ```

   ```js
   function doubleNumbers(arrayOfNumbers) {
      return arrayOfNumbers.map(function(eachNumber) {
         return eachNumber * 2;
      });
   }
   ```

   アロー関数を使っても良いです。

   ```js
   function doubleNumbers(arrayOfNumbers) {
      return arrayOfNumbers.map(eachNumber => {
         return eachNumber * 2;
      });
   }
   ```

   さらに短縮できます。

   ```js
   function doubleNumbers(arrayOfNumbers) {
      return arrayOfNumbers.map(eachNumber => eachNumber * 2);
   }
   ```

3. `getEvenNumber` という関数を作りましょう。引数は数値型が入った配列です。偶数だけ取り出して新しい配列を返します。ただし、高階関数を使ってください。

   ```js
   const numbers = [1, 2, 3, 4, 5];
   const result = getEvenNumber(numbers);
   console.log(result); // 2, 4
   ```

   ```js
   function getEvenNumber(arrayOfNumbers) {
      return arrayOfNumbers.filter(function(eachNumber) {
         return eachNumber % 2 === 0;
      });
   }
   ```

   アロー関数を使っても良いです。

   ```js
   function getEvenNumber(arrayOfNumbers) {
      return arrayOfNumbers.filter(eachNumber => {
         return eachNumber % 2 === 0;
      });
   }
   ```

   さらに短縮できます。

   ```js
   function getEvenNumber(arrayOfNumbers) {
      return arrayOfNumbers.filter(eachNumber => eachNumber % 2 === 0);
   }
   ```

4. `averageNumber` という関数を作りましょう。引数は数値型が入った配列です。その配列に入っている数値の平均を返します。ただし、高階関数を使ってください。

   ```js
   const numbers = [1, 2, 3, 4, 5];
   const result = averageNumber(numbers);
   console.log(result); // 3
   ```

   ```js
   function averageNumber(arrayOfNumbers) {
      let sum = 0;
      arrayOfNumbers.forEach(function(eachNumber) {
         sum += eachNumber;
      });

      return sum / arrayOfNumbers.length;
   }
   ```

   アロー関数を使うことで短縮もできますし、`reduce` という高階関数も使えます。これは難しいのでプログラミングに慣れてきたら、ぜひ[MDN](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)で使い方を理解してみてください。

   ```js
   function averageNumber(arrayOfNumbers) {
      const sum = arrayOfNumbers.reduce((pre, cur) => {
         return pre + cur;
      }, 0);

      return sum / arrayOfNumbers.length;
   }
   ```

5. `pickStringFromArray` という関数を作りましょう。
   - 第一引数は配列とします。
   - 配列の要素のうち、文字列のものだけを抽出して新しい配列を作成して、その新しい配列を返してください。
   - 第一引数として渡す配列の内容は変更してはいけません。
   - ただし、高階関数を使ってください。

   ```js
   const testArray = ["Satoshi", 24, true, "Hello"];
   const result = pickStringFromArray(testArray);
   console.log(result); // ["Satoshi", "Hello"]
   console.log(testArray); // ["Satoshi", 24, true, "Hello"]
   ```

   ```js
   function pickStringFromArray(array) {
      return array.filter(function(element) {
         return typeof element === "string";
      });
   }
   ```

   アロー関数を使っても良いです。。

   ```js
   function pickStringFromArray(array) {
      return array.filter(element => typeof element === "string");
   }
   ```

6. 関数 `pluck` を宣言してください。
   - 第一引数は配列とします。この配列には要素としてオブジェクトが入っています。
   - 第二引数は文字列とします。
   - 第一引数の配列の要素であるオブジェクトから、第二引数の文字列に対応する key に対しての value を抽出し、配列として返してください。
   - ただし、高階関数を使ってください。

   ```js
   const arrayOfObject = [
      { name: "Satoshi", age: 24 },
      { name: "Alice", age: 26 },
      { name: "Bob", age: 28 },
   ];

   const result = pluck(arrayOfObject, "name");
   console.log(result); // ["Satoshi", "Alice", "Bob"]
   ```

   ```js
   function pluck(array, key) {
      return array.map(function(element) {
         return element[key];
      });
   }
   ```
