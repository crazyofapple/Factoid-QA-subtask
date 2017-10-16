# 评测描述
q | a
---- | ---
任务类型 | Factoid Q&A subtask
评价指标 |  Accuracy计算预测答案和标准答案是否精确匹配、F1计算预测答案相对标准答案的词级重合度）
问题类型 | 事实类
问题数量 |  3万
候选篇章 |  每个问题10个候选篇章（提供来源网页URL）
标准答案数量 |  唯一答案
标准答案产生方式 |  完全从候选篇章中截取
标准答案长度 |  20字以内
参赛者提交答案 |  针对每个问题，从候选篇章中提取答案文本

**对于每个事实类问题q，标注人员阅读相应候选答案篇章a1，a2，…，an，从候选篇章中抽取合适的词语、短语或句子，形成一段正确、完整、简洁的文本，作为问题的标准答案a***


# 样例
```
{
“query_id”: 10000,
“query”: “中国最大的内陆盆地是哪个”,
“passages”: [
{“passage_id”: 1, “url”: “https://zhidao.baidu.com/
question/713780769091877645”, “passage_text”: “中国新疆的塔里木盆地，是世界上最大的内陆盆地，东西长约1500公里，南北最宽处约600公里。盆地底部海拔1000米左右，面积53万平方公里。”},
{“passage_id”: 2, “url”: “http://www.doc88.com/p-093375971649.html”, “passage_text”: “中国最大的固定、半固定沙漠天山与昆仑山之间又有塔里木盆地，面积　５３　万平方公里，是世界最大的内陆盆地。　盆地中部是塔克拉玛干大沙漠，面积　３３．７　万平方公里，为世界第二大流动性沙漠。”},
……]
“answer”: “塔里木盆地”,
“type”: “factoid”
}
```


# 结果提交
参赛者每次按要求提交的内容包括：

（1）全部源代码和数据；

（2）程序在测试集上的执行流程说明，以及程序说明文档。

参赛者的测试结果在评测方提供的计算环境里完成计算：基于参赛者提交的代码在评测方提供的平台上按指定命令方式执行

# 时间

时间 | 事项
---- | ---
2017年9月1日 | 开始报名
2017年9月22日 | 发布第一批事实类问答任务的训练集（针对所有参赛选手）
2017年10月10日 | 发布事实类问答任务的验证集（针对所有参赛选手）
2017年10月16日 | 	开放选手提交结果入口
2017年10月23日 | 发布排行榜（持续更新）
2017年11月1日 | 发布第二批事实类问答任务的训练集（针对已经提交结果的参赛选手）
2017年11月24日 | 发布第三批事实类问答任务的训练集（针对已经提交结果的参赛选
2018年 | 2018年CIPS学术年会上举行颁奖仪式


# 模型
## 数据预处理

1. 分词，分字
2. 词性标注，命名实体识别
3. 统计词频，tf-idf
4. 句法分析，依存关系表示学习
5. 训练词向量
6. N-gram向量
7. 建立词库，字库
8. 主题词，关键词抽取

## 数据清洗

## 数据分析

# 特征抽取
1. 词向量
2. 依存关系表示
3. 子向量
4. 上下文表示
5. N-gram
6. 文档中词是否在问题中出现
7. 

## 模型构建


## 模型融合

## 答案选择
