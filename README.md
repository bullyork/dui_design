<p align="center">
  <a href="##">
    <img width="320" src="http://imsproduction.oss-cn-shanghai.aliyuncs.com/9ae88a590d27aef3ff3256ad2ee48c94.png">
  </a>
</p>

# Dui design


[![npm package](https://img.shields.io/npm/v/antd.svg?style=flat-square)](https://www.npmjs.com/package/dui_design)


## 说明

- 基于ant-design
- 用于前端后台快速开发
- 使用react


## Install

```bash
npm install duid
```

## Usage

```jsx
import { DatePicker } from 'duid';
ReactDOM.render(<DatePicker />, mountNode);
```

And import style manually:

```jsx
import 'duid/dist/antd.css';  // or 'duid/dist/antd.less'
```

### Use modularized antd

- Use [babel-plugin-import](https://github.com/ant-design/babel-plugin-import) (Recommended)

   ```js
   // .babelrc or babel-loader option
   {
     "plugins": [
       ["import", { libraryName: "duid", style: "css" }] // `style: true` for less
     ]
   }
   ```

   Then you can import components from antd, equivalent to import manually below.

   ```jsx
   // import js and css modularly, parsed by babel-plugin-import
   import { DatePicker } from 'duid';
   ```

- Manually import

   ```jsx
   import DatePicker from 'duid/lib/date-picker';  // for js
   import 'duid/lib/date-picker/style/css';        // for css
   // import 'duid/lib/date-picker/style';         // that will import less
   ```

### TypeScript

```js
// tsconfig.json
{
  "compilerOptions": {
    "moduleResolution": "node",
    "jsx": "preserve",
    "allowSyntheticDefaultImports": true
  }
}
```

> Note:
> - set `allowSyntheticDefaultImports` to prevent `error TS1192: Module 'react' has no default export`.
> - Don't use @types/antd, antd provide a built-in ts definition already.

## Development

```bash
$ git clone git@github.com:bullyork/dui_design.git
$ npm install
$ npm start
```

Open your browser and visit http://127.0.0.1:8001 
