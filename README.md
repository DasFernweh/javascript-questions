# javascript-questions
github上的js面试题总结  
参考的掘金文章https://juejin.im/post/5d0644976fb9a07ed064b0ca  
需要重复看的题目：`9` `10`、`11`

### 错误问题记录
1. var和let声明变量时的区别  
    <details>
    <summary>答案</summary>
    <pre><code>
    二者都会被变量提升，但是var在创建时即被初始化，所以提前console会显示undefined，而let只会被创建不会初始化，  
    所以提前输出会显示ReferenceError（暂时性死区）
    </code></pre>
    </details>  

 2. 箭头函数this的作用域是  
    <details>
    <summary>答案</summary>
    <pre><code>
    this指向它所在的上下文环境，与普通函数不同
    </code></pre>
    </details>  
  3.  JavaScript的对象赋值  
        <details>
        <summary>答案</summary>
        <pre><code>

        </code></pre>
        </details>  
  4. ES6类的静态方法  
  5. 如何向构造函数添加属性  
  6. prototype模式  
    <details>
    <summary>答案</summary>
    <pre><code>
       js中每一个构造函数都有一个prototype属性，它指向另一个对象，这个对象的所有属性和方法，都可以被构造函数所继承
    </code></pre>
    </details>  
  7. 
