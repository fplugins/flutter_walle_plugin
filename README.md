# flutter_walle_plugin

### 美团 walle 渠道包打包工具 flutter 插件, 支持获取 channel 、hannelInfo,并提供了 walle cli 打包快捷工具

### 使用本插件前应看一下 walle 开发文档 https://github.com/Meituan-Dianping/walle

## 项目内使用

```dart
   xxx.dart


   import 'package:flutter_walle_plugin/flutter_walle_plugin.dart';

   try {
    String channel = await FlutterWallePlugin.getWalleChannel();
    } on PlatformException {

    }


    try {
    String channel = await FlutterWallePlugin.getWalleChannelInfo();
    } on PlatformException {

    }

```

## 快捷打包 apk

channel、channelConfig.json 文件需要放在项目根目录，配置信息实例如下：
[渠道配置文件示例](https://github.com/Meituan-Dianping/walle/blob/master/app/channel)
[渠道&额外信息配置文件示例](https://github.com/Meituan-Dianping/walle/blob/master/app/config.json)

```
  setChannel        编译apk并写入渠道号 flutter pub run flutter_walle_plugin setChannel flutter build apk

  setInfo           编译apk并写入渠道信息 flutter pub run flutter_walle_plugin setInfo flutter build apk

  getInfo           查看指定apk文件渠道信息 flutter pub run flutter_walle_plugin getInfo /Users/hjc1/Documents/flutter/money_answer/channelApks/app-release_huawei.apk

```

## 服务端实现

[multi_channel](https://github.com/colbort/multi_channel.git)
