# vscode

debug webpack

```js
{
    // 使用 IntelliSense 以学习相关的 Node.js 调试属性。
    // 悬停以查看现有属性的描述。
    // 欲了解更多信息，请访问: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "type": "node",
            "request": "launch",
            "name": "Launch Program",
            "program": "${workspaceRoot}//node_modules//webpack//bin//webpack.js"
        },
        {
            "type": "node",
            "request": "launch",
            "name": "启动程序",
            "program": "${file}"
        }
    ]
}
```