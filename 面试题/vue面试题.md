1. MVVM是什么
   1. 它是Model-VIew-ViewModel的缩写
   2. 核心是提供Model与View的双向绑定
   3. Model的主要任务是储存页面中的数据
   4. View的主要任务是展示Model中储存的数据
2. Vue如何实现MVVM
   1. 对数据(Model)进行劫持, 当数据变动时. 触发劫持数据时绑定的方法, 对视图进行更新
   2. vue采用Object.defineProperty的getter与setter, 并结合观察者模式来实现数据绑定