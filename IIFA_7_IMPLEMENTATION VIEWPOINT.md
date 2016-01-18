## 7 IMPLEMENTATION VIEWPOINT
## 7 实现观点


* 一个IIS的一般结构：其结构和元件的分布，从而使它们相互连接的拓扑结构。
* 它的组成部分，其中包括接口，协议，行为等性能的技术说明。
* 在使用视点到上述功能部件，并从功能组件的执行部件确定的活动的实现的地图。
* 一个实现地图的关键系统特性。

[^21]: This version of the RA will not attempt to address regulatory and compliance requirements. These are substantially different by vertical, and may be addressed in more detail in future documents.

### 7.1 ARCHITECTURE PATTERNS
### 7.1 架构模式

* Multi-Tier Data Storage architecture pattern (This pattern supports a combination of storage tiers (performance tier, capacity tier, archive tier.)
* 网关介导边连通性和管理架构模式
* 边到云架构模式（这种模式与对比，因为它假设一个广域连接性和可寻址的设备和资产网关介导的模式。）
* 多级数据存储体系结构模式（这种模式支持的存储层（表现层，能力层，归档层的组合。）
* 分布式分析架构模式。

我们描述了因为在他们的IISS普遍存在较强的前两种模式在前面的列表中。

#### 7.1.1 THREE-TIER ARCHITECTURE PATTERN
#### 7.7.1 三层架构模式
三层架构模式包括边缘，平台和企业层次。这些层在处理数据流和控制流（见第6节）参与使用活动起着特殊的作用。它们通过三个网络相连，如图7-1所示。

![](./IISs/QQ20160115-4.png)	

The edge tier collects data from the edge nodes, using the proximity network. The architectural characteristics of this tier, breadth of distribution, location, governance scope and the nature of the proximity network, vary depending on the specific use cases.




该服务网络，确保了服务于平台层和企业层之间的连接。这可能是一个覆盖专用网络通过公共互联网或互联网本身，使最终用户和各种服务之间的安全的企业级的。
		
![](./IISs/QQ20160115-5.png)		
		
The three-tier architecture pattern combines major components (e.g. platforms, management services, applications) that generally map to the functional domains (functional viewpoint) as shown in Figure 7-3.From the tier and domain perspective, the edge tier implements most of the control domain; the platform tier most of the information and operations domains; the enterprise tier most of the application and business domains. This mapping demonstrates a simple functional partitioning across tiers. The actual functional mapping of IIS tiers is usually not as simplistic and is highly depends on the specific of the system use cases and requirements. For example, some functions of the information domain may be implemented in or close to the edge tier, along with some application logic and rules to enable intelligent edge computing.


该平台层本身的操作域组件提供的服务（在图资产管理服务流。7-2）的其它组件，无论是在同一层或另一个。

例如，该平台层的数据（信息域）组分可以请求服务的操作域组件：
* The verification of asset credentials it receives in the data flows from the edge tier.
* 资产元数据的查询，所以可以增加从资产接收数据之前，在处理的下一阶段的数据被持久或馈送到分析。
Similar operations domain services can be provided to the application domain components in the enterprise tier as well. Conversely, the operations domain components may use data services from the information domain component in order to get better intelligence from asset data, e.g. for diagnostics, prognostics and optimization on the assets.


#### 7.1.2 网关介导EDGE连接和管理架构模式
网关介导的边缘连接和管理体系结构模式包括为IIS边缘的本地连接解决方案，与桥接到广域网络，如图7-4的网关。网关充当广域网的端点同时隔离边缘节点的本地网络。这种架构模式允许本地化操作和控件（边分析和计算）。它的主要优点是在打破IISS的复杂性，以使它们可以扩大两者在管理资产的数量，以及在联网。然而，它可能不适合于系统，其中资产是移动的方式，不允许本地网络边界内稳定簇。

边缘网关还可以用作用于设备和资产和数据聚集点处的一些数据处理和分析，以及控制逻辑本地部署的管理点。

本地网络可以使用不同的拓扑结构。

在一个轮毂和辐条拓扑，边缘网关充当边缘节点集群彼此连接和到广域网络的集线器。它具有集群允许在流数据从边缘节点中的每个边缘实体的直接连接，和出流控制命令给边缘节点。

在这两种拓扑，边缘节点是不能直接从广域网进行访问。边缘网关充当单一的入口点到边缘节点和作为管理点提供路由和地址转换。


* Site-specific decision and application logic that are perform within the local scope.
* 网络和协议桥接支承边缘节点和广域网之间的各种数据传输模式：异步，流，基于事件和存储转发。
* 包括聚合，转换，过滤，整理和分析本地数据处理。
* 设备和资产的控制和管理点局部地管理在边缘节点和作用的药剂经由广域网使边缘节点的远程管理。
* 站点具体的决定和应用程序逻辑中的本地范围内执行。
## 7.2 安全的执行


* confidentiality and privacy of the data collected,
* remote security management and monitoring,
* simultaneously addressing both existing technologies as well as new technologies, and
* seamlessly spanning both information technology (IT) and operational technology (OT)
* 保护设备到设备通信，
* 保密收集到的数据和隐私，
* 远程安全管理和监控，
* 同时解决现有的技术以及新技术，和
* 无缝跨越两个信息技术（IT）和运营技术（OT）子系统和进程，而与运营业务流程的干扰。


* 信息交流
* 管理和控制
* 数据分配和存储
