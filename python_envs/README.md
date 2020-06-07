# Python 環境管理メモ

## packages

リンター、フォーマッタ、テスト:

```
autopep8 black flake8 mypy pyflakes pylint pytest
```

jupyter, jupyterlab:

```
ipykernel jupyterlab notebook
```

- jupyterlab のextension を使うにはnode.js が必要
  - conda でインストール(PATH に気をつける) or
  - (Mac) nodenv 経由でインストール etc.

可視化:

```
matplotlib seaborn arviz bokeh plotly
```

分析:

```
numpy scipy pandas scikit-learn scikit-image statsmodels lightgbm
```

以下はドキュメント等を参照しながら

- pystan
  - コンパイラが正しく使えるかに注意
  - Windows にインストールする時はconda でコンパイラをインストール
  - pip でインストールが良さそう
- numpyro
  - pip から(20/6/7)
  - jax のバージョンに気をつける
- xgboost
  - conda でインストールする時はpy-xgboost
- imbalanced-learn
  - 不均衡データを扱うときに
  - conda ではconda-forge から(20/6/7)
- mlxtend
  - conda ではconda-forge から(20/6/7)
- shap
  - conda ではconda-forge から(20/6/7)

DL:

ドキュメントを見ながら

- tensorflow, tensorflow-datasets
- pytorch, torchvision, ignite
  - conda ではpytorch チャンネルから
- pyro
  - pip から(20/6/7)
- flax
  - pip から(20/6/7)

RL:

- open ai gym
  - conda 環境にインストールする場合はGitHub repository のsetup.py を確認してから
- open ai baseline
  - GitHub repository からclone

## jupyter

### 設定ファイルの作成

```bash
jupyter notebook --generate-config
```

### フォントなどの変更

- /custom/custom.css を.jupyter以下に配置
- 書き方は`./jupyter/custom/custom.css`を参照

### 仮想環境のカーネル追加

```
# 追加したい環境をactivateしてから
python -m ipykernel install --user --name <name of kernel> --display-name <name displayed on Jupyter>
```

## jupyterlab

### コードセルの設定

Settings -> Noteobook -> User Preferences に以下を

```json
{
    "codeCellConfig": {
        "fontFamily": 'Fira Code',
        "lineNumbers": true
    }
}
```

## py.exe の使い方

Windows で https://www.python.org/ からインストールする場合、py.exe でメジャーバージョンの使い分けができる

- インタープリターの起動

```
py -3.7 // python 3.7 が起動
```

- pip の利用

```
py -3.7 -m pip ... // python 3.7 のpip を使う
```
