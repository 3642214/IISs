## 2 KEY SYSTEM CHARACTERISTICS AND THEIR ASSURANCE
## 2 钥匙系统特征及其保证
### 2.1 KEY SYSTEM CHARACTERISTICS
### 2.1 钥匙系统特征
An Industrial Internet System will exhibit end-to-end characteristics, such as safety, security or resilience. Such characteristics are emergent properties or behaviors of the IIS resulting from the properties of its various components and the nature of their interactions. Because IISs are large scale, heterogeneous, built with multi-vendor components, often broadly distributed and continuously evolving, it is a challenge to define, measure, enforce and maintain the system characteristics over time. For these reasons, we give prominent treatment to a few key system characteristics in this document.
一个工业网络系统将展示终端到终端的特性，如安全，安全或韧性。这样的特性是突发属性或从它的各种组件的属性和它们的相互作用的性质而产生的的IIS行为。由于国际战略研究所是大型，异构，建有多个供应商的组件，往往广泛分布和不断发展的，它是定义，测量，实施并随着时间的推移维护系统的特点是一个挑战。由于这些原因，我们给突出治疗本文件中的一些关键的系统特性。
A system characteristic is delivered through four elements:
系统的特点是通过四个要素提供：

* the system’s functional components and their interactions,
* the way the system is used and maintained (system operations) and* the engineering process by which the components are created and the system assembled (system engineering),* the evidence gathered throughout the full lifecycle of the components and systems.[^1]
* 该系统的功能部件和它们的相互作用,
* 该系统的使用和维护的方式（系统操作）
* 通过该组件创建的工程过程和组装系统（系统工程）,
* 聚集整个部件和系统的整个生命周期的证据。

Common system characteristics include upholding privacy expectations, reliability, scalability, usability, maintainability, portability and composability but three are key to the discussion of IISs because of their criticality in ensuring the core functions, rather than the efficiency, of these functions, of the system:
通用系统的特征包括的坚持隐私期望，可靠性，可扩展性，易用性，可维护性，可移植性和可组合，但三个是关键IISs的讨论，因为它们在确保核心功能临界的，而不是效率，这些功能时，系统的：
Safety: the condition of the system operating without causing unacceptable risk of physical injury or damage to the health of people, either directly, or indirectly as a result of damage to property or to the environment.[^2]安全性：系统没有造成人身伤害或损害的不可接受的风险对人的健康运行的前提下，无论是直接或间接的财产损失或环境的结果。
Security: the condition of the system operating without allowing unintended or unauthorized access, change or destruction of the system or the data and information it encompasses.可靠性：该系统操作，而不使系统或它包含了数据和信息的意外或未经授权的访问，改变或破坏的情况。
Resilience: the condition of the system being able to avoid, absorb and/or manage dynamicadversarial conditions while completing assigned mission(s), and to reconstitute operational capabilities after casualties.韧性：该系统能够避免的情况下，吸收和/或管理动态对抗性的条件，同时完成分配的任务和人员伤亡后重建作战能力。
[^1]: Broadly speaking, a lifecycle of a system includes activities for requirement specification, design, development, manufacturing, test, assembly, integration, delivery, deployment, verification, evolution and upgrade, un-deployment, and disposal of the system. We will not hereafter refer to the specific activities unless it is necessary.
[^2]:IEC 61508, Functional Safety [25]

Desired system characteristics and the degree they are needed vary by system. They may be motivated by business context and values, be mandated by regulations and contractual agreements, or simply be commonly expected behaviors for a specific type of system. Note that some of these desired characteristics may be negated by unintended side effect of other unrelated system behaviors.[^3]
所需的系统特性和它们所需要的程度而变化由系统。他们可以通过商业环境和价值的动机，通过法规和合同协议，或者系统的特定类型简单地普遍预期的行为得到授权。注意，其中的一些所需特性可以通过其它无关系统行为意想不到的副作用被否定。

To preserve these system characteristics in the evolving IISs, continuous tracking and auditing should be provided throughout the lifecycle of these systems.
为了保持在不断变化的IISs这些系统的特性，连续跟踪和审核应贯穿这些系统的生命周期中被提供。
The number of reports of security attacks on large enterprise and infrastructure systems is rapidly increasing, along with the level of damage they have wrought. These attacks are better organized, and employ attack techniques of ever-increasing levels of sophistication. The actors in these attacks are becoming more diverse and include anyone from insiders to casual hackers, terrorists and state-sponsored actors. Security for Industrial Internet systems from design, development, and deployment to operations must be heightened to mitigate the increased security risks. We therefore give security, a key system characteristic, a strong emphasis in this document._对大型企业和基础设施系统的安全攻击报告的数量正在迅速增加，随着损伤的程度，他们紧张得要命。这些攻击有更好的组织，并采用复杂程度不断增加的攻击技术。在这些攻击的角色正变得更加多样化，包括任何人从内部人士向业余黑客，恐怖分子和国家支持的参与者。安全用于从设计，开发和部署到操作的工业互联网系统必须被提高以减少越来越高的安全风险。因此，我们给予保障，钥匙系统特征，本文件中的高度重视。_
[^3]:For example, a system that tracks an individual’s location on a ship to provide a man-overboard alert may also violate privacy expectations of that individual.例如，一个系统，在船上追踪个体的位置，以提供一个人为的舷外警报也可能违反该个人的隐私的期望。
### 2.2 SYSTEM CHARACTERISTIC ASSURANCE### 2.2 系统特征保证
System characteristics are often subject to regulations, compliance requirements and contractual agreements and thus need be measured and assessed.[^4] The foundation for claiming such characteristics covers three major aspects:
系统特点常常受到法规，合规要求和合同协议，因此需要进行测量和评估.声称具有这种特性的基础包括三个主要方面：

