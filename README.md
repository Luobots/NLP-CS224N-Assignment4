## NLP-CS224N-Assignment4
#任务三：Seq2Seq模型实现 (1 week ~ 2 week)

__参考__ ：我们提供了LSTM、Seq2Seq、Attention的参考资料

__环境__ ：在Python下配置python=3.5/numpy/scipy/tqdm/docopt/pytorch/nltk/ torchvision；我们提供了conda的env.yml。

- 实现utils.py中的pad sends函数，对batch中的example进行padding补全。
- 实现model_embeddings.py中\__init__函数，对source和target embeddings进行初始化。
- 实现nmt_model.py中的\__init__函数，对NMT模型参数进行初始化，包括embedings(使用model_embeddings中的embedding），LSTM（layer、dropout、projection)。
- 实现nmt_model.py中的encoder函数，将输入句子转换为hidden表示，可以执行：python sanity_check.py 1d进行初步的正确性检查
- 实现nmt_model.py中的decoder函数。该函数通过逐步调用step函数将hidden表示进行解码。可以执行：python sanity_check.py 1e进行初步的正确性检查。
- 实现nmt_model.py中的step函数。该函数对解码过程中的LSTM cell进行计算，包括target word的encoding h\attention encoding e\output encoding o。可以执行：python sanity_check.py 1f进行初步的正确性检查。
- 实现nmt_model.py中的generate sent masks函数，对batch中添加的padding进行mask操作（参考step函数中如何使用mask）
- 运行代码（要求最终BLEU不低于21）
  1. 产生vocab文件：sh run.sh vocab
  2. 训练：sh run.sh train
  3. 测试：sh run.sh test
