Get started section at: https://github.com/Microsoft/vscode/wiki/How-to-Contribute


Checkout release branch. `git checkout 1.19` `git clean -xdf .`?
`yarn`

`yarn gulp vscode-linux-x64-min`

`yarn gulp vscode-darwin-min`

For releasing:
`yarn gulp vscode-linux-x64-build-deb`

`cd ../VSCode-darwin` `zip -r -X -y VSCode-darwin-unsigned.zip *`

For Mac, I've had to replace the `node_modules` in the electron app with
a copy from the distributed version of VS Code

The .deb file should be under `./.build/.../*.deb`


Install with `sudo dpkg -i ./path/to/*.deb`

After installing verify version with about menu.

