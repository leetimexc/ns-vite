### create-react-app

```bash
npx create-react-app create-react-demo

热更新：
传统的19年之前使用 npm 包： react-hot-loader
后续改成 @pmmmwh/react-refresh-webpack-plugin webpack的插件了

vite: 最早之前使用 @vitejs/plugin-react-refresh 官方插件，react刷新插件，后面弃用了
现在使用的是 @vitejs/plugin-react 包含了刷新和JSX语法转换

暴露 webpack 配置：
pnpm eject

webpack入口是： js文件
vite入口是： html文件
```

### vite

```bash
pnpm create vite@latest create-react-demo -- --template react
```
