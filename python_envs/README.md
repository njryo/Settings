# Python環境管理メモ

## Pythonパッケージ

分析用環境、インストールするもの:

```
autopep8, bokeh, flake8, graphviz, ipykernel, lightgbm, matplotlib, networkx, nltk, notebook, numpy, pandas, py-xgboost, python-graphviz, pyflakes, pylint, pytest, scikit-image, scikit-learn, scipy, seaborn, sphinx, statsmodels, sympy
```

- tensorflow
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

## conda環境

### pystan on Windows

- 公式の説明に従ってインストール
- numpy等はconda-forgeから
- pystanはpipでインストールする

### pymc3 on Windows

- 依存パッケージのバージョンの組み合わせによって上手くいったりいかなかったり
- pymc3.ymlは上手くいった例
