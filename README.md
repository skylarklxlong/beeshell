<p align="center">
    <h3 align="center">beeshell 2.0</h3>
    <p align="center">
    一个 React Native 应用的基础组件库，基于 0.53.3 版本，提供一整套开箱即用的高质量组件，包含 JS 组件和复合组件（包含 Native 代码），涉及 FE、iOS、Android 三端技术，兼顾通用性和定制化，支持自定义主题，用于开发和服务企业级移动应用。
    </p>
</p>
[使用文档](./docs/index.md)

[更新日志](./docs/CHANGELOG.md)

在线演示：

- 下载美团 APP（iOS、Android 都可以）
- 进入首页，点击右上角“+”号，选择“扫一扫”，扫描下面二维码

![image](./docs/images/live-demo.png)



修复：

* 修复TimePicker滚动改变数据时onChange的回调中只有当前列数据改变/YktRN/node_modules/beeshell/dist/components/Timepicker/index.js 14行

this.setState({

​    ...this.state,

​    value: ret,

})

* 出现Error: Animated Value: Attempting to set value to undefined的问题是因为在rn0.63中Animated.value()只能接受数字

* mtdEnableAnimated: false,//这个配置没有用，要在/YktRN/node_modules/beeshell/dist/common/styles/variables.js中配置

* /Users/lixuelong/Work/Test/YktRN/node_modules/beeshell/dist/common/animations/index.js 中修改动画配置数组，只能是数字