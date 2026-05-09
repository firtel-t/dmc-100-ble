# Web Bluetooth DMC-100 Logger

This web application allows you to visualize real-time data from the FNIRSI DMC-100 directly in your browser. 
To use this app, you must perform a hardware modification by embedding a **Seeed Studio XIAO nRF52840** into the DMC-100 and flashing it with a Nordic UART Service (NUS) compatible sketch.

Since it uses the **Web Bluetooth API**, you can acquire and visualize data without a dedicated app.
For iOS users, it can be used by running the **Bluefy** app and opening:
[https://firtel-t.github.io/dmc-100-ble/](https://firtel-t.github.io/dmc-100-ble/)

Currently, this web app only supports the simultaneous voltage and current measurement mode of the DMC-100.

---

## Overview
The objectives of this project are:

- **Direct Browser Communication:** Connect BLE (Bluetooth Low Energy) devices directly to the browser.
- **Real-time Visualization:** View measurement data in real-time.
- **CSV Export:** Save logs for later analysis.
- **iOS Compatibility:** Utilize the Bluefy app to bypass iOS system limitations.

---

## Communication Specifications
This application uses **Nordic UART Service (NUS)** over BLE.

- RX (Notify): Receiving measurement data from the device

Currently, this application is **receive-only** and does not send commands to the device.

Data is handled as a byte stream, similar to standard UART communication.

---

## CSV Export
- Save your data anytime using the **"CSV"** button.
- Data is exported as time-series data, ready for analysis.

---

## Related Articles (Development Details)
For more details on the development process, please refer to the following (Japanese):
- [DMC-100 Protocol Analysis](https://firtel.blogspot.com/2026/04/fnirsi-dmc-100-uart-output.html)
- [Sketch for nRF52840](https://firtel.blogspot.com/2026/04/nrf52840-uart-ble.html)
- [Integrating the BLE Module into the DMC-100](https://firtel.blogspot.com/2026/05/fnirsi-dmc-100-bluetooth.html)

---

## Notes
- Web Bluetooth has specific browser limitations.
- It will **not** work on iOS Safari. Please use Bluefy or other Web Bluetooth-compatible browsers on iOS.
- When you cannot find device on iOS. Please check with nRF Connect App that you can scan and connect to device.
