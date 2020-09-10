# while-for

## while loop の使い方

1. 1から5までをコンソールに一行ずつ表示する while ループを作ってください。

   ```js
   let result = 1;
   while (result <= 5) {
      console.log(result);

      result += 1; // result++ でもOk
   }
   ```

2. 以下の配列の要素を一行ずつ表示する while ループを作ってください。

   ```js
   const fruits = ["orange", "apple", "peach"];
   let index = 0;
   while (index <= fruits.index) {
      console.log(fruits[index]);
      index += 1;
   }
   ```

3. 10 から 0 までをコンソールに一行ずつ表示する while ループを作ってください。

   ```js
   let number = 10;
   while (number >= 0) {
      console.log(number);

      number -= 1;
   }
   ```

## for loop の使い方

1. 1から5までをコンソールに一行ずつ表示する for ループを作ってください。

   ```js
   for (let i = 1; i <= 5; i += 1) {
      console.log(i);
   }
   ```

2. 以下の配列の要素を一行ずつ表示する for ループを作ってください。

   ```js
   const fruits = ["orange", "apple", "peach"];
   for (let i = 0; i < fruits.index; i += 1) {
      console.log(fruits[i]);
   }
   ```

3. 10 から 0 までをコンソールに一行ずつ表示する for ループを作ってください。

   ```js
   for (let i = 10; i >= 0; i -= 1) {
      console.log(i);
   }
   ```

※ for loop と while loop とで同じ問題を出題しました。どちらでも同じ実装ができることを確かめてください。

## while loop と for loop の応用

1. `reverseArray` という関数を作ってください。
   - 第一引数に配列を取ります。
   - 第一引数の配列の要素を逆順にした配列を返してください。
   - 第一引数の配列を変更してはいけません。
   - for-loop と while-loop を使った関数を両方作ってみてください。

   ```js
   const numbers = [1, 2, 3, 4, 5];
   const result = reverseArray(numbers);
   console.log(result); // [5, 4, 3, 2, 1]
   console.log(numbers); // [1, 2, 3, 4, 5]
   ```

   ```js
   function reverseArray(array) {
      const newArray = [];

      for (let i = array.length - 1; i >= 0; i -= 1) {
         newArray.push(array[i]);
      }

      return newArray;
   }
   ```

2. `countDown` という関数を作ってください。
   - 第一引数は数値型、第二引数も数値型とします。ただし第二引数はなくても良いものとします。
   - 第一引数から 0 までの数字を一行ずつコンソールに表示する関数を作ってください。
   - 第一引数が 0 以下である場合は "First argument should be more than 0" という文字列を表示してください。
   - 第二引数がない場合は 0 までカウントダウンし、ある場合はその数字までカウントダウンします。
   - 第二引数が第一引数より大きい場合は "Second argument should be less than first one" という文字列を表示してください。

   ```js
   countDown(5);
   // 5
   // 4
   // 3
   // 2
   // 1
   // 0
   countDown(-1);
   // "First argument should be more than 0"
   countDown(2, 5);
   // "Second argument should be less than first one"
   ```

   ```js
   function countDown(num, dest) {
      if (num <= 0) {
         console.log("First argument should be more than 0");
         return; // ここで return を書くことが重要！
      }
      if (!!dest && (num < dest)) {
         console.log("Second argument should be less than first one");
         return; // ここで return を書くことが重要！
      }

      let destination = 0;
      if (!!dest) {
         destination = dest;
      }

      for (let i = num; i >= destination; i -= 1) {
         console.log(i);
      }
   }
   ```

3. `makeOddUpper` という関数を作ってください。
   - 第一引数は文字列とします。
   - 第一引数の文字列の奇数番目の文字列を大文字にして返してください。

   ```js
   const result = removePunctuation("Hello");
   console.log(result); // HeLlO

   const result2 = removePunctuation("You are tall");
   console.log(result2); // YoU ArE tALl

   const result3 = removePunctuation("string");
   console.log(result3); // StRiNg
   ```

   ```js
   function makeOddUpper(str) {
      let result = "";

      for (let i = 0; i < str.length; i += 1) {
         if (i % 2 === 0) {
            result += str[i];
         } else {
            result += str[i].toUpperCase();
         }
      }

      return result;
   }
   ```
