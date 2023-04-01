1. 在assets中新建一个global.scss文件

2. 文件中写入全局样式

   1. ```scss
      // scss全局样式
      $mainColor:#033F77;
      ```

3. 在vue中使用, vue.config.js文件中写入

   1. ```js
      module.exports = {
          css: {
              loaderOptions: {
                  scss: {
                      additionalData: `@import "@/assets/scss/global.scss";`,
                  },
              },
          },
      }
      ```

   2. 注意ssas-loader的版本问题, 目前项目里使用的是10.2.1版本, 在github中查找该版本, 找到的是additionalData属性( 这个属性在不同的sass-loader版本中是不同的 ), 引入全局的global.scss文件, 就可以在vue项目里任何地方直接使用$mainColor了

   3. 注意main.js中不可引入global.scss文件