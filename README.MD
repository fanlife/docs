# 返利网前端文档

> 链接：[https://fanlife.github.io/docs/](https://fanlife.github.io/docs/)

## 使用

本文档采用`gitbook`构建，如需对文档进行维护，首先需要安装全局`gitbook`：

```shell
npm install gitbook -g
```

对文档维护过程中仅需要对`.md`文件进行操作，因此需熟悉`markdown`语法，并选择合适的支持`markdown`语法的编辑器。

### 新增目录及文件

- 无论是新增目录还是文件，均需在`SUMMARY.md`中添加对应目录/文件，例：

```markdown
* [返利网前端文档](README.MD)
    * [fvmu](fvmu/README.MD)
        * [Toast](fvmu/toast.md)
        * [Dialog](fvmu/dialog.md)
```

以上语法会生成三级目录，并生成4个md文件，如需添加对应目录或文件，直接修改`SUMMARY.md`即可。

- 修改`SUMMARY.md`后，执行`gitbook init`命令即可自动生成对应目录及相应文件夹
- 对应文档编辑完成后，直接提交push即可，请**不要本地构建**，本仓库集成了[travis-ci(持续集成工具)](https://travis-ci.org/)，push操作会触发`travis-ci`的部署脚本，`travis-ci`会自动执行`gitbook build`并将生成的代码拷贝并提交到[fanlife.github.io](https://github.com/fanlife/fanlife.github.io)仓库

