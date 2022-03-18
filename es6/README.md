# ES6 基础

#### ES6 新增特性

- 新关键字 let const
- Promise
- 模板字符串
- class 关键字
- 箭头函数
- generator
- Map/Set
- 模块化
- 数组新方法

#### 暂时性死区

- 使用 let，cconst 声明的变量在声明前，变量是不可以进行访问的
- 访问则会出现 TDZ（temporal dead zone）暂时性死区

#### 箭头函数与普通函数的区别

- 箭头函数相对于普通函数书写比较简单
- 箭头函数是匿名的
- 箭头函数没有[[constructor]]方法，也即不能使用 new 关键字来创建对象
- 箭头函数是不绑定 arguments 对象
- this 的指向，箭头函数不绑定 this，当访问到 this 时会向上面的作用域去查找 this

#### promise(todo)

#### axios 的封装(todo)