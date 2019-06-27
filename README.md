# javascript-questions
github上的js面试题总结  
参考的掘金文章https://juejin.im/post/5d0644976fb9a07ed064b0ca  
需要重复看的题目：`9` `10`、`11` `12` `12` `13` `14` `15` `16i` `17` `18` `20` `21` `` `` 

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
    12. 
   
