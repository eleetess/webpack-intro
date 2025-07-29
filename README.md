# Webpack Intro

This project demonstrates a basic setup of Webpack to bundle JavaScript modules. The goal is to understand what Webpack is, why it's useful, and how to configure it to bundle multiple files.

---

## 📦 Project Setup

### 1. Initialize the Project

```bash
mkdir webpack-intro
cd webpack-intro
npm init -y
{
  "type": "module"
}
npm install --save-dev webpack webpack-cli
## JS

export function sayHello(name) {
  return `Hello, ${name}!`;
}

export function sayGoodbye(name) {
  return `Goodbye, ${name}!`;
}

import { sayHello, sayGoodbye } from './greetings.js';

console.log(sayHello('Webpack'));
console.log(sayGoodbye('Webpack'));
import path from 'path';
import { fileURLToPath } from 'url';

const __filename = fileURLToPath(import.meta.url);
const __dirname = path.dirname(__filename);

export default {
  entry: './src/index.js',
  output: {
    path: path.resolve(__dirname, 'dist'),
    filename: 'bundle.js'
  },
  mode: 'development'
};
"scripts": {
  "build": "webpack"
}
npm run build
## ✅ Submission Checklist

- [x] `package.json` is committed
- [x] `package-lock.json` is committed
- [x] `webpack.config.js` is included
- [x] `src/` folder contains:
  - [x] `index.js`
  - [x] `greetings.js`
- [x] `index.html` is in the project root
- [x] Webpack builds successfully (`npm run build`)
- [x] `dist/bundle.js` is generated (can be ignored in `.gitignore` if not required)
- [x] Project is pushed to a GitHub repo named `webpack-intro`
- [x] GitHub repository link is submitted on the assignment platform
