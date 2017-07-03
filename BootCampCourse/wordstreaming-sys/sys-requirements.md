# 文本流处理系统

Ganben

### 1 简介

这个系统提供以下功能：

1. 从新闻网页、[微博](http://open.weibo.com/wiki/Statuses/public_timeline/en)等来源获取数据，解析，抽取转换为中文简体文本
2. 利用监督学习、非监督学习技术实时处理：包括[过滤](http://www.infoq.com/cn/articles/text-filtering-system)和[学习](http://zake7749.github.io/2016/08/28/word2vec-with-gensim/)为[主题模型](https://github.com/RaRe-Technologies/gensim)和其他的模型，并在线更新
3. 使用[NLP技术](http://www.nltk.org/)，将文本进行分词，POS Tag和NER
4. 使用面向大数据的NoSQL数据库存储N-Ary知识库模型的处理结果
5. 使用[GraphQL](https://developer.github.com/v4/)提供系统自身和处理结果的API

### 2 开发环境

- 程序语言：Python3.5+ with PEP8 style, Java JDK 1.8+
- 流处理和消息系统：[Spark2](http://spark.apache.org/docs/latest/programming-guide.html) with [Streaming in Python interface](https://spark.apache.org/docs/latest/streaming-programming-guide.html)
- 数据库：MongoDB + GraphDB
- 运行环境：LVM Ubuntu 16.04 x64 单机/[分布式](http://radimrehurek.com/gensim/distributed.html#why-distributed-computing)

### 3 系统架构

系统由尽可能单一功能，低耦合，方便调用的模块组成。

- 爬虫模块：完成抓取--存储功能
- 分词和清洗模块：完成分词、自定义词典、调用语义推理模块实现逻辑
- 语义推理模块：引入PLY的lex和yacc方法执行规则匹配，实现自然语义推理
- 数据模块：建立数据库连接和大数据（spark）链接，调用推理模块，实现N-Ary关系模型和文档存储
- 语义模型模块：完成text to corpus的训练、更新和查询
- 脚本程序：引入以上模块，1：多线程开爬虫，分词和存储 2：开启服务进程完成语义学习，并提供API

### 4 核心功能

#### 4.1 文本爬取
文本爬取源：

- weibo使用[weibo API](http://open.weibo.com/wiki/2/statuses/public_timeline) ``http://api.t.sina.com.cn/statuses/public_timeline.json``


#### 4.2 在线学习
词汇模型训练与在线更新使用的[models.word2vec 方法](http://radimrehurek.com/gensim/models/word2vec.html)

	model.Word2Vec(sentences, size=250)
	model.build_vocab(sentences, update=True)
	model.train(new_sentences)
	model.update_weights()
	
