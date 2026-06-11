

<div align="center">

# 你好，我是 Zheng Mengyan 👋

**生物医学工程 · 医学 AI · 微流控检测 · 计算建模**

我目前就读于北京航空航天大学智能医学工程专业。  


</div>

---

## 关于我

我关注 **生物医学工程与人工智能交叉** 的问题：  
从分子检测芯片、荧光扩增曲线判读，到医学图像分割、ECG 信号分析、fMRI 视觉重建，以及机器人与智能感知相关的计算建模。

目前的工作主要集中在四个方向：

- **医学 AI**：医学图像分割、ECG 异常识别、基于 fMRI 的视觉重建
- **生物医学检测系统**：微流控芯片、荧光检测、AI 辅助 LAMP 曲线判读
- **科研软件开发**：基于 Python 的数据处理、建模、可视化与交互界面
- **机器人与智能感知**：LEGO EV3 机器人实验、基于 YOLO 的运动检测

---

## 代表项目

### Anatomy-informed Synthetic Pre-training for Medical Segmentation

这是一个面向医学图像分割的研究项目，已作为 **MICCAI 2026 投稿项目进入 rebuttal 阶段**。项目关注一个很核心的问题：医学影像标注昂贵、真实数据受限，那么能不能利用解剖先验生成“更像真的”的合成图像—标签对，并把它们用于分割模型的预训练？

围绕这一目标，项目引入解剖结构先验、空间锚点和拓扑约束，构建用于合成监督预训练的数据生成框架，并在 UNETR、SwinUNETR 等分割模型上验证其对下游任务的迁移价值。相比单纯做数据增强，这个项目更强调“合成数据是否符合解剖结构规律”，也更贴近医学图像分割中数据稀缺和泛化能力不足这两个真实痛点。
<--
**预印本：** https://arxiv.org/abs/2603.00979  
-->
**Repository：** `fdsl`  
**关键词：** 医学图像分割 · 合成数据 · UNETR · SwinUNETR · 解剖先验

---

### Microfluidic Detection Platform for Pathogens and Resistance Genes

这是一个 **2025 国家级大学生创新创业训练计划项目**，围绕脓毒症相关病原体与耐药基因快速检测展开，目前已形成专利和中文综述成果。项目不是单一的软件或单一的芯片设计，而是从检测需求出发，把离心式微流控芯片、LAMP 扩增、荧光采集和 AI 曲线判读串成一个完整的检测平台。

在工程实现上，项目包含芯片结构设计、COMSOL 流体仿真、SolidWorks 建模、实验验证和荧光曲线智能判读。软件部分重点解决 LAMP 曲线中阳性起峰、阴性平稳、异常曲线和多孔结果汇总的问题，让检测结果不只停留在“有曲线”，而是进一步走向自动化解释和可视化输出。

**Repository：** `ai_microfluidics`  
**关键词：** 微流控 · LAMP · 病原体检测 · COMSOL · SolidWorks · AI 判读

---

### Wearable 12-lead ECG Monitoring System

这是一个 **2025 省部级大学生创新创业训练计划项目**，目标是探索基于液态金属智能织物的可穿戴 12 导联 ECG 监测系统，并结合深度学习方法完成心电异常识别。项目的重点不只是“训练一个分类器”，而是把可穿戴采集、信号预处理、表征学习和开放世界异常识别放在同一个 pipeline 里考虑。

算法部分包含 ECG 去噪与切片、ResNet1D 表征学习、监督对比学习、原型距离建模和开放世界识别。相比普通闭集分类任务，项目更关注真实监测场景中“未知异常”和“分布外样本”的识别问题，因此在模型设计上加入了原型空间和距离度量思想。

**Repository：** `Ecg-detection`  
**关键词：** ECG · 可穿戴传感 · ResNet1D · 开放世界识别 · 医学信号处理

---

### AI-assisted Cr(VI) Fluorescence Detection

