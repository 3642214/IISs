
### 12.1建筑作用
技术互操作性是交流位和使用信息交换基础设施字节和明确定义底层网络和协议的能力。句法互操作性是在一个共同的数据格式进行信息交换，以共用通讯协议来组织数据和用于信息交换的明确定义的格式的能力。句法互操作性需要技术的互操作性。

* 连接架构层，有利于信息是如何明确结构和端点解析。它的作用是提供机制，以实现端点之间的语法互操作性。常见的例子有数据结构的编程语言和架构的数据库。该功能通过OSI概念模型或互联网模型的应用层7（应用程序）跨越5层（会话）（见表12-1）。
在数据管理横切函数的数据服务框架基础上提供的连接框架实现端点之间句法互通性的基础。这反过来，提供了对“动态组合和自动互通”需要语义互操作的基础，在第16章中讨论。

------------ | ------------- | ------------ | ------------
Crosscutting Function | Model (ISO/IEC 7498) [15] | |
Connectivity Framework Layer | 7. Application 6. Presentation 5. Session | Application Layer | Syntactic Interoperability Mechanism introduces a common structure to exchange information. On this level, a common protocol to structure the data is used; the format of the information exchange is unambiguously defined.
Communication Transport Layer | 4. Transport 3. Network 2. Data Link 1. Physical | Transport Layer Internet Layer Link Layer | Technical Interoperability: provides the communication protocols for exchanging data between participating systems. On this level, a communication infrastructure is established allowing systems to exchange bits and bytes, and the underlying networks and protocols are unambiguously defined.
IIC参考架构范围|对应于OSI参考|对应于互联网模式（RFC 1122）[16] |对应于概念的互操作性水平[13]
横切功能|模型（ISO / IEC 7498）[15] | |
连接架构层| 7.应用6.表示5.会话|应用层|句法互通机制引入了一个共同的结构，以交换信息。在这个层面上，公共协议来组织数据被使用;的信息交换的格式明确定义。
通信传输层| 4.运输3.网络2.数据链路1.物理|传输层网络层链路层|技术互操作性：提供用于参与系统之间交换数据的通信协议。在这个层面上，一个通信基础设施建立允许系统交换比特和字节，以及底层网络和协议被明确定义。

Table 12-1 Role and scope of the connectivity functional layers
表12-1的连接功能层的作用和范围

### 12.2 KEY SYSTEM CHARACTERISTICS
*时延和抖动：正确的答案发送太晚往往是错误的答案。因此，延迟时间必须在限制和低抖动是需要可预测的性能。
*吞吐量：是需要高吞吐量时，大量的信息交换在很短的时间。

高吞吐量和低延迟经常竞争的要求。因为IISs需要短的反应时间和紧密协调，以保持有效控制所述现实世界的过程低延迟和抖动通常比通过更为关键。

连接安全架构方面的考虑：一系统内不同行为者之间的信息交流发生在记录表12-1中的两个抽象层，这两者在设计安全解决方案时，包括保密性，完整性，可用性，可扩展性，适应能力必须考虑，互操作性和性能。

* cryptographically strong mutual authentication between endpoints
* authorization mechanisms that enforce access control rules derived from the policy, and * cryptographically backed mechanisms for ensuring confidentiality, integrity, and
* 端点之间的保密性强的相互认证
* 强制实施，从政策衍生的访问控制规则授权机制，以及
* 加密备份，确保保密的信息交换，完整性和新鲜度的机制。
操作：IISs一般需要保持连续运行（参见6.3节）。因此，它必须是可以监控，管理和动态替换连通功能的元素。监测可以包括健康，性能和服务水平的连通功能的特性;管理包括配置和管理能力;动态替换可以包括能够替换硬件和软件或同时系统正在运行。

### 12.3 连通框架层重点功能特性
* The data formats associated with the services
* 与服务相关的数据格式
* 端点参与信息交流
在连接框架发现机制应该提供一种手段：

* 授权权限（如读，写），以参与信息交换的端点授予
数据交换模式：一种连接框架应该支持以下信息交换模式，典型的IIS。

* 客户端 - 服务器是一种非对称信息交流，其中终端分为“客户端”或“服务器”角色。 “客户”可以启动由端点在“服务器”角色完成一个服务请求。端点可以工作在一个客户端和一个服务器role.This图案有时也被称为“拉”或“请求 - 应答”或“请求 - 响应”风格图案。
* 发布 - 订阅就是终端分为“发行商”或“用户”的信息交换模式。不考虑用户的发布者可以“发表”一个众所周知的主题。订户可以从著名的主题“预订”信息，而出版商的问候。因此，该主题充当该解耦出版商形成订户的信道。其结果是松散耦合可独立更换上彼此端点。端点可以工作于一个发布者和用户角色。这种模式有时也被称为“推”风格图案。
* 至少一次输送，有时也被称为可靠传送。这是典型的事件和通知的。
* 恰好传递一次：这是典型的工作调度，有时被称为“一次且仅一次”交付。
infrastructure.
## 12.4 通信传输层的主要功能特性
* Broadcast for one-to-all communication between endpoints, where “all” refers to all the endpoints present on the communication transport network at the time of transmission
*组播的端点之间的一个一对多的通信
*广播为一对的所有端点之间的通信，其中，“所有”，是指所有在发射的时间存在的通信传输网络上的端点

* 枢纽和辐条
* 网状
* 等级
* 以上的组合
它不排除其他。

跨度：在逻辑架构视图中的通信传输网络可以跨越多个物理地域跨越。在物理视图，一个逻辑通信传输网络可以跨越只是局部区域（LAN），或跨度横跨大的地理距离的广域网（WAN），或在（MAN）之间跨越的某处。

有两种类型的常部署连接网关：
* 连接框架网关扩大整个连接框架技术连接的逻辑范围。它们保持的数据的逻辑结构，但可以改变表示（例如二进制格式与串格式）。