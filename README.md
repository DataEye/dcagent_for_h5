# DCAgent

[DataEye](http://www.dataeye.com/) SDK for HTML5 game analysis, works on normal HTML5 browser (include WebView without DOM) and Egret Engine (include runtime).

# Latest Version

`0.1.4` released on `2015-05-07`

# Integrate Tutorial

[http://wiki.dataeye.com/h5/document/html5/html5-advanced-guide.html#part4](http://wiki.dataeye.com/h5/document/html5/html5-advanced-guide.html#part4)

----

# DCAgent

[DataEye](http://www.dataeye.com/) HTML5游戏数据分析统计SDK，适用于HTML 5浏览器（支持无DOM环境）以及白鹭引擎（支持runtime）。

# 最新版本

`0.1.4` 发布于 `2015-05-07`

# 集成教程

1.解压DataEye SDK压缩包，拷贝dcagent.json文件和dcagent目录到你的项目根目录

2.修改你的项目根目录下的egretProperties.json，在modules属性中加入DataEye SDK的配置项，参考如下格式或SDK压缩包内的egretProperties.sample.json：

```js
{
    "document_class": "Main",
    "modules": [
        {
            "name": "core"
        },
        {
            "name": "res"
        },
        // 这里加入dcagent的配置
        {
            "name": "dcagent",
            "path": "."
        }
    ],
    "native": {
        "path_ignore": []
    },
    "egret_version": "1.7.0"
}
```

3.初始化代码

```js
var agentConfig = new DCAgentInitConfig();
agentConfig.appId = 'C56B61FB6BBA48B31CB529176B1E9E8D';
DCAgent.init(agentConfig);
    
```

初始化全部配置参数请参见 [http://wiki.dataeye.com/h5/document/html5/html5-quick.html#part2](http://wiki.dataeye.com/h5/document/html5/html5-quick.html#part2)

4.使用付费接口

```js
var paymentConfig = new DCAgentPaymentConfig();
paymentConfig.amount = 10;
DCAgent.onPayment(paymentConfig);
```

付费接口全部配置参数请参见 [http://wiki.dataeye.com/h5/document/html5/html5-advanced-guide.html#part2](http://wiki.dataeye.com/h5/document/html5/html5-advanced-guide.html#part2)