这是一个 **2024 国家级大学生创新创业训练计划项目**，面向六价铬 Cr(VI) 的荧光定量检测。项目基于碳点荧光传感，将实验检测、图像特征提取、机器学习建模和可视化界面结合起来，尝试把传统荧光检测流程做得更自动、更直观。

系统会从荧光图像中提取 RGB 颜色特征，并利用 k-means 等方法定位有效颜色区域，再通过机器学习模型建立颜色特征与 Cr(VI) 浓度之间的映射关系。最终结果通过 Python GUI 展示，形成从图像读取、特征处理、模型预测到结果可视化的一整套小型检测软件。

**Repository：** `Cr-detection`  
**关键词：** Cr(VI) 检测 · 荧光传感 · 机器学习 · RGB 分析 · Python GUI

---

### fMRI-based Cross-modal Face Reconstruction

这是一个基于 fMRI 信号进行跨模态人脸重建的项目，尝试从脑活动信号中联合解码身份、表情和性别等视觉属性。项目的核心难点在于：fMRI 信号维度高、噪声大、样本量有限，而人脸图像又包含高度复杂的语义信息。

因此，项目采用特征解耦、脑区选择性线性映射和多条件对抗生成等方法，将脑信号中的不同视觉属性拆分出来，再通过生成模型完成跨模态重建。这个项目更偏探索性，重点在于理解脑影像信号、视觉表征和生成模型之间的连接方式。

**Repository：** `MTDLN-for-f-mri-reconstruction`  
**关键词：** fMRI · 视觉重建 · mcGAN · 特征解耦 · 医学影像

---

### YOLO Motion Detection

这是一个基于 YOLO 模型的目标检测与运动分析项目，主要面向视频和图像中的实时目标识别、运动状态分析和可视化输出。项目实现了从输入视频读取、目标检测、结果标注到可视化导出的基本流程。

相比只调用现成模型，这个项目更关注如何把检测结果组织成可用的运动分析结果，包括目标框绘制、帧级输出、视频结果保存和后续分析接口，为后续接入实验场景或传感任务提供基础。

**Repository：** `yolo_motion_detect`  
**关键词：** YOLO · 目标检测 · 运动检测 · OpenCV · Python

---

### Lung Tumor Segmentation Task

这是一个基于 UW-Madison 数据集的医学图像分割任务，围绕肺部肿瘤区域分割展开。项目覆盖医学图像预处理、数据读取、模型训练、分割评估和结果可视化等环节，是一个比较完整的医学影像分割练习项目。

项目重点在于熟悉医学图像分割任务中常见的数据组织、mask 处理、指标评估和可视化流程，为后续更复杂的医学分割模型和科研任务打基础。

**Repository：** `UM-Madison-task`  
**关键词：** 肺肿瘤分割 · 医学影像 · 深度学习 · Jupyter Notebook

---


## 妙妙工具

这里放一些**灵光一闪，写着玩玩**的小项目，而且感觉也挺有用的，纯粹是好玩但做得比较完整：能跑、有界面、有配置。
**快下载来玩！😘**

### PaperMate Lit Assistant

一个面向科研阅读流程的本地文献助手。它解决的是“文献越搜越多、摘要越看越乱、笔记不知道放哪”的问题，把论文检索、文献收藏、摘要阅读、阅读卡片整理、笔记管理、文献矩阵导出和学术词汇学习放进同一个 Streamlit 应用里。

这个工具可以覆盖科研阅读中最容易失控的中间环节：先快速判断论文值不值得读，再把读过的内容沉淀成结构化卡片、对比矩阵和可复用笔记。顺手还加了学术词汇本和复习机制，适合边读英文文献边积累专业表达。

**Repository：** `papermate-lit-assistant-v3`  
**关键词：** 文献管理 · 学术阅读 · 论文检索 · 阅读卡片 · 词汇本 · Streamlit

---

