# Part II: Analysis of Key System Concerns
# 第二部分：重点关注系统的分析






## 8 安全
安全是系统有问题的紧急性，并具有系统工程两大影响：

* 一个无法预测在特定情况下的系统的安全性而不先预测该系统在这种情况下的行为。
* A software component corrupting the data or instructions of another.
* A device on the network becomes a “babbling idiot” and preventing other components from communicating in a timely manner.
* A can of liquid on a conveyer spilling and causing the floor near the machine to become
* A motor drawing more power than expected causing a brownout affecting other devices
* 软件组件从另一个占用CPU资源。
* 一个软件组件破坏他人数据或指令。
* 网络上的设备将成为“咿呀学语白痴”，防止其他部件的及时沟通。
* 液体在传送带上溢出而导致机器附近的地板上能够变得湿滑，导致移动机器人失去牵引力。
* 马达吸引更多的权力比预期造成影响同一分支电路中的其他设备掉电。


### 8.1 与其他问题关系

在安全关键系统的可靠性和应变能力方面的作用：无论是“可靠性”，也没有“弹性”意味着系统的安全。实际上，可以有可靠的系统，是不安全的，因为它们可靠地进行不安全行为，并且有可能不可靠的系统是安全的。即便如此，可靠和灵活的基础设施是有用的，有时有必要支持一个更大的系统的安全关键功能。的支持可靠性和弹性特征的示例包括容错计算和通信，复制通信，分布式一致性协议，自适应控制算法，和'硬化“组分，如抗辐射加固的CPU和存储器。不幸的是，更高的可靠性可能会增加成本。这可以在架构层面来缓解：国际战略研究所可分割的基础设施，以便通过安全和非安全功能利用的基础设施之间的分离。安全功能驻留在一高可靠性（或高弹性和高安全性的）分区，而非安全功能部署在一个较不可靠的（但便宜）分区。
