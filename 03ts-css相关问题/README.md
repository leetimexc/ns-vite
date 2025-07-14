### ts

```bash
npm install typescript -D

新建 tsconfig.json

就可以直接去开发了

```

### css

```bash
vue-ts 创建一个项目，然后记录下css需要哪些内容
npm create vite@latest
vite-css-demo // 项目名称
Vanilla + TypeScript // 模版选择
```

#### vite 官方推荐用 css 变量去写的

下面这些 vite 已经集成了，不需要配置

- css 变量

- postcss：里面集成了 css，在根目录创建 postcss.config.cjs

```bash
// 例子：安装后，引入 tailwindcss
modules.exports = {
  plugins: [
    require('tailwindcss')
  ]
}
```

- css modules

```bash
新建 src/styles/test.module.css （xxx.module.css）
.test {
  color: red;
}

// 使用
import testClass from './styles/test.module.css'

<div className={testClass.test}></div>
```

- 重命名

```bash
新建 vite.config.ts：

import path from 'path'
import { defineConfig } from 'vite'

export default defineConfig({
  resolve: {
    alias: {
      '@': path.resolve(__dirname, 'src'),
    },
  },
})

新建 src/styles/reset.css

// style.css 使用
@import '@/styles/reset.css'

所有的预处理器，除了stylus的api没有对外开放，其他的比如less、sass 这里的@重命名也是起作用的

```

- 预处理器

```bash
less、sass、stylus

vite里面安装后直接用就行了，不需要配置，vite已经集成了

npm install less less-loader -D
npm install sass sass-loader -D
npm install stylus stylus-loader -D
```
