# mypkg
[![test](https://github.com/JunichiOmura/mypkg/actions/workflows/test.yml/badge.svg)](https://github.com/JunichiOmura/mypkg/actions/workflows/test.yml)

このパッケージはtalkerがトピックに0から順にカウントアップする整数をメッセージとしてパブリッシュし、それからlistenerが読み取ることでターミナルに表示させるものである。

※このリポジトリは2023年度ロボットシステム学の講義にて制作したものである。

## 使用方法
### ＊インストール方法
以下のコマンドを実行する。
```
$ git clone https://github.com/JunichiOmura/mypkg.git
```

### ＊talker.py
talker.pyはcountupというトピックに０から順に増幅するInt16型の整数のメッセージをパブリッシャとして製作している。

以下のコマンドを実行する。
```
$ ros2 run mypkg talker
```
実行結果は表示されていない

### ＊listener.py
listener.pyはcountupというトピックからInt16型のメッセージを受信し、ターミナルに表示させている。

以下のコマンドを実行する。
```
$ ros2 run mypkg listener
```
```
[INFO] [1703684534.191590416] [listener]: Listen: 0
[INFO] [1703684534.685441583] [listener]: Listen: 1
[INFO] [1703684535.185240049] [listener]: Listen: 2
[INFO] [1703684535.685210521] [listener]: Listen: 3
[INFO] [1703684536.185741719] [listener]: Listen: 4
[INFO] [1703684536.685756526] [listener]: Listen: 5
[INFO] [1703684537.185122089] [listener]: Listen: 6
[INFO] [1703684537.685391720] [listener]: Listen: 7
[INFO] [1703684538.185843868] [listener]: Listen: 8
[INFO] [1703684538.685304763] [listener]: Listen: 9
[INFO] [1703684539.185802176] [listener]: Listen: 10
[INFO] [1703684539.685535859] [listener]: Listen: 11
　　　　　　　　　　　　　・
　　　　　　　　　　　　　・
　　　　　　　　　　　　　・
```
※この場合はtalkerとは別のターミナルを使用しなければならない


## 必要なソフトウェア
* Python 3.8.10
* ROS 2  foxy

## テスト環境
* Ubuntu 20.04.6 LTS

## 著作権/ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
* © 2023 Junichi Omura


