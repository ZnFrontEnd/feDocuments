### 							call和apply的区别

**这两个东西是干嘛的？**

```html
在JavaScript中，`call`和`apply是`Function对象自带的方法，都是为了改变函数体内部this的指向。
```





**相同点：**

```html
apply 、 call 第一个参数都是 this要指向的对象，也就是想指定的上下文；

apply 、 call 都可以利用后续参数传参；
```





**不同点：**

```html
call参数单个传递，apply参数以数组形式传递。
```







```javascript
function add(c, d) {
return this.a + this.b + c + d;
}
const obj = { a: 1, b: 2 };
console.log(add.call(obj, 3, 4)); // 10
```



**call:**

```javascript
Function.prototype.es6Call = function (context) {
  var context = context || window;
  context.fn = this;
  var args = [];
  for (let i = 1; i < arguments.length; i++) {
    args.push(arguments[i] );
  }
  const result = context.fn(...args);
  return result;
}

console.log(add.es6Call(obj, 3, 4))
```





**apply:**

```javascript
Function.prototype.es6Apply = function (context, arr) {
  var context = context || window;
  context.fn = this;
  var result;
  if (!arr) {
     result = context.fn();
  } else {
    if (!(arr instanceof Array)) throw new Error('params must be array');
    result = context.fn(...arr);
  }
  delete context.fn;
  return result
}
console.log(add.apply(obj, [1, 2])); // 6
```





**实例1：**

```javascript
function fn1(){
   console.log(1);
}
function fn2(){
   console.log(2);
}
fn1.call(fn2);     //输出 1
fn1.call.call(fn2);  //输出 2

```

```html
1：把传入的第一个参数作为 call 函数内部的一个临时对象 context；

2：给 context 对象一个属性 fn ， 我称呼其为实际执行函数 context.fn ；让 this **关键字（仅仅是关键字，而不是this对象）**指向这个属性 ，即 context.fn = this ； **注意 ： 在这里的 this 对象指向的是调用call()函数的函数对象。**如 fn1.call(fn2)；在执行 call 函数时，call 函数内部的this指向的是fn1；然而 fn1.call.call(fn2)；在执行 call() 函数时（*注意这里必须是打了小括号“()”才算执行函数,fn1.call访问的是一个对象*），call函数内部的 this 指向的是 fn1.call 。

3：将传入call函数的其他参数，放入临时数组arr[]；

4：利用 eval执行 context.fn( [args] ) ； **实际就是执行 this( [args] )；****结合第2点。**

5：执行完成后再把 context.fn 删除。返回执行 **this( [args] )** 的结果。


首先 调用call 函数时，也就是 fn1.call.call(fn2)，先将 fn2 作为 临时的 context 对象 。然后 将 fn1.call这个函数对象作为 实际执行函数属性 ： context.fn = fn1.call；（注意：fn1.call会通过原型链找到最终的对象。其本质为 Function.prototype.call；） 然后检查其他参数，没有了。直接执行 fn1.call()函数 ,即 context.fn()；此时函数的本质还是 Function.prototype.call 函数对象。不过执行这个函数的环境还是在 Function.prototype.call()中，只不过是第一次调用的call()函数中。（第一次调用的call()函数将this关键字指向了 fn2） ；故而在fn1.call.call(fn2)函数中执行的 call函数执行过程中的 this指向的是 fn2；传入的参数为空，故而 新的 call()函数对象 的this关键字 被替换为window； 而执行 this()时，就是执行 fn2()；不涉及 this操作。故最终输出2。
```





**实例2：**

```javascript
function add (a, b) {
  console.log(a + b);
}

function sub (a, b) {
  console.log(a - b);
}

add.call(sub, 1, 1)
```

```html
call 就是中间牵线的，sub说 我需要 add 你的方法 和技能。

比如：add会飞天 ，但sub 不会飞，现在sub想飞，但add不让它飞，所以sub就叫来了 call 这个东西， call直接把add爆菊 。加上一个 点 然后把sub抱到括号里，然后 sub 就直接把add 的“飞天”技能学会了。


结果是 sub直接集成了 add 的“飞天”技能  sub alert里面 直接变成了 “a+b”！主角还是sub，并不是add ，你要搞清楚！
```









