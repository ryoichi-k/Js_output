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
