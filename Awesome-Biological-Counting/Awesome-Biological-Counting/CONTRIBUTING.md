# Contributing

感谢你愿意补充本合集。提交前请先阅读以下收录标准、分类裁决与格式约定。

## 收录范围

- 任务：用图像 / 视频做**个体计数**（counting），输出总数，或同时给出位置（密度图 / 点 / 框）。
- 对象：人以及其他生物（鸟、鱼、昆虫、海洋哺乳动物、红外相机兽类、细胞、微生物等）。
- 类型：正式发表的论文（会议 / 期刊 / arXiv）、公开数据集、官方开源代码。
- 不收：纯检测、纯分割但不做计数的工作；无法访问的死链；虚构或未公开的代码。

## 分类结构：三大主干 + 两个横切范式

**三大技术主干（公认范式）**，见 [README.md](README.md) 的 Papers 矩阵：

1. **Density Map 密度图回归**：回归密度图再积分得总数（含点监督定位、密度图 Transformer、传统密度估计）。
2. **Detection-based 检测后计数**：先检测框选个体再数框（含检测+跟踪去重）。
3. **Direct Regression 直接全局回归**：直接输出总数（含计数分类、传统非深度回归）。

**两个横切范式（正交叠加，按主要贡献归入）**：

4. **Few-shot / Zero-shot**：少样本 / 零样本泛化计数。
5. **Weakly / Semi / Self-supervised**：弱 / 半 / 自监督。

## 归类裁决规则（一篇只归一类）

1. **先判横切范式**：若论文核心贡献是少/零样本泛化，或弱/半/自监督监督范式，先归入对应横切范式文件，不再按底层技术归主干。
2. **否则按技术主干归**：看输出形式——密度图积分归 Density_Map；检测框计数归 Detection_based；直接输出总数归 Direct_Regression。
3. 一篇论文只出现在一个分类下，不在多处重复。
4. 拿不准时在 PR 里说明"核心贡献是什么、为什么归这一类"，由维护者裁定。

## 暂不单列、先并入最近主干的标签

以下方向先不建独立文件，先按技术主干就近归入，攒到约 10 篇再拆：Video/Tracking 视频时序、Domain Adaptation 域自适应/泛化、Prompt/Open-world 提示式/开放世界、Classical ML 传统非深度方法（在条目后标注 `(classical)`）。

## 条目格式

放入对应文件列表中：

```markdown
- <a name="缩写"></a>**[缩写]** 论文标题（**会议/期刊 年份**）[[论文](论文链接)][[代码](代码链接，无则省略)]![GitHub stars](http://img.shields.io/github/stars/作者/仓库.svg?logo=github&label=Stars)
```

填写要求：

- `缩写`：论文常用简称（网络名），全局唯一，用于 `#缩写` 锚点。
- `会议/期刊`：通用缩写，如 CVPR / ICCV / ECCV / NeurIPS / ICLR / AAAI / TPAMI / TIP / WACV。
- 链接必须真实可达：paper 优先 arXiv / 官方开放获取；code 只填官方仓库，非官方复现需标注 `unofficial code`。
- 没有代码就不要写 `[代码]`，更不要编造仓库地址；Stars 徽章可省略。

## 数据集条目格式（README 的 Datasets 表）

| Dataset | Subject | Scene | Scale | Annotation | Link |
| --- | --- | --- | --- | --- | --- |

- Scale：样本图像数量 / 标注个体数量，写清口径。
- Annotation：Point / Box / Image-level，可组合。

## 提交流程

1. 在对应 `src/*.md` 追加条目；新增数据集填 README 的 Datasets 表。
2. PR 说明：论文标题、年份、归入哪一类、paper/code 链接核验结果。
3. 合并前逐条核验链接可打开，避免死链。
