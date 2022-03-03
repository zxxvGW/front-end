# VUE

#### vue的生命周期钩子有几个？

- vue的生命周期函数有八个，从创建==>  更新  ==> 销毁的一个周期里分别是。

  - beforeCreate，在实例初始化之后，进行数据侦听和事件/侦听器的配置前同步调用

  - **created**，在实例创建完成后被立即调用。

    - 当前钩子函数中是可以访问到data，computed，methods,watch里面的函数和对象的。
    - 但此时挂载阶段还没开始，且`$el`property目前还不能访问

  - beforeMount，挂载开始之前被调用

  - mounted，实例被挂载后调用。此时的el被新创建的vm.$el替换了。

    - **`mounted`不会**保证所有的子组件都会被挂载完成。如果要视图都渲染完毕后在执行某些操作，可以在mounted里使用$nextTick

      ```javascript
      mounted:{
        this.$nextTick(function(){
      
       })
      }
      ```

  - beforeUpdate,数据发生变化，dom还没有更新之前被调用。
  
  - updated，数据的更改导致vdom重新渲染，和更新完毕之前调用。在这个钩子被调用时，dom已经完成了更新
    
    - 同样update不会保证所有的子组件也都会被重新渲染完毕，可以在update里使用$nextTick
  
  - beforeDestory,实例销毁之前被调用。
  
  - destroyed，实例被销毁后调用。

#### 自定义指令

- 自定义指令可以注册到全局或则局部

- 全局

  ```js
  // 注册一个全局自定义指令 `v-focus`
  Vue.directive('focus', {
    // 当被绑定的元素插入到 DOM 中时……
    inserted: function (el) {
      // 聚焦元素
      el.focus()
    }
  })
  ```

- 局部

  ```js
  directives: {
    focus: {
      // 指令的定义
      inserted: function (el) {
        el.focus()
      }
    }
  }
  ```

#### 在生命周期的created阶段能不能访问methods，computed等？

- 文档中明确提到了在created阶段已经完成option的配置，是可以对methods，computed进行调用和使用的。

#### 侦听器watch

- 什么是侦听器
  - 在开发中我们在date返回对象中定义了数据，这个数据通过插值语法等方式绑定到template中，
  - 当数据变化时，template会自动进行更新最新的数据。
  - 在某些情况下我们希望在**代码逻辑**中监听某个数据的变化，这个时候就需要用到watch来完成了

#### watch和computed的区别

- computed是计算属性，依赖其他属性计算值，并且computed的值有缓存，只有计算值变化时才会重新计算
- watch 监听到值的变化就会执行回调函数，可以在回调中进行逻辑操作

#### keep-alive组件有什么作用

- 当组件需要频繁切换时，可以使用keep-alive组件，被包裹的组件会在第一次渲染完成时被缓存下来。

#### router和route

- `route`是 **路由信息对象**,包括path,params,hash,query等信息
- `router`是 **路由实例**,包括了路由的跳转方法和钩子函数





