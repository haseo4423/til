- Mecabと辞書をインストール
```
$ brew install mecab
$ brew install mecab-ipadic
```

- mecab-ipadic-NEologdをインストール
```
$ brew install git curl xz
$ git clone --depth 1 git@github.com:neologd/mecab-ipadic-neologd.git
$ cd mecab-ipadic-neologd
$ ./bin/install-mecab-ipadic-neologd -n
```

- mecab-python3をインストール
```
$ brew install swig
$ pip install mecab-python3
```
