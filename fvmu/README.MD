# fvmu

> github: [git@github.com:Fanli-FE/FVMU.git](git@github.com:Fanli-FE/FVMU.git)

> 文档: [https://fanlife.github.io/docs/fvmu/](https://fanlife.github.io/docs/fvmu/)

## 安装

```nodejs
npm install fvmu --save
```

## 引入

仅支持**按需**引入，需借助[babel-plugin-component](https://github.com/ElementUI/babel-plugin-component)

首先，安装 `babel-plugin-component`

```nodejs
    npm install babel-plugin-component -D
```

然后，在 `.babelrc` 的 `plugins` 中添加：

```json
    "plugins": [
        [
            "component",
            {
                "libraryName": "fvmu",
                "styleLibraryName": "styles"
            }
        ]
    ]
```

接着，在你自己的文件中引入，以`Toast`(plugins)或者`Button`(components)为例

```javascript
    import Vue from 'vue'
    import { Toast, Button } from 'fvmu'

    Vue.component(Button)

    /**********************
    * plugins用法，无需使用Vue.use
        Toast.open("fvmu)
    * 或者
        Toast.open({
            content: "fvmu"
        })
    */
```

> 具体组件使用方法可参考对应文档

## 开发流程

1. 拉取/更新代码
2. 初始化
    ```nodejs
        npm install     //每次更新代码后都需要执行一遍
        npm link        //执行过一次即可，无需每次执行
    ```
3. 开发
    - 维护已有组件
        - 修改对应代码，并添加对应调用示例（如需）
        - `npm run dev`，测试以保证代码良好运行
        - 修改`package.json`中的版本号并提交到`github`和`npm`仓库(`npm publish`)
    - 新增组件
        - `fvmu create 组件名`
        - 开发相应代码，在`examples/pages/组件名.vue`中添加对应调用示例，并测试以保证代码良好运行
        - `npm run build`
        - 修改`package.json`中的版本号并提交到`github`和`npm`仓库(`npm publish`)

 - `fvmu`命令： `fvmu create 组件名`，可选参数：
    - `-E`：不创建组件对应demo，默认创建，如传入则不创建demo
    - `-t`：组件类型，默认`components`，若为全局方法，可传入`-t plugins`
    - `-S`：不启动开发服务器，默认启动并打开demo页（如不创建demo则此项无效），如传入则不启动开发服务器，可通过`npm run dev`手动启动
    - `-v`：版本信息
    - `-h`：帮助信息

----------