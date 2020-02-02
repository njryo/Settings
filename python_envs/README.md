# Python 環境管理メモ

基本Anaconda のconda で管理。Anaconda 関連のパスは通さない。

Windows で普通のPython をインストールする時はパスを通さず、py launcherを活用する。

## py.exe の使い方

インタープリターの起動:

```
py -3.7 // python 3.7 が起動
```

pip の利用:

```
py -3.7 -m pip ... // python 3.7 のpip を使う時
```

## Pythonパッケージ

よく使うもの:

```
autopep8 flake8 mypy nose pyflakes pylint pytest sphinx
```

jupyter 周り:

```
ipykernel jupyterlab notebook
```

- カーネルだけでよければipykernel のみをインストールして、下記のカーネル追加を実行
- nodejs も必要なら入れる(conda で入れられる)

分析用環境:

```
bokeh lightgbm matplotlib networkx nltk numpy pandas scikit-image scikit-learn scipy seaborn statsmodels sympy tensorflow tensorboard 
```
- xgboost (conda ではpy-xgboost)
- pytorch, torchvision


## Jupyter

### 設定ファイル

```bash
# 設定ファイルの作成
jupyter notebook --generate-config
```

### フォント変更

/custom/custom.css を.jupyter以下に配置でJupyter Notebook 
のフォントを変更

./jupyter/custom/custom.cssが普段使っているもの


### 仮想環境のカーネル追加

```
# 追加したい環境をactivateしてから
python -m ipykernel install --user --name <name of kernel> --display-name <name displayed on Jupyter>
```

## pystan on Windows

- 依存パッケージのバージョンの組み合わせによって上手くいったりいかなかったり
- 公式の説明に従ってインストール
- numpy等はconda-forgeから
- pystanはpipでインストールする
- jupyter を使う時はこの環境から起動しないと上手くいかないことがある

## pymc3 on Windows

- 依存パッケージのバージョンの組み合わせによって上手くいったりいかなかったり
- pymc3.ymlは上手くいった例
