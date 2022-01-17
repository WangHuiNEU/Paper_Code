# 蛋白质结构预测

> 总结相应的蛋白质结构预测的论文、科普文章及相关视频

# 1. Alphafold2相关

[TOC]



## 1. Alphafold2，AlphaFold-Multimers讲解 

> https://www.bilibili.com/video/BV1fm4y1D7Wz 

### 1. 什么是结构预测

<img src="蛋白质折叠Fold.assets/image-20220117165157438.png" alt="image-20220117165157438" style="zoom:80%;" />

**蛋白质的折叠过程，如上图所示，蛋白质只有折叠成三级结构或者四级结构才能发挥相应的作用。**

---



  **Anfinesen's dogma(信条)**                                              <img src="蛋白质折叠Fold.assets/image-20220117165221136.png" alt="image-20220117165221136" style="zoom:67%;" />

​        

- **蛋白质折叠成原始结构所需的信息都已经编码在氨基酸序列中**

- **蛋白质折叠到最小能量状态**
- **大多数蛋白质会折叠成一个独特的构象**

---

### 2. 为什么结构预测很重要？

<img src="蛋白质折叠Fold.assets/image-20220117165924030.png" alt="image-20220117165924030" style="zoom: 67%;" />  <img src="蛋白质折叠Fold.assets/image-20220117170110720.png" alt="image-20220117170110720" style="zoom:50%;" />

**现在遇到的问题，实验方法低通量但是高准确度，计算方法高通量但是低准确度**

> https://www.dnastar.com/blog/structural-biology/why-structure-prediction-matters/

```python
从实验的角度来看，最大的挑战是成本、时间和专业知识。使用晶体学和 NMR 解决结构需要极其专业的培训、高超的技能和大量的运气。解决一个新的、独特的结构的成本约为 100,000 美元。鉴于解决实验结构的难度，并考虑到发现新蛋白质序列的速度，很明显，以今天的技术，我们将无法解决所有正在识别和测序的新蛋白质的结构。
将 UniProt 中的蛋白质序列数量与 PDB 中已知结构的数量进行比较），我们发现序列比结构多 1700 倍以上。当这篇文章在 5 年前首次发表时，这个差异只有 400 倍。由于新序列的数量继续呈指数级增长，这种差距将持续存在，并且只会随着时间的推移而变得更大。随着这种差距的增加，寻找预测蛋白质结构的替代方法变得越来越重要。
```

---

<img src="蛋白质折叠Fold.assets/image-20220117170136645.png" alt="image-20220117170136645" style="zoom:80%;" />

<img src="蛋白质折叠Fold.assets/image-20220117170750011.png" alt="image-20220117170750011" style="zoom:50%;" />

**主要就是提升一些困难的蛋白**

### 3. 预测蛋白质结构

<img src="蛋白质折叠Fold.assets/image-20220117170843779.png" alt="image-20220117170843779" style="zoom:80%;" />

**之前的方法都是先得到序列的Contact map，然后再从contact map再去预测序列的结构，因为直接从序列到结构是相对来说有些困难的。**

<img src="蛋白质折叠Fold.assets/image-20220117171049662.png" alt="image-20220117171049662" style="zoom:80%;" />

**从Co-evolution到structure**

---

<img src="蛋白质折叠Fold.assets/image-20220117171205391.png" alt="image-20220117171205391" style="zoom:80%;" />

---

<img src="蛋白质折叠Fold.assets/image-20220117194757764.png" alt="image-20220117194757764" style="zoom:80%;" />



### 4. 1 架构 --- 模型输入

<img src="蛋白质折叠Fold.assets/image-20220117194955694.png" alt="image-20220117194955694" style="zoom:80%;" />



### 4.2 架构 ---- Recycling

<img src="蛋白质折叠Fold.assets/image-20220117195104388.png" alt="image-20220117195104388" style="zoom:80%;" />



### 4.3 架构 --- Evoformer

<img src="蛋白质折叠Fold.assets/image-20220117195145727.png" alt="image-20220117195145727" style="zoom:80%;" />



### 4.4 架构 --- Structure Module

<img src="蛋白质折叠Fold.assets/image-20220117195252390.png" alt="image-20220117195252390" style="zoom:80%;" />

<img src="蛋白质折叠Fold.assets/image-20220117195347990.png" alt="image-20220117195347990" style="zoom:80%;" />

### 4.5 架构 --- 多输出

<img src="蛋白质折叠Fold.assets/image-20220117195537945.png" alt="image-20220117195537945" style="zoom:80%;" />

**不光可以得到模型结构，也可以得到模型结构的置信度**



### 4.6 总结

<img src="蛋白质折叠Fold.assets/image-20220117195638388.png" alt="image-20220117195638388" style="zoom:80%;" />

### <img src="蛋白质折叠Fold.assets/image-20220117195812620.png" alt="image-20220117195812620" style="zoom:80%;" />

### 5. 结构预测的本质

<img src="蛋白质折叠Fold.assets/image-20220117195933141.png" alt="image-20220117195933141" style="zoom:80%;" />



**单体之间的共进化信息和复合物之间的共进化是不同的**



### 6. Alphafold-Multimer

