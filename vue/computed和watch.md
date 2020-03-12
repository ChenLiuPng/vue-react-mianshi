# computed 和 watch 的区别

- computed 有缓存，data 不变则不会重新计算

computed 的设计初衷:

在模版中放入太多声明式的逻辑会让模板本身过重，尤其当在页面中使用大量复杂的逻辑表达式处理数据时，会对页面的可维护性造成很大的影响，而 computed 的设计初衷也正是用于解决此类问题。

使用场景:
适用于重新计算比较费时不用重复数据计算的环境。所有 getter 和 setter 的 this 上下文自动地绑定为 Vue 实例。如果一个数据依赖于其他数据，那么把这个数据设计为 computed

如果依赖的属性没有发生改变的时候，会从缓存中读取

代码:
`./computed/computed.vue`

- watch 如何深度监听？

watch 默认是浅监听 如果要进行深度监听 加上 `deep:true`

- watch 监听引用类型
