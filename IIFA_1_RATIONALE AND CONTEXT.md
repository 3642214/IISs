## 1 RATIONALE AND CONTEXT
## 1 原理及背景
它定义了工业网络系统，并指定一个工业网络体系结构框架中的工业网络参考架构的发展，文件和通讯，以帮助。我们首先描述我们的范围。
### 1.1 工业互联网


The Industrial Internet concept is one that has evolved over the last decade to encompass a globally interconnected network of trillions of ubiquitous addressable devices and collectively representing the physical world.
工业互联网概念是一个已经发展在过去十年中，以涵盖全球互联的无所不在的寻址装置万亿和集体代表物理世界的网络。

The Industrial Internet effort will bring industrial control systems online to form large end-to-end systems, connecting them with people, and fully integrating them with enterprise systems, business processes and analytics solutions. These end-to-end systems are referred to as Industrial Internet Systems (IISs). Within these IISs, operational sensor data and the interactions of people with the systems may be combined with organizational or public information for advanced analytics and other advanced data processing (e.g., rule-based policies and decision systems). The result of such analytics and processing will in turn enable significant advances in optimizing decision-making, operation and collaboration among a large number of increasingly autonomous control systems.
工业互联网的努力会带来工业控制系统网络，形成大的终端到终端系统，与人连接它们，并充分与企业系统，业务流程和分析解决方案整合它们。这些终端到终端系统被称为工业互联网系统（IISs）。在这些国际战略研究所，操作传感器数据和人与系统的交互可以与组织或公共信息高级分析等先进的数据处理（例如，以规则为基础的政策和决策系统）相结合。这样的分析和处理的结果将反过来使在优化中的大量日益自主控制系统的决策，操作和协作显著进展。

Industrial Internet systems cover energy, healthcare, manufacturing, public sector,




>例如：一个参考架构的住宅规定，所有居住房屋需要提供一个或多个卧室，浴室，一间厨房和起居区。这套房间是访问通过门，走廊和楼梯的房子里面，从外面通过主和后门。房子提供了对如火灾，飓风和地震威胁安全的环境。房子的结构需要维持风雪荷载，可能会在其本地环境中找到。房子需要提供合理的措施，以发现并防止未经授权的入侵。

A reference architecture provides a common framework around which more detailed discussions can center. By staying at a higher level of abstraction, it enables the identification and comprehension of the most important issues and patterns across its applications in many different use cases. By avoiding specifics, a reference architecture allows subsequent designs to follow the reference architecture without the encumbrance of unnecessary and arbitrary restrictions.
参考架构提供了一个通用框架，在其周围更详细的讨论能中心。通过住在一个更高的抽象水平，它能够跨越其应用的最重要的问题和模式，在许多不同的使用情况下，识别和理解。通过避免细节，参考架构允许随后的设计遵循参考架构没有不必要的和任意限制的累赘。
### 1.3 INDUSTRIAL INTERNET REFERENCE ARCHITECTURE
### 1.3 工业互联网参考架构
The Industrial Internet Reference Architecture (IIRA) is a standard-based open architecture for IISs. To maximize its value, the IIRA has broad industry applicability to drive interoperability, to map applicable technologies, and to guide technology and standard development. The description and representation of the architecture are generic and at a high level of abstraction to support the requisite broad industry applicability. The IIRA distills and abstracts common characteristics, features and patterns from use cases well understood at this time, prominently those that have been defined in the Industrial Internet Consortium (IIC). The IIRA design is intended to transcend today’s available technologies and in so doing is capable of identifying technology gaps based on the architectural requirements. This will in turn drive new technology development efforts by the Industrial Internet community.
工业网络参考架构（IIRA）是一个基于标准的开放式体系结构的工业互联网系统。为了最大限度地提高它的价值，爱尔兰共和军拥有广泛的行业应用推动互操作性，以映射适用技术，并指导技术和标准的发展。该体系结构的描述和表示法是通用的，抽象，以支持必要的广泛工业应用性高的水平。所述IIRA蒸馏和提取的共同特点，特征和从用例模式很好地理解，在这个时候，显着那些在工业互联网协会（IIC）被定义。该IIRA设计旨在超越当今现有的技术并在这样做能够识别根据建筑要求的技术差距。这将反过来推动由工业互联网界新技术的开发力度。
### 1.4 MAJOR COMPONENTS OF THE TECHNICAL REPORT
### 1.4 技术报告的重要组成部分
This technical report is divided into two parts. The first part (Chapters 1~7) provides rationale and context for the types of system under consideration (Chapter 1), and their key characteristics (Chapter 2), the architectural framework we use to describe the reference architecture (Chapter 3), and each of the component parts (‘viewpoints’) of the reference architecture (Chapter 4~Chapter7). The second part (Chapters 8~16) provides an analysis of key system concerns that require consistent analysis across the viewpoints to ensure concerted system behaviors. We conclude with references (Chapter 17).
此技术报告是分为两部分。第一部分（章节1〜7）提供了所考虑的理由和上下文系统的类型（第1章），并且它们的主要特征（第2章），建筑框架我们用来描述参考架构（第3章），及每个参考架构的组成部分（“视点”）的（第4〜第7章）。第二部分（章节8〜16）提供了需要跨观点考虑一致分析，以确保一致的系统行为的关键系统的关注的分析。最后，我们引用（第17章）。



The publication of this first version of this Technical Report enables feedback. As more use cases are developed, more real systems built, and more IIC testbeds deliver results, we will continuously explore the general architecture of Industrial Internet Systems, guided by the feedback from these activities, both to refine this document and produce new works built on it. Meanwhile, we shall define which standards and technologies fit into the building blocks of the reference architecture, identify gaps and define requirements for improvement.
这个技术报告的第一个版本的发布使反馈。随着越来越多的用例的开发，更真实的系统构建，更IIC测试平台取得成果，我们将不断探索实业互联网系统，通过这些活动的反馈指导的总体结构，既要完善这一文件，并产生建立在新的作品 它。同时，我们将定义哪些标准和技术融入参考架构的基石，找出差距，明确改进的要求。