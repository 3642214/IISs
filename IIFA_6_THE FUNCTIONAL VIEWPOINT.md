## 6 THE FUNCTIONAL VIEWPOINT 
## 6 功能视点
### 6.1 背景	
	
Industrial Control Systems (ICS) have been widely deployed to enable industrial automation
有些人可能会认为，工业互联网是什么传统上两个不同的领域有不同的目的，标准和支持学科成为结合：IT和OT.在IT（信息技术），一切都还原为代表思想在程序员的头部和改造的方式来生产有用的推论位 - 从数字的总和在任何一列电子邮件系统调度优化问题（例如，使用单）。的基本问题与这种方法中，指出作为在人工智能界的基本问题之一是所谓的“符号接地problem'-，在机码元（由处理器周围通过数字）只对应于世界因为用心的对象编程，他们的机器没有任何意义。在OT（作业技术）'控制'（传统模拟）已直接应用于物理过程，没有任何企图制造符号或模型以由机器进行处理。例如，PID（比例 - 综合 - 微分）控制器可以控制上使用由控制工程师定义并表现出特定的反馈方程工作用于特定应用的线的电压 - 有在一般性没有尝试并没有必要划分在多个处理单元的问题。 IT的发病率成OT世界主要来约因需要网络更大的系统，并建立控制机器的层次，同时也希望注入通用的IT理念融入OT世界（如调度和资源消耗的优化）。同时也出现了朝着控制，数字化模拟物理世界，并根据他们的控制决策的仿真模型，而不是一个控制工程师的方程的举动。这使得其他类型的已审查的IT方法，如机器学习，可以申请到OT。这也导致OT系统易受IT问题为好，如网络拒绝服务攻击和欺骗，以及前面提到的符号接地问题。 IT和OT持有来回进步的可能性很大的组合 - 具身认知 - 以一个系统，可以通过立足其表示对世界（而不是提供的编程模型）避免符号接地问题，只有自己的情景体验（和因此，不局限于认识论的人的观念）。然而，即使较近期的突破，将支持基于现实世界的数据，而不是工程模型可能产生实质性的改进先进的分析。关键的障碍是安全性和弹性。关键任务应用OT足够重要的是软件可靠性的一般水平是可以接受的，在IT市场将无法满足OT。此外，在物理世界中通常动作无法复原，这是IT系统通常没有解决一个考虑因素。	

[^15]: http://en.wikipedia.org/wiki/Chinese_room		
Riding on continued advancement of computation and communication technologies, the Industrial Internet can dramatically transform industrial control systems in two major themes:
乘着计算和通信技术的不断进步，工业互联网可以极大地变换两大主题工业控制系统：
增加局部协作自主：新感测和检测技术提供以上，更准确，数据。更大的嵌入式计算能力使这些数据的更先进的分析和更好的模型物理系统的状态，并在其开展业务的环境。这个组合的结果转换控制系统，从单纯自动到自主，使他们能够作出适当反应，即使系统的设计者没有预料到当前的系统状态。此外，对等系统之间无处不在的连接实现融合与合作的水平，这在以前是不切实际的。
通过全球协调提高了系统的优化：来自全国各地的控制系统中收集传感器数据和应用的分析，包括通过机器学习开发的模型，这些数据中，我们可以洞察到企业的运营。有了这些见解，我们可以提高决策，并通过自动和自主编排全局优化系统操作。
这个功能域模型旨在普遍适用于IISs在许多工业垂直行业。然而，用例在某些工业垂直可将更加强调功能中的一个或多个功能性结构域比其他人。在某些情况下，功能结构域可以被实现为一个单独的系统，组合成一个单一的一个，或分裂和实施为其他域的一部分。
The decomposition of functional domains highlights the important building blocks that have been seen to have wide applicability. The set of building blocks is neither a complete nor a minimum set that any system must possess. Rather, it is intended to be a starting point for conceptualizing a concrete functional architecture within these functional domains. A use case under consideration and its specific system requirements will strongly influence how the functional domains are decomposed, so in a concrete architecture derived and extended from this reference architecture, additional functions may be added, some of the functions described here may be left out or combined and all may be further decomposed as needed. 
功能域分解突出已被视为具有广泛适用性的重要组成部分。一组积木的既不是完整的，也不是任何系统必须具备的最小集合。相反，其旨在成为起点这些功能域内概念化的具体功能架构。用例所考虑和其特定的系统要求会强烈影响如何功能结构域被分解，因此，在衍生并从该参考架构可扩展的具体架构，附加功能可被添加，一些这里描述的功能可以被省略或组合和所有可能根据需要进一步分解。

