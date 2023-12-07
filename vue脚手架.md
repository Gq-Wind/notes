### vue-cli旧版本的脚手架

`vue init webpack [project_name]`

> assets与static区别:前者在项目打包时会被打包上传,后者不会;

npm install会在当前项目目录中查找package.json文件,并且检查node_modules是否已经存在满足条件的包,不存在或不满足则安装到当前node_modules

### @vue/cli新版本脚手架

`vue create project_name` 使用`vue ui`可以启用图形化界面创建项目

### vite

基于原生ESM,开发环境下基于rollup打包