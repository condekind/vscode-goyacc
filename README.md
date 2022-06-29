# goyacc syntax highlighting

Fork of LunicLynx/vscode-bison to hopefully get syntax highlight for goyacc

Warning: not working perfectly. It is 'good enough' for simple .y files, such as `tools/cmd/goyacc/testdata/expr/expr.y` file [present in the official goyacc repo](https://github.com/golang/tools/blob/master/cmd/goyacc/testdata/expr/expr.y). From the repo this fork originated, I just replaced all the `.c` occurrences with `.go` and removed the section `meta.declarations.bison`, which was causing the block inside `%{...%}` to not be highlighted (before removing it, I couldn't see the `meta.prologue.goyacc` scope with the '*Inspect Editor Tokens and Scope*' command)

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

### To install the package:

Inside vscode, open the command palette (default `ctrl+shift+p`) type/run "install from vsix" and choose the generated file