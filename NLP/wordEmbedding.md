# Word Embedding

## NNLM
根据前n-gram预测接下来的单词，最大化P(Wt|W1...Wt-1;theta)
W - Onehot编码的原始输入
Q - Embeeding Mat
C=WQ - Embedding值

## word2vec
CBOW: 去掉目标词，上下文预测目标词
Skip-gram: 去点上下文，目标词预测上下文
Word Embedding Layer -- Onehot层到embedding层的网络用预训练好的参数矩阵Q初始化了Forzen/Fine-Tuning
无法区分多义词

## ELMO==Embedding from Language Models
Paper:: Deep contextualized word representation
过程: LM学好embedding，在使用的时候根据上下文动态调整（双层双向LSTM）
原始Emb + 句法Emb + 语义Emb 权重求和整合为输入


