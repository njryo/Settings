# VS Code の設定

## 見た目

- テーマはOne Dark Pro
- アイコンはMaterial Icon Theme

## integrated terminal

- Mac では以下を設定に
  - conda のPATH がうまく通らないのを防ぐため

```jsonc
{
    // cf. https://github.com/microsoft/vscode/issues/70248
    // see also https://github.com/microsoft/vscode/issues/69954
    "terminal.integrated.inheritEnv": false,
}
```

## markdown

- Trailing Space はオフにする

```jsonc
{
    // markdown
    "[markdown]": {
        "editor.renderWhitespace": "boundary",
        "files.trimTrailingWhitespace": false,
        "editor.tabSize": 2
    },
}
```

## python

- `python.pythonPath` と`python.venvPath` は適宜編集
- リンターはpylint かflake8 の設定を有効化、mypy も適宜有効化

```jsonc
{
    // python
    "[python]": {
        "editor.tabSize": 4,
        "editor.renderIndentGuides": true,
        "editor.insertSpaces": true
    },

    "python.autoComplete.addBrackets": true,
    "python.jediEnabled": false,
    "python.analysis.memory.keepLibraryAst": true,
    "python.analysis.memory.keepLibraryLocalVariables": true,

    // "python.pythonPath": "path",
    // "python.venvPath": "path",

    // pylint setting
    // "python.linting.pylintEnabled": true,
    // "python.linting.pylintArgs": [
    //    "--disable=missing-docstring, fixme, invalid-name, too-few-public-methods"
    // ],
    // "python.linting.pylintUseMinimalCheckers": false,
    // "python.linting.mypyEnabled": true,

    // flake8 setting
    "python.linting.pylintEnabled": false,
    "python.linting.flake8Enabled": true,
    "python.linting.flake8Args": [
        "--ignore=E265, E402, W391"
    ],

    // mypy setting
    "python.linting.mypyEnabled": true,

    "python.formatting.provider": "autopep8",

    // auto docstring
    "autoDocstring.docstringFormat": "google",
}
```