We decompose a typical IIS into five functional domains:
我们分解一个典型的IIS为五个功能区：

* Information domain
* Application domain
* Business domain
* 控制域
* 运行领域
* 信息领域
* 应用领域
* 商业领域
数据流和控制流发生在这些功能域之间。图6-1示出了上述的功能结构域如何与彼此有关的数据和控制流。绿色箭头显示的数据流跨域如何循环。红色箭头显示控制流跨域如何循环。其他水平箭头示出了一些处理采取每个域内进行，以处理输入流和生成的数据或控制流的新形式。
		
Controls, coordination and orchestration exercised from each of the functional domains have different granularities and run on different temporal cycles. As it moves up in the functional domains, the coarseness of the interactions increases, their cycle becomes longer and the scope of impact likely becomes larger. Correspondingly, as the information moves up in the functional domains, the scope of the information becomes broader and richer, new information can be derived, and new intelligence may emerge in the larger contexts.
我们描述每个反过来，从图6-1的底部开始，上面的物理系统。
		
### 6.2 THE CONTROL DOMAIN
### 6.2 控制域
控制域代表的是由工业控制系统执行的功能集合。这些功能的芯包括细粒闭合回路，由传感器读出的数据（图中的“有义”），应用规则和逻辑，并行使对通过致动器的物理系统（“致动”）的控制。精度和分辨率在定时通常是至关重要的。部件或实现这些功能（功能元件）系统通常部署在靠近它们控制的物理系统，并且因此可以在地理上分布的。他们可能也不容易接近物理维修人员，而这些系统的物理安全性可能需要特殊的考虑。
		
>Examples: Simple examples of functional components in this domain include a control room in electricity utility plant, control units in a wind-turbine, and control units in autonomous vehicles.
>例子：在此领域的功能性成分简单的例子包括控制室的电力公司厂房，控制单元的风力涡轮机，并在无人驾驶汽车控制单元。

The control domain comprises a set of common functions, as depicted in Figure 6-2.[^17] Their implementation may be at various levels of complexity and sophistication depending on the systems, and, in a given system, some components may not exist at all. We describe each in turn.
控制域包括一组常用的功能，如图6-2所示的。其实现可以是在各级复杂性和完善取决于系统的，并且，在给定系统中，某些组件可能不存在。我们描述依次在每个。
致动是写入数据和控制信号到致动器颁布致动的功能。其实现跨越硬件，固件，设备驱动程序和软件元件。
		
[^16]: Possibly in a hierarchy, at several levels.


内的通信功能，一个连接抽象函数可以用于封装的基本通信技术的具体情况，使用一个或多个通用API以暴露一组连接服务。这些服务可能会提供额外的连接功能，是没有其他可以直接从底层通信技术，如可靠的传送，自动发现和自动重新配置的故障时的网络拓扑。
造型处理的理解状态，条件和控制系统的行为和那些对系统通过解释和相关传感器和对等系统收集的数据。该控制系统的建模的复杂性和复杂性差别很大。它的范围可以从简单的模型（例如时间序列锅炉的温度的简单解释），以中等复杂（飞机发动机的预建物理模型），来构建具有人工智能具有非常复杂的和弹性的（型号学习和认知能力）。这些建模能力，有时被称为边缘分析，一般都需要在控制系统实时应用的本地计算。还需要在用例边缘分析它是不经济的或实用的发送大量原始传感器数据的远程系统即使没有实时性要求进行分析。
		
