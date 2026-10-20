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

> 每篇论文归入其**最主要**的一种方法，避免在多个分类下重复收录。

| [Density Map（密度图回归）](src/Density_Map.md) | [Detection-based（检测后计数）](src/Detection_based.md) | [Point Supervision（点监督/定位）](src/Point_Supervision.md) |
| --- | --- | --- |
| [Direct Regression（直接全局回归）](src/Direct_Regression.md) | [Count Classification（计数分类）](src/Count_Classification.md) | [Transformer / Sequence（序列计数）](src/Transformer_Sequence.md) |
| [Weakly / Semi / Self-supervised（弱/半/自监督）](src/Weak_Semi_Self_Supervised.md) | [Few-shot / Zero-shot（小样本/零样本）](src/Few_Zero_Shot.md) | [Video / Tracking（视频时序计数）](src/Video_Counting.md) |
| [Prompt / Open-vocabulary（提示式/开放世界）](src/Prompt_Open_Vocabulary.md) | [Classical ML（传统机器学习）](src/Classical_ML.md) | [Domain Adaptation（域自适应/泛化）](src/Domain_Adaptation.md) |

## By Subject (cross-index)

> 第二索引：按收录对象反查，便于按物种/场景检索。各方法文件内也可按对象分小节。

- People（人 / 人群）：（待补充）
- Birds（鸟类）：（待补充）
- Fish（鱼群）：（待补充）
- Insects（昆虫：蜂、蚁等）：（待补充）
- Marine mammals（海洋哺乳动物）：（待补充）
- Camera-trap mammals（红外相机兽类）：（待补充）
- Cells & Microorganisms（细胞 / 微生物 / 浮游生物）：（待补充）
- Other（其他）：（待补充）

## Leaderboard

> 在公开数据集上的主流方法指标对比（MAE / MSE 等），待数据集与条目积累后再建。

| Method | Dataset | MAE | MSE | Paper | Code |
| --- | --- | --- | --- | --- | --- |
| （待补充） | | | | | |

## Contributing

欢迎补充，收录标准与条目格式见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## Related

- [gjy3035/Awesome-Crowd-Counting](https://github.com/gjy3035/Awesome-Crowd-Counting)：人群计数方向，按年份组织（本仓库的参考对象）。
