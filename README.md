# robotsys2020
# ロボットシステム学課題1
## 概要
LEDの点滅を利用し特定の信号を受け取った時モーレス信号で文字を表示します。また、特定の信号以外の信号を受け取った時は点滅させます。
## 動作環境
・Rasberry Pi 4 ModelB
・Ubuntu 18.04 LTS
## 使用したもの
・LED(赤)
・抵抗300Ω
・ブレットボード
・ジャンパー線
## インストール方法
```
$ git clone https://github.com/kudoken0905/robotsys2020.git  
```
## 使用方法
### ビルド
```
$ make  
$ cd robotsys2020/myled  
$ sudo insmod myled.ko  
$ sudo chmod 666 /dev/myled0  
```
### 実行
```
$echo a >> /dev/myled0 
```
## デモ動画
https://youtu.be/ftzWee-FD-w
## コントリビューション
・モーレス信号の短点と長点をLEDライトの点灯信号で、モーレス信号の点と点の間の無信号部分と文字と文字の区切りの部分をLEDライトの消灯信号でそれぞれ場合分けし、対応するカウント変数に割り当る。そして、特定の信号を受け取った時にこれを実行するようプログラムした
## ライセンス
[GNU General Public License v3.0](https://github.com/AD58-3104/robosys_led_control/blob/main/COPYING)
