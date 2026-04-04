##### 直接量
直接量包含number、boolean、string、null、undefined、Object、Class
##### 变量
let 变量 = 直接量
**var和let的区别**
|--|--|--|
|作用域	|函数作用域	|块级作用域|
|提升行为	|提升至作用域顶部，值为 undefined	|提升至作用域顶部，但存在 “暂时性死区”（TDZ）|
|重复声明	|允许在同一作用域内重复声明变量	|不允许在同一作用域内重复声明变量|
|全局对象属性（window 或 global）	|在全局作用域中，成为全局对象的属性	|在全局作用域中，不会成为全局对象的属性|
```ts
let flag = true
console.log(typeof(flag))   //使用typeof判断变量类型为boolean
```
```ts
let a = 1
let b
let sum = (b = a++ + --a) + a-- + b++
//b = 1 + 1 = 2
//sum = 2 + 1 + 2 = 5
```
##### 数组
```ts
let arr = new Array()
let arr = new Array(5)   //[empty × 5]
let arr1 = ['first', 'second']
let arr2 = new Array('first', 'second')
```
```ts
let arr = [1,2,3,4,5]
arr.splice(2,1,33,44)   //[1,2,33,44,4,5]
```
##### 对象
```ts
let container = {
  caoyao: '草药'
}
let key = 'caoyao'
console.log(container.caoyao)
console.log(container[key])  //[]可放字符串和变量
console.log(container['caoyao'])
```
