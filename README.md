# M5StackSolenoid

<img src="https://github.com/akita11/M5StackSolenoid/blob/master/M5StackSolenoid1.jpg" width="240px">

ソレノイド（[タカハの5Vソレノイド](http://takaha.co.jp/co/product-ss#productWrapSec1)など）を制御するM5Stack用の拡張基板です。
最大4個のソレノイドをON/OFF制御できます。

# 機能

実装するコネクタ・部品によって、以下の2通りの使い方ができます。
- [使い方1] USBコネクタ実装（[タカハの5Vソレノイド](http://takaha.co.jp/co/product-ss#productWrapSec1)用）：以下のようになります
<img src="https://github.com/akita11/M5StackSolenoid/blob/master/M5StackSolenoid2.jpg" width="240px">

- [使い方2] 2.ネジ端子実装（一般のソレノイド）：以下のようになります
<img src="https://github.com/akita11/M5StackSolenoid/blob/master/M5StackSolenoid3.jpg" width="240px">

※[スイッチサイエンスで託販売しているもの](https://www.switch-science.com/catalog/6328/)（5Vソレノイド用のショートピン端子が5個付属しています）は、「使い方1」の状態のものです。

# 用意するもの
- M5Stack
- USB Type-C端子のある電源（ACアダプタ、モバイルバッテリ等。ソレノイド駆動用の電源）
- ソレノイド（用いているnMOS、ダイオードの定格内のものを用いてください）
  - [使い方1] [タカハの5Vソレノイド](http://takaha.co.jp/co/product-ss#productWrapSec1)、microUSBケーブル、[ショートピン端子](http://akizukidenshi.com/catalog/g/gP-03687/)※「タカハの5Vソレノイド」に「ショートピン端子」を差し込んだ状態で使用します
  - [使い方2] ソレノイド、ネジ端子[HT396R-4P](https://ja.aliexpress.com/item/33027266661.html)、IP2721（USB PDで5V以外の電圧をソレノイド駆動に用いる場合：IP2721の使い方の詳細はIP2721のデータシートを参照してください）

# 使い方
1. M5Stackの本体(Core、底板を外した状態)に本ボードを差し込み、USB Type-C端子に電源をつなぎます。
1. M5Stackの以下のGPIOピンに1を与えるとソレノイドがONに、0を与えるとOFFになります。（M5Stackのプログラムは、ArduinoIDE、UI Flow等で開発できます）使用例としてtest.m5f (UI Flowプログラム）を参照してください。
   - Ch.A : GPIO26
   - Ch.B : GPIO12
   - Ch.C : GPIO13
   - Ch.D : GPIO5

※なおソレノイドの番号は、[使い方1]の場合は基板上の[A]-[D]で表示されているUSBコネクタに対応します。[使い方2]の場合は、基板上の"Ch.A"-"Ch.D"の表示に対応し、1つのネジ端子(HT396R)に2個のソレノイドを接続できます。

# Author

Junichi Akita (@akita11, akita@ifdl.jp)
