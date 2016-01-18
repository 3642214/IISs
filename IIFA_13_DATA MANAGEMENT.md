# 13 DATA MANAGEMENT
# 13 数据管理
* Publish and Subscribe
* Storage, Persistence and Retrieval
* Integration
* Data Framework
* Rights Management
* 削减和分析
* 发布和订阅
* 查询
* 存储，持久性和检索
* 积分
* 说明和状态
* 数据框架
* 权限管理

## 13.1 REDUCTION AND ANALYTICS
## 13.1还原和分析
Sensors and other systems in the IIS produce extremely large amounts of data.[^36] Transmitting all this raw data over the networks to a central data center is often unnecessary and prohibitively expensive, but insights contained in the raw data must not be lost.
通过发布和订阅部件在两个位置（位置透明）和时间（异步传送）去耦发布 - 订阅有贡献到IIS可靠性，维护和恢复能力。这降低了断层传播的可能性，并简化了增量更新和进化。在接收器侧的相互作用可以是周期性的（时间驱动）或响应（事件驱动），根据用户的需要。异步传输也可以处理IIS组件故障，如通过延迟而不是取消正在进行的数据传送操作的数据路径上的网络故障。

发布 - 订阅服务这些目的：

* 的数据源的一个大的，进化的数目可扩展的处理，如设备，以及大量数据的消费者。
* 最终用户，应用程序级的数据消费往往需要订阅模式，从整合在一个平台上的应用程序组件的数据。
* 从应用程序或管理服务，设备可靠的控制流程：控制命令可以多播的方式，使设备得到这些命令时，他们已经准备就绪。

*选择，使用为中心，以合并数据，最终用户和分析云中的访问，有可能
重播支持检索先前通过重放数据项中接收的顺序记录的IIS数据的集合。回放支持创建仿真环境，回归测试以及相关的II的用例。

大数据解决方案支持大量IIS Control Domain系统的数据。

* reliable storage and scalable archiving (Big Data).
* 用于模拟和各种形式的测试（录制和回放）的支持，
* 可靠的存储和可扩展的归档（大数据）。
* 支持功能类似传统的ETL，典型地在数据传输的第一阶段产生的，并初始存储前述。

描述和状态达到以下目的：

* design of a system management console applicable to various IISs and
* 增加新的类型具有不同的数据模型和通信方式的设备中，
* 系统管理控制台的设计适用于不同的IISs和
* IIS与不同的数据模型组成。
* 持续部署IIS测试和诊断
* 外包的IIS给第三方，如云提供商的数据相关的功能和
* 监管和合规性要求的支持。
# 14 分析和先进的数据处理
先进的数据处理可以根据各种架构模式来实现。一个共同的体系结构是一个管道和过滤器结构[17]，它允许将创建管道，在并联和串联，根据应用的要求，如在图14-2所示。在此组合性的值是双重的：

* pipelines need not be co-located allowing the processing to be deployed as appropriate.
* 管线不必共同位于允许处理被部署为适当。
一个管道饲料调度数据，与其他管线的挖掘这些数据流组成。每个分析管道具有特征的模型集：

* 存储：临时或长期性的资源，如缓冲器，存储器，磁盘，存储簇，分布式文件系统，使得提供给其他组件的数据，
* 分析：配置了算法的功能，这是使用的工程设计的接口，
* outgress：负责公开管道结果，
* 调度：管理并发访问，存储和调度分析的任务，
* 工程界面：设计时环境，用于指定和分析算法进行实验，并
* 客户端接口：提供访问数据，包括分析结果。
每个管道应具有一个入口和出口规范限定兼容性标准的调度和其它管道，并服务质量的一个规范设定响应时间的期望。

------------ | ------------- 
Data Flexibility  | New/unknown data types, without data model modification
数据灵活性|新的/未知的数据类型，而没有数据模型修正
算法的灵活性|多款支持库，查询交涉
生产力|付出与成本比率
静电容量|存储或配置永久
动态容量|处理或并发任务的同时管理数据
分析延迟|延时经历了核心数据处理
往返响应|经过时间的请求和响应之间
可扩展性|轻松，速度和变化的性能品质的负担能力
可靠性|平均无故障时间，运行时出现故障，采出程度，没有数据丢失
* 预测分析：确定预期行为，或基于使用统计和机器学习技术的预测模型的结果。
* 规范分析：建议用优化决策，模拟等。
分析的结果可以通过使用可视化分析，以支持人类的决策，以提高人的理解和产生信心的决定

* Streaming: continuous results flow of on-the-fly analysis of live streaming data in memory without storage persistence until after analysis completion.
* 实时：具有使适当和及时的行动，正确的定时信息近瞬时分析结果。
* 流：上即时分析在存储器实时流数据的连续结果流无存储装置的持久性，直到分析结束后。
* 活动：以使得能够发现系统的变化快速，准确的答复等组成积极共享实时模式的发现。
* 因果导向：识别挂靠在使用新的方法，如物理建模，并结合神经网络的深度学习的能力，物理模拟更好的分析很好理解的物理定律的数据复杂，因果关系。
* 分布：共享处理和结果的产生利用内部和跨II系统动态间和细胞内功能区的关系。
时序约束：如果网络延迟无法满足实时性要求或通信是不可靠的，分析必须在靠近数据源和消耗的结果的系统来执行。例如，自主汽车的图像分析的结果必须提供给模型执行人控制在几毫秒内驱动系统。