[^4]:Examples of security related compliances include Common Criteria [23] and various Federal Information Processing Standards (FIPS) specifications. Examples of safety related compliance include the application of DO-178B/C to avionics software systems certification by the FAA. Compliance will not be taken up by the RA but may be addressed by future more detailed documents, as they are greatly dependent on the specific vertical and deployment scenario.安全与遵从性的例子包括通用标准[23]和各联邦信息处理标准（FIPS）规格。安全相关的合规性的例子包括DO-178B/ C的应用，航空电子软件系统认证，通过了美国联邦航空局。遵守不会被吸收由RA，但可以通过将来更详细的文件加以处理，因为它们是极大地依赖于特定的垂直和部署方案。
System engineering: Evidence supporting system characteristics must be gathered and provided, with proper tracking and certification, on the components and the system formed from their combination throughout the entire lifecycle of activities. It may include specific attributes of the software and hardware, documentation on the way it was constructed, where it was developed and by whom, and records of the types of component testing and analysis carried out, and the results thereof.
系统工程：支撑系统特性的证据必须收集和提供适当的跟踪和认证，对部件，并从他们的组合在整个活动的整个生命周期构成的系统。它可以包括软件和硬件的特定属性，在途中文档它被建造，在那里它被开发和由谁，和组件测试和分析的类型的记录进行的，并且其结果。System operations: A system characteristic may depend on how a system is being used independent from the quality of the system design and components. Evidence must be available to demonstrate that the system operational processes support the characteristic. This may include evidence that the system is being used for its intended purpose and the qualification of the personnel who play a role in its operations.系统的操作：甲系统特性可以取决于如何一个系统正在从系统设计和组件的质量中使用独立的。证据必须可用于证明该系统的操作流程支持特性。这可以包括证据，该系统被用于其预期目的和谁玩在其动作的角色的人员的资格。
System auditing: The system and its processes shall support the collection and the evaluation of metrics and logs necessary for monitoring and auditing the important characteristics. Monitoring and audit processes should be established and audit records must be maintained.
系统审计：系统和流程应支持收集和必要的监控和审计的重要特征指标和日志的评价。监控和审核过程应建立审计记录必须保持。

Because IISs are built from multi-vendor components and solutions, possibly composed
dynamically after deployment, engineers must be able to access recorded claims and their supportive evidences of specific system characteristics in components to evaluate, select, acquire and assemble qualified components into the desired IIS.
由于IISs是由多厂商组件和解决方案构建，可能是由部署后动态，工程师必须能够访问记录，权利要求和具体的系统特性中的组件的支持性的证据，以评估，选择，获得和装配合格的组件到所需的IIS。

>Example: In the residential house example above, information about fire resistance, load bearing capabilities and structural integrity of the materials must be available to support the claimed “key system characteristic” of safety for individually constructed homes.>例子：在上面的住宅为例，约耐火性，承载能力和材料的结构完整性的信息必须提供能支持这种说法“钥匙系统的特点”安全的单独修建的家。Similarly, the software in a Bluetooth-enabled device that controls the Bluetooth interface and communicates with external entities should have information available to support the assessment of the key characteristics in its fitness for a given use case. This information may include coding practices and reviews, tests and assessments done with respect to its strength to accidental inputs, malicious attacks, and the known issues and their risks in coding, design and architecture if any. It may also include regular and contingent update process and methods to address newly discovered vulnerabilities.
>同样地，在具有蓝牙功能的设备，其控制所述蓝牙接口和与外部实体进行通信应该要支持的关键特征的评估在其适应一个给定的用例可用信息的软件。这些信息可能包括编码惯例和评价，测试和评估方面做了它的实力意外投入，恶意攻击，以及已知的问题和他们的编码，设计和建筑，如果任何风险。它也可以包括常规和队伍更新过程和方法来解决新发现的漏洞。

>Supported by the information along with testable results as evidence, we can ascertain that it is, for example, safe and secure enough to use in an interface to an insulin pump.
>支持连同可测试结果作为证据的信息，我们能够确定它是，例如，安全有保障足够的接口使用到胰岛素泵。

An assurance case [2] [3] [4] is an argument supporting a claim that an IIS satisfies given provide a means to structure the reasoning about system creators can gain confidence that systems will work as expected. The assurance case also becomes a key element in the documentation of the system and provides a map to more detailed information.
一个保证的情况下[2] [3] [4]为支持主张给予IIS满足提供结构关于系统创作者的推理能够获得信心，系统会按预期的方式的参数。该保证的情况下也成为该系统的文档中的一个关键因素，并提供地图，以更详细的信息。

The activities required to construct an assurance case are similar to those that would normally occur when developing a system with required behaviors and characteristics. Assurance cases highlight and explicitly present the claims, evidence and reasoning that relates them together in a reviewable form. The explicit connections between what is claimed and the evidence used to support that claim makes the assurance case a useful tool for third parties who need to have confidence that the IIS exhibits the desired characteristics.
构造一个保证情况下所需的活动是类似于显影所需的行为和特征的系统时，通常会发生的。保证案件突出，并明确提出了索赔，证据和推理涉及他们在一个审查的形式在一起。所主张并用于支持该请求的证据，使案件的保证谁需要有信心，在IIS具有所要求的特性第三方的有效工具之间的明确联系。
Assurance cases are also often used to support the iterative review and revision of the implementation of the claimed characteristics until the stakeholder gains sufficient confidence about the system displaying the claimed behaviors.保证的情况也经常被用来支持所要求的特性实施的反复审查和修订，直到利益相关者获得有关显示所要求的行为的系统足够的信心。