# 强化学习自学

- [AlphaZero五子棋](https://github.com/hangzhang23/ReinforcementLearning/tree/main/AlphaZero)

这个项目使用了价值策略网络和MCTS，其中game.py建立了五子棋的游戏环境，train.py包括了整个五子棋的训练过程。整个训练过程可以通过设置TrainPipeline()中的参数调整迭代次数epoch，棋盘长宽，随机走子playout模拟的局数。

只在colab上训练10$\times $10的棋盘500个epoch，策略情况不是很好，看其他教程至少需要3000才能得到更好的效果。目前提交的最优model是大约迭代350次（7/3）的模型，有时会出现current_policy保存的胜率跟best_policy一样，但是loss更低，这时推荐用更新的policy。

执行代码：
```
python human_play.py <modelname>
```
会读取保存好的current_policy或者best_policy模型，后面参数modelname根据情况选择输入best_policy.model或者current_policy.model，然后就可以人机对弈，直到得出胜负。