### DataScope AutoML Report

一个面向科研表格数据和影像数组数据的自动分析、建模与报告生成工具。它的目标是把“拿到一张表之后不知道先看什么、怎么建模、怎么写结果”的流程自动串起来：从数据读取、EDA、数据质量检查，到模型训练、解释分析和报告导出，都可以在一个界面里完成。

项目支持 CSV、TSV、Excel、多 sheet 表格数据，也支持 NPZ / DICOM 等常见科研数据格式的读取和预览。功能上包含缺失值分析、异常值检测、数据泄漏检查、高基数类别处理、交叉验证、超参数搜索、XGBoost / LightGBM 接口、SHAP 解释，以及 HTML / Markdown 报告导出。

**Repository：** `datascope-automl-report-v3`  
**关键词：** AutoML · EDA · 科研数据分析 · 机器学习 · SHAP · DICOM · NPZ · Streamlit

---

### AITI Test

一个基于 React + Vite 的趣味 AI 类型测试网页，主打“测测你像哪个 AI”。用户完成 30 道选择题后，系统会根据人格向量和 AI 权重向量计算相似度，生成最匹配的 AI 类型、主人格、副人格和隐藏标签。

题目、选项、人格标签、AI 权重和图标都可以通过 JSON 文件修改；计分逻辑基于向量累加、余弦相似度和 softmax 归一化；结果页则负责把计算结果包装成更有传播感的展示文案。

**Repository：** `AITItest`  
**关键词：** React · Vite · 趣味测试 · 人格向量 · 交互网页 · 前端项目

---

## 技术栈

**编程语言：** Python, MATLAB, R, Verilog HDL, LaTeX, Kotlin, JavaScript  
**AI / 数据分析：** PyTorch, NumPy, pandas, scikit-learn, OpenCV, XGBoost, LightGBM  
**医学影像与信号：** AFNI, FSL, ECG processing, medical image segmentation, DICOM / NPZ processing  
**工程设计：** SolidWorks, COMSOL, Multisim, ModelSim  
**界面与部署：** Streamlit, Python GUI, React, Vite, data visualization

---

## 仓库导航

| Repository | 方向 |
|---|---|
| `fdsl` | 解剖先验驱动的医学图像分割合成预训练 |
| `ai_microfluidics` | AI 辅助微流控检测与 LAMP 曲线判读 |
| `Ecg-detection` | ECG 信号处理与开放世界异常识别 |
| `Cr-detection` | 机器学习辅助 Cr(VI) 荧光检测 |
| `MTDLN-for-f-mri-reconstruction` | 基于 fMRI 的跨模态人脸重建 |
| `UM-Madison-task` | 肺肿瘤医学图像分割任务 |
| `facialmuscle-segmentation` | 面部肌肉分割与解剖感知分析 |
| `CBIS_task` | 乳腺影像分类与分析任务 |
| `yolo_motion_detect` | 基于 YOLO 的目标检测与运动分析 |
| `lego_ev3_robotics` | LEGO EV3 机器人编程与传感控制 |
| `papermate-lit-assistant-v3` | 科研文献检索、阅读卡片与词汇学习工具 |
| `datascope-automl-report-v3` | 科研数据 AutoML 分析与自动报告生成工具 |
| `AITItest` | 基于 React 的 AI 类型趣味测试网页 |

---

## 最近正在做

- 改进 AI 辅助 LAMP 荧光扩增曲线判读流程
- 为生物医学检测软件开发更简洁的移动端 / Web 交互界面
- 构建医学图像分割相关的数据处理、训练和评估流程
- 将生物医学检测系统从芯片设计、实验验证延伸到智能结果解释
- 开发轻量级科研工具，用于文献阅读、数据分析和交互式展示

---

## 联系方式

- Email: zmy050516@buaa.edu.cn
- GitHub: [ZhiMayou0516](https://github.com/ZhiMayou0516)
