# if 条件文を使う

## 比較演算子

条件文を作り出せるのは比較演算子でした。この比較演算子の使い方を練習します。それぞれの文章に見合ったコードを書いて、コンソールに表示してみましょう。

### 問題

1. 32という数値を `age` という変数に格納した上で、その変数の内容が `32` と一致するかどうか

   ```js
   let age = 32;
   console.log(age == 32);
   ```

2. 32という数値を `age` という変数に格納した上で、その変数の内容とデータ型が `32` と一致するかどうか

   ```js
   let age = 32;
   console.log(age === 32);
   ```

3. 32という数値を `age` という変数に格納した上で、その変数の内容が `"32"` と一致するかどうか（ダブルコーテーションを付けていることに注意）

   ```js
   let age = 32;
   console.log(age == 32);
   ```

   ここから言えることは、`==` ではデータ型の一致までは確認しないということです。

4. 32という数値を `age` という変数に格納した上で、その変数の内容とデータ型が `"32"` と一致するかどうか（ダブルコーテーションを付けていることに注意）

   ```js
   let age = 32;
   console.log(age === 32);
   ```

   ここから言えることは、`===` ではデータ型の一致まで確認するということです。状況によって文字列の数値と、数値型の数値の療法を扱わないといけなくなる場合があるので、この3つのイコールを基本的に使用して、文字列なのか数値型をはっきりと区別するコードを書くようにしましょう。

5. 今日の天気を `weather` という変数に格納した上で、その変数の内容が `"sunny"` と一致するかどうか

   ```js
   let weather = "sunny";
   console.log(whether == "sunny");
   ```

6. 今日の天気を `weather` という変数に格納した上で、その変数の内容とデータ型が `"sunny"` と一致するかどうか

   ```js
   let weather = "sunny";
   console.log(weather === "sunny");
   ```

7. 32という数値を `age` という変数に格納した上で、その変数の内容が `56` と一致しないことを確かめる

   ```js
   let age = 32;
   console.log(age != 56);
   ```

8. 32という数値を `age` という変数に格納した上で、その変数の内容とデータ型が `56` と一致しないことを確かめる

   ```js
   let age = 32;
   console.log(age !== 56);
   ```

9. 32という数値を `age` という変数に格納した上で、その変数の内容とデータ型が `"32"` と一致しないことを確かめる（ダブルコーテーションを付けていることに注意）

    ```js
    let age = 32;
    console.log(age !== "32");
    ```

10. 32という数値を `age` という変数に格納した上で、その変数の内容が `20` 以上かどうか

    ```js
    let age = 32;
    console.log(age >= 20);
    ```

11. 32という数値を `age` という変数に格納した上で、その変数の内容が `19` より上かどうか

    ```js
    let age = 32;
    console.log(age > 19);
    ```

12. 西暦を `reiwa` という変数に格納した上で、その変数の内容が `2019` 以上かどうか

    ```js
    let reiwa = 2019;
    console.log(reiwa >= 2019);
    ```

13. 西暦を `heisei` という変数に格納した上で、その変数の内容が `2020` 未満かどうか

    ```js
    let heisei = 2019;
    console.log(heisei < 2020);
    ```

## if 条件文内の比較演算子

これ以降に問題に取り組む前に、比較演算子の問題を難なく解けるように繰り返し練習することをおすすめします。

1. 以下のコードで足りないところを書き足して、コンソールにメッセージが表示されるようにしてください。

   1. もし年齢が20歳以上なら、お酒を買える

   ```js
   let age = 32;
   if (age >= 20) {
      console.log("You can drink alcohol.");
   }
   ```

   2. あなたはゴルフプレイヤーですか？

   ```js
   let isGolfPlayer = true;
   if (isGolfPlayer) {
      console.log("You are a golf player.");
   }
   ```

   3. あなたはゴルフプレイヤーではないですね。

   ```js
   let isGolfPlayer = false
   if (!isGolfPlayer) {
      console.log("You are NOT a golf player.");
   }
   ```

   4. 今日の天気は良い天気？

   ```js
   let weather = "sunny";
   if (weather === "sunny") {
      console.log("It's great sunshine!");
   }
   ```

   5. 今日は傘が必要？

   `let weather = "sunny";` の部分は変えない前提で考えてみてください。ヒントは晴れでなければ傘が必要になるんですよね。

   ```js
   let weather = "sunny";
   if (weather !== "sunny") {
      console.log("You might need an umbrella.");
   }
   ```

