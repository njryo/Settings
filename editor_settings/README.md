# エディターの設定メモ

## IntelliJ, PyCharm共通

### エディターの設定

#### 保存時に最終行に改行を挿入

設定のEditor > GeneralのOther, Ensure line feed ad file end on Saveにチェック。

#### リッチテキストコピーをオフ

設定のEditor > GeneralのRich-text copy, Copy as rich text by defaultのチェックを外す。

#### スペースなどを表示

設定のEditor > General > AppearanceのShow Whitespacesにチェック。

#### 選択文字列を囲む機能

設定のEditor > General > Smart KeysのSurround selection on typing quote or braceにチェック

### 見た目

Material Theme UI pluginを導入

#### 全体的な調整

ツールバーのTools > Material Themeから変更できるものは以下のように設定中

- Mateial Theme Chooser: Atom One Dark
- Accent Color: Brick Accent Color
- Panel Options:
    - Toggle Contrast
    - Toggle Compact Sidebar
    - Toggle Compact Menus
    - Toggle Compact Status Bar
- Material Theme Options: default


#### エディターフォント

設定のEditor > Color Scheme > Color Scheme Fontから変更する（Editor > Fontの方ではなく）。

- Font: Source Han Code JP R
- Size 13
- Line spacing 1.0


#### コンソールフォント

設定のEditor > Color Scheme > Console Fontから変更する。

- Font: Source Han Code JP R
- Size 12
- Line spacing 1.1

(PythonだとPython Consoleをよく使うからエディターフォントに合わせた方が見やすそう。  
IntelliJだともっと見やすい設定が他にあると思う。)



