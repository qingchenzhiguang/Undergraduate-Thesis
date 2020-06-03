# 基于LDA主题模型的投资者情绪对股价影响研究

## 摘要
投资者情绪一直是金融领域研究的热点，并且从短期看，股票市场波动受投资者情绪影响较大。我国A股市场的散户投资者比例较高，使得对众多散户投资者情绪的研究具备了现实意义。

本文基于行为金融学理论和自然语言处理技术，选取上证50指数15只成分股，以东方财富股吧投资者发帖和评论文本为研究对象，分析其表现的投资者情绪对股票超额收益率的影响，进一步的，探究了投资者情绪对股价影响的非对称效应和对超预期盈余的解释力度。针对帖子常常反应投资者抱怨，从而产生大量噪声的问题，采用LDA主题模型对帖子进行主题分类，提取出海量帖子中与股价相关的隐含信息。针对帖子长度普遍较短而无法准确训练主题模型的问题，采用帖子+评论聚合模式将同一帖子下的内容连接成长文本进行主题模型训练。利用百度AI情感倾向分析技术和Python中文情感分析包snownlp，以句子为单位进行情感倾向分析，分析各主题帖子展现的投资者情绪。

研究结果表明：（1）使用经主题分类的情绪指标能提取出海量股票文本中的价值信息，与股票超额收益率正相关；（2）不同主题情绪对股票超额收益的影响程度和持续性不同；（3）主题情绪对股票超额收益率的影响存在非对称效应；（4）主题情绪能有效解释公司超预期盈余。本文研究结论对股市投资者情绪研究具有一定意义和价值，为该领域研究提供了一种独特的切入视角。

## 代码运行步骤

1. `1 财富网贴吧爬虫-帖子列表.py`，得到帖子列表
2. `2 财富网贴吧爬虫-帖子明细.py`，得到帖子详细内容
3. `LDA.py`，确定LDA最优主题数、训练LDA模型、生成词云图
4. `Sentiment_Analysis.py`，情感分析
5. `Summary.py`，生成样本和情感分析结果概览
6. `回归.ipynb`，进行回归