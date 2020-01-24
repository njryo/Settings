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

設定の`Editor` > `General` のOther

- Ensure line feed ad file end on Save にチェック。

#### リッチテキストコピーをオフ

設定の`Editor` > `General` のRich-text copy

- Copy as rich text by default のチェックを外す

#### スペースなどを表示

設定の`Editor` > `General` > `Appearance`

- Show Whitespacesにチェック
- `Editor` > `Color Scheme` > `General` のText > Whitespace の色を明るく

#### 選択文字列を囲む機能

設定の`Editor` > `General` > `Smart Keys`

- Surround selection on typing quote or brace にチェック

#### keymap

VS Code Keymap プラグインを導入。設定の`Keymap` でVS Code を選択し、

- `Main Menu` > `View` > `Appearance` のQuick Documentation に何か振る(Ctrl + Q とか)
- `Other` のSave Document に何かフル(Ctrl + S とか)

### 見た目

Material Theme UI pluginを導入

#### 全体的な調整

設定の`Appearance & Behavior` > `Material Theme` で

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

設定の`Editor` > `Color Scheme` > `Color Scheme Font`から変更する（`Editor > Font`の方ではなく）。

- Font: Source Han Code JP R
- Size 13
- Line spacing 1.0
- Use color scheme font instead of the default にチェック

#### コンソールフォント

設定の`Editor` > `Color Scheme` > `Console Font`から変更する。

- Font: Source Han Code JP R
- Size 12
- Line spacing 1.0
- Use console font instead of the default にチェック

### Java 使用時

`Editor` > `Code Style` > `Java` でインデントサイズを変更

### PyCharm 使用時

設定の`Tools` > `Python Integrated Tools` でtest, docstring 等の設定
