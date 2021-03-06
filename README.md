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
__ubuntu 20.04 LTS__

# 回路

<img width="411" alt="20220112-0556_c744b8febe7aa6388e6c8082e806e99b" src="https://user-images.githubusercontent.com/96018191/149020656-6ffb6681-681d-4f0d-9148-dae717e2dc2b.png">

この回路では、三つのピンを使って三つのLEDを点滅させるもので、それぞれ25はグー、21はチョキ、20はパーにつながっています。

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
sudo insmod myled.ko
sudo chmod 666 /dev/myled0
```
上記のコマンドで実行の準備を終えたら、下記のコマンドでLEDを点灯・消灯することができる。
```
echo 0 > /dev/myled0   
echo 1 > /dev/myled0 
echo 2 > /dev/myled0 
echo 3 > /dev/myled0 
```
0~2は順番にグー、チョキ、パーのLEDを点灯させることができ、3はすべてのLEDを消灯することができる。

# ライセンス
[GNU General Public License v3.0](https://github.com/umezawa0315/janken1/blob/master/LICENSE)
