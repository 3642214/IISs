# 9 SECURITY, TRUST AND PRIVACY
# 9 安全，信任和隐私
* usage viewpoint, for a description of security procedures, and of how to secure end-to- end activities in an IIS, including privileges assigned to their roles,
* functional viewpoint, for a detailed assessment of security functions required to support end-to-end secure activities and operations and
* implementation viewpoint, for ensuring secure architectures and the best use of relevant
* 使用观点出发，为的安全程序和，如何保护端到端活动的IIS，包括分配给自己的角色的权限的描述，
* 官能观点考虑，为安全功能的详细评估须支持端至端的安全活动和业务和
* 实现的观点，确保安全架构和相关的安全技术，物尽其用。

* management and monitoring security of both the endpoints and the communication mechanisms and
* data distribution and secure storage.
* 端点安全，
* 在端点之间通信的安全性，
* 两个端点和通信机制的管理和监测的安全性和
* 数据分发和安全存储。

The following subsections examine each of these concerns.
以下小节检查每个这些问题。

### 9.1 端点安全

有很多方法来攻击一个端点，因此很多问题需要解决。这些问题需要解决包括：

* Separation of security agent
* Logging and event monitoring
* Application whitelisting
* Dynamically deployed countermeasures
* Remote and automated endpoint update
* Access control
* 安全代理分离
* 端点标识
* 端点攻击响应
* 远程管理软件的政策
* 记录和事件监控
* 应用程序沙箱
* 应用程序白名单
* 网络白名单
* 端点和配置控制，以防止未经授权的更改端点
* 动态部署对策
* 远程和自动端点更新
* 在多个端点政策协调
* 外围设备管理
* 端点存储管理
* 访问控制
#### 9.1.1 安全启动证明
#### 9.1.3 端点标识
包括事件有关的安全违规，用户登录/注销，数据访问，配置更新，应用程序的执行和沟通。
应用程序代码（白名单），包括二进制文件，脚本库被允许在端点上执行，以防止端点受到侵害恶意代码。所有其他执行企图应当停止，记录和报告。安全管理系统可以在其执法的端点安全代理更新策略中的应用程序白名单。
####9.1.8网络白名单
#### 9.1.11政策协调横跨多个端点

* Security in request-response and publish-subscribe communications
* User authentication and authorization
* 安全的请求 - 响应和发布 - 订阅通信
* 端点之间的相互认证
* 通讯授权
* 身份代理/整合点
* 用户身份验证和授权
* 加密通信

#### 9.2.3 端点之间的相互认证
#### 9.2.4通信授权
Before granting access of any resource, to an authenticated party, authorization must be performed at the endpoint according to the security policy. The security policy may specify fine-grain authorization rules such as what data records to share with whom, under what condition (e.g. encryption, anonymization or redaction of certain data fields) including temporal and spatial conditions.
管理和监控安全包括以下方面：

* Provisioning and commissioning
* Endpoint activation management
* 配置和调试
* 安全策略管理
* 端点激活管理
* 凭证管理
* 管理控制台
* 对情况的意识
* 远程更新
* 管理和监控的弹性
远程策略管理涉及到策略的创建，分配和分发。策略在安全管理系统中定义，并通过安全代理传达给终端。
* additional credential generation (particularly for temporary credentials)
* credential update
* credential revocation/de-recognition
* 凭证提供/报名/识别
* 附加凭证生成（特别是对临时凭证）
* 证书更新
* 凭证撤销/去识别

The credentials at an endpoint are managed remotely and securely by one or more security management systems via the secure agent. The endpoint’s credentials can be provisioned, updated and revoked by a security management system, and this should be able to be done
In addition to single-event issues, patterns emerging a sequence of events can contribute to an understanding of the current environment of the IIS. For example, while a single failed login may not be interesting, a series of failed login attempts is significant and contributes to situational awareness. A detection of a single port scan event is not as interesting as a series of events of port scans. By correlating information, the IIS is able to detect system-wide attacks, whereas less coupled systems would miss them.
* 数据为中心的政策
* 数据分析和隐私
* IT系统和云
这些行动者所提供的资料必须进行翻译，并自动实施，以防止错误。
