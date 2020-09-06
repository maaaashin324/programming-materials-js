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

   ```js
   const numbers = [1, 2, 3, 4, 5];
   for (const element of numbers) {
      console.log(element);
   }
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

   ```js
   function sayHelloToEveryone(arrayOfNames) {
      for (const eachName of arrayOfNames) {
         const greeting = "Hello, " + eachName;
         console.log(greeting);
      }
   }
   ```

2. `doubleNumbers` という関数を作りましょう。引数は数値型が入った配列です。全ての数値を2倍した配列を返します。

   ```js
   const numbers = [1, 2, 3, 4, 5];
   const result = doubleNumbers(numbers);
   console.log(result); // [2, 4, 6, 8, 10] が出れば正解
   ```

   ```js
   function doubleNumbers(arrayOfNumbers) {
      const result = [];

      for (const number of arrayOfNumbers) {
         const doubledNumber = number * 2;
         result.push(doubledNumber);
      }

      return result;
   }
   ```

3. `getEvenNumber` という関数を作りましょう。引数は数値型が入った配列です。偶数だけ取り出して新しい配列を返します。

   ```js
   const numbers = [1, 2, 3, 4, 5];
   const result = getEvenNumber(numbers);
   console.log(result); // 2, 4
   ```

   ```js
   function getEvenNumber(arrayOfNumbers) {
      const result = [];

      for (const number of arrayOfNumbers) {
         if (number % 2 === 0) {
            result.push(number);
         }
      }

      return result;
   }
   ```

4. `averageNumber` という関数を作りましょう。引数は数値型が入った配列です。その配列に入っている数値の平均を返します。

   ```js
   const numbers = [1, 2, 3, 4, 5];
   const result = averageNumber(numbers);
   console.log(result); // 3
   ```

   ```js
   function averageNumber(arrayOfNumbers) {
      let sum = 0;

      for (const number of arrayOfNumbers) {
         sum += number;
      }

      const average = sum / arrayOfNumbers.length;
      return average;
   }
   ```
