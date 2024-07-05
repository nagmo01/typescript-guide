## 型注釈による型の利用

変数名: 型名

## 変数宣言と型注釈

let firstName: string = "Bill";
let age: number = 22;

## 変数に対して明示的に型を指定することを型注釈という

## 型推論

let firstName = "Bill"; //初期値Billからstring型を推論
let age = 22; // 初期値22からnumber型と推論


## 異なる型の値を代入した場合

let age = 22; //初期値22からnumber型を推論

age = "23"; //string型を代入

// >> Type 'string' is not assignable to type 'number'.
//(型stringを型numberに割り当てることができません)

## パラメータに型を指定しない場合

function greet(firstName) {
  console.log("hello, " + firstName)
}

// >> Parameter 'firstName' implicitly has an 'any' type.
// (パラメーター 'firstName' の型は暗黙的に 'any' になります。)

## 型に許されていない操作(演算)をしようとした場合

console.log(2 + true)

// >> Operator '+' cannot be applied to types 'number' and 'boolean'.
// (演算子 '+' を型 'number' および 'boolean' に適用することはできません)

