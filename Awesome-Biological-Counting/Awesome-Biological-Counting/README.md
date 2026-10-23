# Awesome Biological Counting

> 用计算机视觉 / 机器学习方法统计图像或视频中**生物个体数量**的论文、数据集与代码合集。
> 收录对象包含人，但不限于人：鸟类、鱼群、昆虫、海洋哺乳动物、红外相机兽类、细胞与微生物等。
>
> 与人群计数（Crowd Counting）合集的区别：本仓库以**方法（Method）**为主轴组织，而非按年份罗列。

<!--
仓库英文名（目录名 / GitHub repo name）可在发布前自行修改，例如：
Awesome-Biological-Counting / Awesome-Vision-Counting / Awesome-Animal-Counting。
修改后同步更新本标题与下方所有相对链接即可。
-->

## Contents

- [News](#news)
- [Datasets](#datasets)
- [Papers (by Method)](#papers-by-method)
- [By Subject (cross-index)](#by-subject-cross-index)
- [Leaderboard](#leaderboard)
- [Contributing](#contributing)
- [Related](#related)

## News

<!-- 按时间倒序记录新数据集 / 新综述 / 重要更新，格式：- [YYYY.MM] 事件描述（链接，可选） -->

- （暂无）

## Datasets

> 单独收录计数任务常用数据集。标注类型区分：Point（点）/ Box（框）/ Image-level（仅图级总数）。

| Dataset | Subject | Scene | Scale | Annotation | Link |
| --- | --- | --- | --- | --- | --- |
| （待补充） | | | | | |

## Papers (by Method)

> 分类采用**三大技术主干 + 两个横切范式**。一篇论文只归入最主要的一类，避免重复收录。

### 三大技术主干（公认范式）

| [Density Map（密度图回归）](src/Density_Map.md) | [Detection-based（检测后计数）](src/Detection_based.md) | [Direct Regression（直接全局回归）](src/Direct_Regression.md) |
| --- | --- | --- |

### 两个横切范式（按监督 / 样本条件，正交叠加在主干之上）

| [Weakly / Semi / Self-supervised（弱/半/自监督）](src/Weak_Semi_Self_Supervised.md) | [Few-shot / Zero-shot（少样本/零样本）](src/Few_Zero_Shot.md) |
| --- | --- |

> **暂不单列、先作标签并入最近主干**（攒够约 10 篇再拆成独立文件）：Video/Tracking 视频时序、Domain Adaptation 域自适应/泛化、Prompt/Open-world 提示式/开放世界、Classical ML 传统非深度方法。归类裁决规则见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## By Subject (cross-index)

> 第二索引：按收录对象反查，便于按物种/场景检索。各主干文件内也按对象分小节。

- People（人 / 人群）：<a name="FSSA"></a>[**FSSA,2020**][[paper]](https://arxiv.org/abs/2002.00264),<a name="CS-SLR"></a>[[**CS-SLR**]][[paper]](https://ieeexplore.ieee.org/document/7552905),<a name="CrowdNet">[[**CrowdNet**]]</a>[[paper]](https://arxiv.org/abs/1608.06197),<a name="DeepCount"></a>[**DeepCount**][[paper]](https://arxiv.org/abs/1908.03314);
- Birds（鸟类）：（待补充）
- Fish（鱼群）：（待补充）
- Insects（昆虫：蜂、蚁等）：（待补充）
- Marine mammals（海洋哺乳动物）：（待补充）
- Camera-trap mammals（红外相机兽类）：（待补充）
- Cells & Microorganisms（细胞 / 微生物 / 浮游生物）：<a name="DE-VOC"></a>[**DE-VOC**][[paper]](https://web.pkusz.edu.cn/adsp/files/2015/10/Fast-Visual-Object-Counting-via-Example-based-Density-Estimation.pdf),<a name="GP"></a>[**GP**][[paper]](https://link.springer.com/chapter/10.1007/978-3-319-46448-0_22);
- Other（其他）：（待补充）

## Leaderboard

> 在公开数据集上的主流方法指标对比（MAE / MSE 等），待数据集与条目积累后再建。

| Method | Dataset | MAE | MSE | Paper | Code |
| --- | --- | --- | --- | --- | --- |
| （待补充） | | | | | |

## Contributing

欢迎补充，收录标准、分类裁决与条目格式见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## Related

- [gjy3035/Awesome-Crowd-Counting](https://github.com/gjy3035/Awesome-Crowd-Counting)：人群计数方向，按年份组织（本仓库的参考对象）。
