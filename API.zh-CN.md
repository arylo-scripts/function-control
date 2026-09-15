# API

[English](./API.md) | 简体中文

## `headParams(fn, ...headArgs)`

返回一个新函数。调用 `fn` 时，会先传入 `headArgs`，再传入新函数接收到的参数。

```ts
const logWithScope = headParams(console.log, '[build]')
logWithScope('started') // 输出: [build] started
```

## `tailParams(fn, ...tailArgs)`

返回一个新函数。调用 `fn` 时，会先传入新函数接收到的参数，再传入 `tailArgs`。

```ts
const logDone = tailParams(console.log, 'done')
logDone('build') // 输出: build done
```
