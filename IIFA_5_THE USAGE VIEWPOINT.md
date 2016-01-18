## 5 THE USAGE VIEWPOINT
### 5.1 ELEMENTS OF THE USAGE VIEWPOINT
### 5.1 用法观点元素

图5-1描绘了用法观点的主要概念，以及它们如何相互关联的。工作的基本单元是一个任务，诸如一个操作的调用，数据的传送或一方的作用。任务是由当事人承担角色。
* 一个角色介绍（如适用）的作用负责该任务的执行。
* 功能图描述了哪些功能或功能部件的任务列表。这可以定义仅当系统的功能沉积可用于执行该映射。该映射包括输入和输出的背景下定义，其中该任务将被执行（即一个特定的活动）。
* 一个实现地图介绍任务依靠其执行的执行元件。如果角色（多个）相关联的任务，在地图上还定义如何将这些角色映射的能力的成分和相关业务。同样地，该属性可以被定义仅当系统的实施架构变得可用来执行该映射。

*注册新设备的边缘网关（角色：管理员），
*运行测试程序对处理链X无源RFID阅读器（角色：管理员，QA）
*验证用户请求（角色：安全剂）和
*汇总来自各温度传感器上的资产X数据流（角色：相同的角色
发起的边缘到云数据流处理和合并的活动，这个任务是的一部分）。
一个活动是工作的指定协调（和其他活动的可能性，递归的）以实现一个良好定义的用法的IIS或过程必需的。一个活动可以重复执行。一项活动有以下内容：
* An effect is the difference in the state of the IIS after successful completion of an activity. 
* Constraints are system characteristics that must be preserved during execution and after the new state is achieved, such as data integrity, data confidentiality and resilience. These characteristics may be affected by the enacting of the tasks beyond what is enforceable by the system design or its functional components alone.
* 触发器是一个或一个以上条件（多个）在其下的活性被启动。它可以与一个或多个角色（多个）负责启动或使能执行相关联。
* 工作流程由一个连续的，平行的，有条件的，重复的任务组织。
* 一个效果是成功完成的活动的后在IIS的状态的差别。
* 限制是系统特征它必须在执行期间被保留，并在新的状态实现之后完成，如数据的完整性，数据的保密性和复原能力。这些特性可能受到颁布的任务超出了可执行的系统设计或单独的功能组件。

	Trigger: Administrator approval of the new addition.
	触发：新增加了管理员的批准。
	工作流：
		任务1：注册新设备到边缘网关。
		任务2:注册由所有网关自动发现和查询的基于云管理平台中的新设备。
		任务3:运行远程测试程序适用于该设备类型和验证生成的值是预期的范围内，并与附近类似的设备一致的范围内。
		
Initially, an abstract description of the activity is sufficient. During design, the activities serve as inputs to the requirements for the system, thus guiding the design of the functional architecture and its components. An activity then requires each task to be mapped to, and supported by, one or more functions. An activity is not restricted to one functional domain but may involve a sequence of tasks that span several functional domains.[^10]
最初，活动的抽象描述就足够了。在设计中，活动作为输入到该系统的要求，从而引导功能架构及其部件的设计。一个活动则需要每个任务映射到，并由一个或多个功能的支持。一个活动不限于一个功能域，但可能涉及跨越几个功能域的任务的顺序。

### 5.2 COMMON SECURITY ACTIVITIES
### 5.2 常见的安全活动
安全策略的强制执行，需要控制中涉及的活动在通用的和一致的方式的各种端点和它们的通信，以确保完全的端至端的覆盖的能力。四种常见的安全活动介绍如下。
安全监控采集并连续分析的活动中进行安全相关的数据。它可以采取不同的形式取决于操作的与上安全事件的上下文。例如，不同的任务是适当的前，中，攻击后。

安全审计收集，存储和相关的IIS安全信息分析。
安全策略管理通过记录他们的使用和约束管理自动和人力驱动的安全管理任务。
加密支持管理包括全球通用的密钥管理，安全证书存储和撤销。