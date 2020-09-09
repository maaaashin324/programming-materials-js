# for-in-loop

## for-in-loop の使い方

1. 以下のオブジェクトの key と value ペアを for-in-loop で取り出し、key と value を各行にわけて表示しましょう。

   ```js
   const person = { name: "Satoshi", age: 24, country: "Japan" };
   // 以下のように表示できれば正解
   // name
   // Satoshi
   // age
   // 24
   // country
   // Japan
   for (const key in person) {
      console.log(key);
      console.log(person[key]);
   }
   ```

2. 以下のオブジェクトの各ペアの value だけを一行ずつ表示しましょう。

   ```js
   const shoe = { name: "Air Force", brand: "NIKE", size: 28 };
   // 以下のように表示できれば正解
   // Air Force
   // NIKE
   // 28
   for (const key in shoe) {
      console.log(shoe[key]);
   }
   ```

## for-in-loop の使用方法

1. 関数 `pickStringFromObj` を宣言してください。
   - 第一引数はオブジェクトとします。
   - 新しいオブジェクトを作成し、第一引数のオブジェクトのそれぞれの key-value ペアの value が文字列のものだけを新しいオブジェクトに入れて、返します。
   - 第一引数として渡すオブジェクトの内容は変更してはいけません。

   ```js
   const person = { name: "Satoshi", age: 24, country: "Japan" };
   const result = pickStringFromObj(person);
   console.log(result); // { name: "Satoshi", country: "Japan" }
   console.log(person); // { name: "Satoshi", age: 24, country: "Japan" }
   ```

   ```js
   function pickStringFromObj(obj) {
      const result = {};

      for (const key in obj) {
         if (typeof key === "string") {
            result[key] = obj[key];
         }
      }

      return result;
   }
   ```

2. 関数 `removeEmptyString` を宣言してください。
   - 第一引数はオブジェクトとします。
   - 第一引数のオブジェクトから value が空の文字列であるペアを除いて返してください。
   - 第一引数として渡すオブジェクトの内容は変更してはいけません。

   ```js
   const game = { title: "programming", madeIn: "", when: 1997 }
   const result = removeEmptyString(game);
   console.log(result); // { title: "programming", when: 1997 }
   console.log(game); // { title: "programming", madeIn: "", when: 1997 }
   ```

   ```js
   function removeEmptyString(obj) {
      const result = {};

      for (const key in obj) {
         if (!!obj[key]) {
            result[key] = obj[key];
         }
      }

      return result;
   }
   ```

3. 関数 `swapObj` を宣言してください。
   - 第一引数はオブジェクトとします。
   - オブジェクトのすべての key-value ペアの key と value をひっくり返した新しいオブジェクトを返してください。

   ```js
   const obj = { q: 1, w: 2, e: 3, r: 4 };
   const result = swapObj(obj);
   console.log(result); // { 1: q, 2: w, 3: e, 4: r }
   console.log(obj); // { q: 1, w: 2, e: 3, r: 4 }
   ```

   ```js
   function swap(object) {
      const result = {};

      for (const key in object) {
         result[object[key]] = key;
      }

      return result;
   }
   ```

4. 関数 `getSpecificKey` を宣言してください。
   - 第一引数はオブジェクト、第二引数は文字列とします。
   - 第二引数と一致する key が第一引数のオブジェクトにあれば、その value を返してください。もしなければ、"This object doesn't have that key." という文字列を返してください。

   ```js
   const obj = { q: 1, w: 2, e: 3, r: 4 };
   const result = getSpecificKey(obj, "w");
   console.log(result); // 2

   const result2 = getSpecificKey(obj, "a");
   console.log(result2); // This object doesn't have that key.
   ```

   ```js
   function getSpecificKey(object, targetKey) {
      if (!object[targetKey]) {
         return "This object doesn't have that key."
      }
      return object[targetKey];
   }

## 配列とオブジェクトのあわせ技

1. 関数 `pluck` を宣言してください。
   - 第一引数は配列とします。この配列には要素としてオブジェクトが入っています。
   - 第二引数は文字列とします。
   - 第一引数の配列の要素であるオブジェクトから、第二引数の文字列に対応する key に対しての value を抽出し、配列として返してください。

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
   function pluck(array, targetKey) {
      const result = [];

      for (const eachObj of array) {
         for (const key in eachObj) {
            if (key === targetKey) {
               result.push(eachObj[key]);
            }
         }
      }

      return result;
   }
   ```
