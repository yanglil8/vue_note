## Vue

Vue(读音/vju:/，类似于 view）是一套用于构建用户界面的渐进式框架目前流行的框架 vue react 小程序

## 搭建 vue 开发环境

- 安装 node
- 安装 vue-cli(官方推荐的搭建 vue 项目开发环境的工具当前版本是 5.0.4)`npm i -g @vue/cli`，安装好了之后 vue 命令就可以使用了。
- 利用该工具搭建开发环境
- 使用 vue ui 命令调出创建开发环境的图形化界面工具(vue 项目管理器)，前提是 vuecli 的版本是 3+
  2．使用 vue 命令直接在命令行搭建项目。创建命令`vue create`项目名 -如何运行项目 -如果是使用 vue-cli 官方脚手架创建的项目环境，那么 package.json
  的 scripts 字段没有被修改的话，项目启动命令是
  `npm rum serve`，也可以使用 vue ui 启动可视化工具来启动项目，前提是 vuecli 版本是 3+
  ·不知道是怎么搭建的环境，直接去 package.json 找 scripts 字段，一般 serve 或者 start 命令就是启动项目命令。需要使用`npm run命令`启动。

### vue-cli 创建的项目的项目构成

README.md 项目的说明文档，创建时自带的
package.json 和 package-lock.json node 项目的标志

- 如果是使用 vue-cli 官方脚手架创建的项目环境，那么 package.json
  的 scripts 字段没有被修改的话，项目启动命令是
  `npm rum serve`，也可以使用 vue ui 启动可视化工具来启动项目，前提是 vuecli 版本是 3+
  ·不知道是怎么搭建的环境，直接去 package.json 找 scripts 字段，一般 serve 或者 start 命令就是启动项目命令。需要使用`npm run命令`启动。

### vue-cli 创建的项目的项目构成

- README.md 项目的说明文档，创建时自带的
- package.json 和 package-lock.json node 项目的标志，着重看 package.json 中的 scripts 字段- .gitignore 当你的项目是 git 仓库时，忽略上传的文件和文件夹都写在
  .ignore 内
- babel.config.js 是 js 编译(就是高版本的 js 编译成低版本的，比如 es6 +编译成 es5)的配置。

### 如何运行项目

- 如果是使用 vue-cli 官方脚手架创建的项目环境，那么 package.json 的 scripts 字段没有被修改的话，项目启动命令是`npmrum serve`，也可以使用 vue ui 启动可视化工具来启动项目，前提是 vuecli 版本是 3+
- 不知道是怎么搭建的环境，直接去 package.json 找 scripts 字段，一般 serve 或者 start 命令就是启动项目命令。需要使用'npm run 命令`启动。

### vue-cli 创建的项目的项目构成

- README.md 项目的说明文档，创建时自带的
- package.json 和 package-lock.json node 项目的标志，着重看 package.json 中的 scripts 字段- .gitignore 当你的项目是 git 仓库时，忽略上传的文件和文件夹都写在
  .ignore 内
- babel.config.js 是 js 编译(就是高版本的 js 编译成低版本的，比如 es6 ＋编译成 es5)的配置。- jsconfig.js 项目的 js 的配置文件。
- vue.config.js vuecli 的配置文件。- node_modules node 项目包存放的地方- public 项目的首页模版页面
- src 开发源代码，开发的主要工作。

### 单页面应用(SPA)

现在的框架基本上搭建出来的页面都是单页面应用(可以做多页应用).整个项目只有一个页面，利用框架的路由功能实现多页效果。

### src 文件夹

项目开发主要就在这个文件夹内。

- main.js 项目的入口文件 是 webpack 打包的文件
- App.vue vue 项目中都是以组件为基础组成页面,个组件就是页面中的一部分结构(包括 html css js)。
- components 其他组件
- assets 放图片 css 字体等资源

### 组件

.vue 后缀的就是组件，有三部分构成 template script style
template 只能有一个子级 里面可以嵌入 vue 语法
script 需要默认导出一个对象 对象内需要严格
style 就是样式但是样式是全局的(可能和其他组件的样式冲突）
组件名两种命名方式
1．首字母大写大驼峰方式比如 Helloworld.vue ShoppingCart.vue 2.烤串方式 比如 hello-world.vue
组件如何划分

### 组件的嵌套

- 在父组件中的 script 内导入需要使用的子组件(默认导入即可，导入的名字跟组件名一致)
- 在 script 默认导出的对象内，的 components 属性(该属性的属性值是一个对象)内注册子组件。就是写个属性属性值是组件(导入的那个)，属性名和组件名一致。
- 在 template 内使用 components 内注册好的属性名当成标签直接使用

### 组件的复用之 prop

当我们有些组件大部分一样，个别地方不一样，那么我们就需要针对个别的地方使用 prop
prop 就是一个组件标签的属性,作用是可以让父组件提供内容给子组件，让子组件更方便复用。比如替换图片文字等

### 模板语法

其实就是 js 怎么在 template 中使用,使用的时候必须是一个值
使用方式

- {{}}
  当你想要将 js 写在开始闭合标签之间的时候使用例如`<span>{{js内容}}<span>`
- 指令
  v-bind 指令 当你想要在属性值中使用 js 的话需要使用该指令．例如`<img v-bind:src="js内容'/>` 指令可以简写成 :

哪些 js 内容可以直接使用?
1．组件接收的 prop
使用的时候将本地(项目文件夹内的)图片当做 prop 写成路径使用的时候，vuecli 环境是无法解析的。只能解析原本 html 或者 css 原来自带的。那么需要使用网图或者将图片当作模块导入进来，然后制作成 data 再使用。导入的图片是可以被解析使用的
2．组件的 data
当页面的内容需要发生改变的时候(按照以前的说法要使用 js 控制页面变化的时候)，vue 中需要将这个变化的值定义为 data，并且将这个 data 绑定到 template 中，在 script 直接修改这个 data 页面自动回响应 data 的变化，从而更新页面内容

data 变页面变|页面的变化必须由 data 控制
data 可以直接在 template 中使用

# 组件中的 this

组件中的 this 指的就是组件实例，就是组件本身。
当函数内想要使用 this 表示组件本身的话，最外层函数需要写成普通函数，嵌套的内层函数需要写成箭头函数,或者在外层函数内定义变量存储 this 再拿到内层使用
通过 this 可以访问 data props methods 等
如何使用获取 data 1.在 tempalte 中直接使用模板语法就可以使用 data
2．在 script 中使用 this.data 名可以获取 data
如何修改 data
直接使用`this.data名=新的值`即可

### 事件处理

vue 中的事件绑定有点像原生的行内事件绑定在 vue 中使用 v-on 指令绑定事件例如

```html
<button v-on: click='事件名’>按钮</button>
v-on:可以简写成@
事件需要定义在 script导出的对象下的 methods属性内，methods属性的属性值是一个对象，该对象下的方法就是可以当做事件函数
```

```js
export default {
  methods: {
    myclick() {
      console.log(this.bgc);
      setTimeout(() => {
        console.log(this.title);
      }, 1000);
    },
  },
};
```
v-on:可以简写成@
事件需要定义在 script 导出的对象下的 methods属性内，methods属性的属性值是一个对象，该对象下的方法就是可以当做事件函数
```js
export default i
methods: {
myClick(){
console.log('啊哈哈哈哈哈')}
}}
```
-将函数调用写在事件内一般传递参数的时候才这样写
如何获取事件对象 event
-普通的事件绑定 @click='函数名’在函数内直接设置参数第一个参数就是事件对象
-直接写操作的话，操作内直接使用$event表示事件对象
-写成函数调用的话需要将参数$event在函数调用的时候传递
事件修饰符
- .stop阻止事件冒泡
- .prevent阻止默认行为
- .capture用的少
- .self当点击的那个真正的元素绑定了事件的话才会触发 .once只触发一次
- .passive
### class 与 style 绑定

vue 中提供了 class 与 style 的其他写法 
style 绑定
- 对象语法 就是将 style 的值写成对象，对象的属性名就是样式名，属性值就是样式的值。 一个样式写成一个对象
- 数组语法 就是将 style 的值写成数组，数组内写对象[对象,对象]用的很少

class 绑定
- 对象语法 就是将class的值写成对象，对象的属性名就是class 名，属性值是true class就生效
- 数组语法 就是将class的值写成数组，数组的一项就是class 名，默认直接生效.当数组的一项是’的时候，什么class都没有
- 数组对象语法 上面两个语法的组合 数组内可以使用对象语法
- 用在组件上 在父组件使用子组件的时候 传递 class 属性
### 条件渲染
###条件渲染
就是元素的消失和出现
两个指令的值都是布尔值，填写别的值会自动转化成布尔值，转化方式就是 Boolean1．样式的消失和出现使用v-show指令实现
2．结构的消失和出现使用v-if 指令实现v-else v-else-if
v-show和v-if 的区别
v-show 用于切换次数较多的功能，并且 v-show的元素上来无论是什么状态都会渲染出来
v-if 用于切换次数较少的功能，并且初始状态为false 的话，那么不会渲染任何元素在浏览器中
v-if可以在 template标签上使用，也可以直接在组件上使用
v-show也可以在组件标签上
### 22
- metods 内的函数可以当做事件函数
- vue tempalte中的事件绑定
1．@事件名='函数名'这个函数就是事件函数
2．@事件名= '函数()'这个函数就不是事件函数了，就是普通函数，需要用事件对象的需要传递参数，vue 中的事件对象使用$event表示
### 列表渲染
- 当使用v-for的时候必须添加key 而且每一个key的值是不同的在当前v-for中 key 不能相同
### 表单的输入绑定
vue中用户在表单中输入内容也认为是页面发生改变，那么这个改变就需要使用data 去控制。
input:text以及textarea的数据绑定
### vue中的各种数据在tempalte中和 script如何使用数据包括 data props methods
在tempalte中直接使用其名字即可
在 script中需要使用this.名字获取。需要注意 this的指向 
### Vue指令
- 指令 是模板语法 辅助开发者渲染页面的基本结构
- 按照不同的用途
- 内容渲染指令
- v-test {{}} v-html 
v-text 有内容覆盖的问提
- 属性绑定指令
v-bind 如果需要元素的属性动态绑定属性值 就需要v-bind 指令 
v-bind 还可以遍历属性内所用的内容
给属性进行动态绑定
插值表达式只能用在元素的内容节点 不能用在元素的属性节点上
v-bind用来给元素的属性动态绑定值 简写用英文的:
如果需要进行动态拼接 则字符串的外面需要包裹单引号
- 事件绑定指令
vue 提供了内置变量 名字叫做 $event 就是原生dom 的事件对象
- 双向绑定指令
- 条件渲染指令
- 列表渲染指令

- 事件修饰符 
加在事件绑定的后面
- .prevent 阻止默认行为 a跳转 表单的提交
- .stop 阻止事件冒泡
- .capture 以捕获模式触发事件
- .once 事件只触发一次
- .self 只在事件的目标是自身的时候触发函数