## if 条件文

それぞれのコードを自分で書いてみましょう。

1. お酒を飲めますか？
   - 年齢を格納する変数を宣言する。もしその変数が20歳以上なら、お酒を買えることを示す `true` をコンソールに表示する。

   ```js
   let age = 32;
   if (age >= 20) {
     console.log(true);
   }
   ```

2. 今日の天気は良い天気？
   - 天気を格納する変数を宣言する。もしその変数が晴れなら、晴れであることを示す `true` をコンソールに表示する。

   ```js
   let weather = "sunny";
   if (weather === "sunny") {
     console.log(true);
   }
   ```

3. 今日は傘が必要？
   - 天気を格納する変数を宣言する。もしその変数が晴れでなければ、傘が必要であることを示す `true` をコンソールに表示する。

   ```js
   let weather = "rainy";
   if (weather !== "sunny") {
     console.log(true);
   }
   ```

## if - else 条件文

それぞれのコードを自分で書いてみましょう。

1. お酒を飲めますか？
   - 年齢を格納する変数を宣言する。もしその変数が20歳以上なら、お酒を買えることを示す `true` をコンソールに表示し、そうでなければ `false` をコンソールに表示する。

   ```js
   let age = 32;
   if (age >= 20) {
     console.log(true);
   } else {
     console.log(false);
   }
   ```

2. 今日の天気は良い天気？
   - 天気を格納する変数を宣言する。もしその変数が晴れなら、晴れであることを示す `true` をコンソールに表示し、そうでなければ `false` をコンソールに表示する。

   ```js
   let weather = "sunny";
   if (weather === "sunny") {
     console.log(true);
   } else {
     console.log(false);
   }
   ```

3. 今日は傘が必要？
   - 天気を格納する変数を宣言する。もしその変数が晴れでなければ、傘が必要であることを示す `true` をコンソールに表示し、そうでなければ `false` をコンソールに表示する。

   ```js
   let weather = "rainy";
   if (weather !== "sunny") {
     console.log(true);
   } else {
     console.log(false);
   }
   ```

## if - else if 条件文

1. 今日の天気は良い天気？
   - 天気を格納する変数を宣言する。その変数の内容によって以下のように処理を切り分ける。
     - もしその変数の内容が晴れなら、`It's great weather today!` をコンソールに表示する。
     - もしその変数の内容が曇りなら、`It's not fine weather today!` をコンソールに表示する。
     - もしそれ以外なら、`I need to bring an umbralla.` をコンソールに表示する。

   ```js
   let weather = "sunny";
   if (weather === "sunny") {
     console.log("It's great weather today!");
   } else if (weather === "cloudy") {
     console.log("It's not fine weather today!");
   } else {

   }
   ```

## if を持つ function

条件文を持つ関数を実装します。以下の問題文をコードに実装してみましょう。

   1. `canDrinkAlcohol` という関数を作ってください。
      - 引数は `age` とします
      - その `age` が20以上であれば、`true` を返すし、そうでなければ `false` を返します。

   ```js
   function canDrinkAlcohol(age) {
      if (age >= 20) {
         return true;
      } else {
         return false;
      }
   }
   ```

   ```js
   // もしくはこの書き方でも良いです
   function canDrinkAlcohol(age) {
      if (age >= 20) {
         return true;
      }
      return false;
   }
   ```

   1. `needUmbrella` という関数を作ってください。
      - 引数は `weather` とします
      - その `whether` が `sunny` であれば、`no` を返す
      - その `whether` が `cloudy` であれば、`maybe` を返す
      - その `whether` が `rainy` であれば、`yes` を返す

   ```js
   function needUmbrella(weather) {
      if (weather === "sunny") {
         return "no";
      } else if (weather === "cloudy") {
         return "maybe";
      } else if (weather === "rainy") {
         return "yes";
      }
   }
   // 理想的にはどのパターンにも当てはまらない場合にも
   // 何かしら返すべきなのですが、現時点では気にせず
   // この条件分岐が作れることに焦点を当ててみましょう。
   ```
