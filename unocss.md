# Unocss

这是一个新的css插件库，他是一个新的css原子化概念的库，原先我们写css需要定义id 类 或者使用标签在css和html直接切换的书写我们页面的样式，稍微多一点就头昏脑疼，还有需要使用ico的时候可能组件库的不够完善我们还需要去自己定义一个ico库引入ico，现在在unocss中我们可以使用纯css的ico

## 使用

下面我们在vite中使用一下unocss

安装

yarn add unocss @unocss/preset-uno @unocss/preset-attributify @unocss/preset-icons

第一个就是unocss我们的unocss的主体，第二个@unocss/preset-uno是我们工具类预设，第三个@unocss/preset-attributify是我们的属性化的模式支持，@unocss/preset-icons这是对我们的icon的支持

安装完后我们像如下配置我们的vite.config.js

import { defineConfig } from 'vite'

import vue from '@vitejs/plugin-vue'



import Unocss from 'unocss/vite';

import { presetUno,presetAttributify,presetIcons  } from 'unocss'



// https://vitejs.dev/config/

export default defineConfig({

 plugins: [

  vue(),

  Unocss({

   presets:[

​    presetUno(),

​    presetAttributify(),

​    presetIcons()

   ]

  })

 ],

})

然后我们在下面的网址去搜索我们要使用的css样式，就可以查到我们需要的unocss的class对标样式

https://unocss.dev/interactive/

然后就是我们的icon样式的网址

https://icones.js.org/

这里要注意的是我们选择一个ico库后在我们的链接https://icones.js.org/collection/vscode-icons collection后面的vscode-icons就是我们要添加到项目的库

yarn add @iconify-json/collection

然后我们在网址中点击我们要的ico就可以找到我们需要的unocss的class

