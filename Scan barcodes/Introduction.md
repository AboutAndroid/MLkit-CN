# 条形码扫描

使用ML Kit的条码扫描API，您可以读取大多数使用标准条码格式编码的数据。

条形码是将信息从现实世界传递到应用程序的一种便捷方式。特别是，使用QR码等二维格式时，您可以编码结构化数据，如联系人信息或WiFi网络凭证。由于ML Kit可以自动识别和解析这些数据，因此当用户扫描条形码时，您的应用可以进行智能响应。

[iOS](https://github.com/Quorafind/MLkit-CN/blob/master/Scan%20barcodes/Scan%20Barcodes%20with%20ML%20Kit%20on%20iOS.md) [Android](https://github.com/Quorafind/MLkit-CN/blob/master/Scan%20barcodes/Scan%20Barcodes%20with%20ML%20Kit%20on%20Android.md)

## 关键功能

| 阅读大多数标准格式 | 线性格式：Codabar，Code 39，Code 93，Code 128，EAN-8，EAN-13，ITF，UPC-A，UPC-E                                                                                                                                                                 2D格式： Aztec, Data Matrix, PDF417, QR Code |
| ------------------ | ------------------------------------------------------------ |
| 自动格式检测       | 一次扫描所有支持的条码格式，而无需指定要查找的格式。或者，通过将检测器限制为您感兴趣的格式来提高扫描速度。 |
| 提取结构化数据     | 使用其中一种支持的2D格式存储的结构化数据将被自动分析。支持的信息类型包括URL，联系信息，日历事件，电子邮件地址，电话号码，SMS消息提示，ISBN，WiFi连接信息，地理位置以及AAMVA标准驱动程序信息。 |
| 适用于任何方向     | 条形码被识别并扫描，无论其方向如何：正面向上，倒置或侧向。   |

## 示例结果

![](https://github.com/Quorafind/MLkit-CN/blob/master/Scan%20barcodes/EAN-Obst.jpg)	

| 结果   |                                          |
| ------ | ---------------------------------------- |
| 坐标   | (49,125), (172,125), (172,160), (49,160) |
| 原始值 | 2404105001722                            |

![](https://github.com/Quorafind/MLkit-CN/blob/master/Scan%20barcodes/qrcode.png)	

| 结果         |                                     |          |
| ------------ | ----------------------------------- | -------- |
| **坐标**     | (87,87) (612,87) (612,612) (87,612) |          |
| 原始值       | WIFI:S:SB1Guest;P:12345;T:WEP;;     |          |
| **WiFi信息** | **SSID**                            | SB1Guest |
|              | **密码**                            | 12345    |
|              | **类型**                            | WEP      |