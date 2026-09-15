# function-control

[English](./README.md) | 简体中文

面向 TypeScript 项目的小型函数参数辅助工具。

## 安装

```sh
npm install @arylo-scripts/function-control
```

## 使用

```ts
import { headParams, tailParams } from '@arylo-scripts/function-control'

const logWithScope = headParams(console.log, '[build]')
logWithScope('started') // 输出: [build] started

const logDone = tailParams(console.log, 'done')
logDone('build') // 输出: build done
```

## API

参见 [API 参考](./API.zh-CN.md)。

## 开发

```sh
npm install
npm run lint
npm run build
```
