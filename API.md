# API

English | [简体中文](./API.zh-CN.md)

## `headParams(fn, ...headArgs)`

Returns a function that calls `fn` with `headArgs` followed by the arguments
received by the returned function.

```ts
const logWithScope = headParams(console.log, '[build]')
logWithScope('started') // Output: [build] started
```

## `tailParams(fn, ...tailArgs)`

Returns a function that calls `fn` with the arguments received by the returned
function followed by `tailArgs`.

```ts
const logDone = tailParams(console.log, 'done')
logDone('build') // Output: build done
```
