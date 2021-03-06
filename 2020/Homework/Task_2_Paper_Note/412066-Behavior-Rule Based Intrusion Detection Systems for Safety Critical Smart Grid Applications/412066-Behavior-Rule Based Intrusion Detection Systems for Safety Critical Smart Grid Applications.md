# 1.论文信息
标题： Behavior-Rule Based Intrusion Detection Systems for Safety Critical Smart Grid Applications 

作者：Anthony R. Metke,  Randy L. Ekl

出处： IEEE TRANSACTIONS ON SMART GRID, VOL. 4, NO. 3, SEPTEMBER 2013 

链接： http://people.cs.vt.edu/~irchen/ps/Mitchell-TSG13a.pdf 

# 2.论文简要及主要内容

针对以往传统基于特征和基于异常情况的IDS系统在智能电网领域检测效率低下问题，作者提出了一种基于行为规则的入侵检测系统（BRIDS），主要用于为现代电网CPS中的HE，DAP与SEM提供超安全保护。

本文提出的BRIDS其中心思想在于将来自HE，DAP与SEM三类设备中22个传感器的读数作为状态组件，借助针对每类设备精心设计的行为规则将状态组件值量化到有限范围内，最后通过合取范式的形式，利用量化后的状态组件分别为CPS中上述3类设备构建出3456，1728和3456种状态机，BRIDS由此将该状态机作为智能电网中HE，DAP与SEM三类设备的规范针对异常行为进行检测。

作者针对自己所提出的BRIDS进行了实验验证，其结果表明对于HE，DAP与SEM三种设备无论是蛮力攻击还是随机攻击，BRIDS对攻击威胁的检出率始终接近于1，该种入侵检测方案对于本文所设想的应用场景具有较高的现实意义。

# 3.创新点
1. BRIDS系统的行为规则是从CPS控制环派生的，这些控制环将IDS于CPS的关键业务联系在一起，而不依赖于其他检测方法中使用的运行或追踪数据，IDS系统的稳健性有所增强。
2. BRIDS系统的行为规则充分保障了的CPS中的核心经济利益与关注目标价值最大化。
3. 专门考虑了WAN，NAN，HAN设备控制执行器和物理环境中嵌入式传感器的行为规范。
4. 提出了一种将行为规则转换为状态机的方法，进而可以将被监视设备的行为转换为状态机检测其是否偏离行为规范。
5. 研究了攻击者在智能电网生产，传输，分发和消费环节中各种攻击行为对入侵检测有效性的影响。
6. BRIDS系统漏报率很低，实时性较高，能很好地解决在智能电网CPS威胁检测中HE，DAP与SME设备面临的复杂攻击挑战。
# 4.目前缺点
1. BRIDS系统的在智能电网领域的部署范围有限，仅适用于不考虑物理环境和闭环控制结构的通信网络，例如HE，DAP和SEM。
2. BRIDS系统针对未知攻击的误报率较高。
3. 人工构建行为规则代价较大，系统行为状态的改变需重新改写规则的状态机，无法高效率地适应大型电网系统的入侵检测需求。
4. 可扩展性较低，无法较好地检测未来可能出现的新攻击模式。
5. BRIDS系统直接将设备传感器读数用作状态组件，可能会面临假数据注入攻击的风险。
6. 没有继续深入研究相应的入侵响应，防御，修复策略。
7. 并没有在应用层面实现BRIDS的行为规则。

# 5.其他解决方案或改进方法
1. 针对缺陷６，在BRIDS系统检测到威胁时，可采用驱逐单个受损节点，隔离受损段以及调整IDS参数提高检测强度的方法来进行入侵响应，同时采取停运受损网段，重置密钥密码，将所有节点回退至安全认证的软件负载与配置的策略来进行入侵防御和修复。
2. 针对缺陷7，可采用高级编程语言对状态机，主机IDS软件与系统IDS软件进行编码实现，并对感兴趣目标进行交叉编译，最后根据期望和实际的误报率和检测率等指标对参数进行优化并最终实现在应用层面的部署。
3. 针对BRIDS中误报率较高的问题，可进一步研究基于良好状态偏差累积的其他入侵检测标准，或是进一步调整相关参数以降低系统的误报率。
4. 针对BRIDS适用范围窄，可扩展性低，人工构建规则代价较大等问题，可采用深度学习，数据挖掘的技术手段自动或半自动构建行为规则与状态机，以提高其在大型电网系统中的广适度。
5. 针对缺陷5，可采用密码学的方法对传感器收集数据进行处理，以降低其遭受假数据注入攻击的可能。