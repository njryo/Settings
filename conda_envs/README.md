## conda環境

conda環境のカーネルをJupyterに追加:

```
python -m ipykernel install --user --name <name of kernel> 
--display-name 
<name displayed on Jupyter>
```

### pystan on Windows

- 公式の説明に従ってインストール
- numpy等はconda-forgeから
- pystanはpipでインストールする
