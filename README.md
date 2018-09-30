# se-hw1-vue_learning_report
#Vue.JS

##介绍
----
Vue (读音 /vjuː/，类似于 view) 是一套用于构建用户界面的渐进式框架。与其它大型框架不同的是，Vue 被设计为可以自底向上逐层应用。Vue 的核心库只关注视图层，不仅易于上手，还便于与第三方库或既有项目整合。另一方面，当与现代化的工具链以及各种支持类库结合使用时，Vue 也完全能够为复杂的单页应用提供驱动

----
###模板语法

在vue中，常见到的是指令<br>
1.v-bind 指令被用来响应地更新 HTML 属性<br>
2.v-html 指令用于输出 html 代码<br>
3.v-on 指令，它用于监听 DOM 事件<br>
4.v-model 指令可以使用来实现双向数据绑定

###条件与循环

条件判断 在元素 和 template 中使用 v-if 指令：<br>
v-else与v-else-if 类似c++中用法<br>
**v-show 与 v-if 区别：在需要大量输入渲染时，选择v-show<be>**

###循环 
v-for 指令需要以 site in sites 形式的特殊语法， sites 是源数据数组并且 site 是数组元素迭代的别名。<br>
v-for 可以循环整数，列表，也可以是属性。

###计算属性

例子：reversedMessage

###监听属性

我们可以通过 watch 来响应数据的变化。<br>

侦听属性 vs 计算属性。当你有一些数据需要随着其它数据变动而变动时，你很容易滥用 watch——特别是如果你之前使用过 AngularJS。然而，通常更好的做法是使用计算属性而不是命令式的 watch 回调。

----

###样式绑定

####class 属性绑定
我们可以为 v-bind:class 设置一个对象，从而动态的切换 class:，也可以吧数组传给 class<br>
Vue.js style(内联样式)<br>
也可以在 v-bind:style 直接设置样式：<br>

###时间处理器 v-on

Vue.js 为 v-on 提供了事件修饰符来处理 DOM 事件细节<br>
***按键修饰符***<br>
Vue 允许为 v-on 在监听键盘事件时添加按键修饰符：<br>
全部的按键别名：
.enter
tab
.delete (捕获 "删除" 和 "退格" 键)
.esc
.space
.up
.down
.left
.right
.ctrl
.alt
.shift
.meta

###组件(component)
组件系统让我们可以用独立可复用的小组件来构建大型应用，几乎任意类型的应用的界面都可以抽象为一个组件树
 
####prop 是父组件用来传递数据的一个自定义属性。

父组件的数据需要通过 props 把数据传给子组件，子组件需要显式地用 props 选项声明 "prop"：
类似于用 v-bind 绑定 HTML 特性到一个表达式，也可以用 v-bind 动态绑定 props 的值到父组件的数据中。每当父组件的数据变化时，该变化也会传导给子组件：

###钩子函数


#####1、beforeCreate 钩子

   该阶段组件实例刚创建，组件属性计算之前（可理解为组件属性还未初始化，未绑定，未挂载元素el），比如：el，data，methods等，如果你试图在beforeCreated钩子中获取这些属性值，会得到ubdefined 的结果，但是

可以获取到this对象，因为此时组件刚被创建好，所以this已经引用了该组件对象。

#####2、created 钩子

 该阶段组件实例创建完成，组件属性绑定完成，但DOM还未生成，el属性还不存在

#####3、beforeMount 钩子

 该阶段组件实例已经创建完成，但是el还未挂载具体元素

#####4、mounted钩子

 该阶段组件实例已经创建完成，但是el 已挂载具体元素，此时的el属性不为undefined

 

#####5、Vue：router 的beforeEach 与afterEach 钩子函数

 在路由跳转的时候，我们需要一些权限判断或者其他操作。这个时候就需要使用路由的钩子函数。

定义：路由钩子主要是给使用者在路由发生变化时进行一些特殊处理而定义的函数

###过渡

6 class(1.v-enter 2.v-enter-active 3.v-enter-to 4.v-leave 5.v-leave-active 6.v-leave-to)

----

###not the end 9.30

