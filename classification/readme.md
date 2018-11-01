﻿# 画像分類

## keras_nn.py: Neural networkを用いてMNIST手書き数字を10クラス分類

実行方法
```bash
python keras_nn.py
```

### データの準備
MNISTデータは手書き数字とラベル（0から9の数値）の組が70000組格納されたデータベースです．手書き数字は28x28画素のグレースケール画像です．今回は70000のうち60000枚をトレーニング用，10000枚をテスト用に使います．
トレーニング用及びテスト用の手書き数字とラベルを読み込みます．Neural Networkはデータを1次元ベクトルとして入力する必要があるため，28x28画素の手書き数字は1x784の1次元ベクトルに変換します．そして手書き数字データは0から1の実数をとるように正規化します．ラベルはone-hot vector表現に変換します． 