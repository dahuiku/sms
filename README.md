# sms
云之讯等短信接口SDK汇聚

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Software License][ico-license]]
[![Total Downloads][ico-downloads]][link-downloads]

将常用的各大验证码短信提供商的接口汇聚在一起，方便实际应用。会不断完善补充。

## 安装
推荐使用`composer`安装：
```
composer require yjc/sms
```

或者在composer.json里追加：
```
"require": {
	"yjc/sms": "1.0"
},
```

## 使用示例
首先需要到各大提供商注册并审核。然后进行配置。

极光验证码：
``` php
$sms = new \Yjc\Sms\Jsms('appkey', 'masterkey');
$sms->send('13482827633', 'temp_id');
```
可以在SDK里配置appkey和masterkey，也可以代码里实时配置。

云之讯：
``` php
$sms = new \Yjc\Sms\Ucpaas('token', 'appid', 'accountsid');
$sms->send('13482827633', 'temp_id');
```

[ico-version]: https://img.shields.io/packagist/v/yjc/sms.svg?style=flat-square
[ico-license]: https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/yjc/sms.svg?style=flat-square

[link-packagist]: https://packagist.org/packages/yjc/sms
[link-downloads]: https://packagist.org/packages/yjc/sms
[link-author]: https://github.com/52fhy