<img src="蛋白质折叠Fold.assets/image-20220117200154076.png" alt="image-20220117200154076" style="zoom:80%;" />

<img src="蛋白质折叠Fold.assets/image-20220117200252977.png" alt="image-20220117200252977" style="zoom:80%;" />

### 7. 结果

<img src="蛋白质折叠Fold.assets/image-20220117200603619.png" alt="image-20220117200603619" style="zoom:80%;" />

<img src="蛋白质折叠Fold.assets/image-20220117200642549.png" alt="image-20220117200642549" style="zoom: 80%;" />

<img src="蛋白质折叠Fold.assets/image-20220117200712705.png" alt="image-20220117200712705" style="zoom:80%;" />

并不推荐随便增加Recycling的轮数，在训练的时候Recycling是三轮，因此在测试的时候不要随意加轮数，在默认3轮效果不好的情况下可以看看增加轮数的效果。

<img src="蛋白质折叠Fold.assets/image-20220117200919273.png" alt="image-20220117200919273" style="zoom:80%;" />

结论：

- **MSA的deep超过30就可以取得非常好的结果，MSA的deep超过100对效果的提升并不明显，deep变为1000和100000对效果提升并不大。**
- **当MSA的效果可以的话，有没有模板的效果相差不大，红色是Coverage> 0.6，可以找到一个好的模板，和蓝色Coverage<0.3，没有一个好的模板，二者在MSA的deep大于100的时候效果相差并不大。**

**因此，对于Alphafold2l来说，模板的影响并不大，MSA的质量很高的话，即使没有模板，出来的结构也是可以的。**



### 8. Alphafold2 结构探究

<img src="蛋白质折叠Fold.assets/image-20220117201545814.png" alt="image-20220117201545814" style="zoom:80%;" />

**因此，Alphafold2并没有学习到蛋白真实的结构，而是这个蛋白在结晶情况下得到的结构是什么，晶体结构并不代表蛋白质的构象。**



### 9. Alphafold-Multimer 结果

<img src="蛋白质折叠Fold.assets/image-20220117201928397.png" alt="image-20220117201928397" style="zoom:80%;" />

<img src="蛋白质折叠Fold.assets/image-20220117201946757.png" alt="image-20220117201946757" style="zoom:80%;" />

###10.  Alphafold 速度优化

> https://github.com/WangHuiNEU/ParallelFold

<img src="蛋白质折叠Fold.assets/image-20220117202208470.png" alt="image-20220117202208470" style="zoom:80%;" />

<img src="蛋白质折叠Fold.assets/image-20220117202223588.png" alt="image-20220117202223588" style="zoom:80%;" />

<img src="蛋白质折叠Fold.assets/image-20220117202251588.png" alt="image-20220117202251588" style="zoom:80%;" />



### 11. Alphafold2预测结果评估标准

<img src="蛋白质折叠Fold.assets/image-20220117202404491.png" alt="image-20220117202404491" style="zoom:80%;" />



**PLDDT表明这个结构local的置信度，范围在0~100，高于70才具有置信度，高于90的置信度非常高。**

**PAE表明预测出来的和真实的距离，可以预测domain的效果和domain和domain直接的效果**

### 13. Alphafold2 是否可以预测突变

<img src="蛋白质折叠Fold.assets/image-20220117202933306.png" alt="image-20220117202933306" style="zoom:80%;" />



### 14. Alphafold-Multimer 预测多聚体

<img src="蛋白质折叠Fold.assets/image-20220117203010401.png" alt="image-20220117203010401" style="zoom:80%;" />

<img src="蛋白质折叠Fold.assets/image-20220117203038402.png" alt="image-20220117203038402" style="zoom:80%;" />

Alphafold-Multimer并不能够预测抗原和抗体结合

### 15. Alphafold-Multimer 预测新冠病毒

#### 1. 预测RBD和ACE-2结合

**Alphafold-Multimer预测新冠病毒的RBD和ACE-2结合 【结果并不能预测出来】**

<img src="蛋白质折叠Fold.assets/image-20220117203613258.png" alt="image-20220117203613258" style="zoom:80%;" />

Alphafold-Multimer有在无规区域的结合

#### 2. 预测S蛋白同源三聚体

<img src="蛋白质折叠Fold.assets/image-20220117203740634.png" alt="image-20220117203740634" style="zoom:80%;" />

Alphafold-Multimer预测出来一团毛线，但是Colabfold预测出来的效果还比较可以

<img src="蛋白质折叠Fold.assets/image-20220117203844507.png" alt="image-20220117203844507" style="zoom:80%;" />



<img src="蛋白质折叠Fold.assets/image-20220117203924696.png" alt="image-20220117203924696" style="zoom:80%;" />

### 16. Alphafold2能否预测蛋白质稳定性

<img src="蛋白质折叠Fold.assets/image-20220117204024297.png" alt="image-20220117204024297" style="zoom:80%;" />

<img src="蛋白质折叠Fold.assets/image-20220117204054465.png" alt="image-20220117204054465" style="zoom:80%;" />

<img src="蛋白质折叠Fold.assets/image-20220117204147958.png" alt="image-20220117204147958" style="zoom:80%;" />



# 2. Rosettafold相关

