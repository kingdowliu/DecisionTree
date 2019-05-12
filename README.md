### 决策树

- 决策树是一种机器学习算法，常用于分类问题的研究。
&nbsp;
- 其决策过程是按照样本特征不断对样本进行分类划分。我们以二分类为例，首先，我们按照其特征一对样本进行划分，假定样本类别为1和-1，如果是特征一，就将其划入集合 <a href="https://www.codecogs.com/eqnedit.php?latex=$S_1$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?$S_1$" title="$S_1$" /></a> 中，否则将其划入 <a href="https://www.codecogs.com/eqnedit.php?latex=$S_2$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?$S_2$" title="$S_2$" /></a> 中，经过一次划分，我们得到了两个集合，如果集合 $S_1$ 中全是正类，我们将按照这个特征进行划分所得的集合成为正类，反之为负类。如果集合中既有正类样本、又有负类样本，我们将对这个集合继续进行划分，直至集合中元素纯净，接下来，我们选择特征二进行同样操作，最终，我们将得到一个类似于一颗树状的分类模型，按照这个模型，我们可以对其它训练样本之外的数据进行分类，从而判定其所属的类别。
&nbsp;
- 决策树的生成过程是一个递归过程，在决策树算法中，有三种情况会导致递归返回。
  - 当前结点所包含的样本全属于同一类别，无需划分；
  - 当前属性集为空，或是所有样本在所有属性上取值相同，无法划分；
  - 当前结点所包含的样本集合为空，不能划分；
- 对于上述第二种情形，我们把当前结点标记为叶子结点，并将其类别设定为<font color="#00f">该结点</font>所含样本最多的类别，如果集合中正类多于负类，即为正类，反之，为负类。对于第三种情形，我们同样将当前结点标记为叶子结点，但将其类别设定为<font color="#00f">其父结点</font>所含样本最多的结点。
&nbsp;
- 先根据哪个特征进行划分最佳？
  1. 根据信息增益划分
     - [信息熵](https://baike.baidu.com/item/%E4%BF%A1%E6%81%AF%E7%86%B5/7302318?fr=aladdin)：度量样本纯度的一个指标，其值越小，代表集合中元素越纯，所包含的类别越少，越倾向于同一类。公式为 <a href="https://www.codecogs.com/eqnedit.php?latex=$Ent(D)&space;=&space;-&space;\sum_{k=1}^{|\gamma|}p_klog_2p_k$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?$Ent(D)&space;=&space;-&space;\sum_{k=1}^{|\gamma|}p_klog_2p_k$" title="$Ent(D) = - \sum_{k=1}^{|\gamma|}p_klog_2p_k$" /></a>，其中 <a href="https://www.codecogs.com/eqnedit.php?latex=$p_k$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?$p_k$" title="$p_k$" /></a> 是指当前样本中第 <a href="https://www.codecogs.com/eqnedit.php?latex=$k$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?$k$" title="$k$" /></a> 类样本所占的比例，范围是 <a href="https://www.codecogs.com/eqnedit.php?latex=$(k=1,2,...\gamma)$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?$(k=1,2,...\gamma)$" title="$(k=1,2,...\gamma)$" /></a>
     - [信息增益](https://baike.baidu.com/item/%E4%BF%A1%E6%81%AF%E5%A2%9E%E7%9B%8A/8864911?fr=aladdin)：类似于信息熵的增量。



**施工中...**
