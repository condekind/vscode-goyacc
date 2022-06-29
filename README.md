# goyacc syntax highlighting

Fork of LunicLynx/vscode-bison to hopefully get syntax highlight for goyacc

Warning: not working perfectly

**This is currently unpublished, there are instructions below on how to get this in your vscode**

<hr>

To get an installable package file, you'll need `vsce`. To install it with `npm`, run:

```bash
npm install -g vsce
```

This will generate `goyacc-{VERSION}.vsix`:
```bash
vsce package
```

Inside vscode, open the command palette (default `ctrl+shift+p`) type/run "install from vsix" and choose the generated file