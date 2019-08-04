## js-cookie

### 安装方式：

```javascript
npm install js-cookie --save
```

### 引用方式

```javascript
import Cookies from 'js-cookie'
```

### 使用方法

- **存到cookie**  `Cookies.set('name', 'value');`

- **cookie中取出**  `Cookies.get('name');`

- **删除** `Cookies.remove('name');`

- **特殊的用法**

  ```javascript
  const user = {
    name: 'lia',
    age: 18
  }
  Cookies.set('user', user)
  const liaUser = JSON.parse(Cookies.get('user'))
  ```

  

## Store

### 安装

```javascript
cnpm install --save vuex
```

### 引入到main.js

```javascript
import Vuex from 'vuex'

Vue.use(Vuex)

const store =new Vuex.Store()
然后注入到vue实例当中。
```

### 调用数据的方法

```javascript
this.$store.state.element
```

### 状态管理的五个核心

- **state** 

  state为单一状态树，在state中需要定义我们所需要管理的数组、对象、字符串等等，只有在这里定义了，在vue.js的组件中才能获取你定义的这个对象的状态。

- **getter**

  当我们需要从store的state中派生出一些状态，那么我们就需要使用getter，getter会接收state作为第一个参数，而且getter的返回值会根据它的依赖被缓存起来，只有getter中的依赖值（state中的某个需要派生状态的值）发生改变的时候才会被重新计算。

- **mutation**

  更改store中state状态的唯一方法就是提交mutation，就很类似事件。每个mutation都有一个字符串类型的事件类型和一个回调函数，我们需要改变state的值就要在回调函数中改变。我们要执行这个回调函数，那么我们需要执行一个相应的调用方法：store.commit。

- **action**

  action可以提交mutation，在action中可以执行store.commit，而且action中可以有任何的异步操作。

- **module**

  







