#Ch1 Introduction to Software Design
设计思想四大主题：**模块化、信息隐藏、抽象、分解**  
*（此处2-4节是最根本的东西）*

##一、什么是软件设计
**（广义）**设计是一种规划活动，建造真正的东西之前所要做的规划活动  
规划内容：结构  
软件设计：开发软件之前所做的规划活动，做出软件的组织结构，满足客户的期望，并符合某些约束。  
> ***SRS->产品***

设计需要考虑功能和审美以及其它方面，*本课更多地考虑审美*
##二、设计的目标与衡量标准
###什么是好的设计
* 效用、坚固、美感（《De Architectura》）  
美感？  
仍然来用于衡量设计的好坏
* 简洁性、结构清晰、一致性（《设计原本》）

###设计的标准
功效是**必备价值**，坚固是**工程价值**，美感是**艺术价值**（*艺术价值在工程上反正不作为必备要求，用来判断工程师伟大与否*）

类比：杰出建筑师  
美感无法被教育，只能靠天赋，到了一定层次就有了（玄学？）

坚固性是本课的重点

设计师的追求：**用软件功能解决用户的问题是需求分析的价值**

###***准则1：用“好”（工程与艺术兼备）的方式实现功能，是设计的价值***  
任何设计方法与技术，要么提高坚固，要么提高美感
##三、外部表现与内部结构问题
> ######例：拆闹钟、收音机、手机……

良好的设计外部永远很简单，隐藏内部的复杂结构  
**核心问题：抽象与分解**

将外部系统分解为坚固的解决方案，将内部结构抽象后展现给用户  
抽象用于提升层次或屏蔽细节，在两个维度上进行

* 抽象：外部表现
* 分解：内部结构

整个设计工作而言，其外部表现就是*需求*（效用体现的层次），内部表现就是*代码*（包括类型声明、操纵+代码组织）
> 从不同的设计层次而言，外部表现与内部结构的不同概念见ppt

总的目的：**实现简单的外部表现，构造复杂、坚固、美感的内部结构**  
内外必须分开，内部不受外部功能的影响，不使需求的变化改变软件的设计

***准则2.1（分解）：设计重在内部结构，不是外在表现***  
不要依据外部表现设计内部结构  
应该**分解外部表现**，根据坚固、美感的考虑设计内部结构

***准则2.2（抽象）：从设计师而不是用户的角度分析问题***  
> ######内外不分的典型
> * 几个功能，几个模块  
> 模块设计时就要考虑质量
> * 几个职责，几个类  
> 非信息类
> * 算法逻辑就是代码逻辑  
> 优化逻辑  
> * 现实特征组织就是数据特征组织  
> 特征规范化
##四、逻辑设计与物理设计问题
* 逻辑设计：不考虑载体介质的设计  
更纯粹，更容易  
* 物理设计：考虑载体介质的设计  
更繁杂，更困难  
* 逻辑设计最后一定要转换到物理上去  
* 物理就是语言机制的局限性  
###模块层面：
* 逻辑：一个模块调用（通知）另一个模块——物理：两层实际没有任何关系  
* 逻辑：一个模块给另一个模块传递数据流——物理：？  
* 逻辑：一个模块与另一个模块共享数据——物理：？  
> 逻辑设计与物理设计的举例见ppt

###***准则3：设计复杂度=逻辑设计复杂度+物理设计复杂度***  
逻辑设计复杂度=事物自身复杂度  
物理设计复杂度=事物与载体的匹配复杂度  
##五、复杂度控制问题
* 设计的难度在于事物的复杂性与思维的有限性（7±2规则）
* 关注点分离和层次分解（多视角）

###***准则4：只有高层设计良好，底层设计才可能良好***
##六、决策问题
在多个解决方案中选择一个的过程

* 约束满足与决策  
需求越多越能为设计师指明方向（约束不是设计师的敌人）  
约束会随着设计过程的深入而逐渐地出现
* 决策的选择性  
未必能找出一定最好的一个决策来
* 决策的顺序影响  
前一个决策会影响后一个，而且不可预见
* 决策的不可逆性  
前期错误决策的影响无法完全消除

> ######软件设计过程的几个要点：  
> 见ppt

###***准则6：软件设计的关键就是在不确定和信息不充分的情况下进行正确的决策***
##七、总结
* 设计是一中建造之前的规划活动
* 可以在潜意识中进行，也可能在设计板上进行
* 可以是单人活动，也可以是团队设计
* 可以一次性完成，也可以迭代进行

* 设计的目标：**功效、坚固、美感**

* 区分外部表现与内部结构  
*完全依照外部表现仿制内部结构是山寨者的基本技能*

* 逻辑设计与物理设计
	* 逻辑设计是思维体操
	* 物理设计是现实规则
	* 聪明的设计师**先进行逻辑设计，再转换为物理设计**

* 复杂度是设计师的终生对手 
	* 分解、关注点分离是控制复杂度的主要武器
* 决策是设计师每天的行为
	* 不确定与信息不充分是决策存在的理由
	* 优秀的设计师是一个好的决策者  
	*技术层面*
	* 逻辑是设计师的基本思维方式
	* 经验与直觉对好的设计师至关重要

