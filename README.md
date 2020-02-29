# import-sort-style-rn

Sensible [import sorting](https://github.com/renke/import-sort/) style for React Native projects.

## Installation

```
yarn add --dev import-sort-cli import-sort-style-rn
```

## Setup

Add the following to your `package.json`:

```json
"importSort": {
  ".js, .jsx, .ts, .tsx": {
    "style": "rn"
  }
}
```

## Style

```javascript
// Modules with side effects (not sorted internally because order may matter)
import 'c';
import 'a';

// React (Native) modules
import React from 'react';
import { Text, ... } from 'react-native';

// Node.js modules
import { readFile } from 'fs';

// Installed modules
import axios from 'axios';

// "External" project modules ("../")
import Divider from '../components/Divider';

// "Internal" project modules ("./")
import Bubble from './Bubble';

// Resource files (.png, .jpg, .jpeg, .svg)
import Logo from '../assets/logo.png';

```

### References

- https://github.com/renke/import-sort/tree/master/packages/import-sort-style-module
- https://github.com/pietile/import-sort-style-pietile
