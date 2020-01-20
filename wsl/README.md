# WSL環境構築メモ

## Ubuntu 18.04 (16.04)

### ミラーの変更

```bash
sudo sed -i.bak -e "s%http://[^ ]\+%http://ftp.riken.go.jp/Linux/ubuntu/%g" /etc/apt/sources.list
```


### よく使うもののインストール

```bash
sudo apt -y install zip build-essential gdb
```

- sdkman
    - java, sbt のインストールに (公式ドキュメント参照)
- Anaconda (or miniconda)
    - 直にインストールしてパスも通す (pyenv などは挟まない方が楽、問題が起きたら考える)


### 日本語化

```bash
sudo apt -y install language-pack-ja
sudo update-locale LANG=ja_JP.UTF8
# ここで再起動
sudo dpkg-reconfigure tzdata
sudo apt -y install manpages-ja manpages-ja-dev

# 英語に戻す場合、以下を実行後再起動
sudo update-locale LANG=en_US.UTF8
```
