# vue_3.0_std
vue 3.0 new featrues

1. 更好的支持typescript
2. config配置项，devtools类型
    - app.config.devtools = true
    - 表示是否开启 vue-devtools 工具的检测，默认情况下开发环境是 true，生产环境下则为 false
    - errorHandler类型
    ```
    app.config.errorHandler = (err, vm, info) => {
        // info 为 Vue 在某个生命周期发生错误的信息
    }
    ```
    - globalProperties类型
        - 定义一个全局属性或者方法
        ```
        // 2.0 
        Vue.prototype.$md5 = () => {}
        // 3.0
        app.config.globalProperties.$md5 = () => {}
        ```
    - performence
        - 将其设置为 true 可在浏览器 devtool 性能/时间线面板中启用组件初始化，编译，渲染和补丁性能跟踪。 仅在开发模式和支持 Performance.mark API的浏览器中工作
3. Application API
4. Composition API
    - 由于相关业务的代码需要遵循option 的配置写到特定的区域，导致后续维护非常的复杂，同时代码可复用性不高
    - Composition API 解决了这个令人头疼的问题
    - 它为我们提供了几个函数
        - reactive
        - watchEffect
        - computed
        - ref
        - toRefs: toRefs 提供了一个方法可以把 reactive 的值处理为 ref，也就是将响应式的对象处理为普通对象
        - hooks
            - setUp()
            - onBeforeMount
            - onMounted
            - onBeforeUpdate
            - onUpdated
            - onBeforeUnmount
            - onUnmounted
            - onErrorCaptured
            - onRenderTracked
            - onRenderTriggered
