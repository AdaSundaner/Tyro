## 决策树
### 算法原理：
#### 按照数据集中的某个特征对数据集进行数据分类。我们需要对每个特征进行评估，找到决定性的特征，从而对数据集进行划分以最好的结果。
#### 完成测试之后，原始数据集就会被划分为几个数据子集。这些数据子集会分布在第一个决策点的所有分支上。
#### 如果数据子集内的分类不属于同一类，则需要重复划分数据集。所以，我们需要选择具有关键作用的特征用来划分数据集。
#### 那么如何选择具有关键作用的特征呢，可以使用信息论的概念来进行划分。
### 信息论：
#### 划分数据集的最大原则为：将无序的数据变的更加有序。
#### 信息增益：在划分数据集前后信息发生的变化称为信息增益。
#### 熵：集合信息的度量方式称为香农熵或熵（熵即 信息的期望值）l(xi)=-log2P(xi).熵越高，混合的信息越多。
#### 判断当前是否正确的划分了数据集：我们需要对每个特征划分数据集的结果计算一次信息熵，然后判断按照哪个特征值划分数据集最好。
#### （可理解为：熵值变化最大的划分方式为最好的方式，即使用该特征值进行划分，数据集的无序程度降低的最多）

### 试用范围：
#### 只试用于标称型数据，所以数值型数据必须是离散的。
### 优点：
#### 复杂度不高，输出结果易于理解（可使用不熟悉的数据集合），对中间值的缺失不敏感。
### 缺点：
#### 可能会产生过度匹配问题。
