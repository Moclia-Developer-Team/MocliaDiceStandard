<div align="center">


# MocliaDiceStandard

**墨可莉雅高级掷骰表达式开发标准**  
**The reference for the Online TRPG players and developers**  

</div>

## 概述

MocliaDiceStandard，是基于OneDice V1标准衍生出的根据MocliaDice需求整理的高级掷骰计算开发标准。相较于OneDice,我们考虑更加复杂的用户需求，为拥有复杂需求的开发者提供参考。

## 背景

MocliaDice，原本是为了更好的掷骰体验和适合新的部署方式开发出的项目，功能参照w4123开发的[Dice! v3]()，并成功实现了第一代MocliaDiceCore，进行闭源内测。之后，OneDice V1标准发布，进行参照修正第一代MocliaDiceCore后，完成目前的第二代MocliaDiceCore，同时，依据该核心，补充OneDice标准，发布此MocliaDiceStandard，供各位开发者参考。

在基于通用文字聊天软件的线上Trpg跑团过程中，根据规则的不同，衍生出了不同的掷骰方式，如1D100，2D6等，甚至使用到了数学运算，如2D6+10。在这里，将这些各式各样的掷骰方式统称为掷骰表达式（Roll Dice Expression），通过研究这些掷骰表达式，得出了一个既方便程序统一处理，又方便了用户使用统一的表达式标准。

## 通用掷骰表达式

简单理解的掷骰表达式，是一种扩展的数学计算法则。在基础的四则运算及乘方，甚至科学计算的基础上，引入特定的掷骰运算符，所组合成的符合掷骰需求的特殊表达式。

例如：
* d —— 普通多面掷骰  
* k —— 取所有掷骰结果中最大的几个结果  
* q —— 取所有掷骰结果中最小的几个结果  

等字母标识的运算符，并辅以特定参数，实现计算效果如：  
* 2D100 —— 骰出两个100面骰，并求和  
* 10D6K3 —— 骰出十个6面骰，并求和得数最大的三个骰子的值  
* 5D20Q3 —— 骰出五个20面骰，并求和得数最小的三个骰子的值  

同时支持特殊计算需求如：
* (( 2 ^ 5 ) D ( 13 * 4 ) + 20 ) / 5

随着开发工作的进行和与用户的交流，该标准将会日益完善，以适应越来越丰富的TRPG规则和越来越复杂的掷骰需求。

## 规则特定或掷骰系统特定的掷骰表达式

规则特定的掷骰表达式是不宜与通用掷骰表达式一同实现，但却依赖通用掷骰表达式和特定规则或掷骰系统描述的特殊表达式。此类表达式一般采取单独的首字母标识，并提供单独说明。

例如：
* b —— COC7奖励骰
* p —— COC7惩罚骰
* w —— 无限加骰池
* c —— 双重十字加骰池
* f —— fudge掷骰池

## 支持骰系

[MocliaDice](https://github.com/Moclia-Developer-Team/MocliaDice)

## 参考

墨可莉雅掷骰核心[MocliaDiceCore](https://github.com/Moclia-Developer-Team/MocliaDiceCore)  
