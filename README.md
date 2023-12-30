# mypkg
[![test](https://github.com/JunichiOmura/mypkg/actions/workflows/test.yml/badge.svg)](https://github.com/JunichiOmura/mypkg/actions/workflows/test.yml)

このパッケージはtalkerがトピックに0から順にカウントアップする整数をメッセージとしてパブリッシュし、それからlistenerが読み取ることでターミナルに表示させるものである。

※このリポジトリは2023年度ロボットシステム学の講義にて制作したものである。

## 使用方法
### インストール方法
以下のコマンドを実行する。
```
$ git clone https://github.com/JunichiOmura/mypkg.git
```

### talker.py
talker.pyはcountupというトピックに０から順に増幅するInt16型の整数のメッセージをパブリッシャとして製作している。

以下のコマンドを実行する。
```
$ ros2 run mypkg talker
```
実行結果は表示されていない

### listener.py
listener.pyはcountupというトピックからInt16型のメッセージを受信し、ターミナルに表示させている。

以下のコマンドを実行する。
```
$ ros2 run mypkg listener
```
以下のように実行結果が表示される。
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

### talkerとlistenerを同じターミナル上で同時に実行する方法
以下のコマンドを実行する。
```
$ ros2 launch mypkg talk_listen.launch.py

```
以下のように実行結果が表示される。
```
[listener-2] [INFO] [1703689869.798613476] [listener]: Listen: 0
[listener-2] [INFO] [1703689870.290407114] [listener]: Listen: 1
[listener-2] [INFO] [1703689870.790520111] [listener]: Listen: 2
[listener-2] [INFO] [1703689871.291008816] [listener]: Listen: 3
[listener-2] [INFO] [1703689871.790622211] [listener]: Listen: 4
[listener-2] [INFO] [1703689872.290361272] [listener]: Listen: 5
[listener-2] [INFO] [1703689872.790439424] [listener]: Listen: 6
[listener-2] [INFO] [1703689873.290564526] [listener]: Listen: 7
[listener-2] [INFO] [1703689873.790342674] [listener]: Listen: 8
[listener-2] [INFO] [1703689874.290513093] [listener]: Listen: 9
[listener-2] [INFO] [1703689874.790406557] [listener]: Listen: 10
　　　　　　　　　　　　　　　・
　　　　　　　　　　　　　　　・
　　　　　　　　　　　　　　　・
```

## 必要なソフトウェア
* Python 3.8.10
* ROS 2  foxy

## テスト環境
* Ubuntu 20.04.6 LTS

## 著作権/ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
* © 2023 Junichi Omura


