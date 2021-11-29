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

  