# function-control

Small function parameter helpers for TypeScript projects.

## Install

```sh
npm install @arylo-scripts/function-control
```

## Usage

```ts
import { headParams, tailParams } from '@arylo-scripts/function-control'

const logWithScope = headParams(console.log, '[build]')
logWithScope('started')

const logDone = tailParams(console.log, 'done')
logDone('build')
```

## API

- `headParams(fn, ...headArgs)` returns a function that prepends `headArgs`.
- `tailParams(fn, ...tailArgs)` returns a function that appends `tailArgs`.

## Development

```sh
npm install
npm run lint
npm run build
```
