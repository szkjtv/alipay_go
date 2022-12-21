# alipay_go
一个Go文件搞定支付宝支付系列，包括电脑网站支付，手机网站支付，扫码支付等

网上的很多Go支付宝支付接入教程都颇为复杂，且需要配置和引入较多的文件，本人通过整理后给出一个单文件版的，每个文件独立运行，不依赖和引入其他文件。希望可以给各位想接入支付宝的带来些许帮助和借鉴意义。


# 文件对应说明
pc.go 电脑网站支付

wap.go   手机网站支付

qrcode.go   当面付（扫码支付）

# 使用说明
1.需要用到支付宝哪一种支付方式，就只下载对应的单个文件即可。

2.文件开头的配置信息必须完善

3.运行

```
go run qrcode.go
```

运行后，浏览器打开`http://localhost:8080`即可体验支付

4.参数传递
```
#传递支付金额：
http://localhost:8080/?total_fee=0.02
#传递订单号：
http://localhost:8080/?out_trade_no=123456
#传递订单标题：
http://localhost:8080/?order_name=订单测试
#全部传递
http://localhost:8080/?total_fee=0.02&out_trade_no=123456&order_name=订单测试
```#   a l i p a y _ g o  
 