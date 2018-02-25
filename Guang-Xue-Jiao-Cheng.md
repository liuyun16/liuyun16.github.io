[TOC]

## 偏振(Polarization)
- **印象**：按理说，光是横波，电场矢量与磁场矢量均只需与传播方向垂直即可。但是，若光的电场矢量沿着**固定方向振**动，则称之为光的**偏振**。与此相反的，自然光，电矢量在各个方位都有。
![img](https://farm5.staticflickr.com/4699/25799177728_ef5903f4e3_o.png)

- 原文：**偏振**（polarization）指的是[横波](https://zh.wikipedia.org/wiki/%E6%A8%AA%E6%B3%A2 "横波")能够朝着不同方向[振荡](https://zh.wikipedia.org/wiki/%E6%8C%AF%E8%8D%A1 "振荡")的性质。理论而言，只要垂直于传播方向的方向，振荡的电场可以呈任意方向。假若电场的振荡只朝着单独一个方向，则称此为“线偏振”或“平面偏振”；假若电场的振荡方向是以电磁波的波频率进行旋转动作，并且电场矢量的矢端随着时间流意勾绘出圆型，则称此为“圆偏振”。
![](https://www.edmundoptics.com/contentassets/bd02b4a1c6a1433c97387c11d52ac0c7/fig-2-itp.gif)
![](https://farm5.staticflickr.com/4608/39640384092_410cbe016b_o.gif)
- **s, p偏振光**：按照入射光与反射光组成的**入射平面**来确定。**平行于入射平**面的称之为p偏振光（parallel），**垂直于入射平面**的为s偏振光。
![](https://farm5.staticflickr.com/4628/39641419852_193ab723a3_o.png)
- 出处：
  - [偏振 - 维基百科，自由的百科全书](https://zh.wikipedia.org/wiki/%E5%81%8F%E6%8C%AF)
  - [Polarization (waves) - Wikipedia](https://en.wikipedia.org/wiki/Polarization_(waves))
  - 动画很不错，[Introduction to Polarization | Edmund Optics](https://www.edmundoptics.com/resources/application-notes/optics/introduction-to-polarization/)
- 2018年1月13日

## 反常识：光矢量即电场矢量。
- 印象：电场矢量可以描述光的很多性质。
- 原文：由于光的许多方面的效应（如感光、光电效应）都是通过**电场**作用表现，因此将光波的电矢量称之为光矢量。
   - 光的频率就是光矢量每秒钟振动的次数；
   - 光是横波，光矢量方向与传播方向垂直。
- **出处**：激光原理及应用，陈家壁，第二版，P2
- 2018年1月13日22:31:23


## 光波，电介质与复数

- 出处：费曼物理学讲义，第2卷，P419，chap31.


## 张量
- 印象：描述某一种方向性的矩阵，与方向性有关，各向异性有关。
- 原文：
- 例子：
  - 极化张量：
    $$ P_i = \sum_{i}\alpha_{ij}E_j $$
    其中，i，j代表x，y或z.
    类似于：![img](https://farm5.staticflickr.com/4709/39674811281_368154db4f_o.png)
    - 物理意义：若电场E具有沿x,y和z的各个分量，极化强度P在在每个方向上都会产生分量，且其方向不一定与$E_i$方向相同，而是各自在坐标上的贡献之和。
- 出处：费曼物理学讲义(新千年版)，第2卷，P417

## 激光种类
### 激光工作方式：(CW、Pulse、Ultrafast)
- Continuous-wave (CW)：激光连续的泵浦、发射激光，其输出功率可用W表示。
  - 例子：气体激光：如HeNe激光，CO2激光；

- 脉冲式：激光是一连串的短脉冲尖峰组成，尖峰的出现频率也称之为重复频率。输出性能用**脉冲宽度**和**峰值功率**表示。
  - 如一般的固体激光器。为了改善光脉冲序列，有人提出调Q(Q-Switch)的概念。利用调Q，使得开始谐振腔在泵浦开始时处于低Q值，粒子密度反转数积累的到很高的水平也不会产生振荡。当粒子反转达到峰值时，突然使Q增大，激光介质快速阈值，此时产生峰值功率高，宽度窄的巨脉冲。

- 出处：
 - [Lasers: Understanding the Basics | lasers | Photonics Handbook](https://www.photonics.com/a25161/Lasers_Understanding_the_Basics)
 - 激光原理及应用，P154

### He-Ne激光
- 波长：0.6328μm的红光(3S-->2P)；
- 工作物质：Ne原子受激辐射，He提高Ne的泵浦速率。
- 工作方式：连续，Continuous-wave (cw)
- 出处：陈家壁，激光原理及应用，P172.


### CO2激光
- CO2为工作物质的气体激光器。
- 波长：10.6 μm和9.6 μm。
- 优点：既能连续工作，也可脉冲工作。连续输出功率可达万兆瓦，脉冲输出可达万焦耳，脉冲宽度可压至ms-μs。
- 出处：陈家壁，激光原理及应用，P172.
- Q？？？？？: SNOM 下，都是脉冲式？还是连续式？

### quantum cascade lasers(QCL，量子级联)
- 原理：半导体激光器，但不是带隙间的电子--空穴转换，而是量子限域的级联势阱导致的电子束反转。
![](https://farm5.staticflickr.com/4742/39679986822_fe9b570006_o.png)
- 具体实现：分子束外延多层超晶格薄膜。在垂直方向构建级联电势，可通过级联的薄膜层数实现激光波长的调节。
- 频率范围：3.6～19μm 中远红外。
- 工作方式：连续式、脉冲式均可。
- 出处：
  - [量子级联激光器的原理及主要应用概述](http://laser.ofweek.com/2015-08/ART-240002-11000-28990516.html)
  - [Quantum cascade laser - Wikipedia](https://en.wikipedia.org/wiki/Quantum_cascade_laser)

### 自由电子激光
- 时间结构：
![img](https://farm5.staticflickr.com/4769/25762839648_337c4d1f96_o.png)
- 出处： 
> FB Talk，2017， Dr.Kuhlenbeck

### Repetition Rate(重复频率)：
当激光为脉冲式(许多固体激光器，因为需要实现受激辐射，都为脉冲式)时，每秒脉冲数目或者频率称之为脉冲重复频率。
 Pulse energy = peak power x pulse width
  - ![img](https://farm5.staticflickr.com/4746/24786426737_3e29ba632a_o.png)
  - 出处：[Pulse Repetition Rate | Definition Pulse Repetition Rate](http://www.amadamiyachi.com/glossary/glosspulserepetitionrate)
    
**Q**: Is the response of the materials could be followed by the THz pulse?

