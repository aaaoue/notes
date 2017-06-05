# 第三章： DOM
- DOM：文档document 对象object 模型model
- nodes： 元素节点、文本节点、属性节点、CSS
- DOM的基础操作： 获取元素、获取和设置属性
---

## 一、DOM

-  D→document，当创建了一个网页并把它加载到Web浏览器中，DOM就在幕后将你编写的网页文档转为一个文档对象。

-  O→object，对象，一种数据集合，相关联的变量是对象是的属性，只能通过特定对象调用的函数称为这个对象的方法。  
        2.1 JavaScript语言中对象可分为三类  
    - 用户定义对象： 程序员自行创建
    - 内建对象：内建再JS语言中，如Array、Math、Date
    - 宿主对象：由浏览器提供的对象

    - 补充： BOM与DOM

-  M→model
    - DOM把文档表示为一家谱树（节点数）,使用parents\child\sibling 等记号表明家族成员之间的关系

## 二、节点 nodes  
节点：共有三种类型

#### 元素节点 element node
- HTML标签的名字就是元素的名字，没有被包含在其他元素里的唯一元素是HTML元素，它是节点树的根元素

#### 文本节点 
- 文本节点总是被包含在元素节点的内部

#### 属性节点 attribute node
- 在html中，属性总是被放在起始标签里，所以所有属性节点总是被元素节点所包含

- 补充：注释属于注释节点

## 三、操作DOM
#### 获取元素  
document 对象特有的函数
1. getElementById('') 返回与 指定id属性值的 元素节点对应的 对象  ，注意该方法只会返回特定ID的第一个匹配节点

2. getElementsByTagName('') 返回 匹配指定标签的 元素节点对应的集合→数组
    - 该方法允许以通配符 * 作为参数。可以判断一个对象包含多少元素节点
    - 可以以 数组索引的方式访问 集合中的任意元素

3. getElementsByClassName('') 通过指定类名，返回与元素节点对应的 数组。
    - 指定多个class名时在字符串内以空格分割
    - HTML5 DOM 新增 有兼容问题

#### 获取/设置 属性

1.  获取getAttribute，设置setAttribute。只能通过 **元素节点** 调用
- element.getArribute() 只返回 字符串
- element.setArribute('属性名','值') 为当前元素新增属性，如过属性已存在则重新赋值 
