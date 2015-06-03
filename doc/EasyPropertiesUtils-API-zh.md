# EasyCommons-EasyPropertiesUtils

---------------
[EasyCommons](readme-zh.md "EasyCommons")  项目下的 Properties 文件操作工具类。 

Java提供的 java.util.Properties 不仅仅在设计上存在问题，并且功能异常简陋，一般除了读，在写上不具备实用性（会导致文件原格式和注释丢失）。在维护或写properties文件时必须自行实现写方案。

**使用EasyProperties可以完全替代java.util.Properties。**

## 1. Javadoc
[EasyPropertiesUtils Javadoc](../javadoc/easycommons-propertiesutils/index.html "EasyPropertiesUtils Javadoc")

## 2. API 简介
EasyPropertiesUtils 包括如下组件：

1. **EasyProperties**： 用来代替java.util.Properties的properties文件类， 扩展了java.util.Properties，提供了内容合并（merge: 增, 删, 改）和修改（modify: 增,改）功能，修改属性时不影响原格式。
**适合场景**：任何需要对properties文件进行读写操作的场景，不影响文件原格式。 
```JAVA
 /**
 * 两种properties文件修改方式（代替store方法）：
 * - merge：将Properties对象合并到指定文件（增，改，删）
 * - modify：将Properties对象修改到指定文件（增，改，不包括删除原文件中具有的参数）
 * 
 * @param propertiesFile 要修改的properties文件，支持path（字符串路径）和file（文件对象）作为参数
 * @param charset 文件的字符集，可选
 */
 mergeToFile(propertiesFile [, String charset]);
 modifyToFile(propertiesFile [, String charset]);
```

2. **EasyPropertiesUtils**： 直接修改Properties文件的工具类，提供原格式写功能，包括保留注释，支持内容合并（merge: 增, 删, 改）和修改（modify: 增,改）。
**适合场景**：对properties文件进行修改操作，又不影响原格式的情况。 
```JAVA
 /**
 * 直接将Map集合和Properties对象中的数据修改到指定properties文件，两种properties文件修改方式：
 * - merge：将Properties对象合并到指定文件（增，改，删）
 * - modify：将Properties对象修改到指定文件（增，改，不包括删除原文件中具有的参数）
 * 
 * @param propertiesFile 要修改的properties文件，支持path（字符串路径）和file（文件对象）作为参数
 * @param properties 支持Map或Properties类型的参数
 * @param charset 文件的字符集，可选
 */
 merger(propertiesFile, Map<String, String> properties [, charset]);
 merger(propertiesFile, Properties properties [, charset]);
 modify(propertiesFile, Map<String, String> properties [, charset]);
 modify(propertiesFile, Properties properties [, charset]);
```

## 结束

[留言评论](http://www.easyproject.cn/easycommons/zh-cn/index.jsp#about '留言评论')

如果您有更好意见，建议或想法，请联系我。


联系、反馈、定制、培训 Email：<inthinkcolor@gmail.com>

<p>
<strong>支付宝钱包扫一扫捐助：</strong>
</p>
<p>

<img alt="支付宝钱包扫一扫捐助" src="http://www.easyproject.cn/images/s.png"  title="支付宝钱包扫一扫捐助"  height="256" width="256"></img>


[http://www.easyproject.cn](http://www.easyproject.cn "EasyProject Home")