A data abstraction sub-function of modeling may be needed for cleansing, filtering, de- duplicating, transforming, normalizing, ignoring, augmenting, mapping and possibly persisting data before the data are ready for analysis by the models or destroyed.
建模的数据抽象子功能可能需要的清洗，过滤，脱翻炒，转化，正火，忽略，扩增，映射以及可能存留数据之前的数据已准备好由分析模型或销毁。
*精密 - 结合的认知和学习能力，具有高度自治，比如决定哪些障碍车辆要碰撞问题纳入，全校车从小学车辆或前方行人的水坑前拉出的养老院？
执行程序负责确保施加，使得数据移动了它的范围，使用致动器等，是这些政策的范围内其范围的策略。

		
### 6.3 THE OPERATIONS DOMAIN
### 6.3 操作域
		
![](./IISs/QQ20160115-2.png)		
		
Provisioning and Deployment consists of a set of functions required to configure, onboard, register, and track assets, and to deploy and retire assets from operations. These functions must be able to provision and bring assets online remotely, securely and at scale. They must be able to communicate with them at the asset level as well as the fleet level, given the harsh, dynamic and remote environments common in industrial contexts. Provisioning and deployment has a strong dependency on functions in connectivity and security, trust and privacy.
监控和诊断包括功能，使出现问题的检测和预测。它负责实时监控资产的关键绩效指标，收集和情报处理资产的健康数据，以便它可以诊断问题的真正原因，然后报警的异常情况和偏差。这组函数应协助操作和维护人员，以减少检测和解决某个问题的响应时间。监控和诊断，对数据业务和分析功能很强的依赖性。

Prognostics consists of the set of functions that serves as a predictive analytics engine of the IISs. It relies on historical data of asset operation and performance, engineering and physics properties of assets, and modeling information. The main goal is to identify potential issues before they occur and provide recommendations on their mitigation. It may use the analytic functions in the information domain to realize its functions.

* Ability to analyze and assign causes for known problems.
* 能够捕捉和识别重大活动，如停机时间，延迟等
* 能够分析和已知问题分配的原因。
优化对动态的业务流程，并自动集成功能强大的依赖性。它可以使用数据摄取和处理功能和分析功能，在信息领域，以实现其职能的一部分。

### 6.4 THE INFORMATION DOMAIN
### 6.4 信息域

The Information Domain represents the collection of functions for gathering data from various domains, most significantly from the control domain, and transforming, persisting, and modeling or analyzing those data to acquire high-level intelligence about the overall system.[^19] The data collection and analysis functions in this domain are complementary to those implemented in the control domain. In the control domain, these functions participate directly in the immediate control of the physical systems whereas in the information domain they are for aiding decision- making, optimization of system-wide operations and improving the system models over the long term. Components implementing these functions may or may not be co-located with their counterparts in the control domain. They may be deployed in building closets, in factory control rooms, in corporate datacenters, or in the cloud as a service.
信息领域代表了来自各个领域的控制域，并转化收集数据，最显著，坚持和建模和分析这些数据，以获得对整个系统的高级智能功能集合。数据在这一领域收集和分析功能互补的控制域中实现。在控制领域，这些功能在物理系统，而在信息领域，他们是长期协助决策，整个系统的操作的优化，提高了系统模型的直接控制直接参与。实现这些功能部件可以或可以不位于同一位置与其对应于控制域。它们可以部署在建筑物壁橱，工厂控制室，在企业数据中心，还是在云中的服务。

[^19]: Possibly in a hierarchy, at several levels.
* Changing the temperature set-point of a boiler based on energy cost, weather condition and usage pattern.

