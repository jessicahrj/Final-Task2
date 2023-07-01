# Final-Task2
Final-Task2

# 项目要求
设计与第二次作业1模型 “相同参数量” 的Transformer网络模型，进行CIFAR-100的训练，并与期中作业1的模型结果进行比较，可使用data aug。data aug可以选用任何可用的策略，包括第二次作业使用的data aug；利用Tensorboard可视化第二次作业与期末作业2的训练和测试的loss曲线、测试acc曲线；

# 模型架构
## Vision Transformer
-	Batch Size: 128
-	Learning Rate: 1e-3, 学习率下降策略CosineAnnealingLR with eta_min=1e-5; 第一个epoch的warmup从0到1e-3
-	优化器：Adam优化器，betas = (0.9, 0.999)，weight decay=5e-5
-	Epoch：200
-	损失函数：CrossEntropyLoss
-	评价指标：top1 error 和top5 error
-	Data Augmentation: Mix up
-	其他参数：patch size=8；dim=512；depth=6；heads=6；mlp_dim=3072；dropout=0.1；emb_dropout=0.1
-	参数量：23,790,180，与ResNet50参数量基本相同
