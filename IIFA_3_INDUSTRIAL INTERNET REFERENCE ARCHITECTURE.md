## 3 INDUSTRIAL INTERNET REFERENCE ARCHITECTURE
## 3 工业互联网参考架构
### 3.1 INDUSTRIAL INTERNET ARCHITECTURE FRAMEWORK
### 3.1 工业互联网体系结构
Many stakeholders are involved when considering complex systems such as those expected of Industrial Internet Systems (IISs). These stakeholders have many intertwining concerns pertinent to the system of interest. Their concerns cover the full lifecycle of the system, and their complexity calls for a framework to identify and classify the concerns into appropriate categories so that they can be evaluated and addressed systematically.
考虑到复杂的系统，如预期的工业互联网系统（IISs）的时候，许多利益相关者有参与进来。这些利益相关者有关的感兴趣的系统很多相互交织的关注。他们的关注覆盖系统的整个生命周期，和它们的复杂性要求的框架，以识别和分类的问题纳入适当的类别，以便它们可以评估和系统地处理。

在ISO/ IEC/ IEEE42010：2011标准规范编纂的各项公约和共同架构和实践提供了一个核心本体为架构的描述。所述IIAF采用在本说明书中，例如，一般的概念和构造架构和架构框架，关心，利益相关者和观点。

The term concern refers to any topic of interest pertaining to the system. A stakeholder is an individual, team, organization or classes thereof, having an interest in a system. A viewpoint consists of conventions framing the description and analysis of specific system concerns.
术语关注是指与所述系统相关的兴趣的任何主题。风险承担者是个人，团队，组织或类物，有兴趣的系统。视点由公约框架的具体制度关注的描述和分析。
利益相关方，关注，观点和他们的关系，如图3-1所示，形成体系结构框架的基础。工业网络参考架构是完全被分析的一系列观点中的具体问题描述。

>Example: Suppose we want to address the concerns of what the functional subsystems are,

![](./IISs/QQ20160114-0.png)

### 3.2 INDUSTRIAL INTERNET VIEWPOINTS
### 3.2 工业互联网观点

The various concerns of an IIS are classified and grouped together as four viewpoints:
一个IIS的各种关注进行分类，聚合为四种观点：
* 业务
* 用法
* 功能
* 实现

As shown in Figure 3-2, these four viewpoints form the basis for a detailed viewpoint-by- viewpoint analysis of individual sets of Industrial Internet System concerns.
如图3-2所示，这四个观点形成的基础，工业互联网体系的担忧各组的详细观点逐角度的分析。
![](./IISs/QQ20160114-1.png)

The Business Viewpoint attends to the concerns of the identification of stakeholders and their business vision, values and objectives in establishing an IIS in its business and regulatory context. It further identifies how the IIS achieves the stated objectives through its mapping to fundamental system capabilities.
业务视点照顾到利益相关者的识别目标，在业务和管理方面建立IIS的关注，他们的业务愿景，价值观和。它进一步明确了如何在IIS通过其映射到基本的系统功能，实现了既定目标。

These concerns are business-oriented and are of particular interest to business decision-makers,product managers and system engineers.
这些问题都是以企业为主体，并特别感兴趣的企业决策者，产品经理和系统工程师。

用法的观点解决预期的系统使用情况的关切。它通常表示为涉及能够提供在最终实现其基本的系统功能，它的预期功能的人类或逻辑用户的活动序列。
这些问题的利益相关者通常包括系统工程师，产品经理和其他利益相关者，包括参与在IIS中所考虑的规范谁和谁代表了用户在其最终用途的个人。

The functional viewpoint focuses on the functional components in an IIS, their interrelation and structure, the interfaces and interactions between them, and the relation and interactions of the system with external elements in the environment, to support the usages and activities of the overall system.
功能视点集中于在一个IIS的功能部件，其相互关系和结构，它们之间的接口和交互，和指向与该系统与环境中的外部因素的相互作用，以支持整个系统的用途和活动。


这些问题尤其吸引系统和组件架构师，开发人员集成商和系统操作者。

### 3.3 SECURITY ACROSS THE VIEWPOINTS
### 3.3 安全横跨观点

Security of industrial control systems today often relies on physical security, the isolation of the systems and the obscurity of proprietary communication protocols. Industrial Internet Systems, on the other hand, are, by nature, connected and distributed. They continually exchange data; they are deeply integrated with enterprise systems; and they evolve over their lifetimes, converging with other IISs. Consequently, their attack surface is significantly larger than isolated industrial control systems.
工业控制系统今天往往依赖于物理安全，系统的隔离和专有通信协议的默默无闻的安全性。工业互联网系统，另一方面，是在本质上，连接及分发。他们不断地交换数据;他们深深地与企业系统集成;他们发展了自己的一生，与其他国际战略研究所融合。因此，他们的攻击面是不是孤立的工业控制系统显著较大。
IISs要求的综合方法安全跨越物理世界（包括直接观测性），在网络世界（包括保存的权利，使用数据），和商业世界（包括财产权和权利，使合约）。他们根本不把安全性作为一个单独的，附加的设计问题。

#### 3.3.1 AN INTEGRATED APPROACH TO SECURITY
#### 3.3.1 综合处理安全

The IIC Reference Architecture therefore integrates security policies for physical plant, hardware,software and communication as core to system design, across all the viewpoints:
因此，IIC参考架构集成了物理设备，硬件，软件和通信为核心，以系统设计的安全策略，在所有的观点：

* 用法视点力图使安全对用户透明，尽量减少它们的参与，并建立机器对机器的协议和人类交互之间有很强的分化。
* 功能视点定义了安全功能必须被提供用于每个功能域，以及它们如何协同工作，以对整个系统提供一致的安全性。
* 实现观点适用的安全技术相对于通用的架构模式和系统组件。

#### 3.3.2 THREAT MODELING AND SECURE DESIGN
#### 3.3.2 威胁建模和安全设计

[^5]:A structured analysis to identify, quantify, and address the security risks associated with an application or a system.

* 特征是失败与安全相关
* 跨越信任边界分隔不同信任级别或领域的功能。

Secure system design requires consideration of not only threats and the typical software issues,but also hardware design at chip and device level, physical plant design, a robust personnel security program and supply chain security.
安全系统设计需要考虑的不仅是威胁和典型的软件问题，而且在芯片和设备级，物理设备的设计，强大的人才保障计划和供应链安全的硬件设计。