>* 优化植物的发电水平或基于该设施，燃料成本和电力价格的条件的发电机。
* 改变货运卡车车队的路线根据天气，交通和货物的卡车的条件。
* 改变的基础上的设施，能源和材料成本，需求模式和后勤的条件自动生产厂的输出。
* 改变温度设定点基于能量成本，气候条件和使用模式锅炉。

Figure 6-4 illustrates the functional decomposition of the information, application and business domains.
图6-4所示的信息，应用和业务域的功能分解。

![](./IISs/QQ20160115-3.png)	

Data consists of functions for:
* 从所有域摄取传感器和运行状态的数据，
* 质量-的数据处理（数据清洗，过滤，重复数据删除等），
* 语法转换（例如，格式和值正常化）
* 语义转换（语义分配，语境注入和基于元数据的其他数据增强处理（例如从操作域配置数据）和其他合作数据集，
* 数据持久化和存储（例如用于批量分析）和
* 数据分布（如流分析处理）。

数据管理功能可以包括用于数据的安全性，数据访问控制和数据版权管理，以及相关的数据的韧性常规数据管理功能（在储存，快照和恢复，备份和恢复的复制，等等）。

Analytics encapsulates a set of functions for data modeling, analytics and other advanced data processing, such as rule engines. The analytic functions may be done in online/streaming or offline/batch modes. In the streaming mode, events and alerts may be generated and fed into functions in the application domains. In the batch mode, the outcome of analysis may be provided to the business domain for planning or persisted as information for other applications.
数据量在大多数IIS系统级最终将超过一个门槛，传统的分析工具集和方法可在满足要求的性能不再是规模。大数据存储和分析平台，可以考虑实现这些功能。

### 6.5 THE APPLICATION DOMAIN
### 6.5 应用域
### 6.6 商业域
>例子：一个石油转井预测性维护服务可以具有预测故障在该领域的应用。要做到这一点，它可能需要一个资源规划系统，以保证所需的零部件都可以和保留，它可能需要连接到内部或合作伙伴的服务工作日程系统，物流管理系统，以及客户，安排现场 服务。

### 6.7 COMMON SECURITY FUNCTIONS
### 6.7 常见的安全功能

* Security audit involves the collection, storage and analysis of security information related to the industrial system.
* 安全审计工作涉及的相关产业体系的安全信息的收集，存储和分析。
* 在通信身份验证，保证双方的鼻祖和通信在工业系统中的收件人的完整性。
* 加密支持提供必要支持的加密和解密操作（软件和硬件）的资源。
* 数据保护和隐私保证了在运输过程中和静态数据的机密性。如果该数据包含到一个第三方拥有信息或相关所描述的安全策略，它提供了保护的记录的隐私。
* 认证和身份管理，确保了组件仅通过在安全策略中指定的角色访问。
* 物理保护提供了对物理篡改和所描述的安全策略未经授权的观察必要的保护。

These functions contribute to various system security capabilities including:
这些功能有助于各个系统的安全功能，包括：

* secured booting to a known secure state enabled through cryptographically signed software and firmware,
* enhanced trust by network and application whitelisting and reputation-based approaches (or dynamic approvals),
* enhanced privacy through mutual authentication in communication integrated with means to automatically ensure the privacy of data.
* early attack detection through rigorous anomaly detection over established norms of traffic patterns and simplified system,
* secure management of all systems and their update processes and
* automatic threat containment to minimize the damage of a successful attack.
* 启动保障，通过加密签名的软件和固件启用一个已知的安全状态，
* 通过增强网络和应用白名单和信誉为基础的方式（或动态的批准）的信任，
* 通过通信集成方法相互验证增强了私密性，自动保证数据的保密性。
* 早期攻击检测，通过严格的异常检测过的流量模式，并简化系统建立规范，
* 所有的系统及其更新过程的安全管理，
* 自动威胁围堵，以尽量减少成功攻击的伤害。

[^20]:  The Common Criteria for Information Technology Security Evaluation (abbreviated as Common Criteria or CC) is an international standard (ISO/IEC 15408) [23] for computer security certification.