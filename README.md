# Visual Studio Code Tips

## Chrome Debug - Webpack based bundle
Note: before debugging, launch chrome with parameter:
```
/Applications/Google\ Chrome\ Canary.app/Contents/MacOS/Google\ Chrome\ Canary --remote-debugging-port=9222
```
```
{
  // Use IntelliSense to learn about possible Node.js debug attributes.
  // Hover to view descriptions of existing attributes.
  // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
  "version": "0.2.0",
  "configurations": [
    {
        "name": "Attach",
        "type": "chrome",
        "request": "attach",
        "port": 9222,
        "url": "http://localhost:4200/*",
        "webRoot": "${workspaceRoot}",
        "trace": true,
        "sourceMaps": true,
        "sourceMapPathOverrides": {
            "webpack:///./*":   "${workspaceRoot}/*"
        }
    }
  ]
}
```

## License MIT :)
