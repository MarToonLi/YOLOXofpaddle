# 2021年8月份

### 12号
- ubuntu下的 tree命令 比较清晰的了解当前目录下的文件树结构；
  
- 查看 文本内容 的方式是 cat 全部读取并显示在shell中，tac是从最后一行开始显示；
head 读取前几行 tail 显示后几行
  
- COCO数据集以及VOC数据集的数据与标注的 较为详细的信息介绍：https://github.com/PaddlePaddle/PaddleDetection/blob/release/2.1/docs/tutorials/PrepareDataSet.md
包括目标检测区域位置的表示方法、数据集的自动下载以及各类文件各个字段的说明，同时涵盖自定义数据集的说明。
  
### 13号
- 目前完成了对YOLOX模型部分的Paddle化，并通过测试验证了模型结构的可行性，与原模型进行了对比。
- paddle.flops API 能够轻松实现对模型的计算量和参数量信息的输出，比较方便；但是因为其对数据的保存类型为int32，因此在YOLOX模型中，发生了栈溢出，现象是 个别数值含有负号。
目前使用的是paddle2.1.2.post1 仍未对该问题修改。
