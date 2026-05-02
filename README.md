# Web Bluetooth DMC-100 Logger

FNIRSI DMC-100 にnRF52840モジュールを内蔵する改造を行い、リアルタイムデータを
ブラウザから直接表示できるWebアプリです。
使用するにはDMC-100にSeeed Studio XIAO nRF52840にNUS対応のスケッチを書き込んだものを内蔵する必要があります。

Web Bluetooth API を使用して、アプリ不要でデータ取得・可視化が可能です。
iPhone上でBluefyアプリを実行して
https://firtel-t.github.io/dmc-100-ble/
を開くと使うことが出来ます。

---

## 概要
このプロジェクトは以下を目的としています：

- BLE（Bluetooth Low Energy）デバイスとブラウザで直接通信
- 測定データのリアルタイム表示
- CSVエクスポートによるログ保存
- iOSの制約でBluefyアプリが必要

---

## 通信仕様
本アプリは BLE の Nordic UART Service (NUS) を使用します。
- TX Characteristic：データ送信
- RX Characteristic：データ受信
UARTのようにバイト列をそのまま扱う構成です。


## CSVエクスポート
- 「CSV」ボタンでいつでも保存可能
- 時系列データとして解析可能

---

##  関連記事
開発の詳細はこちら：
- [DMC-100通信内容解析](https://firtel.blogspot.com/2026/04/fnirsi-dmc-100-uart-output.html)
- [nRF52840用スケッチ](https://firtel.blogspot.com/2026/04/nrf52840-uart-ble.html)
- [DMC-100にBLEモジュールを内蔵](https://firtel.blogspot.com/2026/05/fnirsi-dmc-100-bluetooth.html)

---

## 注意事項
- Web Bluetoothはブラウザの制限があります
- iOS Safariでは動作しません
