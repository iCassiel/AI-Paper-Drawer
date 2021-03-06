# [GATED GRAPH SEQUENCE NEURAL NETWORKS](https://arxiv.org/pdf/1511.05493.pdf)

## 模型流程
- 首先通过类似`GCN`的操作获得的单层输出作为`GRU的输入`，结合`上一层的隐向量`计算`GRU输出`作为`本层输出`，具体公式如下：

![](ggnn1.png)
- 考虑输入为一个有向图
- 1）对于每个节点，以它的初始值`x_v`作为`GRU`的初始隐向量`h_v`，如果`x_v`的维度小于预定义的`h_v`维度则在后面补`0`
- 2）进行一次局部传播，把入边和出边所连接到的局部领域信息聚合到中心节点作为`当前时间步GRU单元`的输入
- 3/4/5/6）[GRU单元计算](https://github.com/cy69855522/AI-Paper-Drawer/blob/master/sources/papers/5C7571627E797E773040786271637530427560627563757E647164797F7E63306563797E7730425E5E30557E737F7475623D5475737F74756230767F6230436471647963647973717C305D717378797E75304462717E637C7164797F7EBFE673402/README.md)

## 参考
- [CSDN 论文笔记：GGNN (门控图神经网络)](https://blog.csdn.net/lthirdonel/article/details/89286522)
