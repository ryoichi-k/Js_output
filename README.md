# Js_output

変数宣言(constを主流とすることが多い)

```jsx
var a = 'test'
let a = 'test'
const ARR = ['あ']
```

テンプレートリテラル

```jsx
// JSでの変数展開
`私は${name}です`
```

配列

```jsx
const arr = ['abc','def']

const arr = new Array()
arr[0] = ['xyz']
```

条件分岐 (JavaScriptにはelseifという構文は無い)

```jsx
if (条件) {
  // trueのときの処理
} else if (条件) {/* elseとifの間に半角空き */
  // 次の処理
} else {
  // それ以外の処理
}
```

繰り返し for

```jsx
// lengthプロパティで配列数を参照(PHPはcount()関数)
for (let i = 0; i < arr.length; i++) {
  console.log(arr[i])
}
```

配列用の繰り返しはfor~ofを使用

```jsx
for (let a of arr) {
  console.log(a)
}
```

forEach()メソッド

```jsx
const items = [
  {
    id: 1,
    name: "太郎"
  },
  {
    id: 2,
    name: "次郎"
  }
]

items.forEach(function(val) {
  console.log(val.id + ":" + val.name)
})
// 1:太郎
// 2:次郎
```

mapメソッド(配列の「全ての要素」に処理を加えた結果に対し新たな配列を返す。)

```jsx
const nums = [1,2,3,4,5]
const result = nums.map(function(val) {
  return val + val
})
console.log(result)
// [2,4,6,8,10]
```

filterメソッド(配列の「条件に合った要素」に処理を加えた結果に対し新たな配列を返す。)

```jsx
const nums = [1,2,3,4,5]
const result = nums.filter(function(val) {
  return val > 3
})
console.log(result)
// [4,5]
```

配列要素の置換や削除、(要素の中間に)追加する場合はsplice(スプライス)を使う。

```jsx
const arr = ['Sun','Mon','Tue','Wed','Thu','Fri','Sat']

console.log(arr.splice(5,2,'add')) // ['Fri','Sat']
arr.splice(5,2,'add')
console.log(arr)
// ["Sun", "Mon", "Tue", "Wed", "Thu", "add"]
```

関数
```jsx
function abc (xyz) {
  return xyz + 'えお'
}
// 実行結果を変数に代入
const def = abc('あいう')
console.log(def) // あいうえお
```
### join

配列の全ての要素を連結して、新しい文字列を作成する

```js
const date = ['2020', '02', '23'];
const result = date.join('.');

console.log(result); // "2020.02.23"
```
### forEach

配列のループ処理
配列の各要素に対して一度ずつ実行する
```js
const animals = ['dog', 'cat', 'fox'];
/**
 * # forEach
 * value: 現在処理されている配列の要素
 * index: 現在処理されている配列の要素のインデックス
 * array: 元々の配列（あまり使わないので下記では省略）
 */
animals.forEach((value, index) => {
  console.log(index, value);
});

// 0 "dog"
// 1 "cat"
// 2 "fox"
```

### every

配列の 全て の要素が、与えられた条件を満たしているかどうかチェックする

```js
// 例１
const numbers = [1, 2, 3, 4, 5, 6];
const result = numbers.every((num) => num < 5);
console.log(result); // false
// 例2
const numbers = [1, 2, 3, 4, 5, 6];
const result = numbers.every((num) => num < 10);
console.log(result); // true

```

### some

配列の 少なくとも1つ の要素が、与えられた条件を満たしているかどうかチェックする
なお、条件を満たした段階でループは終了する

```js
const numbers = [1, 2, 3, 4, 5, 6];
const result = numbers.some((num) => num > 3);
console.log(result); // true

// numbers[3]以降は評価されずに終了

```

### find

与えられた条件を満たしているか、配列要素の頭から実行（検索）し、
条件を満たした 最初の配列の要素 を返す
なお、条件を満たした段階でループは終了する


```js
const numbers = [1, 2, 3, 4, 5, 6];
const result = numbers.find((num) => num > 3);
console.log(result); // 4

// numbers[4]以降は評価されずに終了

```

### concat

文字列に別の文字列を連結して、新しい文字列をつくる

```js
const str1 = `Hello.`;
const str2 = `World!`;
const result = str1.concat(str2);

console.log(result); // > "Hello.World!"
```

