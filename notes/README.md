# 技术分析  

#### 移动平均本质
移动平均是在平滑度和滞后性之间的权衡。好的移动平均指标在保证平滑度的时候尽可能减小滞后性。

ex.
- 赫尔移动平均（HMA)
- 分形自适应移动平均

link: https://zhuanlan.zhihu.com/p/38276041


# 量化因此

#### 用IC衡量因子的改进方法
通常用correlation或rank correlation来衡量因子和收益之间的关联。
![](https://pic4.zhimg.com/80/v2-a2fa84b1638a1b9f51d754b5320ce143_720w.jpg)
但从上图中来看同样的correlation，左图的因子最大值对应收益最大，但右图不然
__结论除了关注correlation，还要看头部的lift__

link: https://zhuanlan.zhihu.com/p/41454197


# 统计模型  

#### Quantile Regression分析相关性
- 最小化MSE => 样本均值为最优解  
- 最小化MAE => 样本median为最优解  

将中位数推广到一般分位数。在所有分位数中间，中位数（又称 50% 分位数）比较特殊是在于在求解最优化问题中，其两侧样本点的残差是等权重的。
把上述最小化残差绝对值的问题推广到一般的`q`分位数时，只需把`q`分位数两侧的残差赋予不同的权重即可。

具体的，对于`q`分位数左侧样本点的残差，赋予它们`1-q`的权重；对于q分位数右侧样本点的残差，赋予它们`q`的权重。
link: https://zhuanlan.zhihu.com/p/40681570


#### 凯利公式
凯利公式核心：最优化单期对数收益
link: https://zhuanlan.zhihu.com/p/38279377
