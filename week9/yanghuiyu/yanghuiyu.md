# 杨慧宇

1.实验：通过设置词频，使分类器可以区分“不需要”和“需要”。发现的问题：设置词频确实在分词阶段将“不需要”作为一个整体，但embeddings层没有对应的字符，还是无法识别。通过修改embeddings文件，“不需要”的问题已经解决，但还有其他未识别出的字符。

2.代码：找出embeddings层识别为0(unk)的字符集合（目前有bug）。

3.实验：使用刘雨设计的问答use case测试整合进项目的A、C、D分类器。目前存在的问题有：“骗子”一类的对话识别不当，会把一些其中存在否定、疑问等字符（但不是拒绝）的句子判为拒绝。