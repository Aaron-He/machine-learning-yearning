## 9. 优化和满足指标

这是组合多个评估指标的另一种方法。

假设你同时关心算法的准确率和运行时间。你需要从三个分类器中选择：

![](pics/9.1.jpg)

通过将准确性和运行时间放入单个公式中来导出单个度量指标似乎不太自然，例如：

Accuracy - 0.5 * RunningTime

以下是你可以做的事情：首先，定义什么是“可接受”的运行时间。假如任何100ms以内运行时间的算法都是可以接受的。然后，从满足时间要求的分类器里，最大化准确性。这里，运行时间是一个“满足度量”——你的分类器必须在这个度量上做的“足够好”，因为它最多是100ms。准确率是“优化指标”。

如果你需要权衡N个不同的标准，例如模型的二进制文件大小（这对移动应用很重要，因为用户不想要下载大型应用程序）、运行时间和准确率，你可以设置N-1个作为“满意”指标。然后定义最后一个为“优化”指标。例如，二进制文件大小和运行时间设置一定的阈值，并尝试根据这些约束条件的来优化准确率。

最后一个例子，假设你正在构建一个使用麦克风来监听用户说出特定“唤醒词”，检测到“唤醒词就唤醒系统的硬件设备。例如亚马逊的Echo倾听“Alexa”，苹果siri的“Hey Siri”，安卓的“Okay Google”及百度应用的“你好，百度”。你关心的是假阳性率及假阴性率。假阳性率指没有人说唤醒词系统醒来的频率，假阴性率是当有人说唤醒词系统没有醒来的频率。一个合理的目标是在满足每运行24小时不会有一个假阳性（满足指标）的情况下，最大限度的减少假阴性率（优化指标）。

一旦你的团队按照评估指标进行优化，他们将能够加快进度。







