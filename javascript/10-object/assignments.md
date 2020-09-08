# オブジェクトを使おう

## オブジェクトの宣言と要素の追加

1. `person` というオブジェクトを宣言して、以下の key value pair を追加しましょう。
   - `name` という key に対して、あなたの名前を value にする
   - `age` という key に対して、あなたの年齢を value にする
   - `tall` という key に対して、あなたの身長を value にする
2. `lesson` というオブジェクトを宣言して、以下の key value pair を追加しましょう。
   - `name` という key に対して、"object" を value にする
   - `number` という key に対して、10 を value にする

## オブジェクトの要素へのアクセス

1. 以下のオブジェクトのうち、年齢をコンソールに表示するようにコードを書いてください。

   ```js
   const dog = { name: "Marie", age: 10 };
   console.log(???);
   ```

2. 以下のオブジェクトのうち、ブランドをコンソールに表示するようにコードを書いてください。

   ```js
   const shoe = { name: "Air Force", brand: "NIKE" }
   console.log(???)
   ```

## オブジェクトの要素の更新

1. 以下のオブジェクトのうち、年齢に1加算してオブジェクト全体をコンソールに表示してください。

   ```js
   const person = { name: "Satoshi", age: 25, country: "Japan" };
   // オブジェクトを更新してから
   console.log(person);
   ```

2. 以下のオブジェクトのうち、アプリの名前を Twitter に、使用回数を 1000 に変更して、オブジェクト全体をコンソールに表示してください。

   ```js
   const app = { name: "Original one", times: 500 };
   // オブジェクトを更新してから
   console.log(app);
   ```

## オブジェクトを使う関数の作成

1. `createMeishi` という関数を作成しましょう。
   - 第一引数は名前、第二引数は会社、第三引数は電話番号とします。
   - 引数の情報をもとに、名刺を表すオブジェクトを作成して返してください。

   ```js
   const meishi = createMeishi("Satoshi", "ABC", "0120-123-456");
   console.log(meishi); // { name: "Satoshi", company: "ABC", phoneNumber: "0120-123-456" }
   ```

2. `createTripPlan` という関数を作成しましょう。
   - 第一引数は行き先、第二引数は出発日、第三引数は帰着日とします。
   - 引数の情報をもとに、旅行プランを表すオブジェジェクトを作成して返してください。

   ```js
   const tripPlan = createTripPlan("Kagoshima", "2021/3/20", "2021/3/24");
   console.log(tripPlan); // { destination: "Kagoshima", startDate: "2021/3/20". returnDate: "2021/3/24" }
   ```

3. `changeAge` という関数を作成しましょう。
   - 第一引数は人を表すオブジェクト、第二引数は変更後の年齢とします。
   - 第一引数のオブジェクトの年齢を、第二引数で更新します。

   ```js
   const person = { name: "Satoshi", age: 24 };
   const result = changeAge(person, 25);
   console.log(result); // { name: "Satoshi", age: 25 }
   ```
