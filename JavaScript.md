[js教程](https://www.runoob.com/js/js-tutorial.html)

### 基本知识

**异常处理**

```ts
SyntaxError   //语法错误
ReferenceError   //引用错误
TypeError   //类型错误
RangeError   //范围错误

//抛出异常
throw new Error(msg)

//断点：断点允许你在你选择的特定代码行暂停代码执行。暂停后，你可以检查变量、计算表达式并查看调用栈。
//观察者：观察表达式让你在代码运行时监视变量或表达式的值，即使它们不在当前作用域内。
//性能分析：性能分析通过让你捕捉屏幕截图和记录 CPU 使用率、函数调用及执行时间，帮助你识别性能瓶颈。
```

**工具**

- 代码检查工具：Linter 是一种静态代码分析工具，用于标记编程错误、错误、风格错误和可疑构造。一个常见的 linter 示例是 ESLint。
- 格式化工具：格式化工具是自动格式化你的代码以遵循特定样式指南的工具。一个常见的格式化工具示例是 Prettier。

#### 数据类型

* ​**数值**​：数值代表整数和浮点数。 整数的例子包括 7、19 和 90。
* ​**浮点数**​：浮点数是带有小数点的数值。 例子包括 3.14、0.5 和 0.0001。
* ​**字串**​：字串是由字符或文本组成的序列，包含在引用中。`"I like coding"` 和 `'JavaScript is fun'` 是字串的例子。
* ​**布尔**​：布尔代表两种可能值之一：`true` 或 `false`。 你可以使用布尔来表示条件，例如 `isLoggedIn = true`。
* ​**未定义和空**​：`undefined` 值是一个已声明但未赋值的变量。 `null` 值是空值，或者是故意赋值为 `null` 的变量。
* ​**对象**​：对象是键值对的集合。 键是属性名称，值是属性值。

这里， `pet` 对象有三个属性或键：`name`、`age` 和 `type`。 值分别是 `Fluffy`、`3` 和 `dog`。

```js
let pet = {
  name: "Fluffy",
  age: 3,
  type: "dog"
};
```

* ​**符号**​：符号数据类型是唯一且不可变的值，可用作对象属性的标识符。

在下面的示例中，创建了两个具有相同描述的符号，但它们并不相等。

```js
const crypticKey1= Symbol("saltNpepper");
const crypticKey2= Symbol("saltNpepper");
console.log(crypticKey1 === crypticKey2); // false
```

* ​**大整数**​：当数字对于 `Number` 数据类型来说太大时，你可以使用大整数数据类型来表示任意长度的整数。

通过在数字末尾添加 `n` 可以创建大整数。

```js
const veryBigNumber = 1234567890123456789012345678901234567890n;
```

##### typeof

```ts
let flag = true
console.log(typeof flag)   //使用typeof判断变量类型为boolean

//特殊 (typeof 操作符会为 null 值返回 "object")
let user = null;
console.log(typeof user); // "object"
```

#### Math

- 基础计算

| 方法 | 描述 | 示例 |
| --- | --- | --- |
| `Math.abs(x)` | 绝对值 | `Math.abs(-5) // 5` |
| `Math.sqrt(x)` | 平方根 | `Math.sqrt(9) // 3` |
| `Math.cbrt(x)` | 立方根（ES6） | `Math.cbrt(8) // 2` |
| `Math.pow(x, y)` | x 的 y 次幂 | `Math.pow(2, 3) // 8` |
| `Math.hypot(x1, x2)` | Math.hypot(3, 4) | `Math.hypot(3, 4) // 5` |

- 取整方法

| 方法 | 描述 | 示例 |
| --- | --- | --- |
|`Math.round(x)`|四舍五入|`Math.round(4.7) // 5`|
|`Math.floor(x)`|向下取整	|`Math.floor(4.7) // 4`|
|`Math.ceil(x)`|向上取整	|`Math.ceil(4.2) // 5`|
|`Math.trunc(x)`|去除小数部分（ES6）|`Math.trunc(4.9) // 4`|

- 最值与求和

| 方法 | 描述 | 示例 |
| --- | --- | --- |
|`Math.max(x1, x2, ...)`|返回最大值|`Math.max(1, 3, 2) // 3`|
|`Math.min(x1, x2, ...)`|返回最小值|`Math.min(1, 3, 2) // 1`|
|`[x1, x2].reduce((a,b)=>a+b, 0)`|数组求和（非 Math 方法）|`[1,2,3].reduce((a,b)=>a+b, 0) // 6`|
|`Math.max(...list)`| 列表使用扩展运算符`...` |`Math.min(...[1, 2, 3]) // 1` |

- 随机数

| 方法 | 描述 | 示例 |
| --- | --- | --- |
|`Math.random()`|[0, 1) 之间的随机小数|`Math.random() // 0.123...`
|扩展：生成区间随机整数||`Math.floor(Math.random() * 10) // 0-9`|
|||`Math.floor(Math.random() * 10) + 1 // 1-10`|

- 三角函数（参数为弧度）

| 方法 | 描述 | 示例 |
| --- | --- | --- |
|`Math.sin(x)`|正弦|`Math.sin(Math.PI / 2) // 1`|
|`Math.cos(x)`|余弦|`Math.cos(Math.PI) // -1`|
|`Math.tan(x)`|正切|`Math.tan(0) // 0`|
|`Math.PI`|圆周率常量|`Math.PI // 3.141592653589793`|

- 对数与指数

| 方法 | 描述 | 示例 |
| --- | --- | --- |
|`Math.log(x)`|自然对数（底为 e）|`Math.log(Math.E) // 1`|
|`Math.log10(x)`|底为 10 的对数（ES6）|`Math.log10(100) // 2`|
|`Math.log2(x)`	|底为 2 的对数（ES6）|`Math.log2(8) // 3`|
|`Math.exp(x)`|e 的 x 次幂|`Math.exp(1) // ~2.718`|

- 其他实用方法

| 方法 | 描述 | 示例 |
| --- | --- | --- |
|`Math.sign(x)`|符号函数（ES6）|`Math.sign(-5) // -1`|
|`Math.clz32(x)`|32 位二进制前导零数（ES6）|`Math.clz32(1) // 31`|

**使用示例**

```
// 计算圆的面积
const radius = 5;
const area = Math.PI * Math.pow(radius, 2); //78.5398...

// 生成 1-100 的随机整数
const randInt = Math.floor(Math.random() * 100) + 1;

// 数组最大值
const nums = [10, 5, 20];
const max = Math.max(...nums); // 20
```

**注意事项**

- 所有方法通过 `Math` 对象调用（如 `Math.abs()`）。
- 三角函数参数使用弧度制（可用 `degrees * Math.PI/180` 转换）。
- `Math.random()` 不提供加密安全随机数（需用 `crypto.getRandomValues()`）。

#### Set

**Set**

* `Set` 是管理数据集合的内置选项。
* 集合确保其中的每个值只出现一次，使其在从数组中消除副本或处理不同值的集合时非常有用。
* 你可以使用 `Set()` 构造函数创建一个 `Set`：

```ts
//集合
var set = new Set([1,2,3,4,5]); // array -> set，用Set(arr)构造方法
var arr = [...set]; // set -> array，用...rest运算符
var mySet = new Set("Hello"); // str -> setSet(str)，用Set(arr)构造方法
```

* 集合可以使用这些方法进行操作：
  
  * `add()`：为 `Set` 添加一个新建元素。
  * `delete()`：从 `Set` 中移除一个元素。
  * `has()`：查看 `Set` 中是否存在某个元素。
  * `clear()`：从 `Set` 中移除所有元素。
  * `keys()` 和 `values()`：两者都返回包含 `Set` 值的 `SetIterator`。它们是相同的，因为 `keys()` 是 `values()` 的别名。
  * `forEach()`：用于遍历 `Set` 的值。

**Weaksets**

* `WeakSet` 是一个对象集合，允许你保存弱引用的对象。

**区别**

* 与 Set 不同，`WeakSet` 不支持数字或字串等原语。
* `WeakSet` 只保存对象，并且对这些对象的引用是“弱引用”，这意味着如果对象在你的代码中没有被其他地方使用，它会被自动移除以释放内存。

#### Map

**Map**

* `Map` 是一个内置对象，保存着与对象类似的键值对。
* Map 与标准 JavaScript 对象不同，它允许任何类型的密钥，包括对象和函数。
* 当频繁添加和移除键值点对时，`Map` 相较于标准对象提供了更好的性能。
* 你可以使用 `Map()` 构造函数创建一个 `Map`：

```js
const map = new Map([
  ['flower', 'rose'],
  ['fruit', 'apple'],
  ['vegetable', 'carrot']
]);
console.log(map); // Map(3) { 'flower' => 'rose', 'fruit' => 'apple', 'vegetable' => 'carrot' }
```

* 地图可以使用这些方法进行操作：
  * `set()`：为 `Map` 添加一个新建的密钥-值点对。
  * `get()`：从 `Map` 中检索密钥的值。
  * `delete()`：从 `Map` 中移除一个密钥-值点对。
  * `has()`: 查看 `Map` 中是否存在某个密钥。
  * `clear()`：从 `Map` 中移除所有密钥-值点对。

请注意，Maps 和 Sets 都有 `size` 属性，该属性返回其中唯一元素的数量。

**WeakMaps**

* `WeakMap` 是一个键值点对的集合，就像 `Map` 一样，但对键使用弱引用。键必须是对象，值可以是你喜欢的任何内容。

**区别**

* WeakMap 类似于 WeakSet，因为它们只保存对象，并且对这些对象的引用是“弱引用”。

### 变量

**直接量**

直接量包含number、boolean、string、null、undefined、Object、Class

let 变量 = 直接量

|               特性               |                var                |                      let                      |
| :------------------------------: | :--------------------------------: | :--------------------------------------------: |
|              作用域              |             函数作用域             |                   块级作用域                   |
|             提升行为             |  提升至作用域顶部，值为 undefined  | 提升至作用域顶部，但存在 “暂时性死区”（TDZ） |
|             重复声明             |   允许在同一作用域内重复声明变量   |        不允许在同一作用域内重复声明变量        |
| 全局对象属性（window 或 global） | 在全局作用域中，成为全局对象的属性 |     在全局作用域中，不会成为全局对象的属性     |

**命名规范**

```ts
//布尔命名：对于布尔变量，通常的做法是使用诸如 "is"、"has" 或 "can" 之类的前缀。
//命名函数：对于函数，名称应清楚地表明函数的作用。对于返回布尔值的函数（通常称为判断式），你可以使用相同的 "is"、"has" 或 "can" 前缀。当你有获取数据的函数时，通常以 "get" 开头。当你有设置数据的函数时，通常以 "set" 开头。对于事件处理函数，你可以使用 "handle" 作为前缀或使用 "Handler" 作为后缀。
```

```ts
//JavaScript 在[数学操作]中将 null 视为 0，将 undefined 视为 NaN
console.log(null == undefined); // true
console.log(null == 0); // false
console.log(undefined == NaN); // false
console.log(null === undefined); // false

let a = 1
let b
let sum = (b = a++ + --a) + a-- + b++
//b = 1 + 1 = 2
//sum = 2 + 1 + 2 = 5
```

#### String

```ts
//charCodeAt()和 fromCharCode()
const letter = "A";
console.log(letter.charCodeAt(0));  // 65

const char = String.fromCharCode(65);
console.log(char);  // A

//使用 String 构造函数创建的，它将原语值包装在一个对象中
const greetingObject = new String("Hello, world!");
console.log(typeof greetingObject); // "object"

//转字符串
num.toString()   //转字符串
num.toString(2)   // 转二进制字符串
num.toFixed(2)   //保留两位小数
JSON.stringify(obj)   //json -> str

//concat (多个字符串的拼接)
let str1 = 'Hello';
let str2 = 'World';
let result = str1.concat(' ', str2);   // Hello World

result.indexOf("Hello")   //0
result.includes("Hello")   //true
result.slice(0, 5)   //"Hello"

let li = result.split(" "); // ["hello", "world"]
let newS = li.join(" "); // "hello world"

//trim() 方法：该方法用于删除字符串首尾的空白。
//toUpperCase() 方法：该方法将所有字符转换为大写字母，并返回一个包含所有大写字母的新字符串。
//toLowerCase() 方法：该方法将所有字符转换为小写字母。
```

**高级技巧**

```ts
//replace、replaceAll
//正则表达式 /hello/gi ，其中 g 表示全局匹配（替换字符串中所有匹配项）， i 表示不区分大小写。
let str = "Hello World, hello earth.";
let modifiedStr = str.replace(/hello/gi, "");   // " World, earth."
'abcabc'.replace('a', 'A')   //'Abcabc'

//splice(仅支持数组)
let originalString = "hello world";
let splitString = originalString.split(" "); // ["hello", "world"]
splitString.splice(1, 0, "beautiful"); // ["hello", "beautiful", "world"]
let newString = splitString.join(" "); // "hello beautiful world"

//得到字符串含有某个字符的个数
var count=str.split(char).length-1; //数组的长度减一
```

#### Number

​**定义**​：JavaScript 的 `Number` 类型包括整数、浮点数、`Infinity` 和 `NaN`。

```ts
//使用 Number构造函数创建的，它将原语值包装在一个对象中
const myNum = new Number("34");
console.log(typeof myNum); // "object"

//转数字
parseInt(str)
parseFloat(str)
Number(str)
```

```ts
// 传统 isNaN 的陷阱（会进行类型转换）
console.log(isNaN("123"));     // false（字符串可转为数字123）
console.log(isNaN("Hello"));   // true（字符串无法转为数字）
console.log(isNaN(undefined)); // true（转为数字是NaN）
console.log(isNaN(NaN));       // true

// ES6 的严格检测（推荐用法）
console.log(Number.isNaN("Hello"));    // false（非NaN类型）
console.log(Number.isNaN(NaN));        // true
console.log(Number.isNaN(0 / 0));      // true（计算结果为NaN）
console.log(Number.isNaN(+"abc"));     // true（显式转换失败）

// 手动实现 Number.isNaN 的 Polyfill
if (!Number.isNaN) {
  Number.isNaN = function(value) {
    return typeof value === 'number' && value !== value;
  };
}
```

### List

#### 基本函数

```ts
//创建数组
let arr = new Array()
let arr = new Array(5)   //[empty × 5]
let arr1 = ['first', 'second']
let arr2 = new Array('first', 'second')
//增加删除
list.push()       //结尾新增（返回值：数组的长度）
list.unshift()   //开头新增（返回值：数组的长度）
list.shift()       //开头删除（返回值：删除的项）
list.pop()       //结尾删除（返回值：删除的项）
//操作数组
list.includes("first")    // 是否包含特定值（返回值：Boolean）
list.reverse()    //反转数组
newList = list.concat("Perl")      //合并多个数组来创建一个新数组
//截取数组
//list.slice(起始位置, 结束位置)   返回新数组
var a = [1,2,3,4,5]; //定义数组
var b = a.slice(2,5); //截取第三个元素到第六个元素前的所有元素。 返回[3,4,5]
var b = a.slice(2); //截取数组中第三个元素，以及后面所有元素。 返回[3,4,5]
var b = a.slice(-4,-2); //截取倒数第四个元素到倒数第二个元素前的元素。 返回[2,3]
//替换数组
//list.splice(起始位置，删除的个数，新增元素1，新增元素2，...)
list.splice(2,1)   //删除下标为2的元素
list.splice(2,0,'item')   //新增'item'元素到下标为2的位置
list.splice(2,1,'item')   //替换下标为2的元素为'item'

//sort()函数修改原数组
//sort() 默认将元素转换为字符串后进行比较，这可能导致数值排序不符合预期。
let arr = [3, 17, 9]
arr.sort()  //17,3,9
arr.sort((a, b) => {
  return a-b // 升序  3,9,17
})

//解构赋值
let [var1, var2, ...rest] = array
//解构语法实现快速交换
[arr[i], arr[j]] = [arr[j], arr[i]];
//等价于临时变量法
const temp = arr[index1];
arr[index1] = arr[index2];
arr[index2] = temp;

//稀疏数组
//定义：数组中可以有空槽。空槽被定义为其中没有任何内容的槽。这不同于值为 undefined 的数组槽。这类数组被称为稀疏数组。
const sparseArray = [1, , , 4];
console.log(sparseArray.length); // 4
```

#### 数组查询

|方法|描述|参数|返回值|
| --- | --- | --- | --- |
|`indexOf()`|搜索数组中的元素，并返回它所在的位置。|要搜索的元素 ，查找的起始位置|元素第一次出现的`索引`|
|`lastIndexOf()`|搜索数组中的元素，并返回它最后出现的位置|要搜索的元素 ，查找的起始位置|元素最后一次出现的`索引`|
|`includes()`|判断一个数组是否包含一个指定的值	|要查找的元素值|`Boolean`|
|`find()`|返回符合传入测试（函数）条件的数组元素|函数,this|符合条件的第一个元素的`值`|
|`findIndex()`|返回符合传入测试（函数）条件的数组元素索引|函数，this|符合条件的第一个元素的`索引`|
|`every()`|检测数值元素的每个元素是否都符合条件|函数，this|元素的`值`|
|`some()`|检测数组元素中是否有元素符合指定条件|函数，this|元素的`值`|
|`filter()`|检测数值元素，并返回符合条件所有元素的数组|函数，this|`数组`|

#### 遍历数组

```ts
//forEach   遍历数组   无返回值

//map  返回值：数组   作用：对数组中的每个元素进行转换
const numbers = [1, 2, 3, 4, 5];
const newNumbers = numbers.map((item, index, arr) => {
    return number * 2;
});

//every   用于判断数组中的每一项元素是否都满足条件，返回一个布尔值
var isEvery = arr.every(function(item,index,array){
    return item > 0;   // false
});

//some   用于判断数组中的是否存在满足条件的元素，返回一个布尔值
var isSome = arr.some(function(item,index,array){
    return item < 0;   //true
});

//find   用于查找数组中符合条件的第一个元素，如果没有符合条件的元素，则返回undefined
let num = arr1.find(item => item > 1);
let obj = arr.find(item => item.id == 1);   // 结果：{id: 1, name: '张一', age: 25, class: '一班'}

//filter  返回值：数组   作用：筛选出满足条件的元素
const numbers = [1, 2, 3, 4, 5];
const filteredNumbers = numbers.filter(number => number > 3);
console.log(filteredNumbers); 

//reduce  参数：回调函数、初始值   作用：将数组元素汇总为单个值
//优化建议:Reduce 回调函数缺少 return 关键字会导致逻辑中断。
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((prev,cur,index,arr) => {
  return prev + cur
}, 0);
console.log(sum); 

//reduceRight
//该方法用法与reduce()其实是相同的，只是遍历的顺序相反，它是从数组的最后一项开始，向前遍历到第一项。
```

#### 数组拷贝

```ts
//共享引用问题：直接赋值后，新数组变量只是原数组的“别名”，修改新数组会直接影响原数组。这是因为JavaScript对数组的赋值操作是引用传递，而非值传递
const oldArr = [1, 2, 3];
const newArr = oldArr; // 直接赋值
newArr.push(4); // 修改新数组
console.log(oldArr); // 输出 [1, 2, 3, 4] — 原数组被意外修改

//深层问题：如果数组包含嵌套对象或特殊类型（如函数、日期），直接赋值无法解决深层数据共享问题，需深拷贝

//浅拷贝
//扩展运算符（...）
const oldArr = [1, 2, 3];
const newArr = [...oldArr]; // 浅拷贝
newArr.push(4);
console.log(oldArr); // 输出 [1, 2, 3] — 原数组未变[^2]

//slice() 或 concat() 方法：效果类似扩展运算符。
const newArr = oldArr.slice(); // 浅拷贝

//深拷贝
//JSON.parse(JSON.stringify())：简单但有限制（如丢失函数、日期对象转为字符串）。
const oldArr = [{name: "Alice"}];
const newArr = JSON.parse(JSON.stringify(oldArr)); // 深拷贝
newArr[0].name = "Bob";
console.log(oldArr[0].name); // 输出 "Alice" — 原数组未变

//使用库函数或自定义方法：处理复杂场景（如Lodash的_.cloneDeep()）。
// 示例：简单深拷贝函数（支持基本嵌套）
function deepCopy(arr) {
  return arr.map(item => Array.isArray(item) ? deepCopy(item) : item);
}
```

#### 二维数组

```ts
//创建二维数组
const transposed = new Array(n).fill(0).map(() => new Array(m).fill(0));
```

**原地翻转**

```ts
[matrix[i][j], matrix[j][i]] = [matrix[j][i], matrix[i][j]];

// 伪代码解析
const temp = [matrix[j][i], matrix[i][j]]; // 创建临时数组
matrix[i][j] = temp[0]; // 赋值为[j][i]
matrix[j][i] = temp[1]; // 赋值为原[i][j]
```

* ​**功能**​：通过解构赋值（Destructuring Assignment）交换矩阵中 `(i,j)` 和 `(j,i)` 位置的元素
* ​**关键点**​：
  * 右侧创建临时数组 `[matrix[j][i], matrix[i][j]]`
  * 左侧按序赋值：`matrix[i][j] = 临时数组[0]`, `matrix[j][i] = 临时数组[1]`

### Object

#### 基本函数

```ts
let container = {
  caoyao: '草药'
}
let key = 'caoyao'
console.log(container.caoyao)
console.log(container[key])  //[]可放字符串和变量
console.log(container['caoyao'])
//删除
delete container .caoyao;   //undefined

//解构赋值
let {prop1, prop2, ...} = object
//解构重命名
let { name: personName, age: personAge } = person;
//解构默认值
let { name, age, country = "Unknown" } = person;
//嵌套解构
const { ingredients: { flour } } = recipe;
const flour = recipe.ingredients.flour;   //等同于
```

**查看对象是否具有属性**

```ts
//如何检查对象中键是否存在
//in (注意：in 操作符不仅会检查对象本身的属性，还会检查它继承的属性（原型链 上的属性）。因此，如果您只想检查对象本身的属性，in 操作符可能无法满足您的需求。)
//注意：“caoyao”要加引号
console.log("caoyao" in container); // true

//hasOwnProperty (hasOwnProperty 方法只检查对象本身的属性，不会 沿着原型链去查找继承的属性)
//注意：“caoyao”要加引号
console.log(container.hasOwnProperty("caoyao")); // true

//hasOwn (查看对象是否拥有某个自身（非继承）属性的方式。它比 hasOwnProperty() 更安全，也比在值可能为 0、false、null 或 undefined 时使用 if (obj.prop) 更可靠)
//注意：“caoyao”要加引号
console.log(Object.hasOwn(container, "caoyao"))

//可选链[?.]   先[?]后[.]
console.log(container?.caoyao); // "草药"
console.log(container?.name); // undefined
console.log(!!container?.address); // false
```

**处理 JSON**

```ts
const user = {
  name: "John",
  age: 30,
  isAdmin: true
};

const jsonString = JSON.stringify(user);   // '{"name":"John","age":30,"isAdmin":true}'

const userObject = JSON.parse(jsonString);   // result: { name: 'John', age: 30, isAdmin: true }
```

#### Object与Map的区别

1. **键的类型不同**
   * ​**对象(Object)**​：键只能是字符串（String）或Symbol类型。如果使用非字符串键（如数字或对象），JavaScript会自动将其转换为字符串。例如，`{1: 'a'}` 中的键 `1` 会被转换为字符串 `'1'`。
   * ​**Map**​：键可以是任意数据类型，包括对象、函数、数字、布尔值等。这使得Map更灵活，例如可以存储对象作为键：`map.set({}, 'value')`。Map的这种设计避免了键的隐式转换问题​​。
2. **键的顺序保证**
   * ​**对象**​：在ES6之前，对象的属性顺序是不确定的；ES6及之后版本保留了字符串键的插入顺序，但Symbol键的顺序仍不保证。整体上，迭代时顺序可能不可靠。
   * ​**Map**​：严格保留键值对的插入顺序，迭代时（如使用 `for...of` 循环）顺序与添加顺序一致。这在需要顺序处理的场景中非常有用​。
3. **大小(size)的获取方式**
   * ​**对象**​：没有内置属性获取大小，需要手动计算，例如 `Object.keys(obj).length`，这在大型对象中可能影响性能。
   * ​**Map**​：提供 `size` 属性，可直接获取键值对数量（如 `map.size`），操作高效且直观​。
4. **迭代和遍历方式**
   * ​**对象**​：迭代较复杂，需使用 `Object.keys()`、`Object.values()` 或 `Object.entries()` 方法转换为数组后再迭代。不支持直接的迭代器接口。
   * ​**Map**​：内置迭代器，可直接用 `for...of` 循环遍历，或使用 `map.forEach()` 方法。Map实现了 `Iterable` 接口，简化了遍历过程。
5. **性能差异**
   * 两者在键值访问上通常都有 O(1)O(1) 的时间复杂度（即恒定时间访问），但Map在频繁添加/删除键值对时更高效，因为对象可能触发原型链查找或内存重分配。对象在访问键时具有 O(1)O(1) 访问时间，但Map在动态操作中优化更好​。
   * Map对特殊值（如 `NaN`）的处理更一致：Map视 `NaN` 为相等（只能存在一个），而对象会将 `NaN` 键转换为字符串 `'NaN'`，可能导致重复键问题​。
6. **默认键和原型链影响**
   * ​**对象**​：可能继承原型链上的属性（如 `Object.prototype`），导致意外键冲突。例如，`obj.toString` 可能来自原型而非自定义值。
   * ​**Map**​：无原型链污染，键值对完全独立，更安全。
7. **JSON兼容性**
   * ​**对象**​：可直接与JSON互转，使用 `JSON.stringify()` 和 `JSON.parse()`，方便数据序列化​​。
   * ​**Map**​：不能直接序列化为JSON，需要手动转换为对象或数组，增加了额外处理步骤​。

​**总结**​：

* 使用​**对象**​：适合简单键值存储、JSON交互或当键是字符串/Symbol时。例如，配置对象或数据传输。
* 使用​**Map**​：适合键类型多样、需要严格顺序、频繁增删或避免原型链问题的场景。例如，缓存机制或复杂状态管理。
  选择时，考虑键的灵活性和操作需求：Map在现代化应用中更强大，但对象在兼容性和简单场景中仍占优。

#### 装箱拆箱

![image](https://wiki.huawei.com/vision-file-storage/api/file/download/upload-v2/WIKI2026041510777489/42141561/e0bd1783da4749aa987dbc6126250259.png)

```csharp
//C# 只针对值类型，引用类型转换不触发装箱拆箱；拆箱是值拷贝，不是直接引用堆内存
//使用泛型集合（如C#的List<T>或Java的ArrayList<Integer>），避免使用非泛型集合（如ArrayList），因为后者在存储值类型时会强制装箱。
int a = 10;       // 值类型在栈
object b = a;     // 装箱：a的值被复制到堆中，b引用堆对象
Console.WriteLine($"{a}--{b}"); // 输出: 10--10

object obj = i;    // 假设i已装箱
int c = (int)obj;  // 拆箱：obj的值被复制到c
Console.WriteLine(c); // 输出: 10
```

### 条件判断

```ts
//三元运算符
let str = true ? 'sunny' : 'cool';

//二元逻辑运算符
const result = true && 'hello';   // hello
//空值合并（??）运算符：只有当第一个值为 null 或 undefined 时，该运算符才会返回一个值。
const userSettings = {
 theme: null
};
let theme = userSettings.theme ?? 'light';   // light
```

### 循环

```ts
//for循环

//传统for循环：i 是 number
for (var i = 0; i < arr.length; i++) {}

//for…in循环：i 是 key、index(string类型)   //适合遍历对象
for (var i in arr) {}

//for…of循环：i 是 item
for (var i of arr) {}
```

### Function

#### 函数式编程

**纯函数**
指在给定相同 `input` 时，总是返回相同输出且不会修改自身之外任何内容的函数。

```ts
//纯函数
function add(a, b) {
  return a + b;
}

//非纯函数
let total = 0;
function addToTotal(value) {
  total += value;
  return total;
}
```

**副作用**
指在调用函数时程序状态中发生的任何变化。这可能包括`修改全局变量`、`写入文件`或`进行 API 调用`。

```js
//有副作用
function greet(name) {
  console.log(`Hello, ${name}!`);
}

greet("Alice");
//无副作用
function greet(name) {
  return `Hello, ${name}!`;
}
console.log(greet("Alice"));
```

#### 函数柯里化

柯里化是一种技术，我们将一个接受多个参数的函数转换为一系列函数，每个函数只接受一个参数。

* 当处理接受多个参数的函数时，柯里化尤其强大。
* 柯里化使你的代码更灵活且更易于重用。
* 你可以使用箭头函数更简洁地创建柯里的函数：

```js
function add(a, b) {
  return a + b;
}

console.log(add(3, 4)); // 7
```

这是一个接受两个参数并返回它们和的函数。现在，让我们看看如何对这个函数进行柯里化：

```js
function curriedAdd(a) {
  return function(b) {
    return a + b;
  }
}

console.log(curriedAdd(3)(4)); // 7
```

在这个柯里转换的代码中，我们不是一次接受两个参数，而是有一个函数接受第一个参数并返回另一个函数。这个返回的函数随后接受第二个参数并执行加法。我们像 `curriedAdd(3)(4)` 这样调用它，其中每对括号表现一次函数调用。

但是为什么我们要这样做？

柯里化使我们能够轻松创建一些特殊的函数。例如，我们可以创建一个函数，总是将五添加到任何数字上：

```js
function curriedAdd(a) {
  return function(b) {
    return a + b;
  }
}

const addFive = curriedAdd(5);
console.log(addFive(10)); // 15
console.log(addFive(20)); // 25
```

这里，`addFive` 是一个函数，它总是准备好为我们提供的任何数字添加五。这是部分应用的一个简单示例，我们将一定数量的参数固定到一个函数上，从而生成一个接受更少参数的函数。

虽然我们的示例集中在具有两个参数的函数上，但柯里化可以应用于具有任意数量参数的函数。

#### arguments

```ts
//arguments
function add() {
  let sun = 0
  for(let i = 0; i < arguments.length; i++) {
    sum += arguments[i]
  }
  return sum
}
```

#### 闭包

```ts
//基本使用
function outerFunction(x) {
let y = 10;
  function innerFunction() {
    console.log(x + y);
  }
  return innerFunction; 
}
let closure = outerFunction(5);
closure(); // 15

//计数器
var createCounter = function(init: number) {
  let currentCount = init;
  return {
    increment: () => ++currentCount,   //加1
    decrement: () => --currentCount,   //减1
    reset: () => (currentCount = init),   //重置
  }
};

const counter = createCounter(5)
counter.increment(); // 6

//判断是否相等
type ToBeOrNotToBe = {
  toBe: (val: any) => boolean;
  notToBe: (val: any) => boolean;
};

const expect = (val: any): ToBeOrNotToBe => {
    return {
        toBe: (val2: any): boolean => {
            if(val !== val2) throw new Error("Not Equal");
            return true;
        },
        notToBe: (val2: any): boolean => {
            if(val === val2) throw new Error("Equal");
            return true;
        }
    };
};

 expect(5).toBe(5); // true
 expect(5).notToBe(5); // throws "Equal"
```

#### Promises

Promise 有三种状态：挂起（pending）、已完成（fulfilled）或拒绝（rejected）。

Promise 提供了像 `.then()` 和 `.catch()` 这样的方法来处理已解析的值或错误。

**async**：用于定义异步函数，确保函数始终返回一个 Promise。当在函数声明或函数表达式前使用 async 关键字时，它变成一个异步函数。请注意，从异步函数返回的非 Promise 对象会自动包装成 Promise 对象。

**await**：用于暂停异步函数的执行，直到 Promise 解析。它只能在异步函数内部使用。当在 Promise 之前使用 await 时，它等待 Promise 解析或拒绝。如果已解析，它继续执行下一行代码；如果等待的 Promise 被拒绝，将抛出异常。使用 await 允许您以更顺序且可读的方式编写异步代码，而无需使用 .then() 显式链接 Promise。

```ts
new Promise((resolve,reject) => {
  resolve('响应结果'); //这里调resolve方法，则then方法会被调用
  console.log('resolve里面的log');
})
```

```ts
// 使用 promises 和显式的 .then() 和 .catch()
fetchData()
  .then(response => {
    // 处理响应
    console.log("响应：", response);
    return processData(response);
  })
  .then(result => {
    // 处理处理后的数据
    console.log("处理后的数据：", result);
  })
  .catch(error => {
    // 处理任何错误
    console.error("错误：", error);
  });

// 使用 async/await
async function fetchDataAndProcess() {
  try {
    const response = await fetchData();
    console.log("响应：", response);

    const result = await processData(response);
    console.log("处理后的数据：", result);
  } catch (error) {
    console.error("错误：", error);
  }
}

fetchDataAndProcess();
```

```ts
//Promise.all
const [res1, res2] = await Promise.all([promise1, promise2]);

//await
return await promise1 + await promise2;
```

#### Time

```ts
setTimeout 只在延迟后执行一次，而 setInterval 会每隔指定时间重复执行。
两者都会返回一个定时器 ID，分别配合 clearTimeout 和 clearInterval 来取消定时。
```

```ts
//setTimeout
function delayedFunction() {
  console.log("延迟函数执行！");
}
const delay = 2000;
const timerId = setTimeout(delayedFunction, delay);

// 在延迟到期之前取消执行：
clearTimeout(timerId);
```

### Class

```ts
//super
class FilledRectangle extends RectangleSize {
  color = ''
  constructor (h: number, w: number, c: string) {
    super(h, w); // 父类构造函数的调用
    this.color = c;
  }

  draw() {
    super.draw(); // 父类方法的调用
    /* 填充矩形 */
  }
}
```

#### 静态方法和静态属性

* ​**静态方法**​：这些方法通常用于不需要访问对象特定状态的实用函数。它们定义在类中以封装相关功能性。

```js
class Movie {
  constructor(title, rating) {
    this.title = title;
    this.rating = rating;
  }

  static compareMovies(movieA, movieB) {
    if (movieA.rating > movieB.rating) {
      console.log(`${movieA.title} has a higher rating.`);
    } else if (movieA.rating < movieB.rating) {
      console.log(`${movieB.title} has a higher rating.`);
    } else {
      console.log("These movies have the same rating.");
    }
  }
}

let movieA = new Movie("Movie A", 80);
let movieB = new Movie("Movie B", 45);

Movie.compareMovies(movieA, movieB);  // Movie A has a higher rating.
```

静态方法对于实现“工厂”方法也很有帮助。工厂方法是你在构造函数之外定义的一个方法，用于根据特定条件创建对象。

```js
class Pizza {
  constructor(type, price) {
    this.type = type;
    this.price = price;
  }

  static createMargherita() {
    return new this("Margherita", 6.99);
  }
}

let myPizza = Pizza.createMargherita();
console.log(myPizza);  // Pizza { type: "Margherita", price: 6.99 }
console.log(myPizza.type);  // Margherita
```

* ​**静态属性**​：这些属性用于定义与类本身关联的值或属性，而不是与类的实例关联。静态属性在类的所有实例之间共享，并且可以在不创建类实例的情况下访问。

```ts
class Car {
  // Static property
  static numberOfWheels = 4;

  constructor(make, model) {
    this.make = make;
    this.model = model;
  }

  // Instance method
  getCarInfo() {
    return `${this.make} ${this.model}`;
  }

  // Static method
  static getNumberOfWheels() {
    return Car.numberOfWheels;
  }
}

// Accessing static property directly from the class
console.log(Car.numberOfWheels);  // 4
```

### 持久存储

* ​**定义**​：持久存储指的是一种保存数据的方式，即使断电或设备重启后数据仍然可用。

#### `localStorage` 和 `sessionStorage` 属性

* ​**Web Storage API**​：该 API 为浏览器提供了一种机制，可以在浏览器内直接保存键值对，允许开发者存储可跨不同页面重载和会话使用的信息。Web Storage API 的两个主要组件是 `localStorage` 和 `sessionStorage` 属性。
* `localStorage` 属性​：`localStorage` 是 Web Storage API 的一部分，允许数据即使在浏览器窗口关闭或页面刷新后仍然保持持久。该数据将一直可用，直到被应用或用户显式移除。
* `localStorage.setItem()` 方法​：此方法用于在 `localStorage` 中保存一个密钥-值对。

```js
localStorage.setItem('username', 'Jessica');
```

* ​`localStorage.getItem()` 方法​：此方法用于从 `localStorage` 中检索给定密钥的值。

```js
localStorage.setItem('username', 'codingRules');

let username = localStorage.getItem('username');
console.log(username); // codingRules
```

* `localStorage.removeItem()` 方法​：此方法用于通过其密钥从 `localStorage` 中移除特定项。

```js
localStorage.removeItem('username');
```

* ​`localStorage.clear()` 方法​：此方法用于清除 `localStorage` 中保存的所有数据。

```js
localStorage.clear();
```

* ​`sessionStorage` 属性​：存储仅在当前会话中存在的数据，浏览器标签（页）或窗口关闭时会被清除。
* ​`sessionStorage.setItem()` 方法​：此方法用于在 `sessionStorage` 中保存一个密钥-值点对。

```js
sessionStorage.setItem('cart', '3 items');
```

* ​`sessionStorage.getItem()` 方法​：此方法用于从 `sessionStorage` 中检索给定密钥的值。

```js
sessionStorage.setItem('cart', '3 items');

let cart = sessionStorage.getItem('cart');
console.log(cart); // '3 items'
```

* ​`sessionStorage.removeItem()` 方法​：此方法用于通过其密钥从 `sessionStorage` 中移除特定项。

```js
sessionStorage.removeItem('cart');
```

* ​`sessionStorage.clear()` 方法​：此方法用于清除存储在 `sessionStorage` 中的所有数据。

```js
sessionStorage.clear();
```

#### 使用 Cookie

* ​**定义**​：Cookie，也称为网页 Cookie 或浏览器 Cookie，是服务器发送到用户网页浏览器的小块数据。这些 Cookie 存储在用户设备上，并在后续请求中发送回服务器。Cookie 对于帮助网页应用维护状态和记住用户信息至关重要，这一点尤其重要，因为 `HTTP` 是无状态协议。
* ​**会话 Cookies**​：这些 Cookies 仅在用户在网站上的会话期间有效。一旦用户关闭浏览器或标签（页），会话 Cookie 就会被删除。这些 Cookies 通常用于保持用户在访问期间的登录状态等任务。
* ​**安全 Cookie**​：这些 Cookie 仅通过 `HTTPS` 发送，确保它们在传输过程中不会被攻击者截获。
* ​**HttpOnly Cookies**​：这些 Cookie 无法被浏览器中运行的 JavaScript 访问或修改，从而使它们在防范跨站脚本（XSS）攻击方面更安全。
* ​**Set-Cookie 头部**​：当你访问一个网站时，服务器可以在 HTTP 响应中发送一个 Set-Cookie 头部。该头部告诉你的浏览器储存一个包含特定信息的 cookie。例如，它可能保存一个唯一 ID，帮助网站在你下次访问时识别你。

你可以使用 `document.cookie` 在 JavaScript 中手动设置 cookie：

```js
document.cookie = "organization=freeCodeCamp; expires=Fri, 31 Dec 2021 23:59:59 GMT; path=/";
```

要删除 cookie，你可以将其过期时间设置为过去的某个时间。

```js
document.cookie = "username=; expires=Thu, 01 Jan 1970 00:00:00 GMT; path=/";
```

#### 其他

##### 增删改查（CRUD）

* ​**创建**​：这指的是创建新数据的过程。例如，在一个网页应用中，这可能是用户为博客添加新帖子的时候。
* ​**读取**​：这是从数据库中检索数据的操作。例如，当你访问博客文章或查看你的网站评测时，你正在执行读取操作以获取并显示保存在数据库中的数据。
* ​**更新**​：这涉及修改数据库中现有的数据。一个例子是编辑博客文章或更新你的评测信息。
* ​**删除**​：这是从数据库中移除数据的操作。例如，当你删除一篇博客文章或账户时，你正在执行删除操作。

##### HTTP 方法

* ​**定义**​：HTTP 代表超文本传输协议，它是网络上数据通信的基础。存在 HTTP 方法，用于定义可以在网络资源上执行的操作。常见的方法有 GET、POST、PUT、PATCH、DELETE。
* ​**`GET` 方法**​：这用于从服务器获取数据。
* ​**`POST` 方法**​：这用于向服务器提交数据，从而创建一个新资源。
* ​**`PUT` 方法**​：用于通过完全替换来更新资源。
* ​**`PATCH` 方法**​：用于部分更新资源。
* ​**`DELETE` 方法**​：用于从数据库中删除记录。

##### 缓存

* ​**定义**​：缓存是将文件副本存储在临时存储位置的过程，以便可以更快速地访问它们。Cache API 用于保存网络请求和响应，使网页应用更高效，甚至可以离线运行。它是更广泛的 Service Worker API 的一部分，对于创建能够在不可靠或缓慢网络条件下工作的渐进式网页应用（PWA）至关重要。

Cache API 是一种存储机制，用于存储 `Request` 和 `Response` 对象。当向服务器发出请求时，应用可以保存响应，并在以后从缓存中检索，而不是发出新的网络请求。这减少了装载时间，节省了带宽，并提升了整体用户体验。

* ​**缓存存储**​：用于保存超文本传输协议请求及其对应响应的键值点对。这使得能够高效地检索先前请求的资源，减少后续访问时从网络获取的需求，从而提升性能。
* ​**Cache-Control**​：开发者可以定义缓存资源应保留多长时间，以及是否应重新验证或直接从缓存中提供。
* ​**离线支持**​：通过使用 Cache API，你可以创建离线优先的网页应用。例如，当用户断开网络时，PWA 可以提供缓存的资源。

##### 负面模式和客户端存储

* ​**过度跟踪**​：指在没有明确、知情同意或合法需求的情况下，在客户端存储（例如 cookie、local storage 或 session storage）中收集和存储过多的用户数据的做法。这通常涉及跨多个站点或会话跟踪用户行为、偏好和交互，可能侵犯用户隐私。
* ​**浏览器指纹识别**​：一种基于设备和浏览器的独特特征来跟踪和识别单个用户的技术，而不是依赖于 cookie 或其他传统的跟踪方法。与存储在用户设备上的 cookie 不同，指纹识别涉及收集一系列信息，这些信息可用于创建用户浏览器会话的独特“指纹”。
* ​**在 LocalStorage 中设置密码**​：这看起来可能是一个更明显的负面模式，但在局部存储中设置任何敏感数据如密码都会带来安全性风险。局部存储未加密且可以轻松访问。因此，你绝不应该将任何类型的敏感数据保存其中。

##### IndexedDB

* ​**定义**​：IndexedDB（索引数据库） 用于在浏览器中保存结构化数据。它内置于现代网页浏览器中，允许网页应用高效地保存和获取 JavaScript 对象。

##### Service Worker

* ​**定义**​：Service Worker（缓存/服务工作者） 是一个在后台运行的脚本，独立于你的网页。它可以拦截网络请求，访问缓存，并使网页应用离线工作。这是渐进式网页应用的关键组件。

### 异步编程

* **同步的 JavaScript** 是循序执行的，并且在继续下一个操作之前会等待前一个操作完成。
* **异步的 JavaScript** 允许多个操作在后台执行而不会阻塞主线程。
* **线程** 是一条可以独立于主程序流程执行的指令序列。
* **回调函数** 是作为参数传递给其他函数的函数，并在操作完成后或作为事件的结果执行。

异步的编程通常涉及`回调`、`promise` 或 `async/await` 来处理非阻塞操作。

#### 定时器

* ​**setTimeout() 方法**​：此方法允许你延迟指定时间后执行一个操作。

```js
setTimeout(() => {
 console.log('This runs after 3 seconds'); 
}, 3000);
```

* ​**setInterval() 方法**​：此方法会以设定的间隔重复运行一段代码。由于`setInterval()`会在指定的间隔持续执行提供的函数，你可能想要停止它。为此，你必须使用`clearInterval()` 方法。

```js
setInterval(() => {
 console.log('This runs every 2 seconds');
}, 2000);

// Example using clearInterval
const intervalID = setInterval(() => {
 console.log('This will stop after 5 seconds');
}, 1000);

setTimeout(() => {
 clearInterval(intervalID);
}, 5000);
```

#### Promise

* **Promises** 是表现异步操作最终完成或失败及其结果值的对象。只有当 `async` 操作完成时，promise 的值才被知晓。
* 这是一个创建简单 `promise` 的示例：

```js
const promise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Data received successfully');
  }, 2000);
});
```

* `.then()` 方法用于 Promise 中指定当 Promise 完成时应发生的操作，而 `.catch()` 用于处理任何发生的错误。
* 下面是使用 `.then()` 和 `.catch()` 处理 Promise 的示例：

```js
promise
  .then(data => {
    console.log(data);
  })
  .catch(error => {
    console.error(error);
  });
```

在上述示例中，使用 `.then()` 方法记录从 Promise 接收到的数据，而使用 `.catch()` 方法记录发生的任何误差。

* ​**Promise 链式调用**​：Promise 的强大特色之一是我们可以将多个异步的操作串联在一起。每个 `.then()` 都可以返回一个新的 Promise，使你能够依次执行一系列异步的操作。
* 这是一个 Promise 链式调用的示例：

```js
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => {
    console.log(data);
    return fetch('https://api.example.com/other-data');
  })
  .then(response => response.json())
  .then(otherData => {
    console.log(otherData);
  })
  .catch(error => {
    console.error(error);
  });
```

在上述示例中，我们首先从一个 URL 获取数据，然后根据第一个响应从另一个 URL 获取数据，最后记录收到的第二个数据。

`catch` 方法会处理进程中发生的任何误差。这意味着你不需要为每个步骤添加误差处理器，这可以大大简化你的代码。

#### async/await

Async/await 使编写和读取异步的代码更容易，它是建立在 Promise 之上的。

* ​**async**​：`async` 关键字用于定义一个异步的函数。`async` 函数返回一个 Promise，该 Promise 会解析为 `async` 函数返回的值。
* ​**await**​：`await` 关键字用于 `async` 函数内部，暂停函数执行直到 Promise 被解析。它只能在 `async` 函数内部使用。
* 这是使用 `async/await` 的示例：

```js
async function delayedGreeting(name) {
  console.log("A Messenger entered the chat...");
  await new Promise(resolve => setTimeout(resolve, 2000));
  console.log(`Hello, ${name}!`);
}

delayedGreeting("Alice");
console.log("First Printed Message!");
```

在上述示例中，`delayedGreeting` 函数是一个 `async` 函数，它会暂停 2 秒钟，然后打印问候消息。`await` 关键字用于暂停函数执行，直到 `Promise` 被解析。

* `async/await` 最大的优势之一是通过 `try/catch` 块进行误差处理。以下是一个示例：

```js
async function fetchData() {
  try {
    const response = await fetch('https://api.example.com/data');
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

fetchData();
```

在上述示例中，`try` 块包含可能抛出误差的代码，而 `catch` 块在发生误差时处理该误差。这使得误差处理更加直接且易读。

#### 其他

##### JavaScript引擎

* **JavaScript 引擎** 是一个在网页浏览器中执行 JavaScript 代码的程序。它就像一个转换器，将你的代码转换成计算机能够理解并据此工作的指令。
* V8 是 Google 开发的一个 JavaScript 引擎示例。
* **JavaScript 运行器** 是执行 JavaScript 代码的环境。它包括处理和执行代码的 JavaScript 引擎，以及像网页浏览器或 Node.js 这样的附加特色。

##### Fetch

* Fetch API 允许网页应用发起网络请求，通常用于从服务器检索或发送数据。它提供了一个 `fetch()` 方法，你可以用来发起这些请求。
* 你可以使用 Fetch API 获取文本、图像、音频、JSON 和其他类型的数据。

**Fetch API 的超文本传输协议方法**

Fetch API 支持多种与服务器交互的超文本传输协议方法。最常用的方法有：

* ​**GET**​：用于从服务器检索数据。默认情况下，Fetch API 使用 `GET` 方法来检索数据。

```js
fetch('https://api.example.com/data')
```

要使用获取的 `data`，必须使用 `.json()` `method` 将其转换为 JSON 形式：

```js
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => console.log(data))
```

在这段代码中，来自 Fetch API 的响应是一个 promise，`.then` 处理器将响应转换为 JSON 形式。

* ​**POST**​：用于向服务器发送数据。`POST` 方法用于在服务器上创建新资源。

```js
fetch('https://api.example.com/users', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
  },
  body: JSON.stringify({
    name: 'John Doe',
    email: 'john@example.com'
  })
})
```

在这个示例中，我们正在发送一个 `POST` 请求以创建一个新用户。我们已将方法指定为 `POST`，设置了适当的头部，并包含了我们想要发送的数据体。体需要是一个字串，因此我们使用 `JSON.stringify()` 将我们的对象转换为 JSON 字串。

* ​**PUT**​：用于更新服务器上的数据。`PUT` 方法用于更新服务器上的现有资源。

```js
fetch('https://api.example.com/users/45', {
  method: 'PUT',
  headers: {
    'Content-Type': 'application/json',
  },
  body: JSON.stringify({
    name: 'John Smith',
    email: 'john@example.com'
  })
})
```

在此示例中，我们正在更新 URL 末尾指定的 ID `45`。我们在代码中使用了 `PUT` 方法，并且将数据指定为体，用于更新所识别的数据。

* ​**DELETE**​：用于删除服务器上的数据。`DELETE` 方法用于删除服务器上的资源。

```js
fetch('https://api.example.com/users/45', {
  method: 'DELETE'
})
```

在此示例中，我们发送一个 `DELETE` 请求以删除 ID 为 `45` 的用户。

##### async和defer

* `async` 属性告诉浏览器在继续解析超文本标记语言文档的同时异步地下载脚本文件。
* 脚本下载完成后，超文本标记语言解析暂停，脚本执行，然后超文本标记语言解析恢复。
* 你应该为执行顺序无关紧要的独立脚本使用 `async`

```
<script src="example.js" async></script>
```

* `defer` 属性也会异步地下载脚本，但它会推迟脚本的执行，直到超文本标记语言文档完全解析之后。
* `defer` 脚本维护它们在超文本标记语言文档中出现的执行顺序。
* 重要的是要注意，`async` 和 `defer` 两个属性都会被内联脚本忽略，仅对外部脚本文件有效。
* 当同时存在 `async` 和 `defer` 属性时，`async` 属性具有优先级。

```
<script src="example.js" defer></script>
```

##### 地理位置

* Geolocation API 提供了一种让网站请求用户位置的方法。
* 下面的示例演示了用于获取用户当前位置的 API `getCurrentPosition()` 方法。

```js
navigator.geolocation.getCurrentPosition(
  (position) => {
    console.log("Latitude: " + position.coords.latitude);
    console.log("Longitude: " + position.coords.longitude);
  },
  (error) => {
    console.log("Error: " + error.message);
  }
);
```

在这段代码中，我们调用 `getCurrentPosition` 并传入一个函数，该函数将在成功获取位置时被调用。

`position` 对象包含各种信息，但这里我们只选择了 `latitude` 和 `longitude`。

如果获取 `position` 出现问题，则该误差将被记录到控制台日志中。

* 尊重用户的隐私非常重要，只有在必要时才请求他们的位置。
