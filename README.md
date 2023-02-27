# myunsplash

This template should help get you started developing with Vue 3 in Vite.

## featrues 
* you can see a list of photos that you have added
* you can add a new photo to the list
* you can search photos by label
* When you hover a photo, you can see a label and a delete button
* you can delete images

## 实现过程

1. 主页打开调用get请求，获取图片对象数据， for循环加载图片。
2. 在主页的add按钮路由切换到 imageuploader模块，进行添加图片操作，添加完成之后，点击其他部分可以返回主页。
3. 删除模块
4. 查询功能 - 查询之后进行筛选（展示特性的图片）

## 请求接口

* 获取全部图片 
* 上传图片
* 删除图片
* 按label查询图片

## 实现难点
* 这个add按钮功能实现 通过添加另外一个页面还是切换加载模块，怎样的的路由实现思路（路由转换到其他模块，或者调用别的项目）？
* 删除模块， hover的时候展示一个操作框，可以进行删除。



## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```
