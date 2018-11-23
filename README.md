# test
引入element-ui
https://github.com/ElemeFE/element/tree/master 下载一个master分支。在src文件夹下建立一个element-ui文件夹，将下载的分支解压到该文件夹下

在我们的项目中main.js 中引入
import ElementUI from './element-ui' // dev
import './element-ui/lib/theme-chalk/index.css' // dev

在我们项目的webpack配置webpack.base.conf.js中增加别名配置element-ui，把'element-ui'指向我们项目中element-ui根目录的位置src/element-ui:

    alias: {
      'vue$': 'vue/dist/vue.esm.js',
      '@': resolve('src'),
      'element-ui':resolve('src')+'/element-ui'
    }
	
	到element-ui的build文件夹

exports.alias = {
  main: path.resolve(__dirname, '../src'),
  packages: path.resolve(__dirname, '../packages'),
  examples: path.resolve(__dirname, '../examples'),
  'element-ui': path.resolve(__dirname, '../')
};


在我们项目中 引入 
  import ElCollapse from "../../../element-ui/packages/collapse";
  import ElCollapseItem from "../../../element-ui/packages/collapse-item";
