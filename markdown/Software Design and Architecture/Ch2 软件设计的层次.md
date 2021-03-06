#Ch2 软件设计的层次
##一、低层设计：代码设计
小代码的测试代价都极其高昂，能否通过*良好的设计*保证正确性？

* Niklaus：数据结构+算法=程序
* McConnell：数据结构为中心->算法设计为中心，即软件构造

###低层设计支持
* 程序流程图
* 决策表
* 伪代码
* ……

###低层设计总结
* 问题：程序设计语言提供的类型与语句有限（只有三种控制结构和基本的结构化类型）  
因此要自行规划数据类型和算法中的结构
* 对外：ADT与算法
* 对内：如何用语言提供的有限类型组织复杂类型，用语言提供的结构组织复杂的控制结构  
*对外表现可用类型，提供的方法只是接口*  
*逻辑概念上是类型概念，物理上是用什么方式实现这种机制*
##二、中层设计：模块与类结构设计
* 关注程序的分割，满足7±2的处理方式
* 中层设计的目的是分割，如何将复杂的系统分割成更小的片段，同时满足各种需求（质量的，等等）
* 模块划分的基本目的是隐藏程序的内部组织
* 模块划分的质量评价：简洁性、可观察性
* 模块化的目标：完全独立

*但这是不可能的，所以只能以高内聚低耦合的方式实现尽可能的独立*

###信息隐藏
* 模块化的另一种方式
* 标准的模块化讲究功能内聚，但信息隐藏从另一个角度出发，将模块按秘密来组织
> **模块化=按功能设计**  
> **信息隐藏=模块化+可修改性**

###面向对象
> **模块化+信息隐藏+（ADT、封装、继承、多态……）=面向对象**

###设计模式
* 优点不在于加深，而在于解决了一些设计中的难点

中层设计由UML来做设计支持  
####评价
* 测试（持续集成、单元测试）
* 评审（Checklist）
* 度量

###总结
* 中层设计的外部表现是职责，实际上就是需求
* 内部是分割和分配，代码上看是分割，职责上看是分配
* 看中层设计时，层次得到提升，可以更少地关注细节
* 逻辑上，是需求的分配，自治（且平等）的类和对象协作完成任务
* 物理上，是怎么将代码分成片段，并且将片段组织起来体现整体

*注：中层设计在某些方面会有补充*

##三、高层设计：体系结构设计
* 程序大到一定程度时，接口也无法被有效管理
* 详细设计过于依赖细节，导入与导出依赖名词匹配进行控制，但这本身也带来复杂度

###详细设计机制的不足
* 关注点偏差（载体失配）  
语言可以描述数据结构+算法，但不能表达质量
* 无法实现交互信息本地化
* 无法抽象部件的整体性  
部件的总体规则无法被定义
* 接口定义缺乏结构性  
接口太过独立，无法区别对待（为不同的模块公布不同的接口）

总体上：Programming in large就会面临载体复杂度过大、载体的导入导出关系本身有缺陷  
因此需要从根本上超越模型的导入/导出关系，从**纯逻辑**上来考虑功能的分配

高层设计剔除载体（程序本身机制）的影响，进行逻辑设计，实现系统大部分（80-85%）的质量  
体系结构的问题，核心在连接件上
