# 概要
じゃんけんマシンを作りました。

ロボットシステム学の課題１で作成しました。

数字に応じて、__グー__、__チョキ__、__パー__ のランプが点灯します。

# 用意したもの
Rasberry Pi 3b

LED 3つ

ブレッドボード 1つ

ジャンパー線　6本

# 環境
__ubuntu 18.04 LTS__

# 動画
[動画](https://youtu.be/dRgufOXc1_w)

実際に動作させた際の動画です。

# インストールと実行方法
## インストールの際は下記のコマンドを実行
```
git clone https://github.com/umezawa0315/janken1.git
```
## インストール後下記のコマンドで実行可能
```
cd janken1
make
sudo insmod jankenmachine.ko
sudo chmod 666 /dev/jankenmachine0
```
