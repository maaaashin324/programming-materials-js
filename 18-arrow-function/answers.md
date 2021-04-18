# アロー関数

## 問題

以下の問題はすべて、`function` キーワードを使った関数宣言ではなく、アロー関数を使って実装してください。

1. `canDrinkAlcohol` という関数を作ってください。
   - 引数は `age` とします
   - その `age` が20以上であれば、`true` を返すし、そうでなければ `false` を返します。

   ```js
   const canDrinkAlcohol = (age) => {
      if (age >= 20) {
         return true;
      }
      return false;
   }
   ```

2. `needUmbrella` という関数を作ってください。
   - 引数は `weather` とします
   - その `whether` が `sunny` であれば、`no` を返す
   - その `whether` が `cloudy` であれば、`maybe` を返す
   - その `whether` が `rainy` であれば、`yes` を返す

   ```js
   const needUmbrella = weather => {
      if (weather === "sunny") {
         return "no";
      }
      if (weather === "cloudy") {
         return "maybe";
      }
      return "yes";
   }
   ```

3. `calculateLength` という関数を作成しましょう。
   - 引数は配列が与えられるとします。
   - その引数の配列の長さを返してください。

   ```js
   const numbers = [1, 2, 3, 4, 5];
   const result = calculateLength(numbers);
   console.log(result); // 5 が出れば正解
   ```

   ```js
   const calculateLength = array => array.length;
   ```

4. `changeAge` という関数を作成しましょう。
   - 第一引数は人を表すオブジェクト、第二引数は変更後の年齢とします。
   - 第一引数のオブジェクトの年齢を、第二引数で更新します。
   - 第一引数のオブジェクトを直接変更しないでください。

   ```js
   const person = { name: "Satoshi", age: 24 };
   const result = changeAge(person, 25);
   console.log(result); // { name: "Satoshi", age: 25 }
   ```

   ```js
   const changeAge = personObj => {
      const newObj = { ...personObj };
      newObj.age = 25;
      return newObj;
   };
   ```

5. `createAdd` という関数を作成してください。
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

   ```js
   const createAdd = x => {
      return (y) => {
         return x + y;
      }
   }
   ```

   もっと省略すると以下になります。

   ```js
   const createAdd = x => y => x + y;
   ```

   一行で書けてしまいました！
