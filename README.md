![](https://badgen.net/badge/Editor.js/v2.0/blue)

# Code Tool for Editor.js

CodeMirror Tool  for the [Editor.js](https://ifmo.su/editor) allows you to use codemirror lib to include code examples in your articles.

![](E:\html\LPM\@editorjs\codemirror\preview.gif)

## Installation

### Install via NPM

Get the package

```shell
npm i --save-dev editorjs-codemirror
```

Include module at your application

```javascript
const CodeTool = require('editorjs-codemirror');
```

### Download to your project's source dir

1. Upload folder `dist` from repository
2. Add `dist/bundle.js` file to your page.

# 

## Usage

Add a new Tool to the `tools` property of the Editor.js initial config.

```javascript
var editor = new EditorJS({
  ...

  tools: {
    ...
    code: CodeTool,
  }

  ...
});
```

## Config Params

| Field       | Type     | Description                                                     |
| ----------- | -------- | --------------------------------------------------------------- |
| placeholder | `string` | Code Tool's placeholder string                                  |
| mode        | `string` | Mode option for codemirror                                      |
| theme       | `string` | Theme option for codemirror look to use it just import css file |

## Output data

This Tool returns code.

```json
{
    "type" : "code",
    "data" : {
        "code": "body {\n font-size: 14px;\n line-height: 16px;\n}",
        "lang": "css"
    }
}
```
