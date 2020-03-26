# M5StackSolenoid

ソレノイド（[タカハの5Vソレノイド](http://takaha.co.jp/co/product-ss#productWrapSec1)など）を制御するM5Stack用の拡張基板です。
最大4個のソレノイドをON/OFF制御できます。

# 機能

実装するコネクタ・部品によって、以下の2通りの使い方ができます。
- [使い方1] USBコネクタ実装（[タカハの5Vソレノイド](http://takaha.co.jp/co/product-ss#productWrapSec1)用）
- [使い方2] 2.ネジ端子実装（一般のソレノイド）

# 用意するもの
- M5Stack
- USB Type-C端子のある電源（ACアダプタ、モバイルバッテリ等。ソレノイド駆動用の電源）
- ソレノイド（用いているnMOS、ダイオードの定格内のものを用いてください）
  - [使い方1] [タカハの5Vソレノイド](http://takaha.co.jp/co/product-ss#productWrapSec1)、microUSBケーブル、[ショートピン端子](http://akizukidenshi.com/catalog/g/gP-03687/)
  - [使い方2] ソレノイド、ネジ端子[HT396R-4P](https://ja.aliexpress.com/item/33027266661.html)、IP2721（USB PDで5V以外の電圧をソレノイド駆動に用いる場合：IP2721の使い方の詳細はIP2721のデータシートを参照してください）

# 使い方
1. M5Stackの本体(Core、底板を外した状態)に本ボードを差し込み、USB Type-C端子に電源をつなぎます。
2. M5Stackの以下のGPIOピンに1を与えるとソレノイドがONに、0を与えるとOFFになります。（M5Stackのプログラムは、ArduinoIDE、UI Flow等で開発できます）
   - Ch.A : GPIO26
   - Ch.B : GPIO12
   - Ch.C : GPIO13
   - Ch.D : GPIO5

# Author

Junichi Akita (@akita11, akita@ifdl.jp)
