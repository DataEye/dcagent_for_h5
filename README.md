# DataEye SDK for HTML5 - DCAgent

[DataEye](http://www.dataeye.com/) HTML5游戏数据分析统计SDK，适用于HTML 5浏览器（支持无DOM环境）以及白鹭引擎（支持runtime）。

## 最新版本

`0.1.4` 发布于 `2015-05-07`

## 项目结构介绍

- DataEyeDemo 演示项目源代码，包含DataEye SDK初始化代码(src/Main.ts 150行)
- DataEyeDemoApp 打包到安卓APP的演示项目，用于演示DataEye SDK在白鹭引擎runtime下的运行
- dcagent DataEye SDK源代码
- egret-android-support-1.7.0 白鹭引擎打包APP模板

[下载演示代码](https://github.com/DataEye/dcagent_for_h5/archive/master.zip)

## 集成教程

1.解压DataEye SDK压缩包，拷贝dcagent文件夹到你的项目根目录

2.修改你的项目根目录下的egretProperties.json，在modules属性中加入DataEye SDK的配置项：

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
        // 这里加入dcagent的配置，这里的path可以根据你的实际情况填写
        // 比如你将dcagent文件夹放到src目录下，这里就填写 src/dcagent
        {
            "name": "dcagent",
            "path": "../dcagent"
        }
    ],
    "native": {
        "path_ignore": []
    },
    "egret_version": "1.7.0"
}
```

**注意： 如果运行演示代码，请在编译时请运行 `egret build -e`，不要忘记-e参数**

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

----

# DCAgent

[DataEye](http://www.dataeye.com/) SDK for HTML5 game analysis, works on normal HTML5 browser (include WebView without DOM) and Egret Engine (include runtime).

## Latest Version

`0.1.4` released on `2015-05-07`

## Integrate Tutorial

[http://wiki.dataeye.com/h5/document/html5/html5-advanced-guide.html#part4](http://wiki.dataeye.com/h5/document/html5/html5-advanced-guide.html#part4)
