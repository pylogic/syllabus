# 文本流处理系统

Ganben

### 简介

这个系统提供以下功能：

1. 从新闻网页、[微博](http://open.weibo.com/wiki/Statuses/public_timeline/en)等来源获取数据，解析，抽取转换为中文简体文本
2. 利用监督学习、非监督学习技术实时处理：包括[过滤](http://www.infoq.com/cn/articles/text-filtering-system)和[学习]()为[主题模型](https://github.com/RaRe-Technologies/gensim)和其他的模型
3. 使用[NLP技术](http://www.nltk.org/)，将文本进行分词，POS Tag和NER
4. 使用面向大数据的NoSQL数据库存储N-Ary知识库模型的处理结果
5. 使用[GraphQL](https://developer.github.com/v4/)提供系统自身和处理结果的API

### 开发环境

- 程序语言：Python3.5+  Java JDK 1.8+
- 流处理和消息系统：[Spark2](http://spark.apache.org/docs/latest/programming-guide.html) dev by Python
- 数据库：MongoDB + GraphDB
- 运行环境：LVM Ubuntu 16.04 x64 单机/分布式

### 系统架构

系统由尽可能单一功能，低耦合，方便调用的模块组成。
