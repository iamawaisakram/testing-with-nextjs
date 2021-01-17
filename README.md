## Getting Started

# Dependencies Installed:

```
yarn jest @testing-library/react babel-jest @testing-library/jest-dom @testing-library/user-event @testing-library/dom -D

```

## At Root

`touch .babelrc`

- Add in .babelrc

```
{
  "presets": ["next/babel"]
}
```

`touch jest.config.js`

```
// jest.config.js
module.exports = {
  setupFilesAfterEnv: ['<rootDir>/jest.setup.ts'],
  testPathIgnorePatterns: ['<rootDir>/.next/', '<rootDir>/node_modules/'],
  moduleNameMapper: {
    '\\.(scss|sass|css)$': 'identity-obj-proxy',
  },
};
```

`touch jest.setup.js`

```
// jest.setup.ts
import '@testing-library/jest-dom';
```

`package.json`

```
"scripts": {
    ...,
    "test": "jest"
  },
```

First, run the development server:

```bash
npm run dev
# or
yarn dev
```
