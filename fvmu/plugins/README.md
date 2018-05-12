# plugins

plugins起初设计为挂载在Vue原型上的方法，后修改为直接导出模块以供调用，无需使用`Vue.use`。

页面上调用方式(以Toast)为例：

```javascript
import { Toast } from 'fvmu'

Toast.open('我是一个弹窗');
```
