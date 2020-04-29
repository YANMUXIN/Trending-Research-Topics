-   笔记作者：2017141531067 刘浩
-   原文作者：Patrick McDaniel, mcdaniel@cse.psu.edu 
Sean W. Smith, sws@cs.dartmouth.edu
-   原文题目：Security and Privacy Challenges in the Smart Grid
-   原文来源：IEEE Security & Privacy ( Volume: 7 , Issue: 3 , May-June 2009 )

自从电力入户以来，全球电网正处于最大的技术转型期。 为家庭和企业供电的陈旧基础架构已经被一系列产品取代。智能电网是监视和管理能源使用情况的计算机和电源基础结构的网络，每个能源生产商都拥有运营中心，这些运营中心从遍布整个服务区域的收集器设备接收使用信息。文章主要研究了由这种新基础架构引起的一些安全和隐私问题，并确定了可能有助于减少遭受这些不良影响的措施。

### 1、创新点

本文的主要创新点如下：

-   这是当时处于传统电网时代对智能电网的先进思考
-   深入分析了智能电网的重要性，以及保护智能电网安全的必要性
-   突出了对智能电网受到攻击后的损失之大  
-   创新分析了智能电网对用户隐私的泄露问题
-   最后提出了大体的解决方案

### 2、论文缺点

这篇文章在当时前言地预料智能电网的优异性，具有推动行业发展的作用，但当时对智能电网的分析仍然存在许多不足，比如：
-	对智能电网被攻击造成的影响分析不足，仅仅考虑到了经济因素，如伪造电量等，忽略了对国家安全方面的考虑
-	对智能电网的攻击方式分析不足，仅仅考虑针对设备自身漏洞的攻击，忽略了网络层面的风险
-	给出的解决方案偏向于决策层方面，而对具体的技术细节缺乏支持


### 3、改进方法

结合如今智能电网的发展，可以对该论文的不足之处给予弥补，具体应对措施如下：
-	智能电网被攻击所损失的不仅在于经济因素，更重要的是国家安全方面的考量，比如此前发生过的乌克兰、古巴等国的电网停电事故，对国家安全的威胁非常之大。
-	现如今对智能电网的攻击方式已经不限于终端设备修改用电量那么简单，还要多多考虑网络流量等方面的风险因素，电网的智能化所带来的网络风险是无法忽略的。
-	对于给出解决方案方面，还需要对具体的技术细节进行细化，比如采取什么样的具体措施；使用什么通讯协议；如何进行系统安全更新等等。