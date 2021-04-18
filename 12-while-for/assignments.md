# while-for

## while loop の使い方

1. 1から5までをコンソールに一行ずつ表示する while ループを作ってください。
2. 以下の配列の要素を一行ずつ表示する while ループを作ってください。

   ```js
   const fruits = ["orange", "apple", "peach"];
   ```

3. 10 から 0 までをコンソールに一行ずつ表示する while ループを作ってください。

## for loop の使い方

1. 1から5までをコンソールに一行ずつ表示する for ループを作ってください。
2. 以下の配列の要素を一行ずつ表示する for ループを作ってください。

   ```js
   const fruits = ["orange", "apple", "peach"];
   ```

3. 10 から 0 までをコンソールに一行ずつ表示する for ループを作ってください。

※ for loop でも while loop でも同じ実装ができることを確かめてください。

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

2. `countDown` という関数を作ってください。
   - 第一引数は数値型、第二引数も数値型とします。ただし第二引数はなくても良いものとします。
   - 第一引数から 0 までの数字を一行ずつコンソールに表示する関数を作ってください。
   - 第一引数が 0 以下である場合は "First argument should be more than 0" という文字列を表示してください。
   - 第二引数がない場合は 0 までカウントダウンし、ある場合はその数字までカウントダウンします。
   - 第二引数が第一引数より大きい場合は "Second argument should be more than first one" という文字列を表示してください。

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
   // "Second argument should be more than first one"
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
