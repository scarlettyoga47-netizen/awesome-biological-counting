# Datasets（数据集收集）

> 计数任务常用公开数据集汇总。只收录**公开可获取**的数据集，链接必须真实可达，不编造下载地址。
> 下表数据集由首批 5 篇论文实验提取，规模 / 划分均按各篇原文口径；下载链接待核验后补。

## 收录标准

- **公开可获取**：注明是否公开直接下载、是否需要注册 / 邮件申请 / 签协议。
- **标注类型 Annotation**：Point（中心点）/ Box（检测框）/ Region-level（区域计数，弱监督）/ Image-level（仅图级总数），可组合，必须标清。
- **规模 Scale**：写清口径（多少张图像 / 多少标注个体），不写笼统的"大规模"。
- **划分 Split**：写明训练 / 测试划分方式；无公开划分则注明。
- 跨对象数据集在 Subject 栏写多个对象。

## 数据集总表

| Dataset | Subject 对象 | Scene 场景 | Scale 规模 | Annotation 标注 | Split 划分 | Paper | Link |
| --- | --- | --- | --- | --- | --- | --- | --- |
| WorldExpo'10 | People | 多场景监控（108 场景） | 3980 标注图像 / 1132 视频序列 / 108 场景 | Point | 103 场景训练 / 5 场景测试 | [FSCC](#fscc) | 待补充 |
| Mall | People | 商场室内监控 | 2000 帧 | Point | 800 训练 / 1200 测试 | [FSCC](#fscc)、[CS-SLR](#cs-slr)、[DeepCount](#deepcount)  | 待补充 |
| Shanghai Tech Part A | People | 密集人群街头 | 300 训练 / 182 测试图像，241,677 标注，平均 501 人 | Point | 300 训练 / 182 测试 | [DeepCount](#deepcount)、[MSCNN](#mscnn) | 待补充 |
| Shanghai Tech Part B | People | 稀疏街头 | 原文未详述图像数（稀疏街道场景） | Point | 原文未详述 | [DeepCount](#deepcount)、[MSCNN](#mscnn) | 待补充 |
| UCF-QNRF | People | 稀疏 + 密集混合 | 1,251,642 标注，单图最多 12,865 标注 | Point | 原文未详述 | [DeepCount](#deepcount)、[MSCNN](#mscnn) | 待补充 |
| UCSD | People | 室外监控 | 2000 帧，238×158，11–46 人 | Point | 800 训练 / 1200 测试 | [FSCC](#fscc)、[CS-SLR](#cs-slr)、[FE-VOC](#fe-voc) | 待补充 |
| UCF_CC_50 | People | 密集人群静态图 | 50 张灰度图，94–4543 人 | Point | 5 折交叉验证 | [CrowdNet](#crowdnet) | 待补充 |
| Bacterial cell dataset | 细菌细胞 | 显微镜 | 5 个子集（不同训练样本数） | Point | 按子集划分 | [FE-VOC](#fe-voc) | 待补充 |
| Synthetic cells（合成荧光显微镜细胞） | Cells | 荧光显微镜 | 200 张，171±64 细胞 | Region-level（弱监督） | 100 训练 / 100 测试 | [GP-WS](#gp-ws) | 待补充 |
| Pedestrian（室外监控行人） | People | 室外监控视频 | 2000 张，29±9 人 | Region-level（弱监督） | 5 帧稀疏标注训练，其余评测 | [GP-WS](#gp-ws) | 待补充 |
| Malaria（疟疾血涂片红细胞） | Cells | 显微镜血涂片 | 78 张，90±84 红细胞 | Region-level（弱监督） | 5 图训练 / 其余测试 | [GP-WS](#gp-ws) | 待补充 |

### 字段说明

- **Subject**：人 / 鸟 / 鱼 / 昆虫 / 海洋哺乳动物 / 红外相机兽类 / 细胞微生物等，可多个。
- **Scene**：监控 / 航拍 / 水下 / 红外相机 / 显微镜 / 野外地面等。
- **Scale**：图像数 / 标注个体数，注明单位。
- **Annotation**：Point / Box / Region-level / Image-level，可组合。
- **Split**：官方 train/test 划分；无则写 `未公开`。
- **Paper**：使用该数据集的来源论文（见下方条目，锚点跳转）；
- **Link**：下载页 / 项目主页，待核验补全。

## 来源论文（条目格式）

- <a name="fscc"></a>**[FSCC]** Few-Shot Scene Adaptive Crowd Counting Using Meta-Learning（**WACV 2020**）[[论文](https://arxiv.org/abs/2002.00264)][[代码](https://github.com/maheshkkumar/fscc)]
- <a name="DeepCount"></a>[**DeepCount**]Deep Density-aware Count Regressor(**ECAI 2020**)[[论文]](https://arxiv.org/abs/1908.03314)[[代码]](https://github.com/GeorgeChenZJ/deepcount)
- <a name="cs-slr"></a>**[CS-SLR]** Cost-Sensitive Sparse Linear Regression for Crowd Counting with Imbalanced Training Data（**ICME 2016**）[[论文](https://web.pkusz.edu.cn/adsp/files/2015/10/Cost-Sensitive-Sparse-Linear-Regression-For-Crowd-Counting-With-Imbalanced-Training-Data.pdf)]
- <a name="fe-voc"></a>**[DE-VOC]** Fast Visual Object Counting via Example-based Density Estimation（**ICIP 2016**）[[论文](https://web.pkusz.edu.cn/adsp/files/2015/10/Fast-Visual-Object-Counting-via-Example-based-Density-Estimation.pdf)]
- <a name="crowdnet"></a>**[CrowdNet]** CrowdNet: A Deep Convolutional Network for Dense Crowd Counting（**ACMMM 2016**）[[论文](https://arxiv.org/abs/1608.06197)]
- <a name="gp-ws"></a>**[GP-WS]** Gaussian Process Density Counting from Weak Supervision（**ECCV 2016**）[[论文](https://doi.org/10.1007/978-3-319-46448-0_22)]
- <a name="MSCNN"></a>[**MSCNN**]Multi-scale Convolution Neural Networks for Crowd Counting(**ICIP 2016**)[[paper]](https://arxiv.org/abs/1702.02359)[[code]](https://github.com/Ling-Bao/mscnn)

## 按对象速查

- People（人 / 人群）：WorldExpo'10、Mall、UCSD、UCF_CC_50、Pedestrian、Shanghai Tech PartA、Shanghai Tech PartB、UCF-QNRF
- Cells & Microorganisms（细胞 / 微生物 / 浮游生物）：Bacterial cell dataset、Synthetic cells、Malaria
- Birds（鸟类）：（待补充）
- Fish（鱼群）：（待补充）
- Insects（昆虫）：（待补充）
- Marine mammals（海洋哺乳动物）：（待补充）
- Camera-trap mammals（红外相机兽类）：（待补充）
- Other（其他）：（待补充）
