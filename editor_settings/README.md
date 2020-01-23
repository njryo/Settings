# エディターの設定メモ

## VSCode

### Extensions

`./vscode/vscode_extensions.txt` にあるもの。次のように出力:

```bash
code --list-extensions > vscode_extensions.txt
```

### 設定

`./vscode/settings.json` を参照。

## IntelliJ & PyCharm

### エディターの設定

#### 保存時に最終行に改行を挿入

設定のEditor > GeneralのOther, Ensure line feed ad file end on Saveにチェック。

#### リッチテキストコピーをオフ

設定のEditor > GeneralのRich-text copy, Copy as rich text by defaultのチェックを外す。

#### スペースなどを表示

設定のEditor > General > AppearanceのShow Whitespacesにチェック。

#### 選択文字列を囲む機能

設定のEditor > General > Smart KeysのSurround selection on typing quote or braceにチェック

#### keymap

VS Code Keymap プラグインを導入。設定のKeymap でVS Code を選択後、Main Menu > View > Appearance のQuick Documentation に何か振る(Ctrl + Q とか)。

### 見た目

Material Theme UI pluginを導入

#### 全体的な調整

設定のAppearance & Behavior > Material Theme の部分は

- Selected Theme はAtom One Dark
- Contrast Mode にチェック
- Advanced Settings 以下は
    - Tabs はチェックなし
    - Compact
        - Compact Statusbar とCompact Menus にチェック
    - Icons
        - Material UI Icons, File Icons, Folder Decorators, PSI Icons にチェック
    - Project View
        - Custom Sidebar Height にチェックで値は18
    - Components
        - Uppercase buttons, Accent Scrollbars, Transparent Scrollbars にチェック
    - Features
        - Material Theme, Material Design Components, Material File Status Colors にチェック
    - Other Tweaks
        - Hollow Folders, Theme in StatusBar, Language Additions, Colored Open Directories にチェック


#### エディターフォント

設定のEditor > Color Scheme > Color Scheme Fontから変更する（Editor > Fontの方ではなく）。

- Font: Source Han Code JP R
- Size 13
- Line spacing 1.0
- Use color scheme font instead of the default にチェック


#### コンソールフォント

設定のEditor > Color Scheme > Console Fontから変更する。

- Font: Source Han Code JP R
- Size 12
- Line spacing 1.0
- Use console font instead of the default にチェック

(PytCharm の方はPython Consoleをよく使うのでエディターフォントに合わせた方が見やすいかも。)

### PyCharm 使用時

設定のTools > Python Integrated Tools でtest, docstring 等の設定ができる。
