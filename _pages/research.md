---
permalink: /research/
title: "研究方向"
author_profile: true
---

课题组的布局逻辑是：**先把"看得懂"做扎实（感知），再把"造得出"做出来（生成），最后把"用得上"做进产线（工业检测与机器人）**。以下十个方向按这三层组织。

感知与理解
======

## 1. 医学图像分割

医学图像分割旨在把影像中的特定结构或区域从背景中精确提取出来，辅助医生完成影像诊断、手术计划与治疗效果评估。

<div class="archive__image">
  <img src='{{ '/resources/医学分割.png' | relative_url }}' alt="医学图像分割" style="width:80%;height:auto;" />
</div>

## 2. 人体姿态估计

包括 2D/3D 姿态估计、评估方法、DensePose 以及人体参数化模型，应用于动作识别、虚拟现实、人机交互与视频监控。课题组此前提出的局部-全局估计器与大核 CNN + Transformer 结构，已在 IEEE TIM、IEEE TCDS 发表。

<div class="archive__image">
  <img src='{{ '/resources/姿态图.png' | relative_url }}' alt="人体姿态估计" style="width:80%;height:auto;" />
</div>

生成与数字人
======

## 3. 扩散模型与 AIGC

Stable Diffusion 以约 1B 参数、可在普通显卡上推理与微调的优势，成为文生图与图像编辑的主流底座。课题组围绕 SD 的轻量化微调与教学化改造开展工作，并把它带进了课堂与高交会展台。

<div class="archive__image">
  <img src='{{ '/resources/Stable Diffusion.png' | relative_url }}' alt="扩散模型" style="width:80%;height:auto;" />
</div>

## 4. Talking Face Generation（数字人）

给定一段音频和一张驱动人脸图片，生成该人脸随音频"说话"的视频，要求唇形、表情与音频高度同步。课题组已在高交会现场展示基于扩散模型的高保真数字人生成系统。

<div class="archive__image">
  <img src='{{ '/resources/talking face generation.png' | relative_url }}' alt="talking face generation" style="width:80%;height:auto;" />
</div>

## 5. 通用（开放世界）目标检测

不依赖大规模封闭类别基准，具备开放世界泛化能力：面对未知类别也能检测，并能把未标注物体识别为"未知"，在获得标签后增量学习而不遗忘旧类别。

<div class="archive__image">
  <img src='{{ '/resources/通用模型.png' | relative_url }}' alt="通用目标检测" style="width:80%;height:auto;" />
</div>

## 6. YOLO-World 开放词表检测

以单次前向传播完成开放词表检测，无需额外区域建议或复杂后处理，适合实时场景与大规模视觉识别任务。

<div class="archive__image">
  <img src='{{ '/resources/YOLO-World开放目标检测.png' | relative_url }}' alt="YOLO-World" style="width:100%;height:auto;" />
</div>

工业检测与机器人
======

## 7. PCB 缺陷检测

基于改进 YOLO 的 PCB 缺陷检测系统，覆盖 short / open / pin_hole / spur / mouse_bite / missing_copper 六类典型缺陷，面向产线级部署（已申请专利）。

<div class="archive__image">
  <img src='{{ '/resources/PCB-det.png' | relative_url }}' alt="PCB 缺陷检测" style="width:80%;height:auto;" />
</div>

## 8. 工业异常检测

通过识别与分类产品或组件中的缺陷保障质量，涉及质量控制、过程监控、预测性维护与自动化，目标是在提效降本的同时降低缺陷品带来的安全风险。

<div class="archive__image">
  <img src='{{ '/resources/工业异常检测.png' | relative_url }}' alt="工业异常检测" style="width:80%;height:auto;" />
</div>

## 9. X 光安检检测

利用 X 射线穿透能力非侵入地检测行李、包裹中的违禁品与危险品，应用于机场、地铁站与大型活动场所。课题组在该方向获 IEEE PRCV X 光物品检测挑战赛第一名，并申请《一种 X 光违禁品检测方法及装置》专利。

<div class="archive__image">
  <img src='{{ '/resources/X光检测.jpg' | relative_url }}' alt="X 光安检检测" style="width:80%;height:auto;" />
</div>

## 10. 视觉引导的机械臂控制

融合机器视觉与机器人技术：相机捕捉图像，视觉算法解析目标的位置、姿态与特征，进而引导机械臂完成抓取、装配等任务，应用于制造、物流与医疗场景。

<div class="archive__image">
  <img src='{{ '/resources/机械臂.jpg' | relative_url }}' alt="视觉引导机械臂" style="width:70%;height:auto;" />
</div>

---

研究方向是开放的，持续更新中。如果你对某个方向感兴趣，欢迎[联系我们]({{ '/join/' | relative_url }})。
