# Visual Studio Code Tips

## Chrome Debug - Webpack based bundle
Note: before debugging, launch chrome with parameter:
```sh
/Applications/Google\ Chrome\ Canary.app/Contents/MacOS/Google\ Chrome\ Canary --remote-debugging-port=9222
```
```json
{
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
