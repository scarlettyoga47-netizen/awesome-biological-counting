# Metrics（常用评价指标）

> 计数任务常用评价指标定义。公式为标准定义；**具体以各论文采用口径为准**，不同论文个别指标定义可能不同，引用时注明。
> 首批 5 篇论文实际使用的指标已在各指标下标注，条目见文末[使用论文条目库](#使用论文条目库)。

## 一、计数回归指标（三大主干通用，最常用）

### MAE（Mean Absolute Error，平均绝对误差）

- 公式：`MAE = (1/N) Σ |yᵢ − ŷᵢ|`
- 方向：**越低越好**。
- 说明：计数任务第一主指标，反映平均计数偏差，对异常误差不敏感。
- 本批使用：[FSCC](#fscc)、[CS-SLR](#cs-slr)、[FE-VOC](#fe-voc)、[CrowdNet](#crowdnet)、[GP-WS](#gp-ws)、[DeepCount](deepcount) 。

### MSE（Mean Squared Error，均方误差）/ RMSE（均方根误差）

- 公式：`MSE = (1/N) Σ (yᵢ − ŷᵢ)²`；`RMSE = √MSE`
- 方向：**越低越好**。
- 说明：对大误差平方放大，惩罚高估 / 低估较多的样本，常与 MAE 并列报告。
- 本批使用：MSE —— [CS-SLR](#cs-slr)；RMSE —— [FSCC](#fscc)、[DeepCount](deepcount)。

### MDE / 平均偏差（Mean Deviation Error）

- 公式：`MDE = (1/N) Σ |δᵢ − δᵢ^w| / δᵢ`（各论文归一化口径略有差异）
- 方向：**越低越好**。
- 说明：按真实数量归一化的偏差；**各论文口径略有差异**，引用时核对定义。
- 本批使用：[FSCC](#fscc)、[CS-SLR](#cs-slr)。

## 二、检测 / 定位计数指标

### Precision / Recall / F1

- 说明：检测框或中心点按 IOU / 距离阈值匹配后计算。
- Precision = TP / (TP + FP)；Recall = TP / (TP + FN)；`F1 = 2·P·R / (P+R)`。
- 方向：**越高越好**。
- 本批使用：（首批 5 篇未使用，待补充）。

### AP（Average Precision，点定位平均精度）

- 说明：点标注按匹配距离阈值统计的平均精度。
- 方向：**越高越好**。
- 本批使用：（待补充）。

## 三、视频时序计数指标

### MOTA（Multiple Object Tracking Accuracy）

- 说明：用于检测 + 跟踪去重的视频计数，衡量跨帧跟踪与计数一致性。
- 方向：**越高越好**。
- 本批使用：（待补充）。

<a name="使用论文条目库"></a>
## 使用论文条目库

- <a name="fscc"></a>**[FSCC]** Few-Shot Scene Adaptive Crowd Counting Using Meta-Learning（**WACV 2020**）[[论文](https://arxiv.org/abs/2002.00264)][[代码](https://github.com/maheshkkumar/fscc)]
- <a name="deepcount"></a>**[DeepCount]** Deep Density-aware Count Regressor（**ECAI 2020**）[[论文](https://arxiv.org/abs/1908.03314)][[代码](https://github.com/GeorgeChenZJ/deepcount)]
- <a name="cs-slr"></a>**[CS-SLR]** Cost-Sensitive Sparse Linear Regression for Crowd Counting with Imbalanced Training Data（**ICME 2016**）[[论文](https://web.pkusz.edu.cn/adsp/files/2015/10/Cost-Sensitive-Sparse-Linear-Regression-For-Crowd-Counting-With-Imbalanced-Training-Data.pdf)]
- <a name="fe-voc"></a>**[FE-VOC]** Fast Visual Object Counting via Example-based Density Estimation（**ICIP 2016**）[[论文](https://web.pkusz.edu.cn/adsp/files/2015/10/Fast-Visual-Object-Counting-via-Example-based-Density-Estimation.pdf)]
- <a name="crowdnet"></a>**[CrowdNet]** CrowdNet: A Deep Convolutional Network for Dense Crowd Counting（**ACMMM 2016**）[[论文](https://arxiv.org/abs/1608.06197)]
- <a name="gp-ws"></a>**[GP-WS]** Gaussian Process Density Counting from Weak Supervision（**ECCV 2016**）[[论文](https://doi.org/10.1007/978-3-319-46448-0_22)]

## 待补充

- 其他指标按论文实际使用补充，补充时写清：全称、公式、方向、适用场景、使用论文。
