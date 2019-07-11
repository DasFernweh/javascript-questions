# javascript-questions
github上的js面试题总结  
参考的掘金文章https://juejin.im/post/5d0644976fb9a07ed064b0ca  
需要重复看的题目：`9` `10`、`11` `12` `12` `13` `14` `15` `16i` `17` `18` `20` `21` `22~43`   
第二次看仍需要看：10、11、12、13、16、17、20、21、28（重点看分析）、29？、31、34、35、38、42

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
    this指向它定义时所在的上下文环境/对象，而不是使用时所在的对象，与普通函数不同
    </code></pre>
    </details>  
  3. JavaScript的对象赋值  
        <details>
        <summary>答案</summary>
        <pre><code>
        js的对象赋值是引用，即令a=b，修改一个a的值，同时b也会变化，因为使用的是同意内存空间
        </code></pre>
        </details>  
  4. ES6类的静态方法  
        <details>
        <summary>答案</summary>
        <pre><code>
        <strong>静态方法只存在创建他们的构造函数中</strong>  
        他的实例对象是访问不到的
        </code></pre>
        </details>  
  5. 如何向构造函数添加属性  
        <details>
        <summary>答案</summary>
        <pre><code>
           构造函数添加属性需要通过原型来实现
        </code></pre>
        </details>  
  6. prototype模式  
        <details>
        <summary>答案</summary>
        <pre><code>
           js中每一个构造函数都有一个prototype属性，它指向另一个对象，这个对象的所有属性和方法，都可以被构造函数所继承
        </code></pre>
        </details>  
   7. 数字和字符串运算（加减）  
   
            console.log('----1----')   
            console.log('12' + '34')//'1234'    
            console.log('12' + 34 )//'1234'   
            console.log(12 + '34')//'1234'   
            console.log(12 + 34 )//46   
            console.log('----2----')   
            console.log(+'12' + '34')//'1234'   
            console.log(+'12' + 34 )//46   
            console.log(+12 + '34')//'1234'   
            console.log(+12 + 34 )//46   
            console.log('----3----')   
            console.log(-'12' + '34')//'-1234'   
            console.log(-'12' + 34)//22   
            console.log(-12 + '34')//'-1234'   
            console.log(-12 + 34)//22   
            console.log('----4----')   
            console.log('12' - '34')//-22   
            console.log('12' - 34)//-22   
            console.log(12 - '34')//-22   
            console.log(12 - 34)//-22   
            console.log('----5----')   
            console.log(+'12' - '34')//-22   
            console.log(+'12' - 34)//-22   
            console.log(+12 - '34')//-22   
            console.log(+12 - 34)//-22   
            console.log('----6----')   
            console.log(-'12' - '34')//-22   
            console.log(-'12' - 34)//-22   
            console.log(-12 - '34')//-22   
            console.log(-12 - 34)//-22   

   8. 后缀一元运算符和前缀一元运算符  
        <details>
        <summary>答案</summary>
        <pre><code>
            前缀：返回值：0，增加值1 （增加值比返回值多）  
            后缀：返回值与增加值相同
        </code></pre>
        </details>  
   9. 扩展运算符（...）返回什么类型，typeof（数组）返回什么  
        <details>
        <summary>答案</summary>
        <pre><code>
            返回一个带参数的数组，typeof（数组）返回object  
            所有的对象键都会被存为字符串，即使给定的键名不是字符串类型
        </code></pre>
        </details>  
   10. slice()和splice()区别  
        <details>
        <summary>答案</summary>
        <pre><code>
            slice(start,end): 取数组中从start开始到end结束中间的值，并返回一个新数组（相当于返回数组的一个子数组），不改变初始  
            数组  
            splice(start,howmany,item1,...itemX)：向数组中删除或添加指定值。start开始位置，howmany表示删除几个（如果为0  
            则表示不删除），item1,...itemX表示要添加的内容，<strong>返回一个新数组，会改变初始数组</strong>。如果start为负值，  则表示从数组尾部开始
        </code></pre>
        </details>  
   11. 对象有两个具有相同名称的键时怎么处理  
   12. js中的call、apply、bind的区别  
         三个函数的作用就是改变this的指向
         call():  
         apply():   
         bind():  
         call()和apply()区别：call和apply的区别在于传递的参数形式不同，call接受单个参数排列（多个参数），apply接受参数组成的数组。  
          ```
          fn.call(f1,a,b,c)
          fn.apply(f1,[a,b,c])
          ```
          call()和bind()区别：call和apply立即执行，bind返回一个函数在调用时执行
    13. 方法调用模式和函数调用模式  
        方法调用：如果一个函数被保存为一个对象的方法，执行表达式时有提取属性的操作，那么他就被当作一个方法来调用，此时的this绑定在这个对象上。  
        函数调用：  
        构造器调用模式：
    14. reduce()
    15. 有原型的对象和没有原型的对象  
    <details>
        <summary>答案</summary>
        <pre><code>
            创建有原型对象的三种方法：  
            var o = Object.create({})
            var o = {}
            var o = Object({})
            创建没有原型和构造函数的对象：
            var o = Object.create(null) // 注意Object(null)是有原型和原型链的    
            该对象的隐式原型和构造函数都返回undefined
            使用instanceof返回false
        </code></pre>
        </details>  
