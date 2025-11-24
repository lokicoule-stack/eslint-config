<div align="center">
 <img src="https://github.com/lokicoule-stack/eslint-config/blob/main/media/repo-header.svg?raw=true" alt="Lokiverse Eslint Configuration" />
</div>

Shareable ESLint configurations for TypeScript projects.

---------------

# @lokiverse/eslint-config

## Quick Start

```bash
npm install -D @lokiverse/eslint-config eslint prettier typescript
```

**eslint.config.js**

```js
import { lib } from '@lokiverse/eslint-config'

export default lib
```

## Configurations

| Config | Type-Aware | Use Case                          | Performance |
| ------ | ---------- | --------------------------------- | ----------- |
| `base` | No         | Quick setups, no tsconfig needed  | Fast        |
| `lib`  | Yes        | Libraries with strict type safety | Slower      |
| `app`  | Yes        | Applications with relaxed rules   | Slower      |

## Usage

### Base

Fast linting without type checking.

```js
import lokiverse from '@lokiverse/eslint-config'

export default lokiverse
```

### Library

Strict type-aware rules for libraries.

```js
import { lib } from '@lokiverse/eslint-config'

export default lib
```

### Application

Type-aware with browser/node globals.

```js
import { app } from '@lokiverse/eslint-config'

export default app
```

## Customization

```js
import { lib } from '@lokiverse/eslint-config'

export default [
  ...lib,
  {
    rules: {
      'no-console': 'off',
    },
  },
]
```

## What's Included

- ESLint 9+ flat config
- TypeScript support
- Prettier integration
- Type-aware rules (lib/app)
- Test file overrides

## License

MIT
