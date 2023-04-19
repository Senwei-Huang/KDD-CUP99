### KDD CUP99数据集的分类——网络连接异常识别

#### 一、kddcup99数据集的分类过程主要分三步完成：
**第一步：** 数据数值化
目的是将kddcup99数据集中的字符型特征或标签转换为数值型表示。
方法是将字符型特征排序，采用字符型特征的下标表示该字符型特征。

**第二步：** 数据标准化
目的是应对特征向量中数据很分散的情况，防止小数吃大数的情况，同时也可以加速训练。
方法是采用Z-score标准化。假设该数据集的分布近似服从高斯分布，基于数据的均值和方差进行标准化，标准化公式如下： $x^{\prime}=\frac{x-\bar{x}}{\sigma}$ 

**第三步：** 模型训练、预测并输出分类报告
采用数值化和标准化处理后的数据集，进行SVM算法分类并输出混淆矩阵和分类报告，从精确率：precision、召回率：recall、 调和平均f1值:f1-score和支持度:support四个维度评价分类预测效果。

#### 二、文件说明
**（1）数据集**  
原始的数据集：kddcup.data.txt  
数值化后的数据集：kddcup.data.numerization.txt  
数值化并修正错误数据后的数据集：kddcup.data.numerization_corrected.txt  
数值化、修正错误数据、标准化后的数据集：kddcup.data.numerization_corrected_normalizing_StandardScaler.txt  

**（2）程序**  
这三个程序是分步骤完成kddcup数据集分类：  
第一步：数据数值化.ipynb  
第二步：数据标准化.ipynb  
第三步：模型训练与预测.ipynb  

**（3）最终一步实现**  
经过改进后，将所有的数据处理都写一起的程序：数值化_标准化_模型训练与预测三合一.ipynb

#### 三、实验环境配置：python和package的版本
 `python: 3.6.12  
csv: 1.0  
numpy: 1.19.2  
pandas: 1.1.5  
scikit-learn: 0.23.2   
IPython: 7.16.1  
Pytorch：1.4.0`

**知乎文章：** https://zhuanlan.zhihu.com/p/340644293
