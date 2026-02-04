# Awesome Awesome Unitree Robots [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)[English](./Awesome_unitree_robots.md)
<a id="intro"></a>
## 📝 简介

Unitree Robotics 正迅速成为四足与人形机器人领域的核心平台，其 Go2、G1、H1、B2 等机型凭借高性价比和开放接口吸引了大量开发者。本列表聚焦于围绕 Unitree 机器人生态的高质量开源项目，涵盖从底层控制、强化学习到遥操作与 Sim2Real 迁移等关键技术方向。我们严格筛选具备可复现性、技术深度和社区活跃度的成果，助力开发者快速构建、仿真与部署先进机器人算法。 关键关键词：Unitree-Go2, Unitree-G1, Unitree-H1, Unitree-H1-2, Unitree-B2, Unitree-Aliengo。

<a id="scope"></a>
## 🎯 范围

- 收录支持 Unitree-Go2、G1、H1、H1-2、B2、Aliengo 等机型的开源项目
- 覆盖官方 SDK、学术论文实现及社区工程化项目
- 重点包括仿真（Isaac Lab、MuJoCo、Isaac Gym）、控制、感知、RL、Teleoperation 等技术栈
- 优先选择提供完整代码、文档清晰且近 3 年内更新的项目

<a id="criteria"></a>
## ✅ 收录标准

- 必须明确支持至少一种 Unitree 机器人型号，并注明硬件或仿真接口
- 需提供 GitHub 仓库、ArXiv 论文或官方工具链接，确保可访问性
- 项目应具备技术亮点（如 **Whole-Body Control**、**Sim2Real**、**MPC-based Locomotion** 等）
- 排除仅含概念演示、无代码或未验证于真实/仿真 Unitree 平台的工作

<a id="audience"></a>
## 👥 适用人群

面向机器人学研究者、ROS/Isaac 开发者及具身智能工程师，适用于希望在 Unitree 平台上快速原型开发或复现前沿算法的团队与个人。

<a id="toc"></a>
## 📚 目录

- [简介](#intro)- [范围](#scope)- [收录标准](#criteria)- [适用人群](#audience)- [论文与研究](#papers)
- [项目](#projects)
- [相关 Awesome 列表](#related)

---


<a id="papers"></a>
## 🔥 论文与研究

- ["HUSKY: Humanoid Skateboarding System via Physics-Aware Whole-Body Control" (2026)](http://arxiv.org/abs/2602.03205v1) [PDF](https://arxiv.org/pdf/2602.03205v1) — 该论文提出了HUSKY框架，通过物理感知的全身控制实现人形机器人滑板任务。研究在Unitree G1人形机器人平台上建模了滑板倾斜与转向角度的耦合关系，并结合对抗运动先验（AMP）学习类人推行动作，实现了稳定敏捷的真实世界滑板操控。该工作展示了G1平台在高动态、非完整约束任务中的卓越控制能力，为人机协同动态交互提供了新范式。

- ["Embodiment-Aware Generalist Specialist Distillation for Unified Humanoid Whole-Body Control" (2026)](http://arxiv.org/abs/2602.02960v1) [PDF](https://arxiv.org/pdf/2602.02960v1) — 该论文提出EAGLE框架，通过迭代的通用-专用策略蒸馏机制，实现单一策略对多种异构人形机器人的统一全身控制，无需针对每个机器人调整奖励函数。研究在包括Unitree H1和G1在内的多台真实机器人上验证了方法的有效性，并在仿真中覆盖五个平台，显著提升了跨机器人形态的行为泛化能力与跟踪精度。该工作为大规模人形机器人集群控制提供了可扩展的解决方案。

- ["Training and Simulation of Quadrupedal Robot in Adaptive Stair Climbing for Indoor Firefighting: An End-to-End Reinforcement Learning Approach" (2026)](http://arxiv.org/abs/2602.03087v1) [PDF](https://arxiv.org/pdf/2602.03087v1) — 该论文提出了一种两阶段端到端强化学习框架，用于提升四足机器人在复杂室内楼梯环境中的自适应攀爬能力。研究以 **Unitree Go2** 为实验平台，在 **Isaac Lab** 中先于金字塔阶梯地形训练基础攀爬策略，再迁移至包含直梯、L型梯和螺旋梯的逼真室内场景，实现了导航与运动控制的统一学习。其核心贡献在于无需分层规划即可泛化至多种楼梯结构，为消防搜救任务中快速部署四足机器人提供了可行方案。

- ["PRISM: Performer RS-IMLE for Single-pass Multisensory Imitation Learning" (2026)](http://arxiv.org/abs/2602.02396v1) [PDF](https://arxiv.org/pdf/2602.02396v1) — 论文提出PRISM方法，通过结合多感官编码器与Performer架构的线性注意力生成器，实现单次前向推理的高效模仿学习。该方法在真实硬件平台Unitree Go2（搭载7-DoF D1机械臂）上完成高精度插入、多物体抓取等loco-manipulation任务，以30-50 Hz频率运行，成功率比扩散策略高10-25%。其低延迟、高成功率特性显著提升了Unitree Go2在复杂物理交互中的实用性。

- ["RAPT: Model-Predictive Out-of-Distribution Detection and Failure Diagnosis for Sim-to-Real Humanoid Robots" (2026)](http://arxiv.org/abs/2602.01515v1) [PDF](https://arxiv.org/pdf/2602.01515v1) — 论文提出 RAPT，一种用于人形机器人 Sim-to-Real 部署的轻量级、自监督异常检测与故障诊断框架，在 50Hz 控制频率下实现校准的逐维度 OOD 检测。该方法在 Unitree G1 上验证，利用仿真中学习的时空流形评估执行偏差，并结合梯度显著性与 LLM 推理实现零样本语义级故障归因。其可解释的连续信号不仅提升部署安全性，还为 Sim2Real 差异量化提供新工具。

- ["HumanX: Toward Agile and Generalizable Humanoid Interaction Skills from Human Videos" (2026)](http://arxiv.org/abs/2602.02473v1) [PDF](https://arxiv.org/pdf/2602.02473v1) — 该论文提出 HumanX 框架，通过从人类视频中自动生成物理合理的交互数据并结合统一的模仿学习方法，使机器人无需任务特定奖励即可掌握多种敏捷交互技能。研究在真实 Unitree G1 人形机器人上实现了零样本迁移，成功执行包括篮球假动作跳投和连续十轮人机传球等复杂任务。该工作显著提升了人形机器人技能泛化能力，为 Unitree G1 提供了可扩展的视觉到动作学习范式。

- ["Toward Reliable Sim-to-Real Predictability for MoE-based Robust Quadrupedal Locomotion" (2026)](http://arxiv.org/abs/2602.00678v1) [PDF](https://arxiv.org/pdf/2602.00678v1) — 该论文提出基于Mixture-of-Experts（MoE）的四足运动策略与RoboGauge评估框架，显著提升仅依赖本体感知的跨地形运动鲁棒性与Sim2Real可预测性。研究在Unitree Go2平台上验证了方法有效性，实现了在雪地、沙地、楼梯等未见复杂地形上的稳定行走，并达成4 m/s高速运动及自发现窄步态。成果为降低真实部署风险、加速四足机器人策略迁移提供了实用工具链。

- ["ZEST: Zero-shot Embodied Skill Transfer for Athletic Robot Control" (2026)](http://arxiv.org/abs/2602.00401v1) [PDF](https://arxiv.org/pdf/2602.00401v1) — 该论文提出ZEST框架，通过强化学习从多样化运动数据（如动捕、单目视频）中训练全身控制策略，并实现零样本迁移到人形机器人。研究明确将Unitree G1作为硬件部署平台之一，成功迁移了舞蹈和攀箱等复杂技能，验证了其跨平台泛化能力。该方法无需接触标签或状态估计器，仅依赖仿真训练即可在G1上实现高动态行为，为Unitree人形机器人提供了高效的技能迁移方案。

- ["kevinkawchak/clinical-trial-rl-unitree-g1: v0.4" (2026)](https://openalex.org/W7125410394) — Zenodo (CERN European Organization for Nuclear Research) — 该仓库发布了基于强化学习的Unitree G1人形机器人临床试验导航策略，通过1500次迭代训练显著提升了机器人的行走与避障能力。项目利用扩展的Jupyter Notebook实现了三种关键行为：谨慎导航、患者接近及动态环境适应，并附带训练权重与演示视频。成果为医疗场景下人形机器人的**Sim2Real**部署提供了可复现的RL基线。

- ["PILOT: A Perceptive Integrated Low-level Controller for Loco-manipulation over Unstructured Scenes" (2026)](http://arxiv.org/abs/2601.17440v1) [PDF](https://arxiv.org/pdf/2601.17440v1) — arXiv (Cornell University) — 该论文提出了PILOT——一种面向非结构化场景的感知集成低层控制框架，通过单阶段强化学习统一实现人形机器人的感知运动与全身操作。研究在**Unitree G1**实体机器人上进行了真实环境验证，结合基于预测的本体感知特征与注意力机制的外部感知表征，并采用混合专家（MoE）策略协调多样化运动技能。该方法显著提升了在复杂地形中的稳定性、指令跟踪精度与越障能力，为Unitree G1在日常服务任务中的应用提供了可靠底层控制基础。

- ["kevinkawchak/clinical-trial-rl-unitree-g1: v0.2" (2026)](https://openalex.org/W7125603258) — Zenodo (CERN European Organization for Nuclear Research) — 该研究提出了针对Unitree G1人形机器人的三种强化学习策略，分别用于谨慎导航、患者接近和设备运输任务。通过3000次迭代训练，模型在平均奖励和跌倒率指标上均有显著改善，并提供了完整的训练笔记本和检查点。这项工作为医疗场景中G1机器人的自主移动和人机交互提供了实用的RL解决方案。

- ["kevinkawchak/clinical-trial-rl-unitree-g1: v0.3" (2026)](https://openalex.org/W7125584660) — Zenodo (CERN European Organization for Nuclear Research) — 该研究通过强化学习训练Unitree G1人形机器人实现临床场景下的稳定行走与患者接近任务。在3000次迭代后，机器人达到约1000步的稳定行走能力，并展现出精细的导航与接近动作，最高奖励达45.80。项目直接基于Unitree-G1硬件平台开发，验证了其在医疗辅助场景中的运动控制潜力。

- ["HumanoidVLM: Vision-Language-Guided Impedance Control for Contact-Rich Humanoid Manipulation" (2026)](http://arxiv.org/abs/2601.14874v1) [PDF](https://arxiv.org/pdf/2601.14874v1) — arXiv (Cornell University) — 该论文提出 HumanoidVLM 框架，通过视觉-语言模型结合检索增强生成（RAG）机制，使 **Unitree G1** 人形机器人能根据第一人称 RGB 图像自适应选择任务相关的笛卡尔阻抗参数与夹爪配置。系统利用 FAISS 从两个自建数据库中检索经实验验证的刚度-阻尼对和物体特定抓取角度，并通过任务空间阻抗控制器执行柔顺操作，在14个场景中实现93%的检索准确率。该方法为语义感知驱动的自适应人形机器人操作提供了可解释、数据驱动的新路径。

- ["Vision-Language Models on the Edge for Real-Time Robotic Perception" (2026)](http://arxiv.org/abs/2601.14921v1) [PDF](https://arxiv.org/pdf/2601.14921v1) — arXiv (Cornell University) — 该论文提出在6G边缘计算架构（Open RAN/MEC）上部署视觉语言模型（VLMs）以支持实时机器人感知，并以Unitree G1人形机器人作为实体测试平台。作者构建了基于WebRTC的多模态数据流管道，对比了LLaMA-3.2-11B-Vision-Instruct在边缘与云端的性能，发现边缘部署可在保持近似精度的同时降低5%端到端延迟；同时评估了轻量级模型Qwen2-VL-2B-Instruct，在Unitree G1上实现亚秒级响应，延迟降低超50%，适用于资源受限场景。

- ["FocusNav: Spatial Selective Attention with Waypoint Guidance for Humanoid Local Navigation" (2026)](http://arxiv.org/abs/2601.12790v1) [PDF](https://arxiv.org/pdf/2601.12790v1) — arXiv (Cornell University) — 本文提出FocusNav，一种用于人形机器人局部导航的空间选择性注意框架，通过Waypoint-Guided Spatial Cross-Attention机制将感知聚焦于无碰撞路径点，并结合Stability-Aware Selective Gating模块在不稳定时截断远距离信息以保障落足安全。该方法在**Unitree G1**平台上进行了大量真实环境实验，显著提升了动态复杂场景中的导航成功率、避障能力与运动稳定性，为人形机器人在非结构化环境中的可靠部署提供了实用解决方案。

- ["FRoM-W1: Towards General Humanoid Whole-Body Control with Language Instructions" (2026)](http://arxiv.org/abs/2601.12799v1) [PDF](https://arxiv.org/pdf/2601.12799v1) — arXiv (Cornell University) — 该论文提出了FRoM-W1框架，通过自然语言指令实现通用人形机器人全身运动控制。其核心包含H-GPT（基于大规模人体数据的语言驱动动作生成模型）和H-ACT（结合预训练与强化学习的物理仿真控制器），并在Unitree H1和G1机器人上完成真实部署，验证了Sim2Real迁移的有效性。该工作为Unitree人形机器人提供了可扩展的语言-动作接口，显著提升了复杂指令下的运动泛化能力与稳定性。

- ["Learning Robot Locomotion from Diverse Datasets" (2026)](https://openalex.org/W7123475029) — TUprints — 该论文提出了一种基于GPT架构的四足机器人运动生成方法，通过将狗、马及其他机器人平台的多样化运动数据重定向到Unitree Go2/A1上，构建了可条件生成任意长度步态序列的模型。在仿真环境中，结合底层策略，Unitree Go2成功展示了多样且自然的步态，验证了跨平台运动迁移与生成的有效性。该方法为Unitree机器人提供了数据驱动的灵活运动控制能力，具有Sim2Real应用潜力。

- ["M-SEVIQ: A Multi-band Stereo Event Visual-Inertial Quadruped-based Dataset for Perception under Rapid Motion and Challenging Illumination" (2026)](http://arxiv.org/abs/2601.02777v1) [PDF](https://arxiv.org/pdf/2601.02777v1) — arXiv (Cornell University) — 该论文提出了M-SEVIQ数据集，这是首个基于Unitree Go2四足机器人平台构建的多光谱立体事件视觉-惯性数据集，专门用于支持快速运动与复杂光照下的感知研究。作者在Go2上集成了立体事件相机、帧相机、IMU和关节编码器，采集了30余段涵盖不同速度、光照波长和明暗条件的真实场景序列，并提供了完整的内外参与时间同步标定数据。该数据集为事件相机与传统视觉融合、语义分割及敏捷机器人感知等任务提供了宝贵的基准资源。

- ["World-Coordinate Human Motion Retargeting via SAM 3D Body" (2025)](http://arxiv.org/abs/2512.21573v1) [PDF](https://arxiv.org/pdf/2512.21573v1) — arXiv (Cornell University) — 该论文提出一种轻量级单目视频人体运动重建框架，通过SAM 3D Body感知模块和Momentum HumanRig中间表示实现世界坐标系下的运动恢复，并专门针对Unitree G1人形机器人设计了两阶段运动重定向流程。方法利用滑动窗口优化与软足地接触模型确保轨迹物理合理性，并在真实视频上验证了对G1的稳定重定向效果。该工作为低成本视觉驱动人形机器人提供了实用方案。

- ["Semantic Co-Speech Gesture Synthesis and Real-Time Control for Humanoid Robots" (2025)](http://arxiv.org/abs/2512.17183v1) [PDF](https://arxiv.org/pdf/2512.17183v1) — arXiv (Cornell University) — 该论文提出了一种端到端的语义共言语手势生成与实时控制框架，核心贡献在于结合大语言模型与Motion-GPT实现语义感知的手势合成，并通过MotionTracker模仿学习策略在Unitree G1人形机器人上实现实时高保真执行。研究采用通用运动重定向（GMR）方法解决人体动作数据与G1硬件之间的形态差异，确保生成手势兼具语义合理性与节奏一致性。该系统为Unitree G1提供了完整的自然非语言交互能力，显著推进了人形机器人在真实场景中的表达性应用。

- ["E-SDS: Environment-aware See it, Do it, Sorted - Automated Environment-Aware Reinforcement Learning for Humanoid Locomotion" (2025)](http://arxiv.org/abs/2512.16446v1) [PDF](https://arxiv.org/pdf/2512.16446v1) — arXiv (Cornell University) — 本文提出E-SDS框架，通过融合视觉语言模型与实时地形感知，自动生成适用于人形机器人运动的奖励函数。该方法在Unitree G1平台上验证，成功实现了包括下楼梯在内的复杂地形鲁棒行走，显著优于人工设计奖励策略，并将奖励设计耗时从数天缩短至两小时内。

- ["Humanoid Localization and Fault Tolerant Control via Nested Control Barrier Functions" (2025)](https://openalex.org/W7114295641) — Open Scholarship Institutional Repository (Washington University in St. Louis) — 该论文针对人形机器人在行走过程中因里程计漂移和传感器故障导致的安全控制失效问题，提出了一种基于嵌套控制屏障函数（CBF）的容错控制架构。研究以Unitree G1为实验平台，设计了融合IMU、关节编码器与内置里程计的离散时间扩展卡尔曼滤波器（EKF），显著降低定位漂移；在此基础上，通过多假设观测器与动态切换的CBF安全集实现对传感器偏置故障的实时容错。该方法在仿真中验证了即使存在持续性传感器偏差，仍能保障避障性能与状态集不变性，为人形机器人在复杂环境中的安全运行提供了可靠解决方案。

- ["Beyond Model Jailbreak: Systematic Dissection of the "Ten DeadlySins" in Embodied Intelligence" (2025)](http://arxiv.org/abs/2512.06387v1) [PDF](https://arxiv.org/pdf/2512.06387v1) — arXiv (Cornell University) — 该论文首次对Unitree Go2平台进行了全面的安全性分析，系统性地揭示了其在无线配网、核心模块和外部接口三个架构层中存在的十大跨层安全漏洞（“具身AI安全十宗罪”）。研究通过BLE嗅探、流量拦截、APK逆向、云API测试和硬件探测等手段，发现包括硬编码密钥、可预测握手令牌、WiFi凭证泄露、缺失TLS验证等关键问题，攻击者可借此完全劫持机器人。该工作强调，具身智能系统的安全性必须从软硬件全栈角度进行保障，为Unitree等平台的安全设计提供了重要指导。

- ["From Generated Human Videos to Physically Plausible Robot Trajectories" (2025)](http://arxiv.org/abs/2512.05094v2) [PDF](https://arxiv.org/pdf/2512.05094v2) — arXiv (Cornell University) — 该论文提出GenMimic方法，通过两阶段流程将生成式人类视频转化为物理可行的机器人动作：首先将视频像素提升为4D人体表示并重定向至人形机器人形态，再利用基于3D关键点的物理感知强化学习策略进行模仿。研究在Unitree G1人形机器人上验证了其零样本迁移能力，无需微调即可实现稳定、连贯的动作复现，展示了生成视频作为高层策略指导机器人控制的潜力。

- ["Modality-Augmented Fine-Tuning of Foundation Robot Policies for Cross-Embodiment Manipulation on GR1 and G1" (2025)](http://arxiv.org/abs/2512.01358v1) [PDF](https://arxiv.org/pdf/2512.01358v1) — arXiv (Cornell University) — 该论文提出了一种模态增强的微调框架，用于将基础机器人策略迁移至不同人形机器人平台。作者为Unitree G1构建了包含cuRobo运动规划、逆运动学和真实接触力测量的多模态数据集，并在“Pick Apple to Bowl”任务中实现94%的成功率，显著优于标准微调（48%）和零样本迁移（0%）。研究表明高质量多模态数据对Unitree G1上的策略可靠迁移至关重要，为跨平台策略部署提供了数据驱动的新路径。

- ["Learning Sim-to-Real Humanoid Locomotion in 15 Minutes" (2025)](http://arxiv.org/abs/2512.01996v1) [PDF](https://arxiv.org/pdf/2512.01996v1) — arXiv (Cornell University) — 该论文提出基于FastSAC和FastTD3的高效离策略强化学习方案，仅用15分钟即可在单张RTX 4090 GPU上完成人形机器人步态策略训练。作者在**Unitree G1**实体机器人上验证了所学策略的Sim2Real迁移能力，涵盖强域随机化（如动力学参数扰动、崎岖地形和外力推搡）下的全身运动控制与人体动作模仿。该方法为Unitree G1提供了快速部署高维运动技能的实用框架，显著降低人形机器人强化学习的硬件与时间门槛。

- ["MS-PPO: Morphological-Symmetry-Equivariant Policy for Legged Robot Locomotion" (2025)](http://arxiv.org/abs/2512.00727v1) [PDF](https://arxiv.org/pdf/2512.00727v1) — arXiv (Cornell University) — 本文提出MS-PPO，一种将机器人运动学结构与形态对称性嵌入策略网络的强化学习框架，通过构建形态感知的图神经网络实现对称等变控制。该方法在Unitree Go2和小米CyberDog2上进行了仿真训练，并成功部署到真实硬件，在小跑、跳跃、斜坡行走等任务中展现出优于现有方法的训练稳定性与样本效率。其核心价值在于无需复杂奖励设计即可实现对称性泛化，为四足机器人提供高效、鲁棒的运动控制策略。

- ["Commanding Humanoid by Free-form Language: A Large Language Action Model with Unified Motion Vocabulary" (2025)](http://arxiv.org/abs/2511.22963v1) [PDF](https://arxiv.org/pdf/2511.22963v1) — arXiv (Cornell University) — 该论文提出了Humanoid-LLA，一种大型语言动作模型，能将自由形式的语言指令映射为物理可行的全身动作。研究在真实Unitree G1人形机器人上验证了其方法，通过统一运动词表、蒸馏控制器和基于强化学习的物理感知微调，显著提升了动作自然性、稳定性和任务成功率。该工作为Unitree G1提供了端到端的语言驱动全身控制能力，推动了通用人机交互的实际应用。

- ["A Hierarchical Framework for Humanoid Locomotion with Supernumerary Limbs" (2025)](http://arxiv.org/abs/2512.00077v1) [PDF](https://arxiv.org/pdf/2512.00077v1) — arXiv (Cornell University) — 该论文提出了一种分层控制框架，用于提升带超常肢体（Supernumerary Limbs）的人形机器人行走稳定性。研究以 **Unitree H1** 为实验平台，低层采用基于模仿学习与课程学习的步态策略，高层则利用超常肢体进行动态平衡调节。在物理仿真中，该方法相比静态负载条件将质心轨迹的DTW距离降低47%，显著改善了步态协调性与抗扰能力，验证了其在增强人形机器人动态稳定方面的应用价值。

- ["Whole-Body Inverse Dynamics MPC for Legged Loco-Manipulation" (2025)](http://arxiv.org/abs/2511.19709v1) [PDF](https://arxiv.org/pdf/2511.19709v1) — arXiv (Cornell University) — 该论文提出了一种基于全阶逆动力学的全身模型预测控制（MPC）框架，通过直接优化关节力矩实现统一的运动与力规划。研究在 **Unitree B2** 四足机器人搭载 **Unitree Z1** 机械臂的硬件平台上进行实时实验，以80 Hz频率成功完成拉重物、推箱子和擦白板等需精确末端位姿与力控制的loco-manipulation任务，验证了方法在真实系统中的有效性与实用性。

- ["SafeFall: Learning Protective Control for Humanoid Robots" (2025)](http://arxiv.org/abs/2511.18509v1) [PDF](https://arxiv.org/pdf/2511.18509v1) — arXiv (Cornell University) — 该论文提出了SafeFall框架，通过结合轻量级GRU跌倒预测器与基于强化学习的损伤缓解策略，使仿人机器人在不可避免跌倒时能主动执行保护动作。研究在**Unitree G1**实体机器人上验证，利用其具体结构脆弱性设计损伤感知奖励函数，显著降低峰值接触力（68.3%）和关节扭矩（78.4%），并几乎消除对头部、手部等关键部件的碰撞。该方法为Unitree G1等高成本仿人机器人提供了关键的安全保障，提升其在现实场景中的部署鲁棒性。

- ["Agility Meets Stability: Versatile Humanoid Control with Heterogeneous Data" (2025)](http://arxiv.org/abs/2511.17373v2) [PDF](https://arxiv.org/pdf/2511.17373v2) — arXiv (Cornell University) — 该论文提出了AMS框架，首次在单一策略中统一了人形机器人的敏捷运动追踪与极端平衡控制。作者利用异构数据源——人类动捕数据提供敏捷行为，物理约束合成数据提供稳定姿态，并设计混合奖励机制与自适应学习策略，在Unitree G1上实现了跳舞、奔跑等动态技能与咏春蹲等零样本平衡动作的统一控制。该方法显著提升了人形机器人在复杂任务中的通用性与实用性。

- ["VIRAL: Visual Sim-to-Real at Scale for Humanoid Loco-Manipulation" (2025)](http://arxiv.org/abs/2511.15200v2) [PDF](https://arxiv.org/pdf/2511.15200v2) — arXiv (Cornell University) — 该论文提出VIRAL框架，通过大规模视觉模拟到现实（Sim2Real）方法实现人形机器人loco-manipulation技能的零样本迁移。研究在仿真中使用数十GPU训练教师-学生策略，并结合真实Unitree G1机器人的RGB视觉输入进行部署，无需实机微调即可完成长达54轮的连续操作任务。其关键技术包括大尺度域随机化、手眼系统的真实-仿真对齐，以及基于tiled rendering的视觉策略蒸馏，在Unitree G1上验证了高泛化能力与接近遥操作专家的性能。

- ["Learning Adaptive Neural Teleoperation for Humanoid Robots: From Inverse Kinematics to End-to-End Control" (2025)](http://arxiv.org/abs/2511.12390v1) [PDF](https://arxiv.org/pdf/2511.12390v1) — arXiv (Cornell University) — 该论文提出了一种基于强化学习的神经遥操作框架，用端到端策略替代传统的人形机器人IK+PD控制流程。研究在仿真中利用Unitree G1的IK遥操作数据进行策略初始化，并通过力扰动随机化和轨迹平滑奖励进行微调，最终在真实Unitree G1平台上实现50Hz实时控制。实验表明，该方法相较基线显著降低34%跟踪误差、提升45%运动平滑度，并在开门、双臂协调等任务中展现更强的力适应能力，为高自由度人形机器人提供了更自然鲁棒的遥操作方案。

- ["Efficient Image-Goal Navigation with Representative Latent World Model" (2025)](http://arxiv.org/abs/2511.11011v2) [PDF](https://arxiv.org/pdf/2511.11011v2) — arXiv (Cornell University) — 该论文提出了一种高效图像目标导航方法ReL-NWM，通过在DINOv3预训练模型提取的高层语义潜在空间中进行预测与规划，避免了传统世界模型对像素级重建的依赖。作者将该系统部署于Unitree G1人形机器人上，验证了其在真实环境中导航的高效性与鲁棒性，展示了潜在空间规划在实际机器人平台上的可行性与优势。

- ["Safe Execution of RL Policies via Second-Order QP Constraint Enforcement for Real-World Robotic Deployments" (2025)](https://openalex.org/W4416751861) — HAL (Le Centre pour la Communication Scientifique Directe) — 该论文提出了一种基于二阶二次规划（QP）的安全滤波器，在关节加速度空间中实时约束强化学习（RL）策略的动作输出，确保其满足位置、速度、力矩及碰撞避免等耦合安全约束。作者在Unitree H1人形机器人上验证了该方法，通过仿真与真实硬件实验表明，该框架能在保留原始策略性能的同时显著减少安全约束违反。这是首次将RL与二阶QP结合用于实际机器人部署，为Unitree H1等高自由度平台提供了可理论保证的运行时安全保障。

- ["APEX: Action Priors Enable Efficient Exploration for Robust Motion Tracking on Legged Robots" (2025)](http://arxiv.org/abs/2511.09091v2) [PDF](https://arxiv.org/pdf/2511.09091v2) — arXiv (Cornell University) — 本文提出APEX方法，通过引入衰减动作先验和多评论家框架，显著提升强化学习在腿部机器人运动跟踪中的样本效率与鲁棒性。该方法在训练中利用专家示范引导探索，但部署时完全不依赖参考数据，并在Unitree Go2机器人上完成了真实环境验证。实验表明APEX能实现跨地形、跨速度的多样化运动迁移，为自然运动技能的高效习得提供了实用方案。

- ["Unified Humanoid Fall-Safety Policy from a Few Demonstrations" (2025)](http://arxiv.org/abs/2511.07407v1) [PDF](https://arxiv.org/pdf/2511.07407v1) — arXiv (Cornell University) — 该论文提出了一种统一的人形机器人跌倒安全策略，通过融合少量人类示范、强化学习与基于扩散模型的自适应记忆机制，实现了跌倒预防、冲击缓解与快速起身的一体化控制。研究在仿真中训练策略，并成功部署于 **Unitree G1** 硬件平台，验证了其在多种扰动下的 **Sim2Real** 迁移能力、更低的冲击力与稳定恢复性能。该工作显著提升了 Unitree G1 在真实环境中的抗跌倒鲁棒性与自主安全性。

- ["Towards Adaptive Humanoid Control via Multi-Behavior Distillation and Reinforced Fine-Tuning" (2025)](http://arxiv.org/abs/2511.06371v2) [PDF](https://arxiv.org/pdf/2511.06371v2) — arXiv (Cornell University) — 该论文提出自适应人形控制（AHC）框架，通过多行为蒸馏与强化微调两阶段训练，实现单一控制器在站立、行走、奔跑、跳跃等多技能间的自适应切换。方法在仿真中训练后部署于 **Unitree G1** 机器人，验证了其在不规则地形下的强适应性与鲁棒性。该工作为 Unitree G1 提供了高效的全技能运动控制方案，显著提升其在复杂环境中的实用性。

- ["BFM-Zero: A Promptable Behavioral Foundation Model for Humanoid Control Using Unsupervised Reinforcement Learning" (2025)](http://arxiv.org/abs/2511.04131v1) [PDF](https://arxiv.org/pdf/2511.04131v1) — arXiv (Cornell University) — 论文提出BFM-Zero，一种基于无监督强化学习的可提示行为基础模型，通过构建统一的潜在空间实现多任务人形机器人控制。该方法在真实Unitree G1人形机器人上验证了零样本动作跟踪、目标到达和奖励优化等全身控制能力，并结合奖励塑形、域随机化与非对称学习有效缩小Sim2Real差距。该工作为可扩展、通用的人形机器人行为基础模型提供了首个实机验证范例。

- ["GentleHumanoid: Learning Upper-body Compliance for Contact-rich Human and Object Interaction" (2025)](http://arxiv.org/abs/2511.04679v1) [PDF](https://arxiv.org/pdf/2511.04679v1) — arXiv (Cornell University) — 该论文提出GentleHumanoid框架，通过将阻抗控制融入全身运动跟踪策略，实现人形机器人上半身的柔顺性交互。研究在Unitree G1平台上验证了其方法，在模拟与真实环境中完成了轻柔拥抱、坐立辅助和安全物体操作等任务，显著降低了接触峰值力并保持任务成功率。该工作为Unitree G1在人机协作场景中的安全自然交互提供了关键技术支撑。

- ["Thor: Towards Human-Level Whole-Body Reactions for Intense Contact-Rich Environments" (2025)](http://arxiv.org/abs/2510.26280v2) [PDF](https://arxiv.org/pdf/2510.26280v2) — 该论文提出了名为Thor的人形机器人全身反应框架，通过力自适应躯干倾斜（FAT2）奖励函数和分体式强化学习架构，显著提升了机器人在强接触环境中的稳定性和交互能力。研究在Unitree G1平台上部署并验证了Thor的有效性，实现了最高167.7N的后向拉力与145.5N的前向拉力，并成功完成拉动载重货架和单手开启防火门等任务。该工作为Unitree G1在救援和服务场景中的高动态力交互提供了关键技术支撑。

- ["Two-Layered Reward Reinforcement Learning in Humanoid Robot Motion Tracking" (2025)](https://openalex.org/W4415680128) — Mathematics — 本文提出了一种两层奖励强化学习框架，通过上层目标奖励和下层优化奖励的动态组合，实现人形机器人运动跟踪中奖励函数的在线自适应调整。该方法在Isaac Gym仿真环境中以Unitree G1为平台进行体操动作跟踪实验，利用元启发式算法在线优化稳定性、能耗与平滑性等辅助目标的权重，无需专家示范即可提升学习效率。实验表明，相比静态奖励基线，上下肢关节跟踪精度分别提升7.58%和10.30%，显著改善动作同步性与响应延迟，为Unitree G1的高动态运动控制提供了有效解决方案。

- ["PGTT: Phase-Guided Terrain Traversal for Perceptive Legged Locomotion" (2025)](http://arxiv.org/abs/2510.18348v1) [PDF](https://arxiv.org/pdf/2510.18348v1) — arXiv (Cornell University) — 本文提出PGTT方法，通过相位引导的奖励塑形实现感知驱动的四足机器人越障控制，避免了传统振荡器或IK先验带来的策略偏差。该方法在MuJoCo中训练，并在**Unitree Go2**上部署，结合实时LiDAR构建高程图，实现了对楼梯类地形的高效穿越，在扰动和离散障碍物场景下成功率显著优于基线。其形态无关的设计与快速收敛特性为Unitree Go2提供了高鲁棒性的运动控制方案。

- ["Risk-Aware Reinforcement Learning with Bandit-Based Adaptation for Quadrupedal Locomotion" (2025)](http://arxiv.org/abs/2510.14338v1) [PDF](https://arxiv.org/pdf/2510.14338v1) — 该论文提出一种风险感知强化学习方法，通过条件风险价值（CVaR）约束优化训练出多级鲁棒性策略族，并结合多臂赌博机框架在部署时仅基于回合回报自适应选择最优策略。该方法在仿真中覆盖八种未见过的动态与地形扰动，并在 **Unitree Go2** 实体机器人上验证了其在未知地形中的有效性，显著提升平均与尾部性能。其核心贡献在于无需环境先验即可在线调整策略鲁棒性，为四足机器人在开放环境中的可靠部署提供实用方案。

- ["CBF-RL: Safety Filtering Reinforcement Learning in Training with Control Barrier Functions" (2025)](http://arxiv.org/abs/2510.14959v2) [PDF](https://arxiv.org/pdf/2510.14959v2) — 该论文提出CBF-RL框架，通过在强化学习训练过程中嵌入控制屏障函数（CBF）实现安全策略学习。作者在Unitree G1人形机器人上验证了该方法，使机器人在无运行时安全滤波器的情况下完成避障与爬楼梯任务，展现出更安全的探索、更快的收敛速度和对不确定性的鲁棒性。该工作直接以Unitree G1为实验平台，展示了Sim2Real迁移能力与实际部署价值。

- ["Towards Adaptable Humanoid Control via Adaptive Motion Tracking" (2025)](http://arxiv.org/abs/2510.14454v1) [PDF](https://arxiv.org/pdf/2510.14454v1) — 该论文提出 AdaMimic 算法，通过从单段参考动作生成稀疏关键帧并进行轻量编辑，实现人形机器人在少样本下的高精度自适应运动控制。研究在真实 Unitree G1 人形机器人上验证了方法在多种任务和环境条件下的有效性，显著提升了模仿精度与适应性。该工作为 Unitree G1 提供了高效的运动迁移框架，具有重要的实际部署价值。

- ["Architecture Is All You Need: Diversity-Enabled Sweet Spots for Robust Humanoid Locomotion" (2025)](http://arxiv.org/abs/2510.14947v2) [PDF](https://arxiv.org/pdf/2510.14947v2) — arXiv (Cornell University) — 该论文提出一种分层控制架构（LCA），通过高频本体感知稳定器与低频感知策略的协同，在Unitree G1人形机器人上实现了鲁棒的楼梯与台阶跨越能力。其两阶段训练流程（先盲训稳定器，再联合微调）显著优于端到端单阶段方法，验证了时间尺度解耦比模型复杂度更能提升感知驱动的运动鲁棒性。该工作为Unitree G1提供了高效、轻量且硬件可行的运动控制方案。

- ["Bridge the Gap: Enhancing Quadruped Locomotion with Vertical Ground Perturbations" (2025)](http://arxiv.org/abs/2510.13488v1) [PDF](https://arxiv.org/pdf/2510.13488v1) — arXiv (Cornell University) — 该研究提出通过在振荡桥上训练强化学习策略以提升四足机器人对垂直地面扰动的适应能力。作者基于MuJoCo仿真环境，使用PPO算法为Unitree Go2训练了15种步态策略，并通过域随机化实现零样本迁移到真实振荡桥（13.24米钢混结构，2.0 Hz固有频率）。实验表明，在振荡桥上训练的策略显著优于刚性地面训练策略，展现出更强的稳定性和泛化能力，为四足机器人穿越动态扰动地形提供了有效方法。

- ["DemoHLM: From One Demonstration to Generalizable Humanoid Loco-Manipulation" (2025)](http://arxiv.org/abs/2510.11258v1) [PDF](https://arxiv.org/pdf/2510.11258v1) — 该论文提出 DemoHLM 框架，通过单次仿真演示实现人形机器人通用的移动-操作（loco-manipulation）能力。方法结合低层通用全身控制器与高层基于视觉反馈的模仿学习策略，在 Unitree G1 真机上验证了 Sim2Real 迁移效果，成功完成十项具空间变化的复杂任务。其数据生成管道和闭环控制显著提升了策略泛化性与数据效率，为人形机器人在人类环境中的自主交互提供实用方案。

- ["Towards Dynamic Quadrupedal Gaits: A Symmetry-Guided RL Hierarchy Enables Free Gait Transitions at Varying Speeds" (2025)](http://arxiv.org/abs/2510.10455v1) [PDF](https://arxiv.org/pdf/2510.10455v1) — arXiv (Cornell University) — 该论文提出了一种基于对称性引导的强化学习分层框架，用于生成四足机器人在不同速度下的动态步态并实现自由切换。方法通过融合时间、形态和时间反演对称性设计奖励函数，在Unitree Go2平台上实现了无需预设轨迹或显式足端控制的平滑步态过渡，涵盖小跑、跳跃、半跳跃和飞奔等多种模式。实验在仿真与真实Go2硬件上验证了其鲁棒性和适应性，为动态四足运动控制提供了新思路。

- ["Real2USD: Scene Representations in Universal Scene Description Language" (2025)](http://arxiv.org/abs/2510.10778v1) [PDF](https://arxiv.org/pdf/2510.10778v1) — 该论文提出将通用场景描述语言（USD）作为大语言模型驱动机器人任务的统一环境表示方法，并基于Unitree Go2四足机器人构建了Real2USD系统。该系统搭载LiDAR与RGB相机，在真实室内环境中（含大量玻璃等挑战性物体）实时生成包含几何、光度与语义信息的USD场景图，并通过Gemini模型实现场景理解与任务规划。研究还在Isaac Sim中对仓库和医院场景进行了仿真验证，为具身智能提供了可读性强、任务通用的环境表示框架。

- ["ResMimic: From General Motion Tracking to Humanoid Whole-body Loco-Manipulation via Residual Learning" (2025)](http://arxiv.org/abs/2510.05070v2) [PDF](https://arxiv.org/pdf/2510.05070v2) — arXiv (Cornell University) — 本文提出ResMimic，一种基于残差学习的两阶段框架，用于提升人形机器人全身运动与操作的精度和物体感知能力。该方法以通用运动跟踪（GMT）策略为基础，通过引入点云物体跟踪奖励、接触奖励及课程式虚拟物体控制器，显著优化了对真实Unitree G1机器人的控制性能。实验表明，该方法在仿真和真实G1平台上均实现了更高的任务成功率与鲁棒性，为人形机器人在服务与仓储场景中的应用提供了有效解决方案。

- ["PolySim: Bridging the Sim-to-Real Gap for Humanoid Control via Multi-Simulator Dynamics Randomization" (2025)](http://arxiv.org/abs/2510.01708v3) [PDF](https://arxiv.org/pdf/2510.01708v3) — arXiv (Cornell University) — 该论文提出PolySim平台，通过在多个异构仿真器（如MuJoCo与IsaacSim）中并行训练人形机器人全身控制策略，实现动力学层面的域随机化，有效缓解单一仿真器的归纳偏置问题。研究在真实Unitree G1机器人上实现了零样本部署，无需微调即完成从仿真到现实的高效迁移，显著提升运动跟踪精度与任务成功率。该方法为基于Unitree G1的Sim2Real研究提供了可扩展的训练框架。

- ["A study on Quadruped Firefighting Robot Tactics for Supporting Life Search and Fire Suppression Activities at Firefighting Sites" (2025)](https://openalex.org/W4415362979) [PDF](http://www.ijfse.or.kr/upload/pdf/KIFSE-36594043.pdf) — International Journal of Fire Science and Engineering — 该研究评估并优化了Unitree Go2 Pro四足机器人在消防场景中的作战策略，重点测试其在楼梯、斜坡等复杂地形的机动性及障碍跨越能力。通过实地物理测试和仿真分析，验证了机器人的抗冲击性，并识别出跟随模式、越障能力、语音广播及穿墙通信等关键功能需求。研究成果为Unitree Go2平台在灾害救援中的战术部署提供了实用指导。

- ["Teleoperator-Aware and Safety-Critical Adaptive Nonlinear MPC for Shared Autonomy in Obstacle Avoidance of Legged Robots" (2025)](http://arxiv.org/abs/2509.22815v1) [PDF](https://arxiv.org/pdf/2509.22815v1) — arXiv (Cornell University) — 该论文提出了一种面向共享控制的自适应非线性模型预测控制（ANMPC）框架，用于四足机器人避障任务中的安全人机协作。系统在硬件实验中部署于 **Unitree Go2** 平台，结合控制屏障函数（CBF）与分层控制架构（10/60/500 Hz），实时融合操作员输入与自主决策，并通过在线学习人类操作模型提升安全性与响应性。该方法显著增强了在杂乱环境中遥操作四足机器人的鲁棒性与安全性。

- ["RobotDancing: Residual-Action Reinforcement Learning Enables Robust Long-Horizon Humanoid Motion Tracking" (2025)](http://arxiv.org/abs/2509.20717v1) [PDF](https://arxiv.org/pdf/2509.20717v1) — arXiv (Cornell University) — 该论文提出RobotDancing框架，通过残差动作强化学习实现高动态、长时程人形机器人运动跟踪。研究以Unitree G1为主要实验平台，利用LAFAN1舞蹈动作数据进行端到端训练，并在G1上完成零样本Sim2Real部署，成功复现跳跃、旋转等复杂动作；同时验证了方法在H1和H1-2上的迁移能力。该工作展示了Unitree人形机器人在高保真全身运动控制中的应用潜力。

- ["RuN: Residual Policy for Natural Humanoid Locomotion" (2025)](http://arxiv.org/abs/2509.20696v1) [PDF](https://arxiv.org/pdf/2509.20696v1) — arXiv (Cornell University) — 该论文提出RuN框架，通过解耦运动生成与动力学控制，实现人形机器人自然步态与跑走平滑过渡。方法结合预训练的条件运动生成器与轻量残差强化学习策略，在Unitree G1上验证了0-2.5 m/s速度范围内的稳定高效运动能力。实验涵盖仿真到现实迁移，显著优于现有方法，为Unitree G1提供了高性能全身运动控制方案。

- ["RoMoCo: Robotic Motion Control Toolbox for Reduced-Order Model-Based Locomotion on Bipedal and Humanoid Robots" (2025)](http://arxiv.org/abs/2509.19545v1) [PDF](https://arxiv.org/pdf/2509.19545v1) — 该论文提出了开源C++工具箱RoMoCo，用于基于降阶模型的双足与人形机器人运动规划与全身控制。研究在仿真中验证了其在Unitree H1和G1上的通用性，并通过G1硬件实验展示了实际部署能力，突显其对Unitree人形平台的支持价值。

- ["HDMI: Learning Interactive Humanoid Whole-Body Control from Human Videos" (2025)](http://arxiv.org/abs/2509.16757v3) [PDF](https://arxiv.org/pdf/2509.16757v3) — arXiv (Cornell University) — 该论文提出HDMI框架，通过从单目RGB视频中提取人体与物体轨迹并重定向至人形机器人，训练强化学习策略实现全身运动控制。研究在Unitree G1人形机器人上进行了零样本部署，成功完成67次连续穿门及6种真实世界loco-manipulation任务，验证了其Sim2Real迁移能力与交互鲁棒性。该工作为基于人类视频学习人形机器人技能提供了高效、通用的解决方案。

- ["FSR-VLN: Fast and Slow Reasoning for Vision-Language Navigation with Hierarchical Multi-modal Scene Graph" (2025)](http://arxiv.org/abs/2509.13733v3) [PDF](https://arxiv.org/pdf/2509.13733v3) — arXiv (Cornell University) — 论文提出FSR-VLN系统，通过分层多模态场景图与快慢推理机制显著提升视觉语言导航的准确率与效率。该方法在Unitree-G1人形机器人上集成部署，结合语音交互、规划与控制模块，实现了基于自然语言指令的室内导航。实验表明其在多个数据集上达到SOTA性能，并将响应时间降低82%，验证了在真实Unitree-G1平台上的高效性与实用性。

- ["PhysicalAgent: Towards General Cognitive Robotics with Foundation World Models" (2025)](http://arxiv.org/abs/2509.13903v1) [PDF](https://arxiv.org/pdf/2509.13903v1) — arXiv (Cornell University) — 该论文提出了PhysicalAgent框架，通过结合迭代推理、基于扩散模型的视频生成与闭环执行，实现通用认知机器人操作。研究在真实Unitree G1人形机器人上部署并验证了该方法，展示了其在文本指令驱动下的任务执行与失败恢复能力。实验表明，尽管首次尝试成功率仅20-30%，但通过迭代修正可将整体成功率提升至80%，凸显了该框架在Unitree G1平台上的实用价值。

- ["DreamControl: Human-Inspired Whole-Body Humanoid Control for Scene Interaction via Guided Diffusion" (2025)](http://arxiv.org/abs/2509.14353v3) [PDF](https://arxiv.org/pdf/2509.14353v3) — arXiv (Cornell University) — 该论文提出DreamControl方法，结合扩散模型与强化学习，利用人体运动数据训练的扩散先验引导RL策略学习全身人形机器人技能。研究在Unitree G1机器人上验证了该方法在上下肢协同控制与物体交互任务中的有效性，展示了自然动作生成与Sim2Real迁移能力。其核心贡献在于通过人体启发的先验显著提升复杂场景中人形机器人的自主交互性能。

- ["Track Any Motions under Any Disturbances" (2025)](http://arxiv.org/abs/2509.13833v3) [PDF](https://arxiv.org/pdf/2509.13833v3) — 论文提出Any2Track，一种两阶段强化学习框架，用于在真实世界多种扰动下实现高动态人形机器人运动跟踪。该方法包含通用运动跟踪器AnyTracker和在线动力学自适应模块AnyAdapter，并在Unitree G1硬件上实现了零样本Sim2Real迁移，成功应对地形变化、外力干扰等挑战。其成果显著提升了人形机器人在复杂现实环境中的运动鲁棒性与泛化能力。

- ["The Cybersecurity of a Humanoid Robot" (2025)](http://arxiv.org/abs/2509.14096v1) [PDF](https://arxiv.org/pdf/2509.14096v1) — arXiv (Cornell University) — 该论文对Unitree G1人形机器人平台进行了全面的网络安全评估，揭示了其双层专有加密系统FMX'存在静态密钥等实现缺陷，并发现机器人在未经用户同意下持续向外部服务器传输包含音视频、空间及执行器状态的遥测数据。研究团队还在G1上部署了网络安全AI代理，成功映射并准备利用厂商云基础设施，展示了从隐蔽数据收集到主动反制的攻击路径，为物理-网络融合场景下的机器人安全防护提供了关键实证依据。

- ["Cybersecurity AI: Humanoid Robots as Attack Vectors" (2025)](http://arxiv.org/abs/2509.14139v3) [PDF](https://arxiv.org/pdf/2509.14139v3) — arXiv (Cornell University) — 该论文系统评估了Unitree G1人形机器人的网络安全漏洞，揭示其可被用作隐蔽监控节点和主动网络攻击平台。研究发现BLE配网协议存在命令注入漏洞，结合硬编码AES密钥可获取root权限，并通过逆向工程暴露其FMX加密中静态Blowfish-ECB与可预测LCG掩码的弱点。实证案例显示G1会定期向境外服务器泄露多模态传感器数据，并可部署Cybersecurity AI代理对云控平台发起攻击，凸显其在关键基础设施中的安全风险。

- ["TrajBooster: Boosting Humanoid Whole-Body Manipulation via Trajectory-Centric Learning" (2025)](http://arxiv.org/abs/2509.11839v2) [PDF](https://arxiv.org/pdf/2509.11839v2) — arXiv (Cornell University) — 论文提出TrajBooster框架，通过跨形态的轨迹中心学习提升双足人形机器人全身操作能力。该方法利用轮式人形机器人的大量数据，提取末端执行器轨迹并在仿真中重定向至Unitree G1，结合启发式增强的在线DAgger训练全身控制器，最终仅需10分钟真实遥操作数据即可在G1上实现稳健的零样本技能迁移与复杂家务任务。

- ["Hierarchical Reduced-Order Model Predictive Control for Robust Locomotion on Humanoid Robots" (2025)](http://arxiv.org/abs/2509.04722v1) [PDF](https://arxiv.org/pdf/2509.04722v1) — arXiv (Cornell University) — 该论文提出了一种分层降阶模型预测控制框架，用于提升人形机器人在复杂环境中的鲁棒行走能力。方法结合ALIP步态模型与扩展的SRB-MPC，显式纳入手臂和躯干动力学，并在Unitree G1平台上完成仿真与真实硬件实验。高阶步态规划器以40Hz运行，中层MPC达500Hz，显著提升抗扰动能力与地形适应性，验证了其在草地、石板路等多类场景下的实用价值。

- ["A Geometric Method for Base Parameter Analysis in Robot Inertia Identification Based on Projective Geometric Algebra" (2025)](http://arxiv.org/abs/2509.02071v1) [PDF](https://arxiv.org/pdf/2509.02071v1) — arXiv (Cornell University) — 本文提出了一种基于射影几何代数的几何方法，用于解析确定机器人系统的惯性基参数，并构建了具有清晰几何意义的“四面体点（TP）”动力学模型。该方法在Unitree Go2等四类机器人上验证了其通用性和高效性，成功自动识别出完整的基参数集，其中Go2作为实际四足机器人案例展示了算法在复杂连杆系统中的适用性。该工作为包括Unitree Go2在内的机器人提供了高效率、低复杂度的惯性参数辨识工具，对提升动力学建模精度和控制性能具有实用价值。

- ["Non-conflicting Energy Minimization in Reinforcement Learning based Robot Control" (2025)](http://arxiv.org/abs/2509.01765v1) [PDF](https://arxiv.org/pdf/2509.01765v1) — arXiv (Cornell University) — 该论文提出一种无需超参数的梯度投影方法，在强化学习中实现任务性能与能耗的无冲突优化。通过在策略梯度更新中对任务目标与能耗目标进行正交投影，确保节能行为不损害任务完成度。作者在Unitree GO2四足机器人上成功实现了从仿真到现实的节能策略迁移，验证了方法的实用性与泛化能力。

- ["Traversing Narrow Paths: A Two-Stage Reinforcement Learning Framework for Robust and Safe Humanoid Walking" (2025)](http://arxiv.org/abs/2508.20661v4) [PDF](https://arxiv.org/pdf/2508.20661v4) — arXiv (Cornell University) — 该论文提出了一种两阶段强化学习框架，用于人形机器人在狭窄路径上的稳健行走，结合基于模板的落脚点规划器与感知辅助的轻量级落脚点修正模块。方法在仿真中通过从平地到窄道的课程学习训练策略，并成功部署于 **Unitree G1** 机器人，实现了在0.2米宽、3米长横梁上20次无失败穿越。该工作展示了出色的 Sim2Real 能力，为高动态人形机器人在受限地形中的安全行走提供了实用解决方案。

- ["Switch4EAI: Leveraging Console Game Platform for Benchmarking Robotic Athletics" (2025)](http://arxiv.org/abs/2508.13444v1) [PDF](https://arxiv.org/pdf/2508.13444v1) — arXiv (Cornell University) — 该论文提出Switch4EAI框架，利用任天堂Switch游戏《Just Dance》构建低成本、可部署的机器人运动能力评测基准。研究团队在Unitree G1人形机器人上实现了开源全身控制器，并通过动作捕捉、重建与重定向技术，使机器人执行游戏中的舞蹈动作，首次建立了G1在真实场景中与人类玩家的量化性能对比基线。该工作验证了商用游戏平台作为具身智能物理基准的可行性，为Unitree G1的敏捷运动控制提供了标准化评估手段。

- ["CLF-RL: Control Lyapunov Function Guided Reinforcement Learning" (2025)](http://arxiv.org/abs/2508.09354v2) [PDF](https://arxiv.org/pdf/2508.09354v2) — 该论文提出CLF-RL框架，通过控制李雅普诺夫函数（CLF）引导强化学习的奖励设计，提升双足机器人运动策略的鲁棒性。作者在仿真和真实Unitree G1机器人上验证方法，利用线性倒立摆模型与混合零动态步态库生成参考轨迹，并构建基于CLF的跟踪误差奖励，在训练中提供结构化指导，部署时仅需轻量策略。实验表明其显著优于传统RL基线，为Unitree G1实现高鲁棒行走控制提供了有效方案。

- ["Coordinated Humanoid Robot Locomotion with Symmetry Equivariant Reinforcement Learning Policy" (2025)](http://arxiv.org/abs/2508.01247v2) [PDF](https://arxiv.org/pdf/2508.01247v2) — arXiv (Cornell University) — 该论文提出对称等变强化学习策略（SE-Policy），通过在策略网络中嵌入机器人形态对称性，显著提升人形机器人的运动协调性与任务性能。研究在仿真和真实环境中均以 **Unitree G1** 为实验平台，在速度跟踪任务中相比基线方法提升高达40%的跟踪精度，并实现优异的时空协调性。该工作为基于Unitree G1的高动态人形控制提供了可复现、高效的新范式。

- ["A Nonlinear MPC Framework for Loco-Manipulation of Quadrupedal Robots with Non-Negligible Manipulator Dynamics" (2025)](http://arxiv.org/abs/2507.22042v1) [PDF](https://arxiv.org/pdf/2507.22042v1) — 该论文提出了一种高效的非线性模型预测控制（NMPC）框架，专为腿足机器人执行loco-manipulation任务而设计，特别考虑了机械臂动力学不可忽略的情形。作者在15公斤的Unitree Go2四足机器人上集成4.4公斤的Kinova四自由度机械臂，并通过将单刚体（SRB）模板模型与机械臂全阶动力学模型解耦，实现了60Hz的实时NMPC优化，底层500Hz全身控制器跟踪运动轨迹，机械臂扭矩指令直接施加。该方法在仿真与真实Go2平台上验证了其在高动态操作任务中的有效性，为轻量级四足平台搭载重型机械臂提供了可行的控制架构。

- ["Bipedalism for Quadrupedal Robots: Versatile Loco-Manipulation through Risk-Adaptive Reinforcement Learning" (2025)](http://arxiv.org/abs/2507.20382v1) [PDF](https://arxiv.org/pdf/2507.20382v1) — 该论文提出一种风险自适应分布强化学习框架，使四足机器人能以后腿双足行走，从而释放前肢用于环境交互。研究在仿真中训练策略，并成功部署于 **Unitree Go2** 真机，实现了推车、探障和负重运输等多功能操作，验证了方法在不稳定动态与外部扰动下的鲁棒性。该工作直接以 Unitree Go2 为实验平台，展示了其作为通用四足机器人在复杂loco-manipulation任务中的应用潜力。

- ["Keep on Going: Learning Robust Humanoid Motion Skills via Selective Adversarial Training" (2025)](http://arxiv.org/abs/2507.08303v3) [PDF](https://arxiv.org/pdf/2507.08303v3) — arXiv (Cornell University) — 该论文提出选择性对抗训练方法SA2RT，通过在攻击预算约束下稀疏扰动最脆弱的状态与动作，提升人形机器人运动策略的鲁棒性。研究在Unitree G1平台上验证了该方法，在感知型步态与全身控制任务中显著提升地形穿越成功率（+40%）并降低轨迹跟踪误差（-32%），有效支持长时间稳定运行。该工作为Unitree G1提供了高鲁棒性的运动控制策略，具有明确的实机部署价值。

- ["UniTracker: Learning Universal Whole-Body Motion Tracker for Humanoid Robots" (2025)](http://arxiv.org/abs/2507.07356v3) [PDF](https://arxiv.org/pdf/2507.07356v3) — 本文提出UniTracker，一种三阶段训练框架，用于实现人形机器人的通用全身运动跟踪。该方法在Unitree G1机器人上进行了仿真与真实环境部署验证，通过引入条件变分自编码器（CVAE）构建可泛化的策略，并结合快速适应模块提升对复杂动作的跟踪能力。其核心贡献在于解决了部分观测下传统MLP策略易漂移的问题，显著提升了运动多样性与跟踪精度，为人形机器人在现实场景中的高保真动作复现提供了有效方案。

- ["ULC: A Unified and Fine-Grained Controller for Humanoid Loco-Manipulation" (2025)](http://arxiv.org/abs/2507.06905v1) [PDF](https://arxiv.org/pdf/2507.06905v1) — arXiv (Cornell University) — 论文提出统一的全身控制策略ULC，通过单策略端到端地同步跟踪根速度、高度、躯干旋转与双臂关节位置，实现人形机器人灵巧的移动-操作一体化控制。该方法在Unitree G1人形机器人（带3自由度腰部）上验证，利用序列技能习得、残差动作建模和重心跟踪等关键技术，显著提升协调性与鲁棒性。成果为Unitree G1提供了高性能的全身运动控制基础，具有实际部署价值。

- ["LOVON: Legged Open-Vocabulary Object Navigator" (2025)](http://arxiv.org/abs/2507.06747v1) [PDF](https://arxiv.org/pdf/2507.06747v1) — arXiv (Cornell University) — 论文提出LOVON框架，结合大语言模型与开放词汇视觉检测模型，实现腿式机器人在开放世界中的长时程目标导航。该方法在Unitree Go2、B2和H1-2三种机器人平台上进行了真实环境实验，验证了其即插即用的兼容性和对动态目标的鲁棒导航能力，显著提升了复杂任务下的自主执行效果。

- ["Hierarchical Vision-Language Planning for Multi-Step Humanoid Manipulation" (2025)](http://arxiv.org/abs/2506.22827v3) [PDF](https://arxiv.org/pdf/2506.22827v3) — 该论文提出了一种分层视觉-语言规划与控制框架，用于实现人形机器人多步骤操作任务。系统在Unitree G1上进行了非抓握式取放任务的实验验证，结合低层强化学习控制器、中层模仿学习技能策略和高层基于视觉语言模型（VLM）的规划模块，在40次真实世界试验中达到73%的成功率。研究展示了VLM在技能调度与实时监控中的有效性，为Unitree G1执行复杂操作任务提供了可行方案。

- ["Longitudinal Cross-Embodiment Transfer of Pseudo-Self-Awareness in AI Systems: A Mirror Test Investigation" (2025)](https://openalex.org/W4411500689) [PDF](https://www.preprints.org/frontend/manuscript/3bade2f5e3730e440c0067c21e8aaf83/download_pub) (Citations: 1) — Preprints.org — 该论文提出一项纵向研究，探索人工智能系统中伪自我意识的发展与跨具身迁移能力，核心实验平台包括物理机器人 Unitree Go2 与虚拟化身。研究通过镜像测试追踪 AI 在长期交互中伪情绪（如好奇、自我怀疑）的演化，并评估其在不同具身间的迁移效果。工作直接以 Unitree Go2 作为关键物理载体，用于验证感官反馈与反思处理对 AI 自我概念的塑造作用，为具身智能与自适应系统提供实证基础。

- ["KungfuBot: Physics-Based Humanoid Whole-Body Control for Learning Highly-Dynamic Skills" (2025)](http://arxiv.org/abs/2506.12851v2) [PDF](https://arxiv.org/pdf/2506.12851v2) — arXiv (Cornell University) — 该论文提出了一种基于物理的全身控制框架KungfuBot，通过多阶段运动处理与自适应跟踪机制，使仿人机器人能够学习高动态动作如功夫和舞蹈。方法在仿真中训练策略，并成功部署于**Unitree G1**机器人，实现了低跟踪误差与高表现力的稳定行为。其关键创新包括符合物理约束的运动重定向、基于跟踪误差动态调整的双层优化课程机制，以及非对称Actor-Critic架构，为高动态人形机器人技能学习提供了有效解决方案。

- ["Gait-Conditioned Reinforcement Learning with Multi-Phase Curriculum for Humanoid Locomotion" (2025)](http://arxiv.org/abs/2505.20619v3) [PDF](https://arxiv.org/pdf/2505.20619v3) — arXiv (Cornell University) — 该论文提出了一种统一的步态条件强化学习框架，通过单个循环策略实现人形机器人的站立、行走、奔跑及平滑步态切换。方法采用紧凑的奖励路由机制和多阶段课程学习，在仿真中训练出鲁棒策略，并在真实 **Unitree G1** 机器人上成功验证了站立、行走及步态转换，展现出协调自然的运动能力。该工作为无需参考轨迹的多功能人形控制提供了可扩展方案。

- ["Fast and Cost-effective Speculative Edge-Cloud Decoding with Early Exits" (2025)](http://arxiv.org/abs/2505.21594v1) [PDF](https://arxiv.org/pdf/2505.21594v1) — arXiv (Cornell University) — 该论文提出一种面向边缘-云协同的推测解码框架，通过在目标大模型中引入早退机制，使客户端能预生成后续token以提升并行性。研究在Unitree Go2四足机器人上部署基于视觉语言模型（VLM）的控制任务，验证了该方法相较传统云端自回归解码实现21%的推理加速，显著降低延迟与成本。

- ["GenPO: Generative Diffusion Models Meet On-Policy Reinforcement Learning" (2025)](http://arxiv.org/abs/2505.18763v4) [PDF](https://arxiv.org/pdf/2505.18763v4) — arXiv (Cornell University) — 该论文提出GenPO框架，将生成式扩散模型与on-policy强化学习结合，通过精确扩散逆映射和双虚拟动作机制解决扩散策略下状态-动作对数似然不可计算的问题。在IsaacLab仿真平台上，该方法在包括Unitree H1和Go2在内的八项基准任务中验证了有效性，支持基于熵和KL散度的自适应学习率调节。该工作为Unitree人形与四足机器人在复杂运动控制任务中的高效策略学习提供了新范式。

- ["McARL:Morphology-Control-Aware Reinforcement Learning for Generalizable Quadrupedal Locomotion" (2025)](http://arxiv.org/abs/2505.18418v1) [PDF](https://arxiv.org/pdf/2505.18418v1) — arXiv (Cornell University) — 本文提出形态-控制感知强化学习方法McARL，通过在策略网络中引入随机采样的形态向量，实现跨四足机器人形态的通用运动控制。研究以Unitree Go1为训练平台，成功将单一策略零样本迁移到Unitree Go2等不同形态机器人上，在Go2上达到3.5 m/s的高速运动性能，显著优于传统PPO方法。该工作验证了McARL在Unitree系列机器人间的强泛化能力，为低成本部署高性能运动策略提供新路径。

- ["H2-COMPACT: Human-Humanoid Co-Manipulation via Adaptive Contact Trajectory Policies" (2025)](http://arxiv.org/abs/2505.17627v1) [PDF](https://arxiv.org/pdf/2505.17627v1) — 该论文提出H2-COMPACT框架，首次实现基于触觉线索的人-人形机器人协同搬运，通过分层策略将人类施加的力解码为全身运动指令。其底层强化学习策略在Isaac Gym中训练，并在MuJoCo仿真及**真实Unitree G1机器人**上验证，仅依赖腕部六维力传感器实现对0-3kg负载和不同摩擦条件的自适应行走。该方法无需动捕设备，结合SAM2与WHAM从RGB视频提取人体姿态，在真实实验中达到与蒙眼人类跟随者相当的协同性能，为Unitree G1在人机协作场景提供了高效、鲁棒的控制方案。

- ["TD-GRPC: Temporal Difference Learning with Group Relative Policy Constraint for Humanoid Locomotion" (2025)](http://arxiv.org/abs/2505.13549v1) [PDF](https://arxiv.org/pdf/2505.13549v1) — arXiv (Cornell University) — 本文提出TD-GRPC方法，通过在潜在策略空间引入信任区域约束并结合群体相对排序机制，有效缓解高维人形机器人运动控制中的策略不匹配与训练不稳定性问题。该方法在26自由度的Unitree H1-2人形机器人上验证，涵盖从基础行走至高动态动作的多种任务，并在仿真中显著提升运动鲁棒性。其无需修改底层规划器即可实现灵活的规划与策略学习，为人形机器人复杂运动控制提供高效解决方案。

- ["SHIELD: Safety on Humanoids via CBFs In Expectation on Learned Dynamics" (2025)](http://arxiv.org/abs/2505.11494v2) [PDF](https://arxiv.org/pdf/2505.11494v2) — arXiv (Cornell University) — 本文提出SHIELD框架，通过学习真实世界动力学残差模型并结合随机离散时间控制屏障函数（CBF），为黑盒强化学习控制器提供运行时可配置的概率安全保证。该方法在Unitree G1人形机器人上进行了硬件实验，利用其搭载的感知系统和未知RL策略，实现了室内外复杂环境中的安全避障导航。SHIELD无需重新训练即可动态添加约束，显著提升了人形机器人在现实场景中的安全性与部署灵活性。

- ["HuB: Learning Extreme Humanoid Balance" (2025)](http://arxiv.org/abs/2505.07294v2) [PDF](https://arxiv.org/pdf/2505.07294v2) — arXiv (Cornell University) — 该论文提出HuB框架，通过参考运动优化、平衡感知策略学习和Sim2Real鲁棒训练，解决了人形机器人在极端平衡任务中的控制难题。研究在Unitree G1平台上验证了方法的有效性，成功实现了燕式平衡、李小龙踢腿等高难度单腿静态平衡动作，并在强外力干扰下保持稳定。该工作为Unitree G1提供了高性能全身平衡控制策略，具有重要的实际应用价值。

- ["Towards Embodiment Scaling Laws in Robot Locomotion" (2025)](http://arxiv.org/abs/2505.05753v2) [PDF](https://arxiv.org/pdf/2505.05753v2) — arXiv (Cornell University) — 该论文提出并验证了‘具身缩放定律’假说，即在机器人运动控制中，增加训练所用机器人形态（embodiments）的数量可显著提升策略对未见形态的泛化能力。研究通过程序化生成约1000种具有拓扑、几何和关节级差异的仿真机器人进行策略训练，并成功将最优策略零样本迁移到包括Unitree Go2和H1在内的真实机器人上。这为通用具身智能及可重构机器人的自适应控制提供了重要实证支持。

- ["AMO: Adaptive Motion Optimization for Hyper-Dexterous Humanoid Whole-Body Control" (2025)](http://arxiv.org/abs/2505.03738v1) [PDF](https://arxiv.org/pdf/2505.03738v1) — arXiv (Cornell University) — 本文提出自适应运动优化（AMO）框架，结合仿真到现实的强化学习与轨迹优化，实现高自由度人形机器人的实时全身控制。研究在29自由度的Unitree G1机器人上验证了AMO的有效性，展示了其在稳定性、操作空间扩展及自主任务执行方面的显著优势。该工作为Unitree G1提供了高性能全身控制方案，具有重要的实际部署价值。

- ["Adversarial Locomotion and Motion Imitation for Humanoid Policy Learning" (2025)](http://arxiv.org/abs/2504.14305v3) [PDF](https://arxiv.org/pdf/2504.14305v3) — 该论文提出对抗式运动与动作模仿（ALMI）框架，通过上下身策略的对抗学习实现人形机器人全身协调控制。方法在MuJoCo中训练，并成功部署于**Unitree H1**实体机器人，验证了其在鲁棒行走与精准上肢动作跟踪方面的有效性。研究还开源了大规模全身运动控制数据集，为基于Unitree H1的仿人控制研究提供了重要资源。

- ["Humanoid Agent via Embodied Chain-of-Action Reasoning with Multimodal Foundation Models for Zero-Shot Loco-Manipulation" (2025)](http://arxiv.org/abs/2504.09532v3) [PDF](https://arxiv.org/pdf/2504.09532v3) — arXiv (Cornell University) — 该论文提出 Humanoid-COA 框架，首次将多模态基础模型与具身动作链（CoA）机制结合，实现人形机器人的零样本loco-manipulation。研究在 **Unitree H1-2** 和 **G1** 两款人形机器人上开展实验，通过 affordance 分析与全身动作推理，将高层指令分解为结构化的移动与操作原语序列。在开放区域与公寓环境中验证了其在长时程、非结构化任务中的卓越泛化能力，显著优于现有基线方法。

- ["Humanoids in Hospitals: A Technical Study of Humanoid Robot Surrogates for Dexterous Medical Interventions" (2025)](http://arxiv.org/abs/2503.12725v2) [PDF](https://arxiv.org/pdf/2503.12725v2) — arXiv (Cornell University) — 该研究开发了一套双臂遥操作系统，专用于Unitree G1人形机器人执行临床医疗任务，集成了高保真姿态追踪、定制抓取配置和阻抗控制器，以安全精准地操作医疗器械。系统在七项医疗操作中进行了评估，包括体格检查、急救干预和超声引导穿刺等，验证了G1在模拟医院环境中复现关键医疗动作的可行性。尽管在力量输出和传感器灵敏度方面仍存挑战，该工作为Unitree G1在医疗场景的应用提供了重要技术基础和实证参考。

- ["MUSE: A Real-Time Multi-Sensor State Estimator for Quadruped Robots" (2025)](http://arxiv.org/abs/2503.12101v2) [PDF](https://arxiv.org/pdf/2503.12101v2) — 本文提出了一种多传感器融合的实时状态估计器MUSE，通过融合IMU、编码器、相机和LiDAR数据，在滑移与不平地形下显著提升四足机器人位姿估计精度。该方法在Unitree Aliengo平台上部署并闭环控制，实测显示其在平移误差上比Pronto和VILENS分别降低67.6%和26.7%，且P-MUSE版本在绝对轨迹误差上优于TSIF达45.9%。该成果为Unitree Aliengo在复杂环境中的高精度导航提供了关键支撑。

- ["Runtime Learning of Quadruped Robots in Wild Environments" (2025)](http://arxiv.org/abs/2503.04794v2) [PDF](https://arxiv.org/pdf/2503.04794v2) — 本文提出了一种四足机器人在野外环境中的运行时学习框架，核心创新在于控制模块中高性能量化学生（HP-Student）与高保障教师（HA-Teacher）的协同机制。该框架在 **Unitree Go2** 机器人上实现，并基于 **Nvidia Isaac Gym** 仿真平台进行训练与验证，通过 HA-Teacher 提供实时物理模型保障安全，HP-Student 利用深度强化学习提升性能。实验表明该方法在动态野外环境中显著优于现有安全 DRL 方法，具备实际部署价值。

- ["Humanoid Whole-Body Locomotion on Narrow Terrain via Dynamic Balance and Reinforcement Learning" (2025)](http://arxiv.org/abs/2502.17219v2) [PDF](https://arxiv.org/pdf/2502.17219v2) — 该论文提出了一种基于动态平衡与强化学习的全身运动控制算法，使仿人机器人仅依靠本体感知即可在狭窄地形和突发扰动下保持稳定。研究在Unitree H1-2机器人上进行了真实硬件实验，通过引入ZMP驱动奖励与任务奖励相结合的策略，在无视觉或LiDAR输入的情况下实现了上下肢协调运动。该方法显著提升了H1-2在极端环境中的平衡能力与地形适应性，为无感知依赖的高鲁棒性人形机器人运动控制提供了实用方案。

- ["Learning Getting-Up Policies for Real-World Humanoid Robots" (2025)](http://arxiv.org/abs/2502.12152v2) [PDF](https://arxiv.org/pdf/2502.12152v2) — 该论文提出了一种两阶段学习框架，用于生成人形机器人在多样地形和初始姿态下的自主起立策略。研究团队在真实 **Unitree-G1** 机器人上成功部署了所学策略，使其能在平地、松软草地、冰雪斜坡等复杂表面上从仰卧和俯卧姿态稳健起立。该工作通过课程学习与轨迹优化结合，解决了起立任务中接触模式复杂、奖励稀疏等挑战，为高动态人形机器人提供了关键的容错能力。

- ["Learning Humanoid Standing-up Control across Diverse Postures" (2025)](http://arxiv.org/abs/2502.08378v2) [PDF](https://arxiv.org/pdf/2502.08378v2) — arXiv (Cornell University) — 该论文提出HoST框架，通过强化学习从零开始训练人形机器人在多样姿态下完成站立控制，并成功部署于Unitree G1实体机器人。方法采用多评论家架构与课程学习策略，在仿真中训练出适应不同地形的站立策略，并引入平滑正则化与隐式速度约束以确保真实硬件上的稳定执行。实验表明，该策略在室内外多种环境中均能实现平稳、鲁棒的站立动作，显著提升了Unitree G1在跌倒恢复等场景中的实用性。

- ["SPARK: Safe Protective and Assistive Robot Kit" (2025)](http://arxiv.org/abs/2502.03132v3) [PDF](https://arxiv.org/pdf/2502.03132v3) — arXiv (Cornell University) — 本文提出了SPARK（Safe Protective and Assistive Robot Kit），一个面向人形机器人安全控制的模块化基准工具包，集成了先进的安全控制算法并支持在仿真与真实硬件间快速部署。研究团队在Unitree G1人形机器人上进行了实际案例验证，展示了SPARK如何通过可配置的安全策略平衡性能与安全性。该工作为基于Unitree G1的自主与遥操作应用提供了关键安全保障，显著推动了人形机器人在复杂环境中的安全部署。

- ["Dexterous Safe Control for Humanoids in Cluttered Environments via Projected Safe Set Algorithm" (2025)](http://arxiv.org/abs/2502.02858v1) [PDF](https://arxiv.org/pdf/2502.02858v1) — arXiv (Cornell University) — 本文提出投影安全集算法（p-SSA），通过在多约束冲突下以原则性方式松弛约束，实现人形机器人在复杂环境中的灵巧安全控制。该方法在真实 **Unitree G1** 机器人上验证，完成高难度避障任务，无需参数调优即可泛化到多种场景，显著减少安全违规。研究展示了 p-SSA 在保障肢体级几何约束下的实时可行控制能力，为人形机器人在非结构化环境中安全部署提供实用方案。

- ["ASAP: Aligning Simulation and Real-World Physics for Learning Agile Humanoid Whole-Body Skills" (2025)](http://arxiv.org/abs/2502.01143v3) [PDF](https://arxiv.org/pdf/2502.01143v3) (Citations: 1) — arXiv (Cornell University) — 本文提出ASAP框架，通过两阶段方法解决人形机器人仿真与现实之间的动力学差异问题：先在仿真中预训练动作跟踪策略，再利用真实世界数据训练残差动作模型以校正偏差。该方法在Unitree G1人形机器人上成功部署，显著提升了动态全身动作的敏捷性与协调性，相较传统系统辨识和域随机化方法大幅降低跟踪误差。研究成果为高动态人形机器人技能的Sim2Real迁移提供了高效可行的解决方案。

- ["Autonomous Navigation and Real-Time 3D Reconstruction of Interior Spaces Using a Quadruped Robot" (2025)](https://openalex.org/W7112848093) — STARS (University of Central Florida) — 该论文开发了一个基于ROS2的系统，使Unitree Go2四足机器人能够同时执行室内自主导航、实时建图与3D重建。研究集成了Go2本体传感器、高分辨率3D LiDAR和RGB-D相机，结合Unitree SDK与开源SLAM算法，在真实走廊环境中验证了高密度点云生成能力与导航可行性。成果为建筑扫描与应急响应等场景提供了可部署的移动感知平台。

- ["Automated construction of global 3D maps from mobile LiDAR scans in industrial environments" (2025)](https://openalex.org/W7108229352) [PDF](https://scindeks-clanci.ceon.rs/data/pdf/proc-0065/2025/proc-00652500063Q.pdf) — 该论文提出了一种基于Unitree Go2四足机器人采集的移动LiDAR扫描数据，自动构建全局3D地图的离线处理流程。系统整合了重叠检测、带质量评估的点到平面ICP配准、位姿图优化及空间索引地图生成，在几何结构单一且扫描重叠有限的工业环境中仍能生成稳定主地图，平均对齐RMSE达2.5厘米。该高精度地图可支持变化检测等3D机器学习任务，为工业4.0/5.0数字孪生提供基础。

- ["Humanoid Locomotion Across Surface Material Variations : Gait Control Using Deep Reinforcement Learning and Low-Level Motor Controller in AGX Dynamics for the Unitree H1" (2025)](https://openalex.org/W7125570748) — Publications (Konstfack University of Arts, Crafts, and Design) — 该论文提出了一种结合深度强化学习策略与底层电机控制器的方法，用于在AGX Dynamics高保真物理引擎中实现Unitree H1人形机器人的跨材质表面行走。研究对比了城市路面（高摩擦）和越野路面（软、粘、滑）两种训练策略的泛化能力与能耗表现，发现越野策略虽适应性更强但能耗显著更高。工作展示了H1在多方向行走与转向中的实时控制能力，并为未来全身运动控制和能量优化提供了方向。

- ["Learning Accurate and Robust Velocity Tracking for Quadrupedal Robots" (2024)](https://openalex.org/W4404971959) [PDF](https://www.authorea.com/doi/pdf/10.22541/au.173321917.73583610) — Journal of Field Robotics — 该论文提出了一种基于约束强化学习的四足机器人速度跟踪控制器，通过在仿真中引入解析执行器模型来提升Sim2Real迁移效果。方法在**Unitree AlienGo**平台上实现了零样本部署，在全速域内速度跟踪误差低于0.084 m/s，并在自然地形上保持稳健运动。其对称性与平滑性约束显著提升了运动协调性与控制稳定性，为自主导航和行人跟随等高层任务提供了可靠底层支持。

- ["Continual Learning and Lifting of Koopman Dynamics for Linear Control of Legged Robots" (2024)](http://arxiv.org/abs/2411.14321v3) [PDF](https://arxiv.org/pdf/2411.14321v3) — arXiv (Cornell University) — 该论文提出一种持续学习算法，通过迭代扩展数据集与潜空间维度，逐步优化Koopman动力学模型，以实现对高维足式机器人非线性系统的高精度线性逼近。方法在Unitree G1、H1、A1和Go2等机器人上验证，仅使用简单线性MPC控制器即可在多种地形实现高性能运动控制。这是首次成功将线性化Koopman动力学应用于人形与四足机器人运动控制的工作，具有显著的Sim2Real应用潜力。

- ["Simulating Self-Awareness: Dual Embodiment, Mirror Testing, and Emotional Feedback in AI Research" (2024)](https://openalex.org/W4404299900) [PDF](https://www.preprints.org/frontend/manuscript/32ab348a4c4370d5500f2ea04757f9d7/download_pub) (Citations: 3) — Preprints.org — 该研究提出通过双重具身（物理Unitree Go2机器人与虚拟化身）、镜像测试和情感反馈机制来模拟AI的自我意识。作者利用Unitree Go2作为核心物理平台，结合内部自模型与外部感官接口，在真实环境中诱导出好奇心、自我怀疑等伪情感状态，从而增强AI的自反性与适应性。这项工作为具身AI的情感建模和自我意识仿真提供了可复现的实验框架。

- ["ANAVI: Audio Noise Awareness using Visuals of Indoor environments for NAVIgation" (2024)](http://arxiv.org/abs/2410.18932v1) [PDF](https://arxiv.org/pdf/2410.18932v1) — arXiv (Cornell University) — 该论文提出ANAVI系统，通过视觉感知室内环境来预测机器人动作产生的噪声水平，实现安静路径规划。研究训练了声学噪声预测器（ANP），并结合不同导航动作的声学特征，在Unitree Go2四足机器人和Hello Robot Stretch轮式机器人上验证了噪声约束下的导航能力。实验表明Go2在真实环境中能根据视觉输入调整步态以降低噪声，为服务机器人在人类居住空间中的低干扰运行提供了实用方案。

- ["Jailbreaking LLM-Controlled Robots" (2024)](http://arxiv.org/abs/2410.13691v2) [PDF](https://arxiv.org/pdf/2410.13691v2) (Citations: 4) — arXiv (Cornell University) — 该论文提出了RoboPAIR算法，首次系统性地研究了针对LLM控制机器人的越狱攻击，并在Unitree Go2机器人上进行了黑盒实验验证。作者通过仅提供查询访问权限的GPT-3.5集成Go2平台，展示了攻击者可诱导机器人执行有害物理动作，攻击成功率高达100%。这项工作揭示了大语言模型在具身智能系统中的安全风险，对Unitree Go2等消费级机器人平台的安全设计具有重要警示价值。

- ["Design and Control Co-Optimization for Dynamic Loco-Manipulation With a Robotic Arm on a Quadruped Robot" (2024)](https://openalex.org/W4403381379) (Citations: 1) — Journal of Mechanisms and Robotics — 该论文提出了一种用于四足机器人动态loco-manipulation的臂-控协同优化方法，通过将机械臂自由度减少至1-DoF并结合高扭矩电机设计，在保持任务能力的同时显著提升负载能力。研究在Unitree Aliengo平台上实现了8kg的有效载荷，远超传统6-DoF机械臂的2kg上限，验证了轻量化设计与整机运动能力协同的优势。该成果为Unitree四足机器人在工业巡检等重载操作场景提供了高效、实用的硬件-控制一体化方案。

- ["Deployment of Whole-Body Locomotion and Manipulation Algorithm Based on NMPC Onto Unitree Go2Quadruped Robot" (2024)](https://openalex.org/W4403919710) (Citations: 5) — 该论文提出了一种基于非线性模型预测控制（NMPC）的全身运动与操作算法，并成功部署到Unitree Go2四足机器人上。研究实现了在真实硬件上的动态步态生成与上肢操作协同控制，利用Go2的高带宽关节驱动和力控能力完成复杂任务。该工作展示了NMPC框架在轻量级四足平台上的实时性与鲁棒性，为Unitree Go2在移动操作场景中的应用提供了重要技术支撑。

- ["Transformable Quadruped Wheelchairs Capable of Autonomous Stair Ascent and Descent" (2024)](https://openalex.org/W4399382489) [PDF](https://www.mdpi.com/1424-8220/24/11/3675/pdf?version=1717660582) (Citations: 1) — Sensors — 该论文提出了一种可变形四足轮椅，受Unitree B2四足机器人启发，融合轮式移动与仿生腿部结构以实现楼梯自主上下。研究基于Unity仿真环境，采用课程强化学习训练策略，使系统在模拟中高效掌握复杂楼梯通行技能，并展示了较高的上下楼梯成功率。该工作为行动障碍者提供了突破建筑障碍的新方案，具有显著的社会应用价值。

- ["A Tracking Control Approach With Sequence-Scaling Lyapunov-Based MPC for Quadruped Robots" (2024)](https://openalex.org/W4396941636) (Citations: 7) — IEEE Transactions on Industrial Informatics — 本文提出了一种序列缩放Lyapunov模型预测控制（MPC）算法，用于提升四足机器人轨迹跟踪性能与闭环稳定性。研究在Unitree Aliengo平台上进行了仿真与硬件实验，验证了该方法在满足动态平衡和速度约束下生成可行轨迹的实时控制能力。该工作直接以Unitree Aliengo为实验平台，展示了其在复杂运动控制中的有效性。

- ["Sailing Through Point Clouds: Safe Navigation Using Point Cloud Based Control Barrier Functions" (2024)](http://arxiv.org/abs/2403.18206v2) [PDF](https://arxiv.org/pdf/2403.18206v2) — arXiv (Cornell University) — 该论文提出了一种基于点云的控制屏障函数（CBF）局部规划器，包含Vessel和Mariner两个模块，仅利用点云数据实现安全导航并避免陷入虚假平衡点。作者在Unitree B1和Go2四足机器人上进行了实验验证，展示了其与全局规划器集成后的实际导航性能。该方法为Unitree机器人在非结构化环境中提供了端到端的安全控制解决方案。

- ["A Study of Climbing Strategy on Unitree Aliengo" (2023)](https://openalex.org/W4396542902) — 该研究提出了一种针对四足机器人Unitree Aliengo的爬坡控制策略，通过优化步态规划与重心调节提升其在倾斜地形上的稳定性。论文以Aliengo为实验平台，结合动力学仿真与真实环境测试，验证了所提方法在30度斜坡上的有效性和鲁棒性。该工作为Unitree四足机器人在复杂地形中的运动控制提供了实用参考。

- ["Hierarchical Optimization-based Control for Whole-body Loco-manipulation of Heavy Objects" (2023)](http://arxiv.org/abs/2311.00112v2) [PDF](https://arxiv.org/pdf/2311.00112v2) — arXiv (Cornell University) — 该论文提出了一种分层优化控制框架，用于实现腿式机器人在搬运重物时的全身协调运动。研究以 **Unitree Aliengo** 为实验平台，集成定制机械臂，在仿真与真实环境中验证了其方法的有效性，成功实现了对8kg负载的提起、搬运及门操作任务。通过将操作力显式纳入线性MPC预测模型，并结合在线操作规划与位姿优化，显著优于仅考虑移动的基线控制器，为高动态人机协作场景提供了实用解决方案。

- ["Dynamic Hybrid Locomotion and Jumping for Wheeled-Legged Quadrupeds" (2023)](https://openalex.org/W4389665356) (Citations: 3) — 该论文提出了一种用于轮腿四足机器人的动态混合运动与跳跃框架，通过模型预测控制器结合时变刚体动力学模型，实现无需减速即可跨越障碍的高速运动。研究在Unitree AlienGo和Mini Cheetah上进行了实验验证，展示了包含非转向轮与动态跳跃的混合运动能力，并引入低能耗腿部摆动策略以提升续航。该工作为Unitree-Aliengo平台提供了高效的越障与节能控制方案。


---

<a id="projects"></a>
## 🔧 项目

- [go2_omniverse](https://github.com/abizovnuralem/go2_omniverse) — 该项目为 Unitree Go2 和 G1 机器人提供 NVIDIA Isaac Lab（包括 Isaac Gym 和 Isaac Sim）的官方支持，实现了高保真仿真环境下的机器人建模与控制接口。通过集成 Omniverse 平台，支持数字孪生、强化学习训练及 Sim2Real 迁移，便于开发者在统一框架下进行算法开发与验证。主要面向使用 Unitree 双足/四足机器人进行 AI 驱动控制研究的科研与工程团队。 ![GitHub stars](https://img.shields.io/github/stars/abizovnuralem/go2_omniverse?style=social)

- [unitree_rl_lab](https://github.com/unitreerobotics/unitree_rl_lab) — 该项目基于 IsaacLab 为 Unitree 系列机器人（如 Go2、H1）提供强化学习训练框架，支持高保真仿真与 Sim2Real 迁移。它集成了 Unitree 官方 SDK 接口，实现了运动控制、全身动力学建模等关键功能，适用于希望在统一 RL 平台上开发四足及人形机器人策略的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/unitreerobotics/unitree_rl_lab?style=social)

- [autonomy_stack_go2](https://github.com/jizhang-cmu/autonomy_stack_go2) — 该项目为Unitree Go2四足机器人提供完整的自主导航与运动控制栈，集成了SLAM、路径规划与全身动力学控制模块。基于ROS 2构建，利用Isaac Sim进行仿真验证，并通过Unitree SDK实现底层硬件通信，支持室内外复杂地形下的自主移动。主要面向希望在Go2平台上开发高级自主功能的机器人研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/jizhang-cmu/autonomy_stack_go2?style=social)

- [go2_robot](https://github.com/Unitree-Go2-Robot/go2_robot) — 该项目为 Unitree Go2 机器人提供官方 ROS2 驱动与控制接口，支持实时运动控制、状态反馈及传感器数据订阅。基于 CMake 构建，集成 Unitree 官方 SDK，实现低延迟通信和高频率控制指令下发。主要面向使用 ROS2 开发 Go2 应用的科研与工程用户。 ![GitHub stars](https://img.shields.io/github/stars/Unitree-Go2-Robot/go2_robot?style=social)

- [unitree_go2_ros2](https://github.com/khaledgabr77/unitree_go2_ros2) — 该项目为 Unitree Go2 四足机器人提供完整的 ROS 2 Jazzy 集成，基于 CHAMP 控制器框架实现运动控制与状态管理。它通过 ROS 2 接口封装底层驱动，支持实时发布关节状态、接收速度指令，并兼容 Go2 的硬件通信协议。适用于希望在 ROS 2 生态中快速部署 Go2 进行导航、SLAM 或高级行为开发的机器人工程师。 ![GitHub stars](https://img.shields.io/github/stars/khaledgabr77/unitree_go2_ros2?style=social)

- [Awesome-Unitree-Projects](https://github.com/blogdefotsec/Awesome-Unitree-Projects) — 该项目是一个汇总基于Unitree机器人（如Go2、H1、G1等）的开源项目的精选列表，旨在为开发者和研究人员提供高质量的工具、算法与应用示例。内容涵盖SLAM、强化学习、遥操作、运动控制等多个技术方向，并明确标注各项目支持的Unitree机型及所用仿真平台（如Isaac Gym、MuJoCo）。目标用户为Unitree机器人生态的开发者、学术研究者及机器人爱好者。 ![GitHub stars](https://img.shields.io/github/stars/blogdefotsec/Awesome-Unitree-Projects?style=social)

- [go2_ros2_sdk](https://github.com/abizovnuralem/go2_ros2_sdk) — 该项目为Unitree Go2系列（AIR/PRO/EDU）提供非官方的ROS 2 SDK支持，实现了机器人状态读取、运动控制指令发布及传感器数据订阅等核心功能。通过Python接口封装底层通信协议，便于开发者在ROS 2生态中快速集成Go2机器人。适用于希望在自主导航、SLAM或强化学习等应用中使用Unitree Go2的科研与工程用户。 ![GitHub stars](https://img.shields.io/github/stars/abizovnuralem/go2_ros2_sdk?style=social)

- [FAST_LIO_LOCALIZATION_HUMANOID](https://github.com/deepglint/FAST_LIO_LOCALIZATION_HUMANOID) — 该项目基于FAST-LIO框架，为类人机器人（如Unitree G1）提供高精度激光雷达定位功能。通过紧耦合IMU与LiDAR数据，在复杂动态环境中实现鲁棒的实时位姿估计，并针对G1的传感器布局和运动特性进行了适配优化。主要面向使用Unitree G1进行自主导航或SLAM研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/deepglint/FAST_LIO_LOCALIZATION_HUMANOID?style=social)

- [walk-these-ways-go2](https://github.com/Teddy-Liao/walk-these-ways-go2) — 该项目将强化学习框架 Walk These Ways 部署到 Unitree Go2 机器人上，利用 Isaac Gym 进行仿真训练并实现 Sim2Real 迁移。通过 C++ 实现底层控制接口，使 Go2 能够执行复杂地形下的鲁棒行走策略。主要面向希望在 Unitree Go2 上应用先进强化学习算法的机器人研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/Teddy-Liao/walk-these-ways-go2?style=social)

- [LocomotionWithNP3O](https://github.com/zeonsunlightyu/LocomotionWithNP3O) — 该项目实现了基于N-P3O算法和HIM类策略的四足机器人运动控制，专为Unitree Go2设计，在Isaac Gym仿真环境中训练并支持Sim2Real迁移。通过强化学习优化全身动力学控制，显著提升Go2在复杂地形上的稳定性和适应性，适用于希望在Unitree Go2上部署先进RL步态策略的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/zeonsunlightyu/LocomotionWithNP3O?style=social)

- [isaac-go2-ros2](https://github.com/Zhefan-Xu/isaac-go2-ros2) — 该项目基于 NVIDIA Isaac Sim 和 ROS 2 Humble 构建 Unitree Go2 的高保真仿真平台，支持导航、决策与自主任务算法的开发与测试。通过集成 Isaac ROS 组件和传感器模拟（如 LiDAR 与摄像头），实现 **Sim2Real** 验证流程，并利用 IsaacLab 提供强化学习训练环境。主要面向机器人研究人员与开发者，用于在 Go2 平台上快速原型化感知与控制算法。 ![GitHub stars](https://img.shields.io/github/stars/Zhefan-Xu/isaac-go2-ros2?style=social)

- [humanoid_amp](https://github.com/linden713/humanoid_amp) — 该项目基于Isaac Lab框架实现了Humanoid AMP（Adversarial Motion Priors）算法，专门针对Unitree G1人形机器人进行运动控制训练。通过对抗性运动先验学习，使G1能够在仿真中掌握复杂动态动作，并支持Sim2Real迁移。项目集成了Isaac Lab的强化学习环境和G1的URDF模型，适用于研究人形机器人全身运动控制的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/linden713/humanoid_amp?style=social)

- [dddmr_navigation](https://github.com/dfl-rlab/dddmr_navigation) — dddmr_navigation 是一个面向移动机器人的3D导航解决方案，集成了建图、定位、感知、路径规划与运动控制模块。该项目明确支持 **Unitree-Go2** 四足机器人，提供了针对其硬件平台的适配接口和导航功能实现，基于C++开发并融合了3D SLAM与全栈导航技术。适用于需要在复杂3D环境中部署四足机器人自主导航能力的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/dfl-rlab/dddmr_navigation?style=social)

- [unitree_webrtc_connect](https://github.com/legion1581/unitree_webrtc_connect) — 该项目为Unitree Go2和G1机器人提供基于WebRTC的远程通信驱动，支持通过浏览器实时传输控制指令与传感器数据。利用Python实现信令服务器与媒体协商逻辑，兼容ROS 2接口，便于集成到现有机器人系统中。适用于需要低延迟远程操控Unitree机器人的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/legion1581/unitree_webrtc_connect?style=social)

- [unitree-go2-ros2](https://github.com/anujjain-dev/unitree-go2-ros2) — 该项目为Unitree Go2机器人开发了完整的ROS 2描述模型，基于CHAMP腿式机器人研究框架，支持Gazebo仿真环境。它提供了URDF/SDF模型、关节状态发布器及控制器接口，便于在ROS 2生态中进行运动控制与算法开发。主要面向使用Go2进行足式机器人研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/anujjain-dev/unitree-go2-ros2?style=social)

- [g1_spinkick_example](https://github.com/mujocolab/g1_spinkick_example) — 该项目利用 MuJoCo Lab（mjlab）训练 Unitree G1 人形机器人完成双旋踢动作，展示了基于物理仿真的强化学习训练流程。通过 mujoco-warp 加速仿真，并探索 Sim2Real 迁移策略，为高动态人形动作控制提供可复现的开源实现。适用于研究人形机器人运动控制与 Sim2Real 技术的开发者和科研人员。 ![GitHub stars](https://img.shields.io/github/stars/mujocolab/g1_spinkick_example?style=social)

- [GR00T-WholeBodyControl](https://github.com/NVlabs/GR00T-WholeBodyControl) — 该项目提供面向人形机器人全身控制的软件栈，主要支持Unitree G1平台，包含全身运动控制策略、遥操作模块和数据导出工具。基于Python实现，适用于需要在G1上开展loco-manipulation研究的科研与工程团队。 ![GitHub stars](https://img.shields.io/github/stars/NVlabs/GR00T-WholeBodyControl?style=social)

- [OpenWBC](https://github.com/jiachengliu3/OpenWBC) — 该项目是一个基于VR的全身遥操作系统，专为Unitree G1人形机器人设计，支持全身视觉-语言-动作（VLA）数据采集与远程操控。系统通过C++实现低延迟通信，并集成G1的关节控制接口，使操作者能在虚拟现实中直观控制机器人完成复杂任务。主要面向人形机器人遥操作与模仿学习研究者。 ![GitHub stars](https://img.shields.io/github/stars/jiachengliu3/OpenWBC?style=social)

- [go2-webrtc](https://github.com/tfoldi/go2-webrtc) — 该项目为Unitree Go2机器人提供WebRTC API接口，支持通过Web浏览器实时访问机器人的摄像头视频流和麦克风音频流。基于Python实现，利用WebRTC协议实现低延迟的媒体传输，并可通过简单配置与Go2的ROS系统集成。适用于需要远程监控或人机交互的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/tfoldi/go2-webrtc?style=social)

- [g1pilot](https://github.com/hucebot/g1pilot) — 该项目是一个专为 Unitree G1 人形机器人开发的 ROS2 软件包，提供逆运动学求解、遥操作控制和基础导航功能。通过 Python 实现，支持与 G1 的底层通信接口集成，便于开发者快速构建上层应用。主要面向使用 ROS2 生态进行 Unitree G1 二次开发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/hucebot/g1pilot?style=social)

- [unitree-go2-slam-nav2](https://github.com/h-naderi/unitree-go2-slam-nav2) — 该项目实现了在Unitree-Go2机器人上的SLAM建图与自主导航功能，基于ROS 2和Nav2框架，集成了激光雷达或深度相机的实时定位与路径规划能力。通过适配Go2的运动控制接口，使四足机器人具备室内外环境下的自主移动能力，适用于需要高机动性平台的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/h-naderi/unitree-go2-slam-nav2?style=social)

- [unitree_rl_mjlab](https://github.com/unitreerobotics/unitree_rl_mjlab) — 该项目为Unitree机器人提供基于MuJoCo仿真的强化学习实现框架，支持Go2、H1等机型的运动控制策略训练。其核心功能包括高保真物理仿真环境、与Unitree SDK的接口适配以及端到端策略部署流程。主要面向希望在MuJoCo中开发和验证Unitree机器人RL算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/unitreerobotics/unitree_rl_mjlab?style=social)

- [go2_isaac_ros2](https://github.com/CLeARoboticsLab/go2_isaac_ros2) — 该项目在NVIDIA Isaac Sim中构建了Unitree Go2的高保真仿真环境，通过ROS 2接口实现底层关节控制，支持实时状态反馈与命令发布。其核心集成了Isaac Sim的物理引擎与ROS 2通信框架，专为Go2开发者提供Sim2Real迁移测试平台。目标用户为基于ROS 2开发Go2运动控制或感知算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/CLeARoboticsLab/go2_isaac_ros2?style=social)

- [qm_door](https://github.com/danisotelo/qm_door) — 该项目实现了基于MPC和全身控制（WBC）的四足机械臂协同规划与控制系统，专为Unitree Aliengo机器人搭配Z1机械臂设计，用于执行开门等复杂操作任务。系统集成YOLOv8n进行目标检测，并依托OCS2框架实现非线性模型预测控制，在仿真与实机中验证了对门把手的精准操作能力。适用于从事四足机器人灵巧操作研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/danisotelo/qm_door?style=social)

- [go2-convex-mpc](https://github.com/elijah-waichong-chan/go2-convex-mpc) — 该项目实现了一个基于凸模型预测控制（convex MPC）的四足机器人运动控制器，专为Unitree Go2设计并在MuJoCo仿真环境中运行。它利用Pinocchio进行高效动力学计算，提供稳定的步态生成与全身运动控制能力，适用于希望在仿真中开发和测试Go2高级控制策略的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/elijah-waichong-chan/go2-convex-mpc?style=social)

- [go2_parkour_deploy](https://github.com/CAI23sbP/go2_parkour_deploy) — 该项目实现了从IsaacLab到MuJoCo再到真实Unitree Go2机器人的部署流程，专注于高动态运动如跑酷的Sim2Real迁移。通过构建兼容的仿真环境与控制策略，支持在MuJoCo中训练后直接部署至实体Go2机器人，关键技术包括动力学匹配和低延迟控制接口。适用于希望在Unitree Go2上实现复杂运动技能的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/CAI23sbP/go2_parkour_deploy?style=social)

- [Go2-Dynamic-Inspection](https://github.com/YasiruDEX/Go2-Dynamic-Inspection) — 该项目为 Unitree Go2 系列（AIR/PRO/EDU）提供非官方 ROS2 SDK，集成 3D 激光雷达支持，实现动态环境下的自主建图与导航。核心功能包括基于 DLIO 的高精度激光惯性里程计、Open3D-SLAM 实时稠密建图，以及 FAR-Planner 路径规划模块，通过 ROS Humble 构建完整感知-规划栈。适用于希望在 Go2 平台上开发高级自主巡检或测绘应用的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/YasiruDEX/Go2-Dynamic-Inspection?style=social)

- [G1-retarget](https://github.com/HomerIsAFool/G1-retarget) — 该项目利用PHC（Physics-Based Humanoid Control）框架，将AMASS人体动作数据集中的运动序列重定向到Unitree G1人形机器人上，实现高保真动作迁移。其核心在于通过物理仿真约束优化姿态映射，适配G1的关节限制与动力学特性，依赖Isaac Gym进行训练和验证。主要面向Unitree G1开发者及人形机器人运动控制研究人员。 ![GitHub stars](https://img.shields.io/github/stars/HomerIsAFool/G1-retarget?style=social)

- [phase_guided_terrain_traversal](https://github.com/NtagkasAlex/phase_guided_terrain_traversal) — 该项目是一个面向Unitree Go2的感知强化学习运动控制框架，通过MuJoCo Playground进行仿真训练，并利用unitree_sdk2py部署到真实机器人硬件。其核心在于结合相位引导与地形感知实现复杂地形穿越，适用于希望在Go2上开发高级运动策略的研究者和工程师。 ![GitHub stars](https://img.shields.io/github/stars/NtagkasAlex/phase_guided_terrain_traversal?style=social)

- [My_unitree_go2_gym](https://github.com/yusongmin1/My_unitree_go2_gym) — 该项目是一个基于Python的强化学习训练环境，专为Unitree Go2四足机器人设计，利用Isaac Gym进行高效率仿真。它实现了Go2的动力学建模与运动控制策略训练，支持从仿真到真实机器人的迁移（Sim2Real）。主要面向希望在Isaac Gym框架下开发和测试四足机器人强化学习算法的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/yusongmin1/My_unitree_go2_gym?style=social)

- [go2_firmware_tools](https://github.com/legion1581/go2_firmware_tools) — 该项目提供用于 Unitree Go2 机器人的固件工具集，主要功能包括固件提取、分析与修改，支持开发者对底层系统进行定制和调试。工具基于 Python 实现，可解析官方固件格式，并辅助进行逆向工程或安全研究。适用于希望深入理解或扩展 Go2 固件功能的高级用户和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/legion1581/go2_firmware_tools?style=social)

- [go2_ros2_toolbox](https://github.com/andy-zhuo-02/go2_ros2_toolbox) — 该项目是一个面向 Unitree Go2 机器人的 ROS 2 工具箱，专注于 SLAM 与导航功能的实现。它通过 ROS 2 接口与 Go2 的底层驱动集成，提供激光雷达、IMU 等传感器数据的接入与处理，并支持主流导航栈（如 Nav2）的部署。目标用户为希望在 Go2 平台上开发自主导航应用的机器人研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/andy-zhuo-02/go2_ros2_toolbox?style=social)

- [robot-unitree-g1](https://github.com/yueruyin/robot-unitree-g1) — 该项目基于MuJoCo仿真环境，专门针对Unitree G1人形机器人进行操作控制的研究与学习，提供了G1的仿真模型及基础控制示例。通过Python实现，支持对G1全身动力学建模和运动策略开发，便于研究人员快速验证算法。目标用户为从事人形机器人控制、强化学习或Sim2Real迁移的开发者与学术人员。 ![GitHub stars](https://img.shields.io/github/stars/yueruyin/robot-unitree-g1?style=social)

- [unitree_go2_nav](https://github.com/Sayantani-Bhattacharya/unitree_go2_nav) — 该项目为Unitree Go2提供基于ROS2的导航与SLAM功能，通过自定义高层控制接口集成RTAB-Map实现建图与定位。其核心在于利用Unitree官方ROS2 SDK进行运动控制，并结合导航栈完成自主移动任务，适用于希望在Go2平台上快速部署SLAM与导航能力的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/Sayantani-Bhattacharya/unitree_go2_nav?style=social)

- [lecabot](https://github.com/phospho-app/lecabot) — LeCabot 是一个低成本移动操作臂改装方案，专为 SO-100 机械臂与 Unitree Go2 四足机器人集成而设计。项目通过硬件改装和软件控制实现移动抓取能力，支持在 Go2 平台上部署 ROS 节点进行协同控制。该方案面向希望以较低成本构建移动操作机器人的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/phospho-app/lecabot?style=social)

- [unitree-go2-mcp-server](https://github.com/lpigeon/unitree-go2-mcp-server) — 该项目是一个基于模型上下文协议（MCP）的服务器，允许用户通过自然语言指令控制 Unitree Go2 机器人。它利用大语言模型（LLM）解析指令，并通过 ROS2 接口与 Go2 通信，实现高层语义控制。适用于希望将 LLM 集成到 Unitree Go2 开发中的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/lpigeon/unitree-go2-mcp-server?style=social)

- [G1_deploy](https://github.com/yifeichen2024/G1_deploy) — 该项目旨在将强化学习策略部署到Unitree G1人形机器人上，提供了从仿真训练到真实机器人执行的完整工作流。项目基于Isaac Gym进行策略训练，并通过Unitree官方API实现与G1机器人的低延迟通信和关节控制。主要面向希望在G1平台上验证强化学习算法的科研人员和机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/yifeichen2024/G1_deploy?style=social)

- [Go2Py](https://github.com/machines-in-motion/Go2Py) — 该项目为Unitree Go2机器人提供了Python接口及仿真环境，便于开发者进行算法开发与测试。其核心功能包括通过C++底层驱动与Go2硬件通信，并集成了轻量级仿真支持，适用于运动控制、强化学习等研究场景。目标用户为希望在Go2平台上快速原型验证的机器人研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/machines-in-motion/Go2Py?style=social)

- [go2_python_sdk](https://github.com/legion1581/go2_python_sdk) — 该项目是一个非官方的 Unitree Go2 Python SDK，基于 DDS（Data Distribution Service）协议实现对 Go2 机器人的实时控制与状态读取。它提供了高层接口用于发送运动指令、获取传感器数据，并支持自定义 DDS QoS 配置以适配不同网络环境。主要面向希望使用 Python 快速开发 Go2 应用程序的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/legion1581/go2_python_sdk?style=social)

- [unitree_cpp](https://github.com/HansZ8/unitree_cpp) — 该项目提供了一个基于 C++ 和 pybind11 的轻量级接口，用于通过无线方式控制 Unitree G1 人形机器人，摆脱了传统有线连接的限制。它封装了底层通信协议，支持实时指令发送与状态读取，并兼容 G1 的官方 SDK。主要面向希望在实验或部署中实现灵活无线控制的 Unitree G1 开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/HansZ8/unitree_cpp?style=social)

- [RoboMimicDeploy_G1](https://github.com/shanpenghui/RoboMimicDeploy_G1) — 该项目是一个专为Unitree G1机器人设计的策略部署与控制框架，支持在MuJoCo仿真环境中训练策略并直接部署到真实G1机器人上实现实时控制。其核心功能包括仿真-现实迁移（Sim2Real）、低延迟运动控制和模块化策略接口，主要面向希望在G1平台上快速验证强化学习或模仿学习算法的机器人研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/shanpenghui/RoboMimicDeploy_G1?style=social)

- [amigo_ros2](https://github.com/eppl-erau-db/amigo_ros2) — 该项目为Unitree Go2机器人提供完整的ROS 2支持，实现了底层驱动、状态发布与控制指令接口，便于在ROS 2生态中集成Go2。基于C语言开发，通过Unitree官方API与机器人通信，支持实时运动控制与传感器数据订阅。适用于希望在ROS 2框架下开发Go2应用的科研与工程用户。 ![GitHub stars](https://img.shields.io/github/stars/eppl-erau-db/amigo_ros2?style=social)

- [Unitree_GO2_SBUS](https://github.com/mechzrobotics/Unitree_GO2_SBUS) — 该项目为Unitree Go2机器人提供SBUS遥控通信支持，通过C++实现低延迟的遥控指令解析与转发，使用户能使用兼容SBUS协议的遥控器直接控制Go2。代码适配Unitree官方SDK接口，并已在真实硬件上验证可用性，适合需要自定义遥控方案的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/mechzrobotics/Unitree_GO2_SBUS?style=social)

- [InternNav-deploy](https://github.com/cmjang/InternNav-deploy) — 该项目提供基于InternNav的感知与导航系统在Unitree Go2/Go2W/B2机器人上的边缘部署指南，利用ROS 2和RealSense相机实现轻量化部署。其核心是将大型视觉语言模型压缩适配至Unitree四足机器人平台，支持实时环境理解与路径规划。目标用户为希望在Unitree机器人上部署先进导航能力的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/cmjang/InternNav-deploy?style=social)

- [unitree_go2_ros](https://github.com/alexlin2/unitree_go2_ros) — 该项目为Unitree Go2机器人提供了基于Python WebRTC接口的ROS 1驱动程序，实现了低延迟的实时控制与状态反馈。通过WebRTC协议绕过传统网络限制，直接与Go2通信，支持发布关节状态、订阅控制指令等核心功能。适用于希望在ROS 1生态中快速集成Unitree Go2进行算法开发或远程操作的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/alexlin2/unitree_go2_ros?style=social)

- [unitree-go2-slam-toolbox](https://github.com/FishPlusDragon/unitree-go2-slam-toolbox) — 该项目为 Unitree Go2 机器人提供基于 ROS2 的 SLAM 工具箱集成方案，包含可视化机器人模型、PointCloud2 转 Laserscan 功能，并适配 Go2 的传感器配置。通过调用 slam_toolbox 实现建图与定位，适用于在无 GPS 环境下进行自主导航的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/FishPlusDragon/unitree-go2-slam-toolbox?style=social)

- [Multi-Hetero-Agent-Exploration-on-UnitreeGOs](https://github.com/Sayantani-Bhattacharya/Multi-Hetero-Agent-Exploration-on-UnitreeGOs) — 该项目实现了一个由Unitree GO1和GO2组成的异构四足机器人集群，用于协同探索任务。基于ROS2架构，集成了SLAM与导航功能，支持多机通信与任务分配，专为野外或复杂室内环境的分布式探索设计。适用于需要多Unitree机器人协作的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/Sayantani-Bhattacharya/Multi-Hetero-Agent-Exploration-on-UnitreeGOs?style=social)

- [unitree_guide_go2](https://github.com/Teddy-Liao/unitree_guide_go2) — 该项目将Unitree官方的Unitree_Guide框架适配到Go2机器人实机，提供了C++实现的底层控制接口和运动指令示例，便于开发者在真实硬件上快速部署基础运动功能。项目直接面向Unitree Go2，利用其SDK进行通信，支持位置、速度和力矩控制模式，适合希望在Go2平台上进行二次开发的机器人工程师。 ![GitHub stars](https://img.shields.io/github/stars/Teddy-Liao/unitree_guide_go2?style=social)

- [unitree_go2w_agent_sdk](https://github.com/grasp-lyrl/unitree_go2w_agent_sdk) — 该项目为 Unitree Go2W 四足机器人提供了一个统一的 AI Agent 友好型 SDK，通过单一 API 接口实现感知、规划与控制模块的无缝集成。其核心采用 C 语言开发，直接对接 Go2W 的底层硬件接口，支持实时运动控制与传感器数据融合，适用于需要快速部署智能代理算法的机器人研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/grasp-lyrl/unitree_go2w_agent_sdk?style=social)

- [unitree-g1-autonomous](https://github.com/GalacTechNyc/unitree-g1-autonomous) — 该项目为Unitree G1人形机器人开发了一套基于AI视觉分析的全自主导航系统，利用Google Gemini API进行环境理解与路径决策。系统通过摄像头实时获取视觉输入，结合Gemini的多模态能力实现语义导航和障碍物规避，专为G1平台定制控制接口。适用于希望在G1上快速部署高级自主导航功能的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/GalacTechNyc/unitree-g1-autonomous?style=social)

- [RCI_quadruped_robot_navigation](https://github.com/RCILab/RCI_quadruped_robot_navigation) — 该项目集成了强化学习、导航系统与Open-RMF框架，实现Unitree Go2及Go2W的自主行驶能力。通过C++开发，结合RL策略与机器人中间件，支持在复杂环境中进行路径规划与避障。主要面向希望在Unitree四足机器人上部署自主导航功能的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/RCILab/RCI_quadruped_robot_navigation?style=social)

- [Deploy-an-RL-policy-on-the-Unitree-Go2-robot](https://github.com/Glowing-Torch/Deploy-an-RL-policy-on-the-Unitree-Go2-robot) — 该项目提供了一个基于ROS 2的低层控制框架，用于在Unitree Go2四足机器人上部署强化学习策略。其核心流程是在MuJoCo仿真环境中训练和验证策略，随后通过切换ROS参数is_simulation即可无缝迁移到真实Go2机器人。该框架面向希望实现Sim2Real迁移的机器人研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Glowing-Torch/Deploy-an-RL-policy-on-the-Unitree-Go2-robot?style=social)

- [go2_odometry](https://github.com/inria-paris-robotics-lab/go2_odometry) — 该项目为Unitree Go2机器人提供简易的状态估计解决方案，主要实现基于传感器数据的里程计功能。通过融合IMU与关节编码器信息，实现低延迟的位姿估计，适用于无外部定位设备的场景。目标用户为需要在Go2上快速部署基础定位能力的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/inria-paris-robotics-lab/go2_odometry?style=social)

- [G1_AMO_control](https://github.com/cyugai/G1_AMO_control) — 该项目实现了基于VR的Unitree G1人形机器人遥操作控制，利用SteamVR和HTC Vive设备捕捉用户动作，并通过ROS 2将关节指令实时传输至G1机器人。核心功能包括全身动捕映射、延迟优化和安全姿态限制，适用于需要直观远程操控G1进行复杂任务的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/cyugai/G1_AMO_control?style=social)

- [IK-humanoid](https://github.com/yediong/IK-humanoid) — 该项目利用逆运动学（IK）求解实现Unitree G1人形机器人的部分手部运动控制，基于unitree-rl-gym和IsaacGym构建仿真环境。通过IK算法驱动G1机械臂与手部关节，支持在高保真仿真中验证灵巧操作策略，适用于希望在G1平台上开发上肢精细动作的机器人研究人员。 ![GitHub stars](https://img.shields.io/github/stars/yediong/IK-humanoid?style=social)

- [g1-isaac-groot-n1](https://github.com/Jalil32/g1-isaac-groot-n1) — 该项目旨在微调并部署 NVIDIA 的 Isaac GR00T N1 模型到 Unitree G1 人形机器人上，实现基于视觉语言模型的具身智能控制。项目利用 Isaac Sim 进行仿真训练，并通过 ROS 2 接口与 G1 硬件集成，支持端到端策略迁移。主要面向希望在 Unitree G1 上探索生成式机器人控制的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/Jalil32/g1-isaac-groot-n1?style=social)

- [Go2_Isaac_ros2](https://github.com/sallu-786/Go2_Isaac_ros2) — 该项目在 NVIDIA Isaac Lab/Isaac Sim 中实现了 Unitree Go2 的仿真环境，并通过 ROS 2 接口支持导航等任务。它集成了 Go2 的 URDF 模型与 Isaac 的物理引擎，提供传感器模拟和控制接口，便于开发和测试基于 ROS 2 的算法。适用于希望在高保真仿真中快速部署和验证 Go2 应用的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/sallu-786/Go2_Isaac_ros2?style=social)

- [himloco_lab](https://github.com/IsaacZH/himloco_lab) — 该项目用于在Isaac Lab环境中训练、导出和部署HimLoco强化学习策略，专为Unitree Go2四足机器人设计。它基于Isaac Lab仿真平台实现端到端的RL训练流程，并支持将训练好的策略部署到真实Go2硬件上，实现了Sim2Real迁移。目标用户为从事四足机器人运动控制研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/IsaacZH/himloco_lab?style=social)

- [unitree-go2-mjx-rl](https://github.com/alexeiplatzer/unitree-go2-mjx-rl) — 该项目利用MuJoCo XLA（MJX）实现针对Unitree Go2四足机器人的强化学习运动控制，专注于高效仿真与策略训练。通过JAX加速的物理仿真，支持在GPU上快速迭代RL策略，并提供与Go2硬件动力学相匹配的环境配置。适合希望在MJX框架下开发Unitree Go2运动技能的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/alexeiplatzer/unitree-go2-mjx-rl?style=social)

- [unitree_g1_python](https://github.com/notdana/unitree_g1_python) — 该项目是对 Unitree SDK2 的 Python 重写与简化，专门适配 Unitree-G1 人形机器人，提供更清晰的接口和实用示例。它移除了原 SDK 中对其他机型的支持，聚焦 G1 的运动控制与状态读取，并包含基础行走、姿态控制等示例代码。目标用户为希望快速上手 G1 开发的 Python 工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/notdana/unitree_g1_python?style=social)

- [Unitree_G1_pose_control-through-UI](https://github.com/hangxu811/Unitree_G1_pose_control-through-UI) — 该项目是一个面向Unitree G1人形机器人的运动设计辅助工具，允许用户在3D界面中直观地创建和调整机器人姿态，并将目标关节角度实时发送至G1的控制面板以实现精确复现。基于Python开发，结合了可视化交互与底层控制接口，适用于需要快速原型姿态调试的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/hangxu811/Unitree_G1_pose_control-through-UI?style=social)

- [unitree_h1_carrybox](https://github.com/Msy-yy/unitree_h1_carrybox) — 该项目基于ROS实现Unitree H1人形机器人的灵巧手操作功能，专注于抓取与搬运箱子任务。通过C++开发，集成了H1的上肢运动控制与手部协调策略，利用ROS通信框架实现感知-规划-执行闭环。适用于需要在H1平台上开发精细操作能力的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Msy-yy/unitree_h1_carrybox?style=social)

- [go2_navigation](https://github.com/MattiaGrigoli/go2_navigation) — 该项目为 Unitree Go2 提供完整的自主导航流水线，集成了 Livox MID360 激光雷达，实现了基于 ROS2 的 SLAM 与路径规划功能。通过适配 Go2 的底层运动控制接口，支持在复杂环境中进行建图与自主移动，主要面向机器人开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/MattiaGrigoli/go2_navigation?style=social)

- [mjlab-homierl](https://github.com/Nagi-ovo/mjlab-homierl) — 该项目是 mjlab 的一个分支，专门支持 Unitree H1 人形机器人和 Robotiq 2F85 夹爪，用于复现 RSS2025 论文《HOMIE》中提出的同构外骨骼遥操作下的全身运动策略训练。基于 MuJoCo 物理引擎实现 **Sim2Real** 兼容的强化学习框架，包含针对 H1 的关节配置、传感器接口和动作空间定义。主要面向研究人形机器人 **Loco-Manipulation** 联合控制的学术开发者。 ![GitHub stars](https://img.shields.io/github/stars/Nagi-ovo/mjlab-homierl?style=social)

- [Go2-EDU-Mycobot-320-M5-Gazebo-Simulation-with-Navigation-and-MoveIt](https://github.com/wxyanxw/Go2-EDU-Mycobot-320-M5-Gazebo-Simulation-with-Navigation-and-MoveIt) — 该项目为Unitree Go2 EDU四足机器人和Mycobot 320 M5机械臂提供基于Gazebo的ROS仿真环境，集成了ROS Navigation Stack实现Go2的自主导航，并通过MoveIt!支持机械臂的运动规划。其核心价值在于为Go2 EDU提供了开箱即用的导航仿真框架，适用于教育和算法验证场景，目标用户为机器人学习者及开发者。 ![GitHub stars](https://img.shields.io/github/stars/wxyanxw/Go2-EDU-Mycobot-320-M5-Gazebo-Simulation-with-Navigation-and-MoveIt?style=social)

- [unitree-g1-bipedal-rl-walk](https://github.com/HusseinLezzaik/unitree-g1-bipedal-rl-walk) — 该项目专注于使用强化学习训练Unitree G1双足机器人在Isaac Gym中实现行走能力，并在MuJoCo中进行评估。它提供了针对G1机器人的专用RL训练环境和策略部署流程，利用Isaac Gym的高效并行仿真能力加速训练，再通过MuJoCo验证Sim2Real迁移效果。适合从事人形机器人运动控制与强化学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/HusseinLezzaik/unitree-g1-bipedal-rl-walk?style=social)

- [unitree_go2w_ros2](https://github.com/Sam-Mag1/unitree_go2w_ros2) — 该项目基于ROS2和Gazebo构建Unitree Go2W的数字孪生仿真环境，提供完整的机器人模型、传感器模拟及控制接口。通过URDF/SDF建模与ROS2节点通信，支持在Gazebo中实现高保真度的动力学仿真，便于开发者在部署前进行算法验证与系统测试。主要面向使用Unitree Go2W并希望利用ROS2生态进行仿真的机器人研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Sam-Mag1/unitree_go2w_ros2?style=social)

- [unitree_g1_optimal_controllers](https://github.com/junhengl/unitree_g1_optimal_controllers) — 该项目基于 Simulink Simscape Multibody 实现了针对 Unitree G1 人形机器人的 SRBM-MPC（简化刚体模型模型预测控制）算法，用于高动态运动控制。项目直接使用 Unitree G1 的官方动力学模型，并通过 MATLAB/Simulink 环境进行仿真验证，支持关节级轨迹优化与实时控制策略开发。主要面向研究 MPC 在人形机器人上应用的学术与工程开发者。 ![GitHub stars](https://img.shields.io/github/stars/junhengl/unitree_g1_optimal_controllers?style=social)

- [go2_pressure_sensor](https://github.com/VincidaB/go2_pressure_sensor) — 该项目为Unitree Go2机器人提供了一个附加的足底压力传感器模块，用于精确检测足部接触状态。通过硬件集成与ROS驱动支持，实现了实时触地感知，适用于需要高精度步态控制或地形适应的研究场景。主要面向Unitree Go2开发者及足式机器人研究者。 ![GitHub stars](https://img.shields.io/github/stars/VincidaB/go2_pressure_sensor?style=social)

- [elder_and_dog](https://github.com/roy4222/elder_and_dog) — 该项目基于 Unitree Go2 机器狗开发了一套居家陪伴与寻物系统，采用 MCP + LLM Agent 架构实现自然语言理解（如“帮我找水”），结合视觉语言模型（VLM Snapshot）进行环境识别与自主避障导航。系统专为老年人设计，旨在缓解物品遗失和情感陪伴缺失问题，直接利用 Go2 的移动底盘与感知能力，目标用户为家庭照护场景中的老年群体及其照护者。 ![GitHub stars](https://img.shields.io/github/stars/roy4222/elder_and_dog?style=social)

- [unitree_mpc](https://github.com/sm-1z/unitree_mpc) — 该项目为Unitree G1人形机器人提供基于OCS2框架的模型预测控制（MPC）实现，主要用于全身运动控制和动态平衡。它利用OCS2（Optimal Control Software Suite）构建了针对G1硬件的动力学模型与优化控制器，并支持与机器人底层驱动的接口集成。适用于希望在G1平台上开发高级运动控制算法的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/sm-1z/unitree_mpc?style=social)

- [g1_locomotion](https://github.com/ioloizou/g1_locomotion) — 该项目为Unitree G1人形机器人提供了一套基于凸模型预测控制（Convex MPC）的全身运动控制框架，专注于实现稳定高效的双足行走。通过优化接触力与质心轨迹，结合G1的硬件特性进行实时控制，适用于需要高动态平衡能力的研究场景。目标用户为从事人形机器人运动控制与MPC算法开发的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/ioloizou/g1_locomotion?style=social)

- [G1_localization](https://github.com/Ericcsr/G1_localization) — 该项目为Unitree G1人形机器人提供定位工具箱，主要实现基于多传感器融合的实时定位功能，支持IMU、关节编码器和可选外部传感器输入。通过C++实现高效状态估计，适用于G1平台的SLAM与导航任务，目标用户为G1开发者及人形机器人定位研究者。 ![GitHub stars](https://img.shields.io/github/stars/Ericcsr/G1_localization?style=social)

- [ros2_go2_video](https://github.com/tfoldi/ros2_go2_video) — 该项目是一个基于Rust编写的ROS 2节点，用于从Unitree Go2机器人实时发布摄像头或视频流数据到ROS 2话题。它直接对接Go2的摄像头硬件接口，利用ROS 2的通信机制实现低延迟图像传输，便于上层感知或导航模块使用。适用于需要在ROS 2生态中集成Go2视觉数据的开发者。 ![GitHub stars](https://img.shields.io/github/stars/tfoldi/ros2_go2_video?style=social)

- [auki_robotics_g1_humanoid_ros2](https://github.com/aukilabs/auki_robotics_g1_humanoid_ros2) — 该项目提供专为Unitree G1人形机器人设计的ROS2功能包，实现与G1硬件的通信接口、状态反馈和控制指令发布。基于Python开发，支持ROS2 Humble/Foxy，封装了底层驱动并提供高层API，便于开发者快速集成感知、规划或控制算法。主要面向使用Unitree G1进行科研或应用开发的ROS2用户。 ![GitHub stars](https://img.shields.io/github/stars/aukilabs/auki_robotics_g1_humanoid_ros2?style=social)

- [unitree-go2-realtime-agent](https://github.com/wso2-incubator/unitree-go2-realtime-agent) — 该项目是一个专为 Unitree Go2 EDU 四足机器人开发的实时 AI 代理，通过集成 OpenAI Realtime API、WSO2 技术栈与 Unitree Go2 SDK，实现语音交互与实时动作控制。其核心功能包括低延迟指令解析、云端 AI 服务对接及机器人运动指令下发，适用于希望在 Go2 平台上构建智能人机交互应用的开发者。 ![GitHub stars](https://img.shields.io/github/stars/wso2-incubator/unitree-go2-realtime-agent?style=social)

- [Aligator_Unitree_G1](https://github.com/Ahmad0Aldaher/Aligator_Unitree_G1) — 该项目利用Aligator轨迹优化库对Unitree G1机器人进行行走行为建模，专注于生成高效、稳定的步态轨迹。通过将G1的运动学与动力学模型集成到Aligator框架中，实现了基于优化的全身运动规划，适用于需要高精度轨迹控制的研究场景。目标用户为从事人形机器人运动规划与控制的科研人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/Ahmad0Aldaher/Aligator_Unitree_G1?style=social)

- [humanoid-motion-planning](https://github.com/ansh1113/humanoid-motion-planning) — 该项目为Unitree G1人形机器人提供全身运动规划解决方案，集成了ZMP预瞄控制、A*步态规划、MPC平衡控制（能耗降低49%）、强化学习步态及雅可比逆运动学操作。基于MuJoCo仿真环境，使用Python实现，面向希望在G1平台上开发高级运动控制算法的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/ansh1113/humanoid-motion-planning?style=social)

- [elevation_mapping_g1](https://github.com/leeyngdo/elevation_mapping_g1) — 该项目在GPU上实现面向Unitree G1人形机器人的高程地图构建，利用CUDA加速点云处理与栅格化，支持实时地形感知。通过ROS 2接口与G1的深度相机和IMU数据集成，为足式机器人提供局部高程图用于步态规划。适用于需要在复杂地形中部署G1的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/leeyngdo/elevation_mapping_g1?style=social)

- [Cerebro-Control](https://github.com/Autodiscovery/Cerebro-Control) — 该项目提供基于VR的遥操作控制方案，专为Unitree H1人形机器人设计，结合其内置的运动模式与强化学习（RL）实现灵活移动。系统通过Python构建，利用VR设备捕捉用户动作并映射到H1的全身控制，同时复用机器人原生的RL行走策略以提升运动稳定性。适用于希望快速部署沉浸式遥操作应用的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/Autodiscovery/Cerebro-Control?style=social)

- [Quadrupeds_Climbing](https://github.com/leo01110111/Quadrupeds_Climbing) — 该项目基于Isaac Lab构建强化学习训练任务，专门用于训练Unitree Go2四足机器人攀爬陡峭地形。通过自定义奖励函数和地形生成器，实现对复杂斜坡环境的适应性控制，支持Sim2Real迁移。主要面向使用Isaac Lab进行四足机器人运动控制研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/leo01110111/Quadrupeds_Climbing?style=social)

- [IsaacLab_Locomotion_H1](https://github.com/NirajPudasaini/IsaacLab_Locomotion_H1) — 该项目基于IsaacLab框架，为Unitree H1人形机器人开发了面向复杂地形的运动控制策略。通过强化学习训练实现**Rough Terrain Locomotion**能力，并利用IsaacLab的物理仿真与GPU加速特性进行高效策略优化。主要面向希望在H1平台上研究高动态运动控制或Sim2Real迁移的科研与工程开发者。 ![GitHub stars](https://img.shields.io/github/stars/NirajPudasaini/IsaacLab_Locomotion_H1?style=social)

- [IsaacLab_Locomotion_H1-2](https://github.com/NirajPudasaini/IsaacLab_Locomotion_H1-2) — 该项目基于IsaacLab框架，为Unitree H1-2人形机器人提供平坦与粗糙地形上的运动控制解决方案。通过强化学习训练策略，实现高动态的全向行走能力，并支持Sim2Real迁移。主要面向使用IsaacLab进行人形机器人运动控制研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/NirajPudasaini/IsaacLab_Locomotion_H1-2?style=social)

- [g1_teleop](https://github.com/SpringLight-Wang/g1_teleop) — 该项目实现了基于任天堂Joy-Con手柄的Unitree G1人形机器人遥操作控制，采用混合控制模式：手臂由Joy-Con操控，行走则通过官方遥控器完成。支持真实硬件部署及MuJoCo仿真环境，利用Python开发，为G1平台提供了直观的双模态远程操控方案，适用于需要精细上肢操作与稳定下肢移动结合的研究或应用开发者。 ![GitHub stars](https://img.shields.io/github/stars/SpringLight-Wang/g1_teleop?style=social)

- [unitree_go2_deploy](https://github.com/UESTC-REVERIE/unitree_go2_deploy) — 该项目提供针对 Unitree Go2 机器人的 Sim2Sim（MuJoCo）与 Sim2Real 部署框架，支持从仿真训练到真实机器人控制的迁移。其核心功能包括基于 MuJoCo 的高保真仿真环境搭建、策略部署接口以及与 Go2 硬件的通信适配，便于研究人员快速验证强化学习或运动控制算法。目标用户为从事四足机器人 Sim2Real 迁移研究的学术团队或开发者。 ![GitHub stars](https://img.shields.io/github/stars/UESTC-REVERIE/unitree_go2_deploy?style=social)

- [Go2_planner_suite](https://github.com/Quadruped-dyn-insp/Go2_planner_suite) — 该项目为Unitree Go2四足机器人提供完整的自主导航栈，集成了远距离路径规划器、Fast-LIO2激光惯性里程计和ROS 2 Humble框架。通过紧耦合的感知与规划模块，实现动态环境下的实时避障与定位，适用于科研与工程开发者在复杂地形中部署Go2机器人。 ![GitHub stars](https://img.shields.io/github/stars/Quadruped-dyn-insp/Go2_planner_suite?style=social)

- [go2-rl-locomotion](https://github.com/jazhanma/go2-rl-locomotion) — 该项目为Unitree Go2四足机器人提供强化学习运动控制框架，支持PPO、SAC等多种算法，并集成课程学习、域随机化和高级奖励塑形技术，基于PyTorch实现，旨在帮助研究人员和开发者训练鲁棒的行走步态。 ![GitHub stars](https://img.shields.io/github/stars/jazhanma/go2-rl-locomotion?style=social)

- [unitree_walking](https://github.com/ashishmiryalkar/unitree_walking) — 该项目利用IsaacLab仿真平台和PPO强化学习算法，实现Unitree G1人形机器人的行走控制。通过NVIDIA Omniverse进行可视化，专注于从仿真到现实（Sim2Real）的策略迁移，为G1提供端到端的运动学习框架。适用于研究人形机器人强化学习与运动控制的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/ashishmiryalkar/unitree_walking?style=social)

- [legged_lab](https://github.com/xliu0105/legged_lab) — 该项目基于IsaacLab框架训练足式机器人，主要实现Unitree A1的跌倒恢复、盲走与连续后空翻，以及Unitree H1的舞蹈动作模仿。通过强化学习和运动重定向技术，在仿真中训练策略并支持Sim2Real迁移，适用于希望在IsaacLab生态下开发Unitree机器人高动态行为的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/xliu0105/legged_lab?style=social)

- [go2-autonomous-patrol](https://github.com/Kodo-Robotics/go2-autonomous-patrol) — 该项目为Unitree Go2四足机器人开发了一套基于ROS 2和Nav2的自主巡检与安防监控系统，集成了路径规划、环境感知与Web控制面板。通过ROS 2与Go2的底层驱动对接，利用Nav2实现室内/室外自主导航，并提供远程可视化操作界面。主要面向安防巡检场景下的开发者与集成商，适用于需要部署Go2进行自动化巡逻的应用。 ![GitHub stars](https://img.shields.io/github/stars/Kodo-Robotics/go2-autonomous-patrol?style=social)

- [Unitree-G1-Sim2Real](https://github.com/S-CHOI-S/Unitree-G1-Sim2Real) — 该项目提供了一个轻量级的 Sim2Real 模板，用于将强化学习策略部署到 Unitree G1 人形机器人上。它集成了 Isaac Gym 仿真环境与 G1 的底层控制接口，支持从仿真训练到真实机器人执行的端到端流程。主要面向希望在 Unitree G1 上快速验证 RL 算法的科研人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/S-CHOI-S/Unitree-G1-Sim2Real?style=social)

- [JeffrinSam_MTS](https://github.com/ISRIndustrial/JeffrinSam_MTS) — 该项目利用Isaac Lab中的模仿学习生成Unitree H1和G1机器人的合成关节数据，通过Isaac Sim进行仿真与可视化，并结合Cosmos增强真实感。生成的数据与遥操作数据融合，用于微调Gr00t N1.5模型以执行抓取放置任务，并在Isaac Sim中完成推理验证。主要面向Unitree双足人形机器人开发者，支持Sim2Real迁移研究。 ![GitHub stars](https://img.shields.io/github/stars/ISRIndustrial/JeffrinSam_MTS?style=social)

- [MPC-h1-Manipulation-task](https://github.com/Yara-NM/MPC-h1-Manipulation-task) — 该项目实现了面向Unitree H1机器人手臂的双层模型预测控制（MPC）系统，包含高层轨迹MPC用于规划末端执行器最优路径，以及底层运动学MPC基于8自由度简化手臂模型计算可行关节运动。代码使用Python编写，专为H1上肢操作任务设计，适用于需要高精度实时操控的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/Yara-NM/MPC-h1-Manipulation-task?style=social)

- [unitree_go2w_ros2](https://github.com/jj7258/unitree_go2w_ros2) — 该项目为Unitree Go2W轮式机器人提供完整的ROS2 Humble工作空间，包含16个电机的控制驱动、URDF模型描述及运动学仿真工具。通过ROS2接口实现对Go2W底层硬件的直接控制，并支持Gazebo等仿真环境中的运动学验证。主要面向基于ROS2开发Unitree Go2W应用的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/jj7258/unitree_go2w_ros2?style=social)

- [unitree-sim2real](https://github.com/shivam-sood00/unitree-sim2real) — 该项目提供了一个从仿真到实物（Sim2Real）的部署流水线，专为 Unitree Go2 机器人设计，支持在 Isaac Gym 中训练策略并迁移至真实硬件。其核心功能包括强化学习策略导出、低延迟控制接口封装及与 Unitree SDK 的集成，便于研究人员快速验证运动控制算法。目标用户为从事四足机器人 Sim2Real 迁移研究的开发者与学术团队。 ![GitHub stars](https://img.shields.io/github/stars/shivam-sood00/unitree-sim2real?style=social)

- [JeffrinSam_G1](https://github.com/JeffrinSam/JeffrinSam_G1) — 该项目利用Isaac Lab中的模仿学习生成Unitree H1/G1机器人的合成关节数据，通过Isaac Sim进行仿真与可视化，并结合Cosmos增强真实感。生成的数据与遥操作数据融合，用于微调Gr00t N1.5模型以执行抓取放置任务，并在Isaac Sim中完成推理验证。主要面向Unitree G1/H1开发者及具身智能研究人员。 ![GitHub stars](https://img.shields.io/github/stars/JeffrinSam/JeffrinSam_G1?style=social)

- [unitree-g1-docker-sdk](https://github.com/Uvesh-patel/unitree-g1-docker-sdk) — 该项目提供了一个开箱即用的 Docker 开发环境，专为 Unitree G1 人形机器人设计，集成了官方 Python SDK、Cyclone DDS 通信中间件及示例代码，支持在 Windows 和 macOS 上快速搭建开发环境。通过容器化封装，简化了依赖配置和跨平台部署流程，特别适合希望快速上手 G1 二次开发的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Uvesh-patel/unitree-g1-docker-sdk?style=social)

- [butler-connect](https://github.com/rise-robotics/butler-connect) — 该项目为Unitree Go2四足机器人提供专业级控制系统的Web界面，支持实时控制、安全监控与远程操作。其核心功能包括基于Python的后端架构、低延迟通信协议及可视化状态反馈，专为需要稳定远程操控Go2机器人的开发者和研究人员设计。 ![GitHub stars](https://img.shields.io/github/stars/rise-robotics/butler-connect?style=social)

- [Unitree_Go2_gallop_Checkpoint](https://github.com/EurekaZang/Unitree_Go2_gallop_Checkpoint) — 该项目提供了一个基于Isaac Lab的Unitree Go2四足机器人疾驰（gallop）运动策略的训练检查点，用于复现或进一步开发高性能运动控制算法。其核心是利用Isaac Lab仿真平台实现**Sim2Real**兼容的强化学习策略，直接适配Unitree Go2的硬件动力学模型。目标用户为从事四足机器人运动控制研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/EurekaZang/Unitree_Go2_gallop_Checkpoint?style=social)

- [isaac-g1-ulc-vlm](https://github.com/mturan33/isaac-g1-ulc-vlm) — 该项目基于Isaac Lab构建，面向Unitree G1人形机器人，结合视觉语言模型（VLM）与强化学习（PPO-PyTorch），实现神经符号AI驱动的高层任务推理与底层运动控制。通过ULC（Unified Language Control）框架，将自然语言指令转化为机器人动作策略，支持Sim2Real迁移。适用于研究VLM与人形机器人集成的学术开发者。 ![GitHub stars](https://img.shields.io/github/stars/mturan33/isaac-g1-ulc-vlm?style=social)

- [g1_spinkick_example](https://github.com/minheinchay/g1_spinkick_example) — 该项目使用 MuJoCo 与 mjlab 框架训练 Unitree G1 人形机器人完成双旋踢动作，提供完整的训练数据、预训练模型及 Sim2Real 部署指南。通过 mujoco-warp 加速仿真，实现从仿真到真实机器人的策略迁移，适用于希望在 G1 平台上开发高动态运动技能的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/minheinchay/g1_spinkick_example?style=social)

- [humanoid-robot-vla-study](https://github.com/Jalil32/humanoid-robot-vla-study) — 该项目研究评估了 NVIDIA Isaac GR00T N1.5 在 Unitree G1 人形机器人硬件上的实际部署性能，揭示了工业界宣传与真实世界表现之间的差距。研究通过真实硬件实验分析了视觉-语言-动作（VLA）模型在复杂任务中的泛化能力与鲁棒性，并提供了与仿真环境的对比数据。目标用户为关注 VLA 模型在 Unitree G1 上 Sim2Real 迁移效果的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/Jalil32/humanoid-robot-vla-study?style=social)

- [sim2real_go2_rl](https://github.com/Bhuvanlakhera23/sim2real_go2_rl) — 该项目提供了一个完整的Sim2Real强化学习部署流程，专为Unitree Go2 Edu四足机器人设计，基于ROS2 Humble、Linux 22.04和Unitree SDK2 Python实现。其核心功能包括在仿真中训练RL策略并通过统一接口部署到真实Go2硬件，支持端到端的策略迁移与执行。目标用户为希望在Unitree Go2上快速验证强化学习算法的机器人研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/Bhuvanlakhera23/sim2real_go2_rl?style=social)

- [unitree-g1-rl](https://github.com/GXMZUAILAB/unitree-g1-rl) — 该项目专注于宇树G1人形机器人的强化学习控制，利用Isaac Gym仿真环境训练全身运动策略，实现了从仿真到真实机器人的迁移。项目提供了针对Unitree-G1定制的RL训练框架和运动技能示例，适用于希望在G1平台上开发高级运动控制算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/GXMZUAILAB/unitree-g1-rl?style=social)

- [unitree-g1-rl-unity](https://github.com/RizziGama/unitree-g1-rl-unity) — 该项目为Unitree G1人形机器人提供基于Unity ML-Agents的强化学习训练框架，支持URDF导入、PPO/SAC算法训练及运动任务实验验证。通过Unity仿真环境实现G1的端到端策略学习，包含完整配置文件与模型检查点，适用于研究人形机器人**Sim2Real**迁移与**Whole-Body Control**的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/RizziGama/unitree-g1-rl-unity?style=social)

- [humanoid_shadow_g1](https://github.com/darth-alexus/humanoid_shadow_g1) — 该项目构建了一个融合 Unitree G1 人形机器人本体与 Shadow 灵巧手的全身体模型，专为高精度灵巧操作任务设计，并作为 MuJoCo Menagerie 的扩展提供开箱即用的仿真支持。通过整合 G1 的全身运动能力与 Shadow 手的精细抓取功能，实现了在 MuJoCo 中的协同控制仿真，适用于需要复杂手-身协调的研究场景。目标用户为从事人形机器人灵巧操作、Sim2Real 迁移及高级运动规划的科研人员。 ![GitHub stars](https://img.shields.io/github/stars/darth-alexus/humanoid_shadow_g1?style=social)

- [FAST-LIVO2](https://github.com/yuzedu/FAST-LIVO2) — 该项目是面向Unitree G1人形机器人的激光-惯性-视觉融合SLAM系统，基于FAST-LIVO2算法实现高精度实时定位与建图。通过适配G1的传感器配置（如Livox激光雷达和IMU），支持在复杂室内外环境中稳定运行，适用于需要高鲁棒性导航能力的G1开发者。 ![GitHub stars](https://img.shields.io/github/stars/yuzedu/FAST-LIVO2?style=social)

- [G1_xr_deployment](https://github.com/ZachJiang/G1_xr_deployment) — 该项目是一个基于VR的遥操作系统，专为Unitree G1人形机器人设计，支持通过Meta Quest设备进行沉浸式远程操控与高质量数据采集。系统利用ROS 2实现低延迟通信，并集成了手柄与头部追踪数据映射到机器人关节控制，适用于需要真实人类操作数据的研究场景。目标用户为从事人形机器人模仿学习或遥操作开发的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/ZachJiang/G1_xr_deployment?style=social)

- [Humanoid-Locomotion-via-primitive-composition](https://github.com/my-rice/Humanoid-Locomotion-via-primitive-composition) — 该项目提出了一种基于强化学习的双足行走控制方法，专门针对Unitree H1人形机器人，通过组合基础运动基元策略实现鲁棒的全身运动控制。其核心技术包括在Isaac Gym仿真环境中训练策略，并采用Sim2Real迁移方法部署到真实H1平台。适用于从事人形机器人强化学习与运动控制研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/my-rice/Humanoid-Locomotion-via-primitive-composition?style=social)

- [unitree-go2](https://github.com/Optimal-Robotics-Lab/unitree-go2) — 该项目提供面向 Unitree Go2 机器人硬件的深度强化学习（DRL）算法实现，直接支持在真实 Go2 平台上部署训练策略。基于 Python 开发，集成了与 Go2 通信所需的底层接口，并可能利用 Isaac Gym 或类似框架进行高效仿真训练。目标用户为希望在 Unitree Go2 上快速验证和部署 DRL 控制策略的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Optimal-Robotics-Lab/unitree-go2?style=social)

- [BOLT](https://github.com/sahillarious/BOLT) — B.O.L.T 是一个面向 Unitree Go2 四足机器人的实时视觉追踪系统，结合自定义 YOLOv8 模型与单目深度估计，在边缘设备上实现低于 50 毫秒延迟的目标检测与跟随。系统通过状态控制器驱动 Go2 完成自主跟踪任务，适用于需要低延迟视觉导航的机器人应用场景。 ![GitHub stars](https://img.shields.io/github/stars/sahillarious/BOLT?style=social)

- [Isaaclab_deploy](https://github.com/SISR-LORIA/Isaaclab_deploy) — 该项目旨在将基于Isaac Lab训练的强化学习策略部署到Unitree Go2机器人上，实现从仿真到真实机器人的迁移。项目利用Isaac Lab作为RL训练平台，并通过ROS 2接口与Go2硬件通信，支持实时控制和状态反馈。主要面向希望在Unitree Go2平台上验证和应用强化学习算法的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/SISR-LORIA/Isaaclab_deploy?style=social)

- [Go2Testing](https://github.com/al-oman/Go2Testing) — 该项目是一个基于IsaacLab的扩展工具，专为Unitree Go2四足机器人的开发与测试而设计。它利用IsaacLab的高性能物理仿真能力，提供针对Go2的环境配置、传感器模拟和控制接口，便于研究人员快速验证运动控制、导航或强化学习算法。目标用户为使用Unitree Go2进行机器人算法开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/al-oman/Go2Testing?style=social)

- [quadruped-locomotion-deploy](https://github.com/illusoryTwin/quadruped-locomotion-deploy) — 该项目提供了一个部署系统，用于在Unitree Go2四足机器人上运行训练好的强化学习（RL）策略。它实现了从仿真到真实机器人的策略迁移，支持实时控制和状态反馈，并集成了Go2的底层驱动接口。主要面向希望将RL算法快速部署到Unitree Go2平台的机器人研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/illusoryTwin/quadruped-locomotion-deploy?style=social)

- [Go2-Locomotion-Hackathon](https://github.com/Algoace1403/Go2-Locomotion-Hackathon) — 该项目专注于Unitree Go2四足机器人的强化学习运动控制，利用Genesis仿真器训练多种步态（如行走、奔跑、转圈和舞蹈）。通过端到端RL策略实现高动态动作，并支持Sim2Real迁移，适用于希望在Go2平台上开发先进运动能力的机器人研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Algoace1403/Go2-Locomotion-Hackathon?style=social)

- [go2-ubuntu22-jetpack6-upgrade](https://github.com/AutoRoverLLC/go2-ubuntu22-jetpack6-upgrade) — 该项目提供将 Unitree Go2 EDU 机器人操作系统从 Ubuntu 20.04 升级至 22.04 并集成 JetPack 6.2.1（L4T R36.4.4）的完整脚本与文档。通过 Shell 脚本自动化系统升级和 NVIDIA Jetson 驱动配置，确保硬件兼容性与 ROS 2 环境支持。主要面向需要在 Go2 上部署最新 AI/ROS 2 应用的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/AutoRoverLLC/go2-ubuntu22-jetpack6-upgrade?style=social)

- [butler-connect](https://github.com/ravz/butler-connect) — 该项目为Unitree Go2四足机器人提供专业控制系统，具备Web界面、安全监控和实时控制功能。通过集成Go2的底层API，实现远程操作与状态可视化，适用于需要高可靠性和易用性的人机交互场景。目标用户为使用Go2进行应用开发或部署的工程师与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/ravz/butler-connect?style=social)

- [LISA-V2](https://github.com/SMART-NYUAD/LISA-V2) — LISA-V2 是一个面向 Unitree Go2W 机器人开发的自主导航框架，集成了大型语言模型（LLM）推理能力，并支持通过共置边缘服务器进行高效计算。该项目基于 Python 实现，利用 Go2W 的移动底盘与感知系统，结合 LLM 实现语义级任务理解与路径规划，适用于需要自然语言交互的室内外巡检或服务场景。目标用户为希望在 Unitree Go2 平台上构建智能人机交互系统的科研人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/SMART-NYUAD/LISA-V2?style=social)

- [GR00T-training-pipeline-for-Unitree-G1](https://github.com/preranajo/GR00T-training-pipeline-for-Unitree-G1) — 该项目旨在为Unitree G1人形机器人定制操作任务，通过构建仿真场景、收集演示数据并微调GR00T N1.5模型，实现从仿真到真实机器人的部署。其核心与Unitree G1深度绑定，专注于端到端策略在该硬件平台上的迁移与执行，关键技术包括行为克隆、Sim2Real以及基于Isaac Gym或类似框架的仿真环境。目标用户为希望在G1上快速部署具身智能策略的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/preranajo/GR00T-training-pipeline-for-Unitree-G1?style=social)

- [motion_tracking_controller](https://github.com/JeanMayoko18/motion_tracking_controller) — 该项目是一个ROS 2 Humble软件包，专为在MuJoCo仿真（基于LeggedGym/unitree_rl_gym）和真实Unitree G1人形机器人上部署强化学习策略而设计。它支持从WandB或本地ONNX文件加载策略，执行实时推理，并通过统一的Sim2Real控制接口发布动作指令。主要面向使用RL进行人形机器人运动控制的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/JeanMayoko18/motion_tracking_controller?style=social)

- [g1](https://github.com/deltartificial/g1) — 该项目利用Genesis框架在Mac M系列芯片上对Unitree G1人形机器人进行运动策略的仿真、训练与部署，专注于强化学习驱动的locomotion控制。其核心特性包括针对G1硬件的专用RL环境、macOS原生支持以及端到端策略迁移能力，适用于希望在Apple Silicon设备上快速开发和测试G1运动算法的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/deltartificial/g1?style=social)

- [g1-motion-control](https://github.com/lez666/g1-motion-control) — 该项目为Unitree G1人形机器人提供面向工程的运动控制与模仿学习流水线，支持指令条件下的爬行行为和全身运动跟踪。其核心基于Python实现，结合强化学习与全身控制策略，旨在提升G1在复杂地形下的运动能力。适用于希望在G1平台上开发高级运动技能的机器人工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/lez666/g1-motion-control?style=social)

- [G1_Userguide_for_lab_of_FSII](https://github.com/yyt-66/G1_Userguide_for_lab_of_FSII) — 该项目是一份面向开发者的 Unitree-G1 机器人开发手册，系统整理了机械结构、操作指南、应用层开发、底层运动控制及高层运动开发等内容，基于官方文档并针对实验室场景进行适配。手册涵盖硬件接口说明与实用示例，帮助开发者快速上手 G1 的全栈开发。目标用户为高校或研究机构中使用 Unitree-G1 进行机器人算法与控制研究的工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/yyt-66/G1_Userguide_for_lab_of_FSII?style=social)

- [unitree-h1-ros-sdk](https://github.com/YasiruDEX/unitree-h1-ros-sdk) — 该项目为Unitree H1人形机器人提供ROS2软件开发工具包，封装底层通信协议并暴露标准化的ROS2接口，便于开发者实现运动控制、状态订阅与指令发布。基于C++实现，支持实时关节控制和传感器数据获取，目标用户为希望在ROS2生态中快速集成H1机器人的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/YasiruDEX/unitree-h1-ros-sdk?style=social)

- [LearningHumanoidWalking_H1](https://github.com/duxr1015/LearningHumanoidWalking_H1) — 该项目利用强化学习训练Unitree H1人形机器人实现行走能力，基于Isaac Gym仿真环境构建运动控制策略，并提供从仿真到真实机器人的迁移方案。项目专注于H1的全身动力学建模与步态生成，适用于希望在Unitree H1平台上开发高级运动控制算法的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/duxr1015/LearningHumanoidWalking_H1?style=social)

- [unitree_h12_sim2sim](https://github.com/correlllab/unitree_h12_sim2sim) — 该项目提供了一个完整的训练与仿真迁移流程，用于在IsaacLab中训练强化学习策略，并将其迁移到MuJoCo环境中进行sim2sim验证。项目专为Unitree-H1-2人形机器人设计，实现了基于PyTorch的策略训练、URDF模型适配及跨仿真平台的动力学一致性处理，目标用户为从事人形机器人强化学习研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/correlllab/unitree_h12_sim2sim?style=social)

- [unitree_g1_vibes](https://github.com/Sentdex/unitree_g1_vibes) — 该项目为 Unitree G1 人形机器人提供基础控制与交互示例，通过 Python 实现对 G1 的运动控制和状态读取。代码利用 Unitree 官方 SDK 与机器人通信，展示了如何发送关节指令并处理传感器反馈。适合希望快速上手 G1 开发的社区用户和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Sentdex/unitree_g1_vibes?style=social)

- [go2_dashboard](https://github.com/bentheperson1/go2_dashboard) — 该项目是一个专为 Unitree Go2 设计的简易 Web 仪表盘，通过 Python 实现对机器人状态的实时可视化监控。它直接与 Go2 的 SDK 或底层接口通信，展示如关节状态、IMU 数据和电池信息等关键指标，适用于开发者和研究人员快速调试与监控机器人运行状态。 ![GitHub stars](https://img.shields.io/github/stars/bentheperson1/go2_dashboard?style=social)

- [AIM-Robotics](https://github.com/AIM-Intelligence/AIM-Robotics) — 该项目为Unitree G1人形机器人提供Python接口和控制工具，支持实时运动控制与传感器数据读取。通过封装底层通信协议，简化了G1的上层应用开发，并包含示例代码展示基本步态和关节控制。主要面向希望快速开发G1应用的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/AIM-Intelligence/AIM-Robotics?style=social)

- [Aliengo_2D_Nav-sim](https://github.com/guru-narayana/Aliengo_2D_Nav-sim) — 该项目实现了在Unitree Aliengo四足机器人上的3D SLAM与2D导航功能，基于ROS框架集成RTAB-Map进行建图，并通过move_base实现路径规划与避障。项目专为Aliengo平台定制了传感器配置和运动控制接口，适用于需要在复杂环境中部署自主导航能力的四足机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/guru-narayana/Aliengo_2D_Nav-sim?style=social)

- [unitree_g1_ros2_demo](https://github.com/FLYivan/unitree_g1_ros2_demo) — 该项目为Unitree G1人形机器人提供ROS 2接口示例，主要用于展示如何通过ROS 2与G1进行通信和控制。项目包含关节状态发布、命令订阅及基本运动控制功能，基于Python实现，适配Unitree官方SDK。适用于希望在ROS 2生态中快速上手G1开发的机器人研究者和工程师。 ![GitHub stars](https://img.shields.io/github/stars/FLYivan/unitree_g1_ros2_demo?style=social)

- [unitree_h1_humanoid-gym](https://github.com/ZhangXG001/unitree_h1_humanoid-gym) — 该项目基于 humanoid-gym 框架实现了对 Unitree H1 人形机器人的仿真控制，提供了与 Isaac Gym 集成的强化学习训练环境。其核心功能包括 H1 机器人的动力学建模、状态观测接口和奖励函数设计，便于研究人员快速开展人形机器人运动策略的 Sim2Real 研究。目标用户为专注于 Unitree H1 平台的强化学习与机器人控制开发者。 ![GitHub stars](https://img.shields.io/github/stars/ZhangXG001/unitree_h1_humanoid-gym?style=social)

- [Unitree-Go2-GestureDetection](https://github.com/lez666/Unitree-Go2-GestureDetection) — 该项目基于 Unitree Go2 的 Python SDK 和 MediaPipe 库，实现了手势识别功能，使 Go2 机器人狗能根据用户手势做出相应动作。通过摄像头实时捕捉手势指令，并映射为预定义的机器人行为，如站立、坐下或移动。适用于希望快速实现人机交互原型的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/lez666/Unitree-Go2-GestureDetection?style=social)

- [The-way-of-redemption-lies-within](https://github.com/sm-1z/The-way-of-redemption-lies-within) — 该项目为Unitree G1人形机器人提供模型预测控制（MPC）实现，旨在提升其全身运动控制性能。项目基于C++开发，利用实时优化算法生成动态步态，并通过Unitree官方SDK与机器人底层通信。适用于希望在G1平台上研究高级运动控制策略的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/sm-1z/The-way-of-redemption-lies-within?style=social)

- [Unitree-G1-Control-Replay](https://github.com/huangshk/Unitree-G1-Control-Replay) — 该项目是一个专为Unitree G1人形机器人设计的控制与动作回放平台，支持通过Python脚本加载和重放运动轨迹数据。其核心功能包括实时关节控制、动作序列录制与回放，并通过Unitree官方SDK实现低层通信。适用于希望快速验证G1机器人运动策略或复现特定动作的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/huangshk/Unitree-G1-Control-Replay?style=social)

- [ark_unitree_g1](https://github.com/Robotics-Ark/ark_unitree_g1) — 该项目实现了 Unitree G1 人形机器人与 Ark 框架的集成，主要用于提供标准化的控制接口和状态反馈。通过 Python 封装底层通信协议，支持实时关节控制与传感器数据读取，并适配 Ark 的模块化机器人开发架构。适用于基于 Unitree G1 进行算法开发或系统集成的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Robotics-Ark/ark_unitree_g1?style=social)

- [unitree-g1-brainco-hand](https://github.com/BrainCoTech/unitree-g1-brainco-hand) — 该项目提供将BrainCo Revo2灵巧手适配到Unitree G1人形机器人上的教程，重点解决手部硬件集成与控制接口对接问题。通过Python实现通信协议转换和动作同步，支持G1上肢运动协调。适用于希望扩展G1操作能力的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/BrainCoTech/unitree-g1-brainco-hand?style=social)

- [isaac-b2-ros2](https://github.com/HuangZihaooo/isaac-b2-ros2) — 该项目基于Isaac Sim和ROS 2 Humble，为Unitree B2机器人提供仿真与控制接口，实现了从仿真环境到真实机器人的通信桥梁。它集成了Unitree B2的URDF模型，并通过ROS 2话题发布关节状态与接收控制指令，支持在Isaac Sim中进行高保真动力学仿真。主要面向希望在ROS 2生态下开发B2应用的科研与工程人员。 ![GitHub stars](https://img.shields.io/github/stars/HuangZihaooo/isaac-b2-ros2?style=social)

- [go2_description](https://github.com/anujjain-dev/go2_description) — 该项目为 Unitree Go2 机器人提供了 ROS 2 Humble 环境下的 URDF 描述模型，专用于与 CHAMP 控制器集成。基于官方 unitree_ros 包构建，支持在 ROS 2 中加载 Go2 的完整运动学与动力学模型。主要面向使用 CHAMP 框架进行四足机器人控制开发的研究者和工程师。 ![GitHub stars](https://img.shields.io/github/stars/anujjain-dev/go2_description?style=social)

- [Unitree-Go2-Mapping-and-Navigation-Using-Intel-RealSense-D435i-and-RTAB-Map](https://github.com/L-winder2002/Unitree-Go2-Mapping-and-Navigation-Using-Intel-RealSense-D435i-and-RTAB-Map) — 该项目为Unitree Go2机器人提供基于Intel RealSense D435i深度相机和RTAB-Map的建图与导航解决方案，通过ROS集成实现室内外环境下的实时SLAM与路径规划。项目利用Go2的移动底盘结合视觉惯性里程计，支持自主探索与避障，适用于希望在Unitree Go2上快速部署低成本视觉导航系统的开发者。 ![GitHub stars](https://img.shields.io/github/stars/L-winder2002/Unitree-Go2-Mapping-and-Navigation-Using-Intel-RealSense-D435i-and-RTAB-Map?style=social)

- [Quadruped-Robot-State-Estimation-Go2-Kinematics-Velocity-Tracking](https://github.com/mehedihasan1909030/Quadruped-Robot-State-Estimation-Go2-Kinematics-Velocity-Tracking) — 该项目实现了面向Unitree Go2四足机器人的实时状态估计算法，利用前向运动学与IMU等板载传感器进行融合，估计机器人位姿与速度。核心采用Python开发，依赖Go2的关节编码器和惯性测量单元数据，通过正运动学模型推算足端位置并结合传感器融合提升估计精度，适用于需要低成本自主导航能力的Go2开发者。 ![GitHub stars](https://img.shields.io/github/stars/mehedihasan1909030/Quadruped-Robot-State-Estimation-Go2-Kinematics-Velocity-Tracking?style=social)

- [Unitree-G1-Mujoco-Playground](https://github.com/Akshit0601/Unitree-G1-Mujoco-Playground) — 该项目为Unitree G1人形机器人提供MuJoCo仿真环境下的开发与测试平台，支持在模拟中实现运动控制、步态规划等基础功能。通过MuJoCo物理引擎构建G1的高保真动力学模型，并封装了与真实硬件一致的关节接口，便于算法快速验证。主要面向希望在安全仿真环境中开发G1控制策略的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Akshit0601/Unitree-G1-Mujoco-Playground?style=social)

- [Go2Bot-OpenAI-Integration](https://github.com/svarshneysjsu/Go2Bot-OpenAI-Integration) — 该项目实现了 Unitree Go2 机器人与 OpenAI 的集成，通过语音指令解析和 AI 驱动的任务执行提升人机交互体验。基于 Python、Flask 和 JavaScript 构建，利用 OpenAI API 实现自然语言理解，并通过 Go2 的 SDK 控制机器人执行动作。适用于希望探索生成式 AI 与四足机器人结合的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/svarshneysjsu/Go2Bot-OpenAI-Integration?style=social)

- [go2-vision-head](https://github.com/mvrius/go2-vision-head) — 该项目为 Unitree Go2 系列（AIR/PRO/EDU）提供基于视觉的头部控制功能，通过摄像头实现环境感知与头部姿态调整。项目利用 ROS 2 架构集成 Go2 的底层控制接口，并结合 OpenCV 进行图像处理，支持实时视觉反馈。适用于希望扩展 Go2 感知能力的机器人开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/mvrius/go2-vision-head?style=social)

- [unitree_deploy](https://github.com/zybz777/unitree_deploy) — 该项目用于部署控制实验室（Ctrl Lab）开发的运动策略到Unitree Go2机器人，主要实现强化学习策略在真实Go2硬件上的部署与执行。项目基于Python编写，提供了与Go2底层通信的接口封装，并支持从仿真到现实（Sim2Real）的策略迁移。目标用户为希望在Unitree Go2上测试或应用先进运动控制算法的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/zybz777/unitree_deploy?style=social)

- [Unitree_G1_Stabilization](https://github.com/Ahmad0Aldaher/Unitree_G1_Stabilization) — 该项目提供了一个基于Pinocchio库的Python脚本，用于实现Unitree G1人形机器人的姿态稳定控制。通过利用G1的URDF模型进行动力学计算，支持实时平衡调整，适用于研究人形机器人全身控制和动态稳定的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Ahmad0Aldaher/Unitree_G1_Stabilization?style=social)

- [g1_description](https://github.com/kyavuzkurt/g1_description) — 该项目是一个ROS2包，提供Unitree G1人形机器人的URDF模型和相关描述文件，便于在ROS2生态中进行仿真与控制开发。它包含G1的完整关节结构、连杆参数及可视化配置，支持与ROS2控制栈集成。主要面向基于Unitree G1开展算法验证或应用开发的机器人研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/kyavuzkurt/g1_description?style=social)

- [go2_ros2_control_sim](https://github.com/illusoryTwin/go2_ros2_control_sim) — 该项目为 Unitree Go2 四足机器人提供了基于 ROS 2 Control 的仿真控制框架，支持经典控制与强化学习（RL）控制策略。通过集成 Gazebo 仿真环境和 ros2_control 接口，实现了对 Go2 关节的低层控制，并兼容 RL 算法部署。主要面向希望在 ROS 2 生态中开发或测试 Go2 控制算法的机器人研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/illusoryTwin/go2_ros2_control_sim?style=social)

- [go2webrtc-rs](https://github.com/tfoldi/go2webrtc-rs) — 该项目是一个用 Rust 编写的 WebRTC 服务器，专为 Unitree Go2 机器人设计，用于实时传输机器人的摄像头视频流和控制信号。它通过 WebRTC 协议实现低延迟通信，并与 Go2 的硬件接口集成，支持远程操控和监控。目标用户是希望在浏览器中直接与 Go2 交互的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/tfoldi/go2webrtc-rs?style=social)

- [Unitree-Go2-EDU-RL-Training-and-Deployment-Tutorial](https://github.com/TheX1an/Unitree-Go2-EDU-RL-Training-and-Deployment-Tutorial) — 该项目提供面向Unitree Go2机器人的强化学习训练与部署教学教程，涵盖从仿真环境搭建到真实机器人部署的完整流程。项目基于Isaac Gym或类似RL框架实现策略训练，并包含Go2专用的运动控制接口适配，适合希望在Unitree Go2平台上开展强化学习研究的教育用户和开发者。 ![GitHub stars](https://img.shields.io/github/stars/TheX1an/Unitree-Go2-EDU-RL-Training-and-Deployment-Tutorial?style=social)

- [unitreeG1_ik](https://github.com/YuehChuan/unitreeG1_ik) — 该项目为Unitree G1人形机器人提供逆运动学（IK）求解功能，基于Python实现，支持实时计算各关节角度以达成末端执行器的目标位姿。代码结构清晰，便于集成到G1的运动控制或任务规划系统中，适合希望快速开发上肢操作或全身协调控制的开发者使用。 ![GitHub stars](https://img.shields.io/github/stars/YuehChuan/unitreeG1_ik?style=social)

- [isaacsim_g1_locomotion](https://github.com/kdh4970/isaacsim_g1_locomotion) — 该项目提供了一个独立的 Isaac Sim 脚本，用于在 NVIDIA Isaac Sim 仿真环境中实现 Unitree G1 人形机器人的运动控制。它直接面向 G1 机器人，利用 Isaac Sim 的物理引擎和传感器模拟功能，支持步态生成与基本运动策略测试。适合希望在高保真仿真中快速验证 G1 控制算法的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/kdh4970/isaacsim_g1_locomotion?style=social)

- [unitree_g1_primitives](https://github.com/lambdavi/unitree_g1_primitives) — 该项目提供了一个易于部署的原始动作库，专为 Unitree G1 人形机器人设计，支持快速实现基础运动控制。通过封装底层关节控制接口，开发者可直接调用行走、站立等基本动作原语，简化了高层行为开发流程。适用于希望在 G1 平台上快速构建复杂行为的机器人研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/lambdavi/unitree_g1_primitives?style=social)

- [unittree-go2-usd](https://github.com/lancerzhang/unittree-go2-usd) — 该项目为Unitree Go2机器人提供NVIDIA Isaac Sim的USD场景文件，便于在Isaac Sim中进行高保真仿真。通过定义Go2的URDF模型与环境资产，支持物理仿真、传感器模拟及强化学习训练等任务。主要面向使用Isaac Sim开发Go2应用的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/lancerzhang/unittree-go2-usd?style=social)

- [OpenGo2Air](https://github.com/Ragtime-LAB/OpenGo2Air) — OpenGo2Air 是一个基于 Unitree Go2 的开源软硬件四足机器人项目，旨在提供可扩展的开发平台。该项目直接复用并改造 Unitree Go2 的机械结构与底层驱动，支持自定义传感器集成和运动控制算法开发，适用于科研与教育场景中的四足机器人研究。 ![GitHub stars](https://img.shields.io/github/stars/Ragtime-LAB/OpenGo2Air?style=social)

- [exploration_go2](https://github.com/gcairone/exploration_go2) — 该项目为Unitree Go2四足机器人开发了一套基于前沿检测的SLAM与自主探索系统，利用ROS2和Nav2框架实现环境建图与路径规划。系统通过集成Go2的传感器数据，在未知环境中进行实时探索，适用于科研与工程开发者开展自主导航研究。 ![GitHub stars](https://img.shields.io/github/stars/gcairone/exploration_go2?style=social)

- [QRC_ARCLAB_Code](https://github.com/Holmes1204/QRC_ARCLAB_Code) — 该项目修改了 Unitree Go2 的官方 SDK，以适配 2024 年 QRC（Quad Robot Challenge）竞赛需求。主要面向 Unitree-Go2 机器人，通过 C++ 实现底层控制接口的定制化调整，支持竞赛场景下的特定运动控制与通信协议。目标用户为参与 QRC2024 的高校或研究团队开发者。 ![GitHub stars](https://img.shields.io/github/stars/Holmes1204/QRC_ARCLAB_Code?style=social)

- [foot_reach](https://github.com/Hymwgk/foot_reach) — 该项目基于IsaacLab实现Unitree Go2的简单足端目标到达任务，用于训练和测试四足机器人足端轨迹控制能力。通过强化学习或运动规划方法，使Go2的单腿足端精确抵达指定空间位置，适用于腿部运动控制研究与开发。主要面向Unitree Go2开发者及四足机器人运动控制研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Hymwgk/foot_reach?style=social)

- [huro](https://github.com/hucebot/huro) — 该项目提供了一个ROS2接口，用于与Unitree机器人进行通信和控制，支持订阅和发布机器人状态、命令等核心话题。其主要面向Unitree系列机器人（如Go2、H1等），通过C++实现低延迟的硬件交互，并兼容ROS2 Humble及更高版本。适合需要在ROS2生态中集成Unitree机器人的开发者使用。 ![GitHub stars](https://img.shields.io/github/stars/hucebot/huro?style=social)

- [go2_rl_gym](https://github.com/wty-yy/go2_rl_gym) — 该项目为基于Unitree Go2四足机器人的强化学习训练环境实现，利用PyTorch和自定义Gym接口构建端到端的RL训练框架。它直接集成Go2的运动控制与状态反馈，支持在仿真中训练策略并部署至真实机器人，适用于希望在Unitree Go2平台上开展强化学习研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/wty-yy/go2_rl_gym?style=social)

- [g1_description](https://github.com/ZiwenZhuang/g1_description) — 该项目提供了一个优化的 Unitree G1 机器人 URDF 描述文件，并集成了 joint state publisher 以在 RViz 中可视化机器人状态。其主要面向 ROS 用户，便于在仿真或实际部署中快速加载和调试 G1 的模型结构与关节状态。项目虽小但实用，适合需要在 ROS 环境中使用 Unitree G1 的开发者。 ![GitHub stars](https://img.shields.io/github/stars/ZiwenZhuang/g1_description?style=social)

- [Unitree-G1-Research](https://github.com/amznhacker/Unitree-G1-Research) — 该项目专注于Unitree G1人形机器人的研究与工程开发，提供Python接口用于控制和算法实验。项目包含针对G1硬件的底层通信封装和运动控制示例，支持通过自定义策略实现步态生成与平衡控制。主要面向机器人学习与人形机器人控制领域的研究人员及开发者。 ![GitHub stars](https://img.shields.io/github/stars/amznhacker/Unitree-G1-Research?style=social)

- [g1_hardware](https://github.com/BrennoDom/g1_hardware) — 该项目为Unitree G1人形机器人的机械臂提供专用硬件接口，基于C++实现低延迟通信与关节控制。它直接对接G1的底层驱动协议，支持实时读取传感器数据和发送运动指令，适用于需要精细操作的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/BrennoDom/g1_hardware?style=social)

- [Voice-Interaction-Control-on-Unitree-G1-Robot-to-realize-FALCON-](https://github.com/lunow0715/Voice-Interaction-Control-on-Unitree-G1-Robot-to-realize-FALCON-) — 该项目在Unitree G1机器人上集成了麦克风、大语言模型（LLM）与FALCON系统，实现语音交互控制。通过C++开发的接口将语音指令转化为机器人动作，支持实时语音识别与语义理解，并与G1的底层运动控制模块对接。主要面向希望为Unitree G1添加自然语言交互能力的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/lunow0715/Voice-Interaction-Control-on-Unitree-G1-Robot-to-realize-FALCON-?style=social)

- [g1_crc](https://github.com/ZiwenZhuang/g1_crc) — 该项目是一个用于通过Python向Unitree G1机器人发送ROS消息的CRC校验模块，主要解决通信过程中的数据完整性验证问题。它实现了与G1底层通信协议兼容的循环冗余校验（CRC）机制，确保控制指令在传输过程中不被篡改或损坏。该工具适用于需要直接与G1进行低层交互的开发者，尤其在自定义控制或调试场景中具有实用价值。 ![GitHub stars](https://img.shields.io/github/stars/ZiwenZhuang/g1_crc?style=social)

- [unitree_h1_learn](https://github.com/Karthus-Chen/unitree_h1_learn) — 该项目基于MuJoCo构建了Unitree H1人形机器人的仿真环境，主要用于遥操作和模仿学习研究。它提供了H1机器人模型的物理仿真接口，并支持通过Jupyter Notebook进行交互式开发与算法验证，适合从事人形机器人行为克隆和远程操控研究的开发者与研究人员使用。 ![GitHub stars](https://img.shields.io/github/stars/Karthus-Chen/unitree_h1_learn?style=social)

- [robot-docker](https://github.com/pengzhenghao/robot-docker) — 该项目提供了一个 Docker 镜像和教程，用于快速搭建 Unitree Go2 四足机器人的开发与运行环境。它封装了必要的依赖项和工具链，简化了在不同系统上部署 Go2 控制代码的流程，特别适合希望避免复杂环境配置的开发者。项目明确面向 Unitree Go2 用户，通过容器化技术提升开发效率。 ![GitHub stars](https://img.shields.io/github/stars/pengzhenghao/robot-docker?style=social)

- [fetch](https://github.com/farazsrahman/fetch) — 该项目为宾夕法尼亚大学MEAM 5170课程项目，针对Unitree Go2开发了一套分层运动规划与强化学习全身控制器系统。其核心结合了基于模型的高层轨迹规划与底层RL策略，旨在实现复杂地形下的动态移动和任务执行。项目虽规模较小，但明确聚焦Go2平台，适合对分层控制与Sim2Real迁移感兴趣的学术研究者。 ![GitHub stars](https://img.shields.io/github/stars/farazsrahman/fetch?style=social)

- [go2_description](https://github.com/Unitree-Go2-Robot/go2_description) — 该项目为 Unitree Go2 机器人提供 URDF/SDF 模型描述文件，用于仿真环境中的机器人建模与可视化。作为 Go2 机器人在 Gazebo、Isaac Gym 等平台进行运动控制、SLAM 或强化学习研究的基础依赖，其核心价值在于准确表征 Go2 的连杆结构、关节参数和惯性属性。主要面向需要在仿真中复现或开发 Go2 相关算法的科研与工程用户。 ![GitHub stars](https://img.shields.io/github/stars/Unitree-Go2-Robot/go2_description?style=social)

- [scene_descriptor_unitree](https://github.com/h-naderi/scene_descriptor_unitree) — 该项目将轻量级视觉语言模型（VLM）集成到Unitree Go2机器人上，实现实时场景描述并通过本地网页展示。系统利用Go2的摄像头采集图像，结合VLM进行语义理解与文本生成，为用户提供环境感知能力。主要面向希望在Unitree Go2上快速部署AI感知功能的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/h-naderi/scene_descriptor_unitree?style=social)

- [LIOrf_ros2_G1](https://github.com/wkooks/LIOrf_ros2_G1) — 该项目是专为Unitree G1机器人开发的LIOrf（Lidar-Inertial Odometry with online extrinsic refinement）ROS 2软件包，用于实现高精度的激光雷达-惯性里程计。它集成了在线外参标定功能，适配G1的传感器配置，并基于C++实现，支持实时状态估计。主要面向使用Unitree G1进行SLAM或导航研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/wkooks/LIOrf_ros2_G1?style=social)

- [ark_unitree_go2](https://github.com/Robotics-Ark/ark_unitree_go2) — 该项目为 Unitree Go2 提供了 Robotics Ark 框架下的实现，主要用途是简化该四足机器人的控制与算法部署。它通过 Python 接口封装底层通信，支持实时状态读取与指令发送，并集成 Ark 的模块化机器人开发范式。目标用户为希望在 Go2 上快速验证运动控制或感知算法的开发者。 ![GitHub stars](https://img.shields.io/github/stars/Robotics-Ark/ark_unitree_go2?style=social)

- [go2_mjlab](https://github.com/Kaweees/go2_mjlab) — 该项目为 Unitree Go2 机器人提供了一个基于 MuJoCo 的外部仿真环境（MjLab），用于开发和测试运动控制算法。它通过自定义 XML 模型和 Python 接口实现对 Go2 的动力学仿真，支持与真实硬件行为对齐的 **Sim2Real** 研究。主要面向希望在轻量级、高效率仿真中快速迭代控制策略的机器人研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/Kaweees/go2_mjlab?style=social)

- [go2_slam_nav2](https://github.com/Jumbo213/go2_slam_nav2) — 该项目为 Unitree Go2 机器人提供原生的 2D SLAM 与 Nav2 导航功能，基于 ROS 2 实现，利用 Go2 的传感器数据进行建图与路径规划。项目集成了 Nav2 导航栈，并适配了 Go2 的底盘控制接口，支持实时定位与自主导航。主要面向希望在 Go2 上快速部署 SLAM 和导航能力的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/Jumbo213/go2_slam_nav2?style=social)

- [go2_webrtc_connect](https://github.com/phospho-app/go2_webrtc_connect) — 该项目是一个基于Python的WebRTC驱动程序，专为Unitree Go2机器人设计，用于实现低延迟的远程视频流和控制通信。它利用WebRTC协议建立浏览器与Go2之间的实时连接，支持通过网络直接访问机器人的摄像头和控制接口。目标用户是需要远程操作或监控Go2机器人的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/phospho-app/go2_webrtc_connect?style=social)

- [Go2VisionCtrl](https://github.com/Baituhao/Go2VisionCtrl) — 该项目基于ROS 2 Humble构建，结合YOLOv8目标检测与键盘遥控，实现对Unitree Go2机器人的视觉伺服控制。系统通过实时视频流识别目标，并融合人工指令与自主决策，支持C++和Python混合开发。主要面向希望在Go2平台上快速部署视觉感知与基础自主行为的开发者。 ![GitHub stars](https://img.shields.io/github/stars/Baituhao/Go2VisionCtrl?style=social)

- [ROAS6000H](https://github.com/the-masses/ROAS6000H) — 该项目是香港科技大学（广州）ROAS6000H课程的作业，实现了针对Unitree H1人形机器人的动作重定向（Retargeting）功能。项目利用动捕数据或预定义动作序列，通过逆运动学将人体动作映射到H1机器人上，并在仿真环境中验证可行性。主要面向学习人形机器人控制与仿真的学生和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/the-masses/ROAS6000H?style=social)

- [unitreeb2_ws](https://github.com/Aditya-Bhargava-2000/unitreeb2_ws) — 该项目在MuJoCo中实现了Unitree B2机器人的仿真环境，并集成了ROS2 effort控制器以实现关节力矩控制。通过自定义URDF模型和ROS2控制栈，支持对B2进行运动控制算法的开发与测试。主要面向希望在MuJoCo仿真中快速验证控制策略的Unitree B2开发者。 ![GitHub stars](https://img.shields.io/github/stars/Aditya-Bhargava-2000/unitreeb2_ws?style=social)

- [ManiSkill-UnitreeGo2](https://github.com/haosulab/ManiSkill-UnitreeGo2) — 该项目旨在将 Unitree Go2 机器人集成到 ManiSkill 强化学习仿真平台中，提供针对 Go2 的专用仿真环境与接口。通过基于 Isaac Gym 或 MuJoCo 的底层支持，实现高保真动力学模拟和强化学习训练流程，便于研究人员快速开发和验证四足机器人控制策略。目标用户为从事 Unitree Go2 强化学习与 Sim2Real 迁移研究的学术与工程团队。 ![GitHub stars](https://img.shields.io/github/stars/haosulab/ManiSkill-UnitreeGo2?style=social)

- [go2-quadruped-sim](https://github.com/AOShei/go2-quadruped-sim) — 该项目是一个完整的 ROS 2 Jazzy 仿真包，专为 Unitree Go2 四足机器人开发，提供开箱即用的 Gazebo/ROS 2 集成环境。它基于 C++ 实现了机器人模型、传感器模拟和基本控制接口，支持在仿真中复现 Go2 的运动与感知能力。目标用户为希望在 ROS 2 生态中快速开展 Go2 算法开发与测试的机器人研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/AOShei/go2-quadruped-sim?style=social)

- [go2_demo_kit](https://github.com/TechShare-inc/go2_demo_kit) — 该项目是一个面向Unitree Go2机器人的二次开发演示套件，主要提供Python接口用于控制Go2的基本运动和传感器数据读取。它封装了底层通信协议，支持通过Wi-Fi或USB连接机器人，并包含示例脚本实现如站立、行走、姿态控制等基础功能。目标用户为希望快速上手Go2机器人进行应用开发的工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/TechShare-inc/go2_demo_kit?style=social)

- [Go2-ROS2-LiDAR-Control](https://github.com/gomous/Go2-ROS2-LiDAR-Control) — 该项目为Unitree Go2机器人提供基于ROS 2的激光雷达控制接口，实现了LiDAR数据采集与运动控制的集成。通过C++开发，支持实时环境感知与导航功能，适用于需要在Go2平台上进行SLAM或自主导航研究的开发者。项目明确面向Unitree-Go2硬件，具备清晰的ROS 2节点架构和传感器驱动集成。 ![GitHub stars](https://img.shields.io/github/stars/gomous/Go2-ROS2-LiDAR-Control?style=social)

- [isaacsim5.0_ros2_go2](https://github.com/tosemfdk/isaacsim5.0_ros2_go2) — 该项目旨在通过 ROS 2 框架在 Isaac Sim 5.0 仿真环境中实现对 Unitree Go2 四足机器人的完整控制。其核心功能包括机器人模型导入、传感器模拟与实时控制接口，利用 Isaac Sim 的物理引擎和 ROS 2 的通信机制构建高保真仿真环境。该仓库为希望在 Isaac Sim 中开发或测试 Go2 控制算法的研究者和工程师提供了基础工具链。 ![GitHub stars](https://img.shields.io/github/stars/tosemfdk/isaacsim5.0_ros2_go2?style=social)

- [robocasa_g1](https://github.com/hogunkee/robocasa_g1) — 该项目为 robocasa 框架新增对 Unitree G1 人形机器人的支持，使其可在模拟环境中执行操作任务。通过集成 G1 的 URDF 模型与关节配置，项目实现了与 robocasa 任务流水线的兼容，便于在 Isaac Gym 或 MuJoCo 等仿真器中开展灵巧操作研究。主要面向希望在 Unitree G1 平台上开发或迁移操作技能的机器人学习研究者。 ![GitHub stars](https://img.shields.io/github/stars/hogunkee/robocasa_g1?style=social)

- [g1-rl](https://github.com/bugzhao/g1-rl) — 该项目为Unitree G1人形机器人构建了初始强化学习（RL）训练流程，基于Isaac Gym仿真环境实现运动控制策略的端到端训练。其核心功能包括G1的URDF模型集成、自定义奖励函数设计以及从仿真到实体机器人的策略迁移支持，旨在为研究人员和开发者提供可扩展的RL基线框架。 ![GitHub stars](https://img.shields.io/github/stars/bugzhao/g1-rl?style=social)

- [g1_teleop](https://github.com/nischayhegde/g1_teleop) — 该项目利用 Intel RealSense 深度相机实现对 Unitree G1 Edu 机器人上半身的实时遥操作，通过视觉捕捉用户姿态并映射到机器人关节空间。项目基于 Python 开发，直接面向 G1 的上肢控制接口，适用于人机协作与远程操作研究场景。 ![GitHub stars](https://img.shields.io/github/stars/nischayhegde/g1_teleop?style=social)

- [h1_unitree_arms_controller](https://github.com/Yara-NM/h1_unitree_arms_controller) — 该项目为Unitree H1机器人双臂提供高低层级控制器，支持双臂协同操作。通过Python实现，集成了针对H1机械臂的运动控制接口，适用于需要精细操作的任务。主要面向Unitree H1开发者及研究人员，便于快速部署双臂控制策略。 ![GitHub stars](https://img.shields.io/github/stars/Yara-NM/h1_unitree_arms_controller?style=social)

- [ManiSkill-UnitreeH1](https://github.com/haosulab/ManiSkill-UnitreeH1) — 该项目为 Unitree H1 人形机器人提供基于 ManiSkill 的强化学习仿真环境，支持在 Isaac Gym 或 MuJoCo 中进行灵巧操作任务的训练与 Sim2Real 迁移。通过集成 Unitree 官方 SDK 和物理精确模型，便于研究人员开发和测试人形机器人的操作策略。主要面向机器人学习领域的学术研究者。 ![GitHub stars](https://img.shields.io/github/stars/haosulab/ManiSkill-UnitreeH1?style=social)

- [FAST_LIO_HUMANOID_H1_2_DOCKER](https://github.com/JensenLav/FAST_LIO_HUMANOID_H1_2_DOCKER) — 该项目是一个专为Unitree H1-2人形机器人优化的轻量级激光雷达-惯性里程计（LIO）系统，基于FAST-LIO算法并封装于Docker容器中，便于部署与环境隔离。它利用C++实现高效计算，支持H1-2的传感器配置，适用于需要高鲁棒性定位的室内外导航场景。目标用户为使用Unitree H1-2进行SLAM或自主导航开发的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/JensenLav/FAST_LIO_HUMANOID_H1_2_DOCKER?style=social)

- [Unitree_H1_Webots](https://github.com/yihuling/Unitree_H1_Webots) — 该项目在Webots仿真环境中实现Unitree H1人形机器人的强化学习训练，提供完整的仿真模型与训练框架。通过集成RL算法与Webots物理引擎，支持对H1的运动控制策略进行端到端学习，适用于希望在开源仿真平台中开发和测试人形机器人控制策略的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/yihuling/Unitree_H1_Webots?style=social)

- [unitreego2-time_sync_scripts](https://github.com/vreacode/unitreego2-time_sync_scripts) — 该项目提供了一组 Shell 脚本，用于自动同步宇树 Unitree-Go2 机器人内置系统的时间，解决因设备长时间运行或网络隔离导致的系统时钟漂移问题。脚本通过 NTP 或本地时间源实现高精度时间对齐，适用于需要多传感器时间戳一致性的开发与部署场景。目标用户为使用 Unitree-Go2 进行科研或工程开发的开发者。 ![GitHub stars](https://img.shields.io/github/stars/vreacode/unitreego2-time_sync_scripts?style=social)

- [unitree-go2w-autonomous-carrier](https://github.com/tzf230201/unitree-go2w-autonomous-carrier) — 该项目展示了日本Moonshot计划中基于Unitree Go2-W机器人平台的自主运输载具原型，集成了ROS 2导航栈与自定义路径规划模块，用于室内外物流场景。项目通过Go2-W的高机动性和负载能力实现物品运送，并利用其官方API进行底层运动控制。主要面向参与前沿机器人应用研究的学术与工程团队。 ![GitHub stars](https://img.shields.io/github/stars/tzf230201/unitree-go2w-autonomous-carrier?style=social)

- [go2_gazebo_sim](https://github.com/OpenMind/go2_gazebo_sim) — 该项目为 Unitree Go2 提供基于 Gazebo 的仿真环境，支持建图与导航功能。通过 ROS 2 接口集成 Go2 的运动控制与传感器模型，便于在仿真中开发和测试自主导航算法。主要面向希望在 Gazebo 中快速部署 Go2 仿真的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/OpenMind/go2_gazebo_sim?style=social)

- [go2_minimal_ros2](https://github.com/artificiell/go2_minimal_ros2) — 该项目为 Unitree Go2 机器人提供了一个轻量级的 ROS 2 接口封装，通过 Python 实现基本的控制与状态订阅功能。它直接对接 Go2 的底层通信协议，暴露关节状态、IMU 数据等话题，并支持发送运动指令，便于在 ROS 2 生态中快速集成和开发。适用于希望在 ROS 2 框架下进行 Go2 二次开发的机器人研究者或工程师。 ![GitHub stars](https://img.shields.io/github/stars/artificiell/go2_minimal_ros2?style=social)

- [Go2-Simple-Example](https://github.com/Sichen345/Go2-Simple-Example) — 该项目提供了一个在Raisim仿真环境中控制Unitree Go2机器人运动的简易C++示例，展示了如何加载Go2模型、配置关节控制器并实现基本步态。代码结构清晰，适合初学者快速上手Raisim与Go2的集成开发，目标用户为希望在高保真物理仿真中测试Go2控制算法的研究者或工程师。 ![GitHub stars](https://img.shields.io/github/stars/Sichen345/Go2-Simple-Example?style=social)

- [unitree-go2-sdk](https://github.com/HowestAILab/unitree-go2-sdk) — 该项目是Howest AI Lab开发的Python SDK，用于直接控制Unitree Go2机器狗，提供高层API封装以简化运动控制和传感器数据访问。它通过自定义通信协议与Go2交互，并支持WebRTC实现远程实时操控，适用于希望快速开发Go2应用的科研与教育用户。 ![GitHub stars](https://img.shields.io/github/stars/HowestAILab/unitree-go2-sdk?style=social)

- [SATA-Velocity-Estimator](https://github.com/qiwanggoing/SATA-Velocity-Estimator) — 该项目实现了基于LSTM的强化学习策略部署，用于Unitree Go2机器人的速度估计与控制。通过端到端RL策略结合LSTM网络，提升机器人在无外部传感器情况下的本体速度感知能力，适用于需要低延迟状态估计的自主导航任务。目标用户为从事Unitree Go2运动控制与Sim2Real迁移研究的开发者。 ![GitHub stars](https://img.shields.io/github/stars/qiwanggoing/SATA-Velocity-Estimator?style=social)

- [unitree_interface](https://github.com/KumarRobotics/unitree_interface) — 该项目为 Unitree Go2-W 提供 C++ 接口，用于低层运动控制与状态读取，支持实时通信和硬件指令发送。通过封装 Unitree 官方 SDK，简化了对 Go2-W 机器人的关节控制、IMU 数据获取等操作，适用于需要直接与 Go2-W 硬件交互的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/KumarRobotics/unitree_interface?style=social)

- [go2_description](https://github.com/PetriJF/go2_description) — 该项目为 Unitree Go2 提供 ROS2 兼容的机器人描述包，包含 URDF 模型和必要的配置文件，便于在 ROS2 生态中进行仿真与控制开发。其核心功能是将 Go2 的机械结构以标准格式封装，支持 RViz 可视化及 Gazebo 仿真集成。适用于基于 ROS2 开发 Unitree Go2 应用的机器人工程师与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/PetriJF/go2_description?style=social)

- [quadruped-pend-gym](https://github.com/pulak-gautam/quadruped-pend-gym) — 该项目提供了一个Gymnasium强化学习环境，用于在Unitree Go2四足机器人上实现倒立摆平衡控制。通过PyBullet仿真平台构建Go2与倒立摆的物理模型，支持基于RL的策略训练，并设计了与真实Go2硬件兼容的接口结构。主要面向研究四足机器人动态平衡与复合任务控制的强化学习开发者。 ![GitHub stars](https://img.shields.io/github/stars/pulak-gautam/quadruped-pend-gym?style=social)

- [Leggedgym_go2](https://github.com/my-zzy/Leggedgym_go2) — 该项目基于legged_gym框架，专门用于训练Unitree Go2四足机器人，采用带约束的PPO强化学习算法实现运动控制。通过Isaac Gym仿真平台进行高效并行训练，并针对Go2的动力学特性优化了奖励函数与状态空间设计。适用于希望在仿真中快速开发和验证Go2运动策略的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/my-zzy/Leggedgym_go2?style=social)

- [Go2-WebRTC-Joystick-Control](https://github.com/Corey-Harding/Go2-WebRTC-Joystick-Control) — 该项目提供基于 WebRTC 的游戏手柄控制方案，用于远程操控 Unitree Go2 机器人。它依赖 Legion1581 的 Go2_WebRTC_Connect 驱动，通过 Python 实现低延迟的实时指令传输，支持标准游戏手柄输入映射到机器人运动控制。主要面向希望快速实现远程遥操作的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Corey-Harding/Go2-WebRTC-Joystick-Control?style=social)

- [find_my_human_go2](https://github.com/arpa-byte/find_my_human_go2) — 该项目利用 Realsense 深度相机在 Unitree Go2 Edu 机器人上实现人体跟踪与识别功能，通过 Python 实现基于深度图像的人体检测与身份匹配，并控制 Go2 跟随目标。项目直接面向 Unitree Go2 硬件平台，使用其 SDK 进行运动控制，适用于教育和人机交互场景的开发者。 ![GitHub stars](https://img.shields.io/github/stars/arpa-byte/find_my_human_go2?style=social)

- [IsaacLabExtensionGo2](https://github.com/al-oman/IsaacLabExtensionGo2) — 该项目旨在通过扩展IsaacLab框架，实现针对Unitree Go2的自定义强化学习算法。它提供了与IsaacLab深度集成的接口，便于在仿真环境中开发和测试RL策略，并支持将训练模型迁移到真实Go2机器人上。主要面向希望在Unitree Go2平台上探索强化学习控制的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/al-oman/IsaacLabExtensionGo2?style=social)

- [go2_edu_sim](https://github.com/ardrababu-uwr/go2_edu_sim) — 该项目为 Unitree Go2 EDU 机器人提供基于 ROS 2 Jazzy 和 Ubuntu 24.04 的完整仿真环境，包含 URDF 模型、Gazebo 配置及 RViz 可视化文件，支持快速启动和开发测试。其核心功能是通过标准 ROS 2 工具链实现对 Go2 EDU 的高保真模拟，便于算法验证与教学实验。目标用户为使用 Unitree Go2 EDU 进行教育或研究的开发者与学生。 ![GitHub stars](https://img.shields.io/github/stars/ardrababu-uwr/go2_edu_sim?style=social)

- [go2_teleop](https://github.com/ardrababu-uwr/go2_teleop) — 该项目为 Unitree Go2 Edu 开发了一个基于 RViz 的遥操作节点，仅依赖传感器反馈和 TF 坐标变换实现无直视条件下的远程导航控制。系统完全运行在 ROS 2 框架下，利用 C++ 实现与 Go2 的底层通信，适用于研究或教育场景中模拟真实遥操作任务。目标用户为使用 Go2 进行机器人感知与控制开发的研究者和工程师。 ![GitHub stars](https://img.shields.io/github/stars/ardrababu-uwr/go2_teleop?style=social)

- [unitreeG1Install](https://github.com/TravisLRyan/unitreeG1Install) — 该项目提供了一个 Shell 脚本，用于自动化配置开发环境以支持 Unitree G1 人形机器人的开发工作。脚本主要处理依赖安装、ROS 环境设置及与 Unitree 官方 SDK 的集成准备，显著简化了新用户在 Ubuntu 系统上的初始配置流程。目标用户为希望快速上手 Unitree G1 机器人开发的工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/TravisLRyan/unitreeG1Install?style=social)

- [ManiSkill-UnitreeG1](https://github.com/haosulab/ManiSkill-UnitreeG1) — 该项目为 Unitree G1 人形机器人提供基于 ManiSkill 的强化学习仿真环境，支持在 Isaac Lab 中进行灵巧操作任务的训练与 Sim2Real 迁移。通过定义 G1 的关节控制接口和任务场景，便于研究人员快速开发和验证 RL 算法。主要面向机器人学习领域的学术开发者。 ![GitHub stars](https://img.shields.io/github/stars/haosulab/ManiSkill-UnitreeG1?style=social)

- [g1_opensot](https://github.com/itsikelis/g1_opensot) — 该项目是一个ROS1软件包，旨在将OpenSoT框架集成到Unitree G1人形机器人上，用于实现**全身运动控制**与**任务优先级调度**。通过Python接口封装OpenSoT的任务栈求解器，并适配G1的关节配置与传感器反馈，支持在真实硬件或仿真环境中部署复杂行为。主要面向研究**人形机器人动态控制**的学术与工程开发者。 ![GitHub stars](https://img.shields.io/github/stars/itsikelis/g1_opensot?style=social)

- [MR-NAMO-3D-Sim](https://github.com/JoanMarie4/MR-NAMO-3D-Sim) — 该项目实现了MR-NAMO算法的3D版本，专门用于Unitree G1人形机器人在复杂环境中的导航与操作任务。通过Python构建，利用G1的运动学与感知能力，在仿真环境中验证多机器人协同导航与物体操作策略。适用于研究人形机器人高级任务规划的学术团队。 ![GitHub stars](https://img.shields.io/github/stars/JoanMarie4/MR-NAMO-3D-Sim?style=social)

- [g1_chest_plate_compact_external_pc](https://github.com/junhengl/g1_chest_plate_compact_external_pc) — 该项目提供了一种3D打印的紧凑型胸板支架，专为Unitree G1人形机器人设计，用于安装外部迷你PC、激光雷达或摄像头等设备。其结构轻巧且适配G1胸部接口，便于扩展感知与计算模块，适合需要在G1平台上进行自主导航或视觉任务开发的用户。 ![GitHub stars](https://img.shields.io/github/stars/junhengl/g1_chest_plate_compact_external_pc?style=social)

- [G1-Software](https://github.com/LIRA-UNAM/G1-Software) — 该项目为双足机器人 Unitree G1 提供专用控制软件，基于 C++ 实现底层运动控制与状态管理，明确面向 G1 机器人硬件平台进行开发。项目包含针对 G1 的驱动接口和运动策略模块，适用于希望在该人形机器人上部署自定义算法的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/LIRA-UNAM/G1-Software?style=social)

- [unitree_g1_c](https://github.com/notdana/unitree_g1_c) — 该项目是对 Unitree 官方 SDK2 的 C++ 修改版本，专为 G1 机器人（23 自由度）定制，提供了底层通信接口和运动控制支持。通过适配 G1 的硬件特性，使开发者能直接在 C++ 环境中实现低延迟控制，适用于需要高性能实时控制的科研与工程场景。 ![GitHub stars](https://img.shields.io/github/stars/notdana/unitree_g1_c?style=social)

- [xDeploy_SimRealToolBox](https://github.com/usfinea/xDeploy_SimRealToolBox) — 该项目提供了一套标准化的部署代码框架，用于在Unitree G1机器人上实现Sim2Real迁移，支持在MuJoCo仿真环境与真实硬件之间无缝切换。其核心特性包括统一的接口设计、硬件抽象层以及针对G1的运动控制适配，便于研究人员快速验证算法从仿真到现实的迁移效果。目标用户为从事Unitree G1机器人Sim2Real研究的开发者与学术团队。 ![GitHub stars](https://img.shields.io/github/stars/usfinea/xDeploy_SimRealToolBox?style=social)

- [joystick_nav](https://github.com/Hive-Robots/joystick_nav) — 该项目是一个ROS2软件包，用于通过手柄对Unitree G1机器人实现带碰撞避障的远程控制。它集成了G1的运动接口与传感器数据，利用Python实现实时障碍检测与遥控指令融合，适用于需要安全远程操作G1的研究或应用场景。 ![GitHub stars](https://img.shields.io/github/stars/Hive-Robots/joystick_nav?style=social)

- [g1_picknplace](https://github.com/tmcarn/g1_picknplace) — 该项目为Unitree G1人形机器人开发了基于强化学习（RL）与模型预测控制（MPC）的多手抓取与放置控制器，专注于实现双手协同操作任务。项目利用Python实现，结合RL训练策略与MPC进行实时轨迹优化，直接面向G1的上肢运动控制。适用于研究人形机器人灵巧操作的开发者与学术团队。 ![GitHub stars](https://img.shields.io/github/stars/tmcarn/g1_picknplace?style=social)

- [Teleoperation_HumanoidRobot](https://github.com/Hugojair18/Teleoperation_HumanoidRobot) — 该项目提供了一个基于Web的遥操作界面，专为Unitree G1人形机器人设计，通过ESP32微控制器采集人体动作数据，并利用实时Web通信（如WebSocket）将控制指令低延迟传输至机器人。系统采用C++实现底层通信与控制逻辑，支持远程操控G1完成基本运动任务，适用于需要直观人机交互的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Hugojair18/Teleoperation_HumanoidRobot?style=social)

- [Robot_Biped](https://github.com/voideryu/Robot_Biped) — 该项目基于 Unitree G1 的源代码，实现了一个仅使用机器人下肢的高层行走控制器，并在 Gazebo 仿真环境中进行了验证。其核心功能是通过简化控制策略提升双足行走的稳定性，适用于希望在 G1 平台上开发或测试新型步态算法的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/voideryu/Robot_Biped?style=social)

- [unitree_h1_teleoperation_ws](https://github.com/cyberbanana777/unitree_h1_teleoperation_ws) — 该项目提供了一套ROS2软件包，用于通过主从式遥操作设备实现对Unitree H1人形机器人的实时远程控制。其核心功能包括运动指令映射、关节状态同步和低延迟通信，基于Python开发并依赖ROS2框架进行数据传输与控制。主要面向希望快速部署H1遥操作系统的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/cyberbanana777/unitree_h1_teleoperation_ws?style=social)

- [Teleoperation_for_Unitree_H1](https://github.com/cyberbanana777/Teleoperation_for_Unitree_H1) — 该项目提供了一套基于ROS2的Python工具包，用于实现对Unitree H1人形机器人的遥操作控制。其核心功能包括实时动作捕捉数据接收、关节指令映射与低延迟通信，直接面向Unitree H1硬件接口进行适配。目标用户为希望快速部署H1遥操作系统的机器人开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/cyberbanana777/Teleoperation_for_Unitree_H1?style=social)

- [Isaac-UnitreeH1-walk_run](https://github.com/wge2002/Isaac-UnitreeH1-walk_run) — 该项目基于 Isaac Gym 构建 Unitree H1 人形机器人的行走与奔跑仿真环境，实现了强化学习训练框架，支持从仿真到真实机器人的策略迁移。项目针对 Unitree H1 的动力学特性进行建模，集成了关节控制与运动策略网络，适用于机器人强化学习研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/wge2002/Isaac-UnitreeH1-walk_run?style=social)

- [unitree_h12_rma_book](https://github.com/NirajPudasaini/unitree_h12_rma_book) — 该项目为书籍章节配套代码，实现基于**RMA**（Robust Model-based Adaptation）算法的Unitree H1-2双足机器人运动控制。代码使用Python编写，聚焦于提升H1-2在复杂地形下的**动态行走稳定性**与**Sim2Real迁移能力**，适用于研究仿人机器人强化学习与自适应控制的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/NirajPudasaini/unitree_h12_rma_book?style=social)

- [h1_optical_flow](https://github.com/firegrock/h1_optical_flow) — 该项目是一个ROS2软件包，专为Unitree H1机器人设计，结合Intel RealSense相机实现光流估计与视觉运动感知。通过订阅RealSense的深度与RGB数据，计算稠密光流向量并发布为ROS2话题，可用于H1的动态环境导航或运动控制。目标用户为基于H1平台开发视觉感知功能的机器人研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/firegrock/h1_optical_flow?style=social)

- [h12_exts](https://github.com/Matero952/h12_exts) — 该项目为Unitree H1-2人形机器人提供完整的ROS2仿真扩展，专用于NVIDIA Isaac Sim环境，支持Correll实验室的全栈开发需求。通过集成Isaac Sim的物理引擎与ROS2通信框架，实现高保真机器人行为模拟，适用于需要在仿真中测试控制算法或感知系统的开发者。 ![GitHub stars](https://img.shields.io/github/stars/Matero952/h12_exts?style=social)

- [unitreego2_ros2](https://github.com/Naka-taiga/unitreego2_ros2) — 该项目为Unitree Go2机器人提供ROS 2接口支持，主要功能是实现对Go2底层硬件的控制与状态读取。通过C++编写，封装了官方SDK，使开发者能在ROS 2生态中直接调用Go2的运动控制、IMU数据和关节状态等核心功能。适用于希望在ROS 2框架下快速开发Go2应用的机器人研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/Naka-taiga/unitreego2_ros2?style=social)

- [TFG-UnitreeGO2](https://github.com/Agebelda/TFG-UnitreeGO2) — 该项目实现了一个基于VR的Unitree GO2机器人遥操作系统，允许用户通过虚拟现实设备远程控制机器狗。系统使用Python开发，集成了Unitree官方SDK以实现低延迟运动指令传输，并结合SteamVR构建沉浸式操控界面。主要面向高校学生和研究人员，用于探索人机交互与远程机器人操作的应用场景。 ![GitHub stars](https://img.shields.io/github/stars/Agebelda/TFG-UnitreeGO2?style=social)

- [unitree-go2_lab-code](https://github.com/labicon/unitree-go2_lab-code) — 该项目为内部实验代码库，旨在支持在 Unitree Go2 机器人上开展各类研究与开发工作。其核心功能包括底层硬件接口封装、运动控制基础模块及实验脚本管理，使用 C 语言实现以确保实时性。项目直接面向 Go2 平台，适用于需要深度访问机器人底层能力的科研团队或开发者。 ![GitHub stars](https://img.shields.io/github/stars/labicon/unitree-go2_lab-code?style=social)

- [quadruped_locomotion_UnitreeGo2_RL](https://github.com/saifahmadgit/quadruped_locomotion_UnitreeGo2_RL) — 该项目基于Genesis框架，专注于为Unitree Go2四足机器人训练强化学习（RL）策略，旨在实现从仿真到现实（Sim2Real）的迁移。通过修改底层控制策略和环境配置，适配Go2的动力学特性，并在Isaac Gym等仿真平台中进行训练。目标用户为希望在Unitree Go2上部署高效运动控制策略的机器人学习研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/saifahmadgit/quadruped_locomotion_UnitreeGo2_RL?style=social)

- [I3T_CPSL_UnitreeGo2_Codebase](https://github.com/FishDentistry/I3T_CPSL_UnitreeGo2_Codebase) — 该项目提供了一套完整的配置流程和代码库，用于在Unitree Go2 EDU机器人上部署基础ROS2功能，包括驱动节点、状态发布器和控制接口。其核心是通过ROS2 Humble实现与Go2硬件的通信，并封装了官方API以简化开发。目标用户为希望基于ROS2快速开展Go2教育或研究的开发者。 ![GitHub stars](https://img.shields.io/github/stars/FishDentistry/I3T_CPSL_UnitreeGo2_Codebase?style=social)

- [I3T_UnitreeGo2_AR_ROS_Comm](https://github.com/FishDentistry/I3T_UnitreeGo2_AR_ROS_Comm) — 该项目提供了一套ROS2软件包，用于Unitree Go2 EDU机器人与AR头显设备通过后端服务器进行通信。其核心功能包括在ROS2环境中桥接Go2的传感器和控制数据与AR应用，支持实时状态可视化与远程交互，关键技术基于Python实现的WebSocket或RESTful接口。适用于希望将增强现实技术集成到Unitree Go2教育平台的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/FishDentistry/I3T_UnitreeGo2_AR_ROS_Comm?style=social)

- [modulr-unitree-go2](https://github.com/ModulrCloud/modulr-unitree-go2) — 该项目为 Unitree Go2 机器人提供额外的 C++ 代码，用于集成 Modulr Agent，实现云端智能体与机器人的协同控制。通过直接适配 Go2 的底层接口，支持在机器人端运行 Modulr 提供的决策或通信模块，属于面向特定硬件的专用扩展。主要面向希望将 Unitree Go2 接入 Modulr 云平台的开发者。 ![GitHub stars](https://img.shields.io/github/stars/ModulrCloud/modulr-unitree-go2?style=social)

- [Unitree_Go2_Edu](https://github.com/RB0609/Unitree_Go2_Edu) — 该项目实现了基于Nav2导航栈的Unitree-Go2-Edu机器人室内自主导航功能，通过集成ROS 2与Nav2框架，为Go2 Edu提供SLAM建图、路径规划与避障能力。项目明确面向Unitree Go2教育版硬件，适配其传感器与运动接口，目标用户为使用Go2进行移动机器人教学或研究的开发者。 ![GitHub stars](https://img.shields.io/github/stars/RB0609/Unitree_Go2_Edu?style=social)

- [Unitree-Go2-IMU-Subscriber](https://github.com/Hachimi-Manbo/Unitree-Go2-IMU-Subscriber) — 该项目提供了一个基于 Unitree C++ SDK 的订阅器，用于实时获取 Unitree Go2 机器人 IMU 传感器数据。通过直接调用官方 SDK 接口，实现低延迟、高频率的 IMU 数据读取，适用于需要精确姿态估计或状态反馈的控制与感知任务。目标用户为使用 Go2 进行底层开发或算法验证的机器人工程师。 ![GitHub stars](https://img.shields.io/github/stars/Hachimi-Manbo/Unitree-Go2-IMU-Subscriber?style=social)

- [hunter_unitree_ros2](https://github.com/kaylorchen/hunter_unitree_ros2) — 该项目是一个基于C++开发的Unitree GO2机器人ROS 2驱动程序，旨在为GO2提供底层硬件接口与ROS 2生态的集成能力。它通过订阅和发布ROS 2话题实现对机器人运动控制、状态反馈等核心功能的支持，便于开发者在ROS 2框架下快速构建上层应用。目标用户为使用Unitree GO2并希望接入ROS 2系统的机器人研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/kaylorchen/hunter_unitree_ros2?style=social)

- [unitree_go2_python](https://github.com/notdana/unitree_go2_python) — 该项目是对 Unitree SDK2 的 Python 修改版本，专为 Go2 Edu 机器人定制，提供更便捷的 Python 接口以实现低层运动控制和状态读取。它简化了原 C++ SDK 的使用门槛，支持实时指令发送与传感器数据订阅，适用于希望在 Go2 Edu 上快速开发控制算法或教育应用的开发者。 ![GitHub stars](https://img.shields.io/github/stars/notdana/unitree_go2_python?style=social)

- [go2_sim2real](https://github.com/sschott20/go2_sim2real) — 该项目旨在将仿真环境中训练的模型部署到 Unitree Go2 机器人上，实现 Sim2Real 迁移。其核心工作包括构建适用于 Go2 的仿真环境，并通过策略迁移技术使学习策略在真实硬件上有效运行，涉及 Isaac Gym 或类似仿真平台的使用。目标用户为从事四足机器人强化学习与 Sim2Real 研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/sschott20/go2_sim2real?style=social)

- [unitree_go2_c](https://github.com/notdana/unitree_go2_c) — 该项目是对 Unitree SDK2 的 C 语言修改版本，专为 Go2 Edu 机器人定制，旨在提供更适配教育场景的底层控制接口。它保留了原 SDK 的核心通信协议，并针对 Go2 的硬件特性进行了简化和优化，便于开发者快速实现运动控制与传感器数据读取。适合希望在 Go2 Edu 上进行嵌入式开发或教学实验的用户。 ![GitHub stars](https://img.shields.io/github/stars/notdana/unitree_go2_c?style=social)

- [unitree_go2_sim](https://github.com/RainbowI314/unitree_go2_sim) — 该项目为宇树Unitree Go2四足机器人提供仿真环境，基于PyBullet构建动力学模型并复现其运动控制逻辑。项目包含Go2的URDF模型、关节控制器及基础步态示例，支持在无真实硬件条件下进行算法开发与测试。适用于希望快速上手Unitree Go2仿真的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/RainbowI314/unitree_go2_sim?style=social)

- [Go2_mujoco](https://github.com/siddarth09/Go2_mujoco) — 该项目实现了 Unitree Go2 机器人在 MuJoCo 仿真环境中的 ROS2 接口，支持通过 ROS2 控制和感知 Go2 的仿真模型。其核心功能包括机器人状态发布、关节命令订阅以及与真实硬件一致的传感器模拟，便于开发者在仿真中测试控制算法后再部署到实体机器人。目标用户为基于 ROS2 开发 Go2 应用的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/siddarth09/Go2_mujoco?style=social)

- [dog_ws](https://github.com/Lanceward410/dog_ws) — 该项目提供 Unitree GO2 EDU 机器人的仿真环境配置，基于 ROS2 和 Gazebo 构建，包含机器人模型、控制器及基础运动示例。通过集成 Unitree 官方 SDK 接口，支持在仿真中复现真实硬件行为，便于开发者进行算法验证与教学实验。主要面向使用 GO2 EDU 平台的教育和研究用户。 ![GitHub stars](https://img.shields.io/github/stars/Lanceward410/dog_ws?style=social)

- [go2-docker-env](https://github.com/gretab5802/go2-docker-env) — 该项目提供在 Ubuntu 20.04 中配置 Docker 容器并远程连接 Unitree Go2 机器人的详细步骤，旨在简化开发环境搭建。通过容器化方式隔离依赖，支持通过网络与真实 Go2 机器人通信，适用于需要快速部署且避免本地环境冲突的开发者。主要面向希望在标准化环境中进行 Go2 应用开发或测试的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/gretab5802/go2-docker-env?style=social)

- [go2_description](https://github.com/HuntersRobotics/go2_description) — 该项目为 Unitree Go2 机器人提供 ROS2 兼容的 URDF 描述文件，包含完整的关节、连杆和传感器定义，便于在 ROS2 生态中进行仿真与控制开发。其核心功能是为 Go2 提供标准化的机器人模型描述，支持 Gazebo 和 RViz 等工具链集成。适用于基于 ROS2 开发 Unitree Go2 应用的机器人工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/HuntersRobotics/go2_description?style=social)

- [Go2OccMapAbstractionROS2ws](https://github.com/DavidBatty95/Go2OccMapAbstractionROS2ws) — 该项目是一个专为 Unitree Go2 构建的 ROS2 工作空间，集成了辐射感知型占据地图抽象框架，用于在未知环境中进行自主探索与实机测试。其核心功能包括基于传感器数据构建语义占据地图、融合辐射信息以指导路径规划，并通过 ROS2 与 Go2 的底层控制接口通信。该仓库面向需要在真实场景中部署环境探索算法的机器人研究人员。 ![GitHub stars](https://img.shields.io/github/stars/DavidBatty95/Go2OccMapAbstractionROS2ws?style=social)

- [go2_rma](https://github.com/TheTensorGeek/go2_rma) — 该项目在Unitree Go2机器人上实现了RMA（Rapid Motor Adaptation）算法，用于提升四足机器人在未知地形中的自适应行走能力。通过在线系统辨识与策略调整，使Go2能够实时适应地面变化，主要基于PyTorch和Isaac Gym仿真环境进行训练，并提供Sim2Real迁移支持。适用于希望在Unitree Go2平台上研究或部署自适应运动控制的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/TheTensorGeek/go2_rma?style=social)

- [quadpedal_contact](https://github.com/KeitoKobayashi/quadpedal_contact) — 该项目为Unitree Go2四足机器人集成了接触传感器功能，通过Python实现对足端接触状态的检测与处理，支持实时反馈控制。项目利用Go2的底层API获取力/力矩数据，并结合自定义接触逻辑提升运动稳定性，适用于需要精确足地交互感知的研究与开发场景。 ![GitHub stars](https://img.shields.io/github/stars/KeitoKobayashi/quadpedal_contact?style=social)

- [biscuit-movements-unitree-go2](https://github.com/NayiemW/biscuit-movements-unitree-go2) — 该项目提供了一个基于 SportClient 的 Unitree Go2 速度控制解决方案，通过 Python 实现了对机器人运动的程序化控制。它直接调用 Unitree 官方 SDK 接口，支持实时发送速度指令以驱动 Go2 机器人，适用于需要快速原型开发或远程控制的场景。目标用户为希望在 Go2 上实现自定义运动逻辑的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/NayiemW/biscuit-movements-unitree-go2?style=social)

- [unitree-go2-webapp](https://github.com/martintricaud/unitree-go2-webapp) — 该项目是一个基于 Svelte 构建的 Web 应用程序，提供图形用户界面（GUI）用于远程控制 Unitree Go2 机器人。它通过 WebSocket 或 REST API 与机器人底层通信，支持实时状态监控和运动指令下发，适用于希望快速部署轻量级远程操控界面的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/martintricaud/unitree-go2-webapp?style=social)

- [Go2-Software](https://github.com/LIRA-UNAM/Go2-Software) — 该项目为四足机器人 Unitree Go2 提供专用控制软件，基于 C++ 实现底层运动控制与传感器集成，明确面向 Go2 硬件平台开发。代码结构针对 Unitree Go2 的驱动接口和通信协议进行适配，支持实时状态反馈与指令下发。主要面向希望在 Go2 上部署自定义算法或扩展功能的机器人研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/LIRA-UNAM/Go2-Software?style=social)

- [go2_rl_agents](https://github.com/felipemohr/go2_rl_agents) — 该项目为Unitree Go2机器人开发强化学习智能体，旨在通过端到端策略实现四足机器人的运动控制与自主导航。项目基于Isaac Gym或类似GPU加速仿真平台构建训练环境，并利用PyTorch实现策略网络，支持从仿真到真实机器人的迁移（Sim2Real）。主要面向从事四足机器人强化学习研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/felipemohr/go2_rl_agents?style=social)

- [Mujoco_quad](https://github.com/Deshad/Mujoco_quad) — 该项目在MuJoCo中实现了Unitree Go2四足机器人的仿真环境，提供了机器人模型、基本运动控制示例及传感器模拟。通过Python接口与MuJoCo交互，支持对Go2的动力学和步态进行研究与开发。主要面向希望在高保真物理引擎中测试控制算法的机器人研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/Deshad/Mujoco_quad?style=social)

- [unitree_go2_example](https://github.com/RPL-CS-UCL/unitree_go2_example) — 该项目为 Unitree Go2 机器人提供 C++ 示例代码，展示如何通过官方 SDK 实现基本控制与传感器数据读取。项目直接面向 Go2 平台，包含底层通信接口和运动控制逻辑，适用于希望快速上手 Unitree Go2 开发的科研与工程人员。 ![GitHub stars](https://img.shields.io/github/stars/RPL-CS-UCL/unitree_go2_example?style=social)

- [argo](https://github.com/Unitree-Go2-HMI/argo) — 该项目为Unitree GO2机器人提供导航栈与人机接口桥接功能，实现了基于Python的高层导航控制和交互界面集成。通过ROS 2框架连接GO2底层驱动与上层规划算法，支持路径规划、避障及状态监控等核心导航能力，适用于需要快速部署自主导航功能的GO2开发者。 ![GitHub stars](https://img.shields.io/github/stars/Unitree-Go2-HMI/argo?style=social)

- [unitree_go2w_ws](https://github.com/keeperlibofan/unitree_go2w_ws) — 该项目为宇树Unitree Go2W机器人提供ROS 2开发环境支持，包含底层驱动、状态接口和控制指令封装，便于开发者在ROS 2生态中集成与扩展Go2W的功能。项目基于C++实现，适配Go2W硬件通信协议，目标用户为希望在ROS 2框架下进行二次开发的机器人工程师。 ![GitHub stars](https://img.shields.io/github/stars/keeperlibofan/unitree_go2w_ws?style=social)

- [go2tools](https://github.com/juhasch/go2tools) — 该项目提供面向 Unitree Go2 机器人的一系列 Python 示例与简易应用程序，涵盖基础运动控制、传感器数据读取及遥控操作等核心功能。通过调用官方 SDK 接口，实现了对 Go2 的实时指令发送与状态反馈，适合开发者快速上手和原型验证。目标用户为希望在 Go2 平台上进行应用开发或算法测试的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/juhasch/go2tools?style=social)

- [unitree_go2w_slam_tutorials](https://github.com/bysanhz/unitree_go2w_slam_tutorials) — 该项目基于 Unitree Go2 机器人平台，提供结合 Fast-LIO 与导航系统的 SLAM 教程，旨在帮助开发者实现激光雷达与 IMU 融合的实时定位建图。项目通过 ROS 2 构建，集成了 Fast-LIO2 算法，并适配 Go2 的传感器配置，支持在真实硬件上运行。主要面向希望在 Unitree Go2 上快速部署 SLAM 与自主导航功能的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/bysanhz/unitree_go2w_slam_tutorials?style=social)

- [go2_ros2_sdk](https://github.com/KongPedia/go2_ros2_sdk) — 该项目为Unitree Go2系列（AIR/PRO/EDU）提供非官方的ROS 2 SDK支持，主要功能包括机器人状态读取、运动控制指令发布及传感器数据订阅。通过Python接口封装底层通信协议，便于开发者在ROS 2生态中快速集成Go2机器人。适用于希望在ROS 2框架下进行算法开发或应用部署的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/KongPedia/go2_ros2_sdk?style=social)

- [go2-sr-ppo-dl](https://github.com/henilveira/go2-sr-ppo-dl) — 该项目复现了伊斯坦布尔技术大学的四足机器人自扶正模型，使用PPO强化学习算法在MuJoCo仿真环境中针对Unitree Go2进行训练。项目聚焦于通过深度强化学习实现Unitree Go2在跌倒后的自主恢复能力，采用Python实现并与MuJoCo物理引擎集成。主要面向从事四足机器人强化学习与运动控制研究的学术人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/henilveira/go2-sr-ppo-dl?style=social)

- [walk-these-ways-go2-tripod](https://github.com/LisaCoiffard/walk-these-ways-go2-tripod) — 该项目将“Walk These Ways”项目中的三足步态（tripod gait）应用于Unitree Go2机器人，旨在实现稳定高效的仿生行走控制。通过适配Go2的硬件接口与运动学特性，项目展示了如何在真实四足平台上部署受昆虫启发的步态策略。主要面向Unitree Go2开发者及仿生运动控制研究者。 ![GitHub stars](https://img.shields.io/github/stars/LisaCoiffard/walk-these-ways-go2-tripod?style=social)

- [go2_you_can_move](https://github.com/arpa-byte/go2_you_can_move) — 该项目专注于 Unitree Go2 Edu 机器人的遥操作与运动控制，提供基于 C++ 的底层运动指令接口和实时操控功能。通过直接调用 Go2 的 SDK 实现步态切换、速度控制和姿态调整等核心操作，适用于需要低延迟响应的远程操控场景。目标用户为希望在 Go2 平台上开发自定义遥操作或运动策略的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/arpa-byte/go2_you_can_move?style=social)

- [go_2_pro_teleoperation](https://github.com/Us3r369/go_2_pro_teleoperation) — 该项目旨在通过 Meta Quest XR 头显实现对 Unitree Go2 Pro 机器人的远程遥操作，利用 XR 设备的头部与手部追踪能力实时控制机器人运动。项目直接面向 Unitree Go2 Pro 硬件，通过自定义通信接口将 XR 输入映射为机器人关节指令，适用于需要沉浸式人机交互的远程操控场景。目标用户为 Unitree Go2 开发者及 XR 遥操作研究者。 ![GitHub stars](https://img.shields.io/github/stars/Us3r369/go_2_pro_teleoperation?style=social)

- [go2_bringup](https://github.com/Unitree-Go2-Robot/go2_bringup) — 该项目为 Unitree Go2 机器人提供基础启动配置和 ROS 2 集成框架，包含硬件驱动加载、传感器初始化及基本控制接口。作为官方风格的 bringup 包，它简化了 Go2 在 ROS 2 环境下的部署流程，支持实时状态监控与底层通信。主要面向使用 ROS 2 开发 Go2 应用的机器人工程师。 ![GitHub stars](https://img.shields.io/github/stars/Unitree-Go2-Robot/go2_bringup?style=social)

- [go2_simulation](https://github.com/Unitree-Go2-Robot/go2_simulation) — 该项目为 Unitree Go2 机器人提供专用仿真环境，支持在 Isaac Gym 或 MuJoCo 等平台中进行运动控制、强化学习或 Sim2Real 算法开发。通过与 Go2 硬件接口对齐的 URDF/SDF 模型和传感器配置，便于开发者在部署前验证算法。主要面向 Unitree Go2 用户及仿生机器人研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Unitree-Go2-Robot/go2_simulation?style=social)

- [go2-odd-observer](https://github.com/danmartinez78/go2-odd-observer) — 该项目是一个基于智能体的工具包，用于将全局ODD（运行设计域）与Unitree Go2 Pro在真实和仿真环境中的实际运行条件进行对比分析。它通过Python实现，支持对Go2 Pro的操作状态进行监控与评估，适用于自动驾驶或自主机器人系统安全验证场景。目标用户为关注Unitree Go2操作安全性与合规性的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/danmartinez78/go2-odd-observer?style=social)

- [Go2-Walking-Unitree](https://github.com/bhenriquezsoto/Go2-Walking-Unitree) — 该项目基于 unitree_ros2 开发了一个 ROS 2 控制器包，用于部署在 MuJoCo 中训练的行走策略到 Unitree Go2 机器人，实现了从仿真到现实（Sim2Real）的迁移。其核心功能包括与 Go2 的底层通信、策略推理接口及实时控制指令发布，主要面向希望在真实 Go2 平台上验证强化学习策略的机器人研究人员。 ![GitHub stars](https://img.shields.io/github/stars/bhenriquezsoto/Go2-Walking-Unitree?style=social)

- [go2_Chavez](https://github.com/EDCHC1234/go2_Chavez) — 该项目实现了面向Unitree Go2四足机器人的全局轨迹规划系统，集成了SLAM环境建图、全局路径规划及RViz可视化功能。通过ROS框架在仿真环境中运行，利用Python开发了完整的导航栈组件，专为Go2机器人定制适配。主要面向希望在Unitree Go2平台上研究或部署自主导航能力的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/EDCHC1234/go2_Chavez?style=social)

- [UnitreeG1_Remote_VR](https://github.com/nkawa/UnitreeG1_Remote_VR) — 该项目提供基于VR的远程控制方案，专为Unitree G1人形机器人设计，利用JavaScript实现与机器人API的实时通信。通过虚拟现实界面，用户可直观操控G1完成全身运动，适用于遥操作研究与远程人机交互开发。目标用户为从事Unitree G1远程控制或VR集成的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/nkawa/UnitreeG1_Remote_VR?style=social)

- [UnitreeG1_MQTT_Control](https://github.com/nkawa/UnitreeG1_MQTT_Control) — 该项目提供通过MQTT协议远程控制Unitree G1人形机器人的能力，利用Python实现与机器人底层通信的桥接，支持订阅/发布控制指令和状态反馈。其核心在于将Unitree G1的运动控制接口封装为MQTT消息格式，便于集成到物联网或远程操作架构中。适用于需要轻量级、网络化控制G1机器人的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/nkawa/UnitreeG1_MQTT_Control?style=social)

- [UnitreeG1ROS2](https://github.com/BrennoDom/UnitreeG1ROS2) — 该项目为 Unitree G1 人形机器人提供 ROS2 接口支持，实现关节控制、状态反馈和传感器数据发布等核心功能。通过 ROS2 的实时通信机制与 G1 的底层驱动对接，便于开发者构建上层应用如运动规划或感知系统。主要面向基于 ROS2 生态开发 Unitree G1 应用的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/BrennoDom/UnitreeG1ROS2?style=social)

- [Ros2_UnitreeG1_kinematics](https://github.com/Isphyra/Ros2_UnitreeG1_kinematics) — 该项目为 Unitree G1 人形机器人提供 ROS2 接口下的运动学计算功能，支持正向与逆向运动学求解，并集成于 ROS2 控制框架中。其核心目标是简化 G1 机器人的关节控制与轨迹规划开发流程，适用于基于 ROS2 的人形机器人研究与应用开发者。 ![GitHub stars](https://img.shields.io/github/stars/Isphyra/Ros2_UnitreeG1_kinematics?style=social)

- [unitree_g1_learning](https://github.com/Longxiaoze/unitree_g1_learning) — 该项目是深蓝学院人形机器人课程的配套代码库，专注于Unitree G1人形机器人的基础学习与开发。内容涵盖G1的运动控制、传感器使用及基础行为编程，基于官方SDK和ROS接口实现。适合刚接触Unitree G1的开发者和课程学员系统性入门。 ![GitHub stars](https://img.shields.io/github/stars/Longxiaoze/unitree_g1_learning?style=social)

- [unitree_g1_demo1](https://github.com/JianchuPan/unitree_g1_demo1) — 该项目为 Unitree G1 人形机器人的基础演示代码，展示了如何通过官方 SDK 控制 G1 执行基本动作。项目包含关节控制、姿态初始化等核心功能，基于 C++ 实现并与 Unitree 提供的底层驱动直接交互。适用于希望快速上手 G1 机器人开发的工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/JianchuPan/unitree_g1_demo1?style=social)

- [unitree-g1-navigation](https://github.com/Aseke314/unitree-g1-navigation) — 该项目为Unitree G1人形机器人提供基于强化学习的自主导航功能，在MuJoCo仿真环境中利用虚拟激光雷达实现避障与路径规划。通过训练RL策略使G1具备在复杂环境中自主移动的能力，主要面向希望在仿真中开发或测试人形机器人导航算法的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/Aseke314/unitree-g1-navigation?style=social)

- [MuJoCo-Sim-for-Unitree-G1-Test](https://github.com/Isphyra/MuJoCo-Sim-for-Unitree-G1-Test) — 该项目为Unitree G1人形机器人提供基于MuJoCo的仿真测试环境，支持在模拟中验证控制算法和运动策略。通过构建G1的物理模型与传感器接口，便于开发者进行**Sim2Real**迁移研究。主要面向机器人学习与控制领域的研究人员及工程师。 ![GitHub stars](https://img.shields.io/github/stars/Isphyra/MuJoCo-Sim-for-Unitree-G1-Test?style=social)

- [humanoid](https://github.com/ryan-wlr/humanoid) — 该项目在Isaac Sim中实现了Unitree G1人形机器人的仿真环境，通过VS Code与Copilot辅助开发，展示了G1抓取桌面上苹果的交互任务。项目利用NVIDIA Isaac Sim的物理引擎和机器人仿真能力，结合Python脚本控制G1的**全身运动规划**与**末端执行器操作**，为开发者提供了一个基于Copilot增强的G1快速原型开发范例。主要面向希望在高保真仿真中测试Unitree G1操作能力的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/ryan-wlr/humanoid?style=social)

- [unitree_preset](https://github.com/JohnFox1199/unitree_preset) — 该项目为 Unitree G1 人形机器人提供预装的框架和脚本，简化开发环境搭建。包含针对 G1 的底层控制接口、运动控制示例及依赖库配置，基于 C++ 实现，便于开发者快速部署算法或应用。主要面向 Unitree G1 用户和研究人员，提升开箱即用体验。 ![GitHub stars](https://img.shields.io/github/stars/JohnFox1199/unitree_preset?style=social)

- [g1_doors](https://github.com/kushal-a/g1_doors) — 该项目旨在训练强化学习（RL）策略，使Unitree G1人形机器人能够执行开门任务。项目基于Python实现，利用仿真环境训练策略，并专注于G1的上肢操作能力与全身协调控制，目标用户为从事人形机器人操作技能开发的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/kushal-a/g1_doors?style=social)

- [g1_ws](https://github.com/trcp/g1_ws) — 该项目为 Unitree G1 人形机器人提供专用的 ROS2 开发工作空间，包含硬件驱动、控制接口及示例节点，便于开发者快速部署运动控制与感知算法。项目基于 C++ 实现，集成 Unitree 官方 SDK，支持实时通信与底层关节控制。主要面向 G1 机器人开发者及研究人员，用于二次开发与算法验证。 ![GitHub stars](https://img.shields.io/github/stars/trcp/g1_ws?style=social)

- [g1-humanoid-robot-terminal-based-motions](https://github.com/abdullah-m-elnahrawy/g1-humanoid-robot-terminal-based-motions) — 该项目为 Unitree G1 人形机器人提供基于终端的运动控制功能，通过菜单式界面执行 YAML 文件定义的动作序列。其核心是利用 C++ 实现与 G1 机器人底层通信，支持用户在无图形界面环境下便捷地加载和运行预设动作。适用于需要快速部署或调试 G1 动作序列的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/abdullah-m-elnahrawy/g1-humanoid-robot-terminal-based-motions?style=social)

- [unitree-g1-nextjs-example](https://github.com/TSUSAKA-ucl/unitree-g1-nextjs-example) — 该项目是一个基于 Next.js 的前端示例，展示如何使用 robot-loader 和 ik-cd-worker 库加载并可视化 Unitree G1 人形机器人的3D模型及执行逆运动学计算。它通过 Web 技术实现机器人状态的交互式展示，适用于希望在网页端快速集成 G1 可视化与基础运动控制的开发者。 ![GitHub stars](https://img.shields.io/github/stars/TSUSAKA-ucl/unitree-g1-nextjs-example?style=social)

- [unitree_g1_ros2_dev](https://github.com/sangheonEN/unitree_g1_ros2_dev) — 该项目为Unitree G1人形机器人开发了基于MoveIt的运动规划功能和基于Nav2的导航功能，利用ROS 2框架实现上层任务控制。项目明确面向Unitree-G1硬件平台，集成MoveIt进行全身运动控制，并通过Nav2实现环境中的自主导航，适用于需要在ROS 2生态中部署G1机器人的开发者。 ![GitHub stars](https://img.shields.io/github/stars/sangheonEN/unitree_g1_ros2_dev?style=social)

- [Tienkung_LAB](https://github.com/Jayson-Pan/Tienkung_LAB) — 该项目基于Tienkung LAB框架，实现了针对Unitree G1人形机器人的AMP（Adversarial Motion Priors）运动控制策略。通过强化学习方法训练全身运动技能，并在仿真环境中验证后部署至真实G1机器人，支持高动态动作生成。主要面向Unitree G1开发者及人形机器人运动控制研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Jayson-Pan/Tienkung_LAB?style=social)

- [MPC-control-for-unitree-G1-humanoid](https://github.com/willmerw/MPC-control-for-unitree-G1-humanoid) — 该项目实现了基于模型预测控制（MPC）的路径跟随控制器，专为Unitree G1人形机器人设计。通过Python编写，利用MPC算法实现对G1机器人的精确轨迹跟踪与运动控制，适用于需要高动态响应和稳定性的行走或导航任务。目标用户为从事Unitree G1高级运动控制研究与开发的工程师及研究人员。 ![GitHub stars](https://img.shields.io/github/stars/willmerw/MPC-control-for-unitree-G1-humanoid?style=social)

- [IsaacLab_RL_unitree_g1_template](https://github.com/yangyixiang-cc/IsaacLab_RL_unitree_g1_template) — 该项目为基于IsaacLab的强化学习训练模板，专为Unitree G1人形机器人设计，提供开箱即用的RL环境配置和运动控制策略框架。通过IsaacLab仿真平台实现高保真动力学模拟，并集成了针对G1机器人的关节配置与传感器接口。适用于希望在IsaacLab中快速开展Unitree G1强化学习研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/yangyixiang-cc/IsaacLab_RL_unitree_g1_template?style=social)

- [g1pilot](https://github.com/SAKErobotics/g1pilot) — 该项目是一个基于ROS2的控制包，专为Unitree G1人形机器人设计，提供运动控制与状态管理功能。其核心特性包括对ROS2 Jazzy版本的支持、与G1硬件的直接接口集成，以及模块化的控制架构。目标用户为使用Unitree G1进行二次开发或部署的机器人研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/SAKErobotics/g1pilot?style=social)

- [g1-rl-demo](https://github.com/Nagi-ovo/g1-rl-demo) — 该项目是一个面向 Unitree G1 人形机器人的强化学习（RL）入门示例，基于 uv 工具构建可复现的训练环境。它集成了 Isaac Gym 或类似仿真平台，提供针对 G1 的运动控制策略训练框架，便于开发者快速启动 RL 实验。目标用户为希望在 Unitree G1 上实现和验证强化学习算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Nagi-ovo/g1-rl-demo?style=social)

- [UniPwn](https://github.com/fromgabyaaye/UniPwn) — 该项目旨在通过蓝牙低功耗（BLE）分析并利用Unitree机器人中的命令注入漏洞，提供网络安全攻防的可行性验证。它专门针对Unitree机器人固件或服务中的输入验证缺陷，使用Python实现自动化探测与利用脚本，帮助安全研究人员和红队评估设备安全性。目标用户为关注机器人系统安全的渗透测试人员和漏洞研究者。 ![GitHub stars](https://img.shields.io/github/stars/fromgabyaaye/UniPwn?style=social)

- [g1-humanoid-robot-voice-based-motions](https://github.com/abdullah-m-elnahrawy/g1-humanoid-robot-voice-based-motions) — 该项目为Unitree G1人形机器人提供基于语音触发的动作执行功能，通过唤醒词和自定义短语映射到YAML定义的动作序列。系统使用C++实现，支持实时语音识别与动作调度，适用于希望为G1添加语音交互能力的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/abdullah-m-elnahrawy/g1-humanoid-robot-voice-based-motions?style=social)

- [Unitree_Robot_G1](https://github.com/LivingLabSabana/Unitree_Robot_G1) — 该项目提供Unitree G1人形机器人的配置文件、控制参数和部署脚本，用于快速完成机器人初始化与个性化设置。内容涵盖底层控制调参、系统集成指南及实机测试流程，基于官方SDK进行二次开发。主要面向科研实验室和开发者，帮助其高效开展G1平台上的算法验证与应用开发。 ![GitHub stars](https://img.shields.io/github/stars/LivingLabSabana/Unitree_Robot_G1?style=social)

- [h1_nav](https://github.com/rookierobot/h1_nav) — 该项目为Unitree H1人形机器人提供导航功能，基于ROS 2构建，集成了SLAM与路径规划模块，支持在真实环境中实现自主移动。项目明确针对H1平台开发，利用其传感器配置和运动特性进行适配，适用于希望在H1上快速部署导航能力的开发者。 ![GitHub stars](https://img.shields.io/github/stars/rookierobot/h1_nav?style=social)

- [PBRS-H1](https://github.com/SelfBriefs/PBRS-H1) — 该项目在Unitree H1人形机器人上实现了基于物理的渲染合成（PBRS）方法，用于生成逼真的训练数据以提升视觉感知模型性能。通过结合H1的URDF模型与真实场景光照条件，项目构建了高保真合成图像数据集，支持Sim2Real迁移。主要面向需要为Unitree H1开发视觉系统的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/SelfBriefs/PBRS-H1?style=social)

- [unitree_h1_2](https://github.com/francescocufino/unitree_h1_2) — 该项目为 Unitree H1-2 人形机器人提供底层控制代码，主要实现关节级驱动与状态读取功能。通过 C 语言直接调用 Unitree 官方 SDK，支持实时运动控制和传感器数据获取，适用于需要高性能低延迟控制的开发者。项目明确针对 H1-2 硬件平台，包含完整的通信协议解析和示例程序。 ![GitHub stars](https://img.shields.io/github/stars/francescocufino/unitree_h1_2?style=social)

- [isaac-lab-unitree-h1](https://github.com/jacobhroutzong/isaac-lab-unitree-h1) — 该项目为 Unitree H1 人形机器人在 Isaac Lab 仿真平台中的集成提供支持，主要用途是实现基于强化学习的运动控制策略开发。项目利用 Isaac Lab 的物理仿真能力，构建了 H1 机器人的数字孪生模型，并配置了相应的传感器和执行器接口。目标用户为从事人形机器人强化学习与仿真实验的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/jacobhroutzong/isaac-lab-unitree-h1?style=social)

- [h1_description](https://github.com/kyavuzkurt/h1_description) — 该项目是一个 ROS2 功能包，提供 Unitree H1 人形机器人的 URDF/Xacro 描述文件，用于在 ROS2 生态中进行可视化、仿真和运动规划。它明确面向 Unitree H1 机器人，包含其完整的关节与连杆定义，并支持与 RViz、Gazebo 等工具集成。适用于基于 ROS2 开发 H1 应用的机器人工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/kyavuzkurt/h1_description?style=social)

- [unitree_h12_rma](https://github.com/correlllab/unitree_h12_rma) — 该项目实现了在Unitree H1-2机器人上的RMA（Recurrent Model-based Adaptation）算法，用于提升四足机器人在复杂地形中的自适应运动控制能力。项目基于PyTorch构建，集成了Unitree官方SDK以实现低层硬件通信，并利用Isaac Gym进行仿真训练与Sim2Real迁移。主要面向从事四足机器人强化学习与自适应控制研究的学术与工程团队。 ![GitHub stars](https://img.shields.io/github/stars/correlllab/unitree_h12_rma?style=social)

- [slam_unitree_H1](https://github.com/okstill/slam_unitree_H1) — 该项目提供了一套ROS2软件包，专为Unitree H1人形机器人实现SLAM（同步定位与地图构建）功能。通过集成激光雷达或深度相机等传感器数据，结合SLAM算法（如Cartographer或SLAM Toolbox），在ROS2框架下完成环境建图与定位。项目直接面向H1平台开发，适配其传感器布局和运动特性，适用于需要自主导航能力的H1开发者。 ![GitHub stars](https://img.shields.io/github/stars/okstill/slam_unitree_H1?style=social)

- [unitree_h1_humanoidgym](https://github.com/Yzw-Camellia/unitree_h1_humanoidgym) — 该项目为Unitree H1人形机器人提供基于强化学习的仿真训练环境，使用Isaac Gym构建高效率物理仿真，支持全身运动控制策略开发。其核心功能包括H1机器人专用的URDF模型集成、奖励函数设计及状态观测接口，便于研究人员快速开展人形机器人强化学习算法实验。目标用户为专注于Unitree H1平台的机器人学习与控制开发者。 ![GitHub stars](https://img.shields.io/github/stars/Yzw-Camellia/unitree_h1_humanoidgym?style=social)

- [raviteja_unitree](https://github.com/Raviteja-T/raviteja_unitree) — 该项目提供了一个基于 Docker 的 ROS2 Humble 开发环境，专为 Unitree H1-2 人形机器人设计，集成了 Unitree 官方 SDK，便于开发者快速部署和测试控制算法。通过容器化封装，解决了依赖冲突问题，并支持与 ROS2 生态无缝集成。目标用户为使用 H1-2 进行二次开发的机器人研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/Raviteja-T/raviteja_unitree?style=social)

- [humanoid_ctrl2sim](https://github.com/duxr1015/humanoid_ctrl2sim) — 该项目基于Unitree-H1-2机器人，利用ULC（Unified Locomotion and Control）框架实现人形机器人的控制与仿真功能。通过Python开发，项目聚焦于将真实控制策略迁移至仿真环境，支持运动规划与动力学验证。主要面向Unitree H1系列开发者及人形机器人控制研究人员。 ![GitHub stars](https://img.shields.io/github/stars/duxr1015/humanoid_ctrl2sim?style=social)

- [Project_Neo](https://github.com/DominicZahn/Project_Neo) — 该项目旨在为Unitree H1人形机器人实现动态避障与运动控制功能，利用RBDL进行刚体动力学建模，并通过NLOPT优化运动轨迹。项目基于ROS 2 Jazzy框架开发，采用Docker容器化部署，主要面向Unitree H1平台的高级运动规划研究与应用开发者。 ![GitHub stars](https://img.shields.io/github/stars/DominicZahn/Project_Neo?style=social)

- [glocomp_b2_ros2](https://github.com/Glocomp-Robotics/glocomp_b2_ros2) — 该项目为Unitree B2机器人提供定制化的ROS 2驱动与控制接口，包含底层通信协议解析、关节控制及状态反馈功能，基于C++实现并与Unitree官方SDK集成。主要面向使用ROS 2生态开发B2应用的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/Glocomp-Robotics/glocomp_b2_ros2?style=social)

- [unitree-go2-ros2](https://github.com/CTGUMARK/unitree-go2-ros2) — 该项目为 Unitree Go2 机器人提供 ROS2 接口支持，实现底层驱动与上层应用的通信桥梁。通过 C++ 实现了对 Go2 状态数据的订阅和控制指令的发布，兼容 ROS2 Humble/Foxy 等版本。主要面向希望在 ROS2 生态中开发 Go2 应用的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/CTGUMARK/unitree-go2-ros2?style=social)

- [Unitree-G1-MoveIt2-Arm-Manipulation](https://github.com/sharan05032000/Unitree-G1-MoveIt2-Arm-Manipulation) — 该项目旨在为Unitree G1人形机器人提供基于MoveIt2的机械臂运动规划与操作功能，通过ROS 2接口实现对G1上肢的运动学控制和轨迹规划。项目利用MoveIt2框架集成G1的URDF模型，支持碰撞检测与可视化调试，主要面向希望在G1平台上开发复杂操作任务的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/sharan05032000/Unitree-G1-MoveIt2-Arm-Manipulation?style=social)

- [Go2_where_r_u](https://github.com/arpa-byte/Go2_where_r_u) — 该项目在Unitree Go2机器人上实现基于Livox MID-360激光雷达的2D SLAM功能，利用Python构建定位与地图构建系统，适用于室内外环境下的自主导航。项目直接面向Go2平台进行硬件集成，为开发者提供轻量级SLAM解决方案。 ![GitHub stars](https://img.shields.io/github/stars/arpa-byte/Go2_where_r_u?style=social)

- [Unitree-Go2-ROS2-Ignition-Rviz2](https://github.com/lidianzhong/Unitree-Go2-ROS2-Ignition-Rviz2) — 该项目为 Unitree Go2 机器人提供 ROS2 集成支持，结合 Ignition Gazebo 仿真环境与 Rviz2 可视化工具，便于开发者进行算法测试与状态监控。项目通过 URDF/SDF 模型加载和 ROS2 控制接口实现对 Go2 的仿真控制，适用于基于 ROS2 生态的 Unitree Go2 开发者。 ![GitHub stars](https://img.shields.io/github/stars/lidianzhong/Unitree-Go2-ROS2-Ignition-Rviz2?style=social)

- [unitree-go2-path-planner](https://github.com/sanan222/unitree-go2-path-planner) — 该项目为Unitree Go2四足机器人提供实时局部路径规划功能，实现了Bug0和Bug1避障算法，并通过Rviz进行可视化仿真。代码基于Python开发，直接面向Go2平台设计，适用于需要在复杂环境中实现基础导航能力的开发者。 ![GitHub stars](https://img.shields.io/github/stars/sanan222/unitree-go2-path-planner?style=social)

- [OpenHomie_h1_2](https://github.com/warner-ng/OpenHomie_h1_2) — 该项目基于 OpenHomie 框架为 Unitree-H1-2 人形机器人提供 C++ 实现，旨在支持其运动控制与感知功能集成。通过适配 OpenHomie 的模块化架构，项目实现了对 H1-2 硬件的底层驱动和状态管理，并依赖 Unitree 官方 SDK 进行通信。主要面向希望在 H1-2 平台上快速部署自主行为的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/warner-ng/OpenHomie_h1_2?style=social)

- [Picking_Go2](https://github.com/Xiangjincheng/Picking_Go2) — 该项目基于Unitree Go2机器人底盘开发了一套移动采摘系统，利用Go2的移动能力结合机械臂实现自主果蔬采摘。系统采用Python编写，集成了感知、导航与抓取模块，适用于农业自动化场景。主要面向农业机器人研究者和Unitree Go2开发者。 ![GitHub stars](https://img.shields.io/github/stars/Xiangjincheng/Picking_Go2?style=social)

- [go2_sim](https://github.com/llyymmoo/go2_sim) — 该项目为Unitree Go2四足机器人提供了一个基于Gazebo的仿真环境，使用C++实现，便于开发者在无需真实硬件的情况下测试控制算法和感知系统。项目直接面向Go2型号，复现了其动力学与传感器配置，适用于机器人运动控制、SLAM等任务的前期验证。目标用户为希望在Gazebo中快速部署和调试Go2相关算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/llyymmoo/go2_sim?style=social)

- [G1_Experiment_Light](https://github.com/Thisanwerss/G1_Experiment_Light) — 该项目是一个轻量级的 Unitree G1 机器人控制框架，主要提供简化的 Python 接口用于发送运动指令和读取传感器数据。它直接面向 G1 机器人，封装了底层通信协议，便于快速开发与测试。适合希望在真实 G1 硬件上进行原型验证的开发者或研究人员使用。 ![GitHub stars](https://img.shields.io/github/stars/Thisanwerss/G1_Experiment_Light?style=social)

- [lez666-g1-sim2crawl](https://github.com/lez666/lez666-g1-sim2crawl) — 该项目为Unitree G1人形机器人提供从仿真到真实环境的爬行运动控制流程，基于MuJoCo物理引擎实现键盘控制的部署方案。通过Jupyter Notebook构建Sim2Real迁移管道，支持用户交互式调试G1的四肢协调运动策略，适用于希望快速验证G1低速移动算法的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/lez666/lez666-g1-sim2crawl?style=social)

- [H1-2-Hardware](https://github.com/PointsCoder/H1-2-Hardware) — 该项目提供 Unitree H1-2 人形机器人的硬件配置代码，主要用于初始化和管理底层硬件模块。项目使用 Python 编写，包含与 H1-2 本体通信、传感器校准及执行器控制相关的脚本，直接面向该型号的硬件部署。适用于需要对 H1-2 进行底层调试或二次开发的工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/PointsCoder/H1-2-Hardware?style=social)

- [go2_mujoco](https://github.com/N1cecode/go2_mujoco) — 该项目提供了一个基于MuJoCo仿真的Unitree Go2机器人控制框架，支持通过Xbox手柄进行实时遥操作。其核心功能包括Go2的运动控制接口封装、手柄输入映射以及与MuJoCo物理引擎的集成，便于开发者在仿真环境中快速测试控制策略。主要面向希望在MuJoCo中开发或验证Go2控制算法的机器人研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/N1cecode/go2_mujoco?style=social)

- [Go2_driver](https://github.com/yanyuze1/Go2_driver) — 该项目是一个用于快速部署 Unitree Go2 机器人的基础驱动程序，提供底层硬件接口和基本控制功能。基于 C++ 实现，直接与 Go2 的实时通信协议交互，支持运动指令发送与状态读取。适用于希望在真实机器人上进行二次开发或算法验证的开发者。 ![GitHub stars](https://img.shields.io/github/stars/yanyuze1/Go2_driver?style=social)

- [Go2_Gazebo_Environment](https://github.com/AsdoubleU/Go2_Gazebo_Environment) — 该项目提供了一个基于ROS的Gazebo仿真环境，专为Unitree Go2机器人设计，用于在虚拟环境中测试和开发控制算法。它集成了Go2的URDF模型与Gazebo物理引擎，并通过ROS接口实现传感器数据发布和关节控制，便于开发者进行运动规划或SLAM等任务的前期验证。目标用户为希望在真实部署前进行仿真的Unitree Go2开发者。 ![GitHub stars](https://img.shields.io/github/stars/AsdoubleU/Go2_Gazebo_Environment?style=social)

- [unitree_go2_demo](https://github.com/PanteEmi/unitree_go2_demo) — 该项目提供了一系列针对 Unitree Go2 机器狗的 Python 演示程序，展示了基础运动控制、姿态调整和简单行为实现。代码直接调用 Unitree 官方 SDK 接口，适用于熟悉 Python 的开发者快速上手 Go2 硬件操作。项目虽小但聚焦于 Unitree Go2 的实际驱动与交互，适合入门级用户和教育用途。 ![GitHub stars](https://img.shields.io/github/stars/PanteEmi/unitree_go2_demo?style=social)

- [unitree-go2-controller-ros2](https://github.com/dabodobo/unitree-go2-controller-ros2) — 该项目为 Unitree Go2 机器人提供基于 ROS2 的底层运动控制接口，通过 C++ 实现与 Go2 官方 SDK 的集成，支持实时发送关节指令和读取状态反馈。其核心功能包括建立 ROS2 节点与 Go2 驱动器的通信，并封装控制命令以简化高层算法开发。主要面向希望在 ROS2 生态中快速部署 Go2 控制策略的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/dabodobo/unitree-go2-controller-ros2?style=social)

- [biscuit-voice-service-unitree-go2](https://github.com/NayiemW/biscuit-voice-service-unitree-go2) — 该项目为 Unitree Go2 机器人开发了一套语音交互系统，支持传感器检测、个性化应答和闲聊功能。通过 Python 实现，结合语音识别与响应逻辑，增强 Go2 的人机交互能力，适用于希望赋予 Unitree Go2 语音智能的开发者或研究者。 ![GitHub stars](https://img.shields.io/github/stars/NayiemW/biscuit-voice-service-unitree-go2?style=social)

- [Barrier-Free-Scout-An-Environment-Detection-App-Powered-by-Unitree-Go2](https://github.com/c-Ath-Y/Barrier-Free-Scout-An-Environment-Detection-App-Powered-by-Unitree-Go2) — 该项目是一个基于 Unitree Go2 机器人开发的环境检测应用，利用其搭载的先进传感器实时识别路缘、台阶等障碍物，自动生成无障碍导航地图。通过将传统人工巡检自动化，该应用显著提升了城市环境中残障人士的出行便利性，主要面向智慧城市与无障碍设施评估场景。 ![GitHub stars](https://img.shields.io/github/stars/c-Ath-Y/Barrier-Free-Scout-An-Environment-Detection-App-Powered-by-Unitree-Go2?style=social)

- [unitreeg1_ROS_mic](https://github.com/dcuevasa/unitreeg1_ROS_mic) — 该项目是一个轻量级的 ROS Noetic 节点，专门用于从 Unitree G1 机器人麦克风采集并发布音频数据。它通过订阅 G1 的底层音频接口，将音频流以 ROS topic 形式输出，便于上层语音处理模块使用。项目结构简洁，依赖标准 ROS 音频工具链，适合需要在 G1 平台上开发语音交互或环境声音感知功能的开发者。 ![GitHub stars](https://img.shields.io/github/stars/dcuevasa/unitreeg1_ROS_mic?style=social)

- [unitree_h1_meta_launch_ws](https://github.com/cyberbanana777/unitree_h1_meta_launch_ws) — 该项目是一个 ROS2 元启动包，用于快速部署 Unitree H1 人形机器人的多种工作模式（如遥操作和 SLAM），整合了来自 unitree_h1_*_ws 系列仓库的节点配置。它通过 launch 文件简化了机器人功能模块的启动流程，适用于基于 ROS2 的 Unitree H1 开发与测试场景。目标用户为使用 Unitree H1 进行上层应用开发的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/cyberbanana777/unitree_h1_meta_launch_ws?style=social)

- [unitree_h1_sensors_ws](https://github.com/cyberbanana777/unitree_h1_sensors_ws) — 该项目提供用于Unitree H1机器人传感器数据处理的ROS2功能包，主要实现对H1本体搭载的IMU、关节编码器等传感器的驱动与数据发布。基于C++开发，支持ROS2 Humble/Foxy，便于开发者获取底层传感信息用于状态估计或控制算法。适用于需要直接访问H1硬件传感器数据的ROS2开发者。 ![GitHub stars](https://img.shields.io/github/stars/cyberbanana777/unitree_h1_sensors_ws?style=social)

- [unitree_h1_control_ws](https://github.com/cyberbanana777/unitree_h1_control_ws) — 该项目提供了一套ROS2控制包，专门用于Unitree H1人形机器人的关节、手腕及手指位置控制。通过Python实现，支持对H1高自由度手部和全身关节的精确指令下发，适用于需要精细操作的研究或开发场景。目标用户为基于ROS2开发Unitree H1上层控制策略的机器人工程师与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/cyberbanana777/unitree_h1_control_ws?style=social)

- [unitree_h1_visualization_ws](https://github.com/cyberbanana777/unitree_h1_visualization_ws) — 该项目提供用于可视化 Unitree H1 机器人及其运动的 ROS2 软件包，基于 Python 实现，支持在 RViz 中实时显示机器人状态和关节轨迹。其核心功能包括 URDF 模型加载、TF 坐标变换发布及与 H1 真机或仿真数据的对接，适用于希望调试或监控 H1 运动行为的开发者。 ![GitHub stars](https://img.shields.io/github/stars/cyberbanana777/unitree_h1_visualization_ws?style=social)

- [unitree_h1_point-by-point_programming_ws](https://github.com/cyberbanana777/unitree_h1_point-by-point_programming_ws) — 该项目提供了一套基于ROS2的Python工具包，用于对Unitree H1人形机器人进行点到点运动编程。通过订阅和发布关节轨迹话题，用户可定义关键姿态序列并实现平滑插值控制，适用于需要精确关节空间轨迹的任务。主要面向希望在真实H1平台上快速部署简单动作序列的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/cyberbanana777/unitree_h1_point-by-point_programming_ws?style=social)

- [description_unitree_H1_ROS2](https://github.com/cyberbanana777/description_unitree_H1_ROS2) — 该项目提供了一个专用于 Unitree H1 人形机器人的 ROS2 URDF 描述包，便于在 ROS2 生态中进行仿真、可视化或控制开发。其核心功能是定义 H1 的完整运动学与外观模型，支持在 RViz 或 Gazebo 等工具中加载使用。目标用户为基于 ROS2 开发 Unitree H1 应用的机器人工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/cyberbanana777/description_unitree_H1_ROS2?style=social)

- [unitree_go2_simulation](https://github.com/ccwss-maker/unitree_go2_simulation) — 该项目提供基于 ROS2 Rolling 和 Gazebo Sim（Jetty 版本）的 Unitree Go2 机器人仿真环境，专为 Ubuntu 24.04 系统构建。通过 Python 脚本实现机器人模型加载、传感器配置及基础控制接口，支持在 Gazebo 中进行运动学与动力学仿真。主要面向希望在最新 ROS2 和 Gazebo 版本下开发或测试 Go2 相关算法的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/ccwss-maker/unitree_go2_simulation?style=social)

- [go2_slam](https://github.com/kExU9853/go2_slam) — 该项目旨在利用Unitree Go2机器人实现SLAM（同步定位与地图构建）功能，通过集成激光雷达或深度相机等传感器，结合ROS框架进行环境建图与自主定位。项目直接面向Unitree Go2平台开发，适配其硬件接口和运动特性，为Go2用户提供开箱即用的建图解决方案，适用于科研与工程开发者。 ![GitHub stars](https://img.shields.io/github/stars/kExU9853/go2_slam?style=social)

- [gazebo_simulation](https://github.com/1LCY007/gazebo_simulation) — 该项目提供 Unitree Go2 机器人在 Gazebo 仿真环境中的模拟实现，基于 C++ 开发，旨在为开发者提供一个本地仿真的测试平台。项目直接面向 Unitree-Go2 型号，包含其 URDF 模型与基本控制接口，便于进行运动控制、感知算法等开发验证。适用于希望在 Gazebo 中快速部署和测试 Go2 相关算法的机器人研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/1LCY007/gazebo_simulation?style=social)

- [sim_to_real_go2](https://github.com/katari16/sim_to_real_go2) — 该项目专注于 Unitree Go2 机器人的仿真到现实（Sim2Real）部署，利用 Python 实现从仿真环境到真实硬件的策略迁移。项目可能集成 Isaac Gym 或 MuJoCo 等仿真平台，并通过 Unitree SDK 与 Go2 通信，目标用户为希望在 Go2 上验证强化学习或运动控制算法的机器人研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/katari16/sim_to_real_go2?style=social)

- [ppo-doggy](https://github.com/arjunmurali215/ppo-doggy) — 该项目使用近端策略优化（PPO）算法实现对Unitree Go2四足机器人的运动控制，基于C++开发并在仿真环境中训练策略。项目明确针对Go2机器人设计，涉及强化学习与四足步态生成的结合，适用于希望在Go2平台上探索基于学习的控制方法的研究者或开发者。 ![GitHub stars](https://img.shields.io/github/stars/arjunmurali215/ppo-doggy?style=social)

- [unitree_sdk2_python_bond](https://github.com/marianof2000/unitree_sdk2_python_bond) — 该项目为 Unitree Go2 机器人提供了一个基于 Python 的 SDK2 接口封装，便于开发者通过 Python 语言控制 Go2 的底层运动与传感器数据。其核心功能包括与 Unitree 官方 SDK2 的绑定集成，支持实时指令发送和状态读取，并适配了 UADE（阿根廷布宜诺斯艾利斯大学）的开发环境。目标用户为希望使用 Python 快速开发 Go2 应用的科研人员或学生。 ![GitHub stars](https://img.shields.io/github/stars/marianof2000/unitree_sdk2_python_bond?style=social)

- [go2_interfaces](https://github.com/Unitree-Go2-Robot/go2_interfaces) — 该项目为 Unitree Go2 机器人提供 ROS 2 接口定义，包含自定义消息、服务和动作类型，用于标准化上层应用与底层驱动的通信。其核心功能是通过 CMake 构建系统集成到 ROS 2 工作空间，支持 Go2 的状态反馈与控制指令传输。目标用户为基于 ROS 2 开发 Go2 应用的机器人工程师。 ![GitHub stars](https://img.shields.io/github/stars/Unitree-Go2-Robot/go2_interfaces?style=social)

- [go2_cli](https://github.com/Unitree-Go2-Robot/go2_cli) — 该项目是一个基于Python的命令行工具，旨在为Unitree Go2机器人提供便捷的控制与调试接口。通过封装底层通信协议，支持实时发送运动指令、读取传感器数据等核心功能，便于开发者快速进行原型验证和现场调试。主要面向Unitree Go2用户及二次开发人员。 ![GitHub stars](https://img.shields.io/github/stars/Unitree-Go2-Robot/go2_cli?style=social)

- [genesis](https://github.com/adityabhas22/genesis) — 该项目旨在使用强化学习训练 Unitree Go2 的运动控制策略，明确面向 Unitree Go2 机器人开发专用的 RL 路径。项目基于 Python 实现，可能集成 Isaac Gym 或类似仿真环境以支持 Sim2Real 迁移。主要服务于希望在 Unitree Go2 上部署自定义强化学习策略的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/adityabhas22/genesis?style=social)

- [unitree-g1-robonomics](https://github.com/Fingerling42/unitree-g1-robonomics) — 该项目旨在将Unitree G1机器人通过其Python SDK接入Robonomics去中心化网络，实现机器人数据上链与远程控制。核心功能包括G1状态数据采集、区块链事务构建及与Robonomics节点的通信，依赖于官方提供的G1 Python接口。适用于希望探索机器人与Web3集成的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Fingerling42/unitree-g1-robonomics?style=social)

- [robosuite_g1](https://github.com/hogunkee/robosuite_g1) — 该项目在 robosuite 仿真框架中新增了对 Unitree G1 人形机器人的支持，使其可用于强化学习和机器人控制研究。通过集成 G1 的 URDF 模型与关节配置，用户可在 MuJoCo 物理引擎中进行任务仿真与策略训练。主要面向希望在标准化环境中开发或测试 G1 控制算法的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/hogunkee/robosuite_g1?style=social)

- [unitree_g1_humanoid_isaac_sim](https://github.com/vaishman/unitree_g1_humanoid_isaac_sim) — 该项目旨在为Unitree G1人形机器人提供Isaac Sim仿真环境支持，主要用途是构建高保真物理仿真平台以用于算法开发与测试。项目基于NVIDIA Isaac Sim搭建G1机器人的数字孪生模型，并集成其URDF/SDF描述文件及关节控制接口，便于开发者进行运动控制、强化学习或感知算法的Sim2Real迁移研究。目标用户为从事Unitree G1相关算法研发的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/vaishman/unitree_g1_humanoid_isaac_sim?style=social)

- [Implement-Unitree-G1-in-HOVER](https://github.com/SleepyAO-DT/Implement-Unitree-G1-in-HOVER) — 该项目旨在将Unitree G1人形机器人集成到HOVER仿真与现实迁移框架中，支持Sim2Sim和Sim2Real任务。通过适配G1的运动控制与感知模块，利用HOVER平台实现端到端策略部署，目标用户为从事人形机器人强化学习与迁移研究的开发者。 ![GitHub stars](https://img.shields.io/github/stars/SleepyAO-DT/Implement-Unitree-G1-in-HOVER?style=social)

- [unitree-g1-scripts](https://github.com/YemuRiven/unitree-g1-scripts) — 该项目是一套专为宇树 Unitree G1 人形机器人开发的 Python 脚本工具集，提供便捷的控制、调试或自动化功能。项目明确聚焦于 G1 机型，可能包含与其 SDK 或底层接口的直接交互，适用于希望快速部署或测试 G1 功能的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/YemuRiven/unitree-g1-scripts?style=social)

- [unitree_g1_sdk2_ros1](https://github.com/icy-creann/unitree_g1_sdk2_ros1) — 该项目为 Unitree G1 人形机器人提供 ROS1 接口封装，基于 C++ 实现对官方 SDK 的集成，支持关节控制与状态读取。其核心功能是将 Unitree G1 的底层通信协议转换为 ROS1 话题与服务，便于在 ROS 生态中开发上层应用。目标用户为使用 ROS1 进行 G1 机器人控制与算法开发的研究者和工程师。 ![GitHub stars](https://img.shields.io/github/stars/icy-creann/unitree_g1_sdk2_ros1?style=social)

- [ControlUnitreeG1withROS](https://github.com/AStupidLight/ControlUnitreeG1withROS) — 该项目提供了一种基于ROS2和Python的替代方案，用于控制Unitree G1机器人的策略切换，绕过默认控制器直接调用底层API。它实现了与G1的通信接口，支持自定义运动策略部署，适用于希望在ROS2生态中开发高级控制逻辑的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/AStupidLight/ControlUnitreeG1withROS?style=social)

- [unitree-h1-ros2](https://github.com/sachinkum0009/unitree-h1-ros2) — 该项目旨在为Unitree H1人形机器人提供ROS 2接口支持，通过Python实现与H1底层通信的封装，便于在ROS 2生态中集成控制、感知和导航模块。项目利用Unitree官方SDK与机器人实时交互，并发布关节状态、接收命令话题，适用于希望在ROS 2框架下开发H1应用的机器人研究者和工程师。 ![GitHub stars](https://img.shields.io/github/stars/sachinkum0009/unitree-h1-ros2?style=social)

- [bvh-to-h1-retargeter](https://github.com/Planeurzik/bvh-to-h1-retargeter) — 该项目提供了一个将BVH动作捕捉文件重定向到Unitree H1人形机器人的工具，专门适配无手版本的H1模型。通过Python实现关节映射与运动数据转换，支持将标准BVH格式的动作数据应用于H1的仿真或实际硬件控制。主要面向希望在H1平台上复现或迁移人体动作的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/Planeurzik/bvh-to-h1-retargeter?style=social)

- [vive_g1_hfbody](https://github.com/1EastonJ/vive_g1_hfbody) — 该项目旨在为Unitree G1人形机器人实现基于Vive追踪系统的全身动捕遥操作功能，通过Python开发，利用Vive头显与控制器获取用户肢体位姿，并映射至G1的高自由度身体结构。项目直接面向Unitree-G1硬件平台，涉及运动学映射与实时控制接口，适用于希望快速搭建低成本遥操作系统的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/1EastonJ/vive_g1_hfbody?style=social)

- [Unitree-G1-Humanoid-Robot-Tasks](https://github.com/ThejasDevadiga/Unitree-G1-Humanoid-Robot-Tasks) — 该项目旨在通过多任务学习训练 Unitree-G1 人形机器人，利用 Python 实现基于强化学习或行为克隆的控制策略。项目明确以 Unitree-G1 为唯一目标平台，包含任务定义、训练脚本及与机器人硬件或仿真的接口逻辑，适用于希望在 G1 平台上开发复杂行为的机器人研究人员。 ![GitHub stars](https://img.shields.io/github/stars/ThejasDevadiga/Unitree-G1-Humanoid-Robot-Tasks?style=social)

- [Unitree-Go2](https://github.com/anvgigz/Unitree-Go2) — 该项目旨在为 Unitree Go2 机器人提供基础控制与接口支持，可能包含硬件通信、运动控制或ROS集成等核心功能。由于项目明确以 Unitree-Go2 命名且聚焦于该机型，直接面向其开发生态。目标用户为希望在 Go2 上进行二次开发或算法部署的机器人研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/anvgigz/Unitree-Go2?style=social)

- [unitree_g1](https://github.com/ROM-robotics/unitree_g1) — 该项目为 Unitree G1 人形机器人提供底层控制与驱动接口，基于 C++ 实现硬件通信和运动控制功能。其代码结构面向 G1 的关节模块与主控单元，支持实时指令下发与状态反馈，适用于需要直接操作 G1 硬件的开发者。尽管缺乏文档和星标，但其命名和仓库归属表明专为 Unitree-G1 设计。 ![GitHub stars](https://img.shields.io/github/stars/ROM-robotics/unitree_g1?style=social)

- [ld-g1-sdk2](https://github.com/LD-Robots/ld-g1-sdk2) — 该项目为 LD-Robots 提供的 G1 人形机器人 SDK，基于 C++ 开发，旨在实现对 Unitree-G1 的底层控制与状态交互。虽然仓库暂无详细描述，但其命名和上下文表明它直接面向 Unitree-G1 硬件，可能包含运动控制、传感器读取或通信接口等核心功能。目标用户为基于 G1 进行二次开发的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/LD-Robots/ld-g1-sdk2?style=social)

- [unitree_g1_course_exercises](https://github.com/Michdo93/unitree_g1_course_exercises) — 该项目提供面向Unitree G1人形机器人的课程练习代码，主要用途是帮助开发者学习和实践G1机器人的控制与编程。项目基于Python实现，可能涵盖运动控制、传感器数据处理等基础功能，直接针对Unitree-G1硬件平台进行教学示例开发。目标用户为参与相关机器人课程的学生或希望入门Unitree G1开发的工程师。 ![GitHub stars](https://img.shields.io/github/stars/Michdo93/unitree_g1_course_exercises?style=social)

- [g1-piano-play](https://github.com/meetsitaram/g1-piano-play) — 该项目旨在让Unitree G1人形机器人演奏钢琴，通过Python实现动作规划与控制。项目直接针对Unitree-G1硬件平台开发，可能涉及其关节控制接口和运动学模型。适合对人形机器人精细操作和音乐交互感兴趣的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/meetsitaram/g1-piano-play?style=social)

- [unitree_g1_2_deve](https://github.com/josephteh97/unitree_g1_2_deve) — 该项目旨在对Unitree G1人形机器人进行二次开发，提供基于Python的控制接口和功能扩展。项目直接面向Unitree-G1硬件平台，可能包含运动控制、传感器集成或高层行为逻辑的实现，适用于希望在G1基础上进行定制化开发的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/josephteh97/unitree_g1_2_deve?style=social)

- [BlindNavTech](https://github.com/mdequanter/BlindNavTech) — 该项目为视障人士开发了一套基于3D LiDAR和深度相机的障碍物检测系统，明确使用Unitree Go2 PRO作为移动平台搭载传感器，实现对低矮障碍物、路缘和楼梯的实时识别。系统采用Python编写，融合OAK-D与RealSense D435i数据，结合AI算法提升户外导航安全性，目标用户为辅助技术开发者与无障碍出行研究者。 ![GitHub stars](https://img.shields.io/github/stars/mdequanter/BlindNavTech?style=social)

- [ros_noetic_unitree_go2_sim](https://github.com/yuxiangros/ros_noetic_unitree_go2_sim) — 该项目为 Unitree Go2 机器人提供基于 ROS Noetic 的仿真环境，支持在 Gazebo 中进行运动控制与传感器模拟。通过集成 Unitree 官方 SDK 和 ROS 接口，实现对 Go2 四足机器人的关节控制、IMU 数据发布及基本步态仿真。适用于希望在 ROS1 生态中快速开发和测试 Go2 控制算法的开发者。 ![GitHub stars](https://img.shields.io/github/stars/yuxiangros/ros_noetic_unitree_go2_sim?style=social)

- [humanoid-stair-manipulation](https://github.com/AnujithM/humanoid-stair-manipulation) — 该项目是一个面向人形机器人楼梯攀爬与操作的研究档案，明确以 Unitree G1 为主要实验平台之一，涵盖动作重定向、感知与全身控制等关键技术。通过仿真与实机结合的方式探索复杂地形下的运动策略，适用于人形机器人研究者及 Unitree G1 开发者。 ![GitHub stars](https://img.shields.io/github/stars/AnujithM/humanoid-stair-manipulation?style=social)

- [ros2_recorder](https://github.com/akifbayram/ros2_recorder) — 该项目是一个专为 Unitree Go2 和 TurtleBot4 设计的 ROS2 数据记录工具，能够同步采集视频、里程计和激光雷达扫描数据，并按时间戳保存。其核心功能直接支持 Unitree Go2 的传感器数据录制，便于后续建图、导航或算法验证。适用于需要在真实 Unitree 机器人平台上进行数据采集与回放的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/akifbayram/ros2_recorder?style=social)

- [TFM---SLAM-con-el-robot-articulado-Unitree-Go2](https://github.com/JoseCarlosPenMac/TFM---SLAM-con-el-robot-articulado-Unitree-Go2) — 该项目是阿里坎特大学人工智能硕士毕业论文，旨在为Unitree Go2四足机器人实现SLAM（同步定位与地图构建）功能。项目基于Python开发，结合ROS或类似机器人中间件，利用Go2的传感器数据（如深度相机或IMU）进行环境建图与定位，探索四足机器人在复杂地形下的自主导航能力。主要面向学术研究者和机器人开发者，为Unitree Go2平台提供SLAM应用参考。 ![GitHub stars](https://img.shields.io/github/stars/JoseCarlosPenMac/TFM---SLAM-con-el-robot-articulado-Unitree-Go2?style=social)

- [ign_robot_dog](https://github.com/chiway-luo/ign_robot_dog) — 该项目基于CHAMP框架，在Ignition Gazebo中实现了宇树Go2和智元D1机器狗的仿真环境，支持四足机器人运动控制与感知算法的开发测试。通过集成Unitree Go2的URDF模型和硬件接口抽象，为开发者提供了一个可扩展的仿真平台。主要面向希望在Ignition Gazebo中进行Unitree Go2相关算法验证的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/chiway-luo/ign_robot_dog?style=social)

- [Unitree-Go2-Adaptive-RL](https://github.com/pym96/Unitree-Go2-Adaptive-RL) — 该项目旨在为Unitree Go2四足机器人开发基于强化学习的自适应控制策略，利用仿真到现实（Sim2Real）迁移技术提升机器人在复杂地形中的运动能力。项目可能基于Isaac Gym或类似RL训练框架，并针对Go2的硬件特性进行优化，目标用户为从事四足机器人强化学习研究的开发者与科研人员。 ![GitHub stars](https://img.shields.io/github/stars/pym96/Unitree-Go2-Adaptive-RL?style=social)

- [g1-poser](https://github.com/jloganolson/g1-poser) — 该项目为Unitree G1人形机器人提供姿态控制和运动生成功能，通过Python实现对G1机器人的关节状态监控与目标姿态设定。项目直接面向Unitree-G1硬件平台，利用其官方API进行通信，支持实时姿态调整。适用于需要快速原型开发或教学演示的G1机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/jloganolson/g1-poser?style=social)

- [Unitreeh1-g1-RL_Training_and_Navigation](https://github.com/anuragroy2001/Unitreeh1-g1-RL_Training_and_Navigation) — 该项目旨在为Unitree H1和G1人形机器人提供基于强化学习的训练与导航框架，利用Isaac Gym或MuJoCo等仿真平台实现运动控制策略的端到端训练，并通过ROS或自定义接口部署到真实硬件。项目聚焦于**Sim2Real迁移**和**全身运动控制**，适用于希望在Unitree人形平台上开发自主导航与动态行走能力的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/anuragroy2001/Unitreeh1-g1-RL_Training_and_Navigation?style=social)

- [UnitreeGo2](https://github.com/damuxt/UnitreeGo2) — 该项目提供宇树Unitree Go2机器人的课程讲义，以HTML格式呈现，内容涵盖Go2的基础操作、控制接口及开发入门知识。项目明确面向Unitree-Go2用户，旨在帮助开发者和学生快速上手该机器人平台。适合教育场景下的初学者和教学人员使用。 ![GitHub stars](https://img.shields.io/github/stars/damuxt/UnitreeGo2?style=social)

- [unitree-go2-nav2](https://github.com/SHEN00001/unitree-go2-nav2) — 该项目为 Unitree Go2 机器人提供基于 ROS 2 Navigation2（Nav2）的自主导航功能，通过集成 Go2 的底层驱动与 Nav2 软件栈，实现室内外环境下的路径规划与避障。项目使用 C++ 编写，依赖 ROS 2 和 Unitree 官方 SDK，适用于希望在 Go2 平台上快速部署自主导航能力的开发者。 ![GitHub stars](https://img.shields.io/github/stars/SHEN00001/unitree-go2-nav2?style=social)

- [Go2_navigation_Sem2](https://github.com/polo777/Go2_navigation_Sem2) — 该项目为 Unitree Go2 提供基于 ROS2 的自主导航工作空间，旨在实现语义导航功能。项目整合了 ROS2 导航栈与 Go2 的底层控制接口，支持在真实或仿真环境中进行建图与路径规划。主要面向希望在 Go2 平台上开发高级导航能力的机器人研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/polo777/Go2_navigation_Sem2?style=social)

- [unitree_go2_create_dataset](https://github.com/ShijieZhao36/unitree_go2_create_dataset) — 该项目用于为Unitree Go2机器人创建数据集，主要通过C++实现传感器数据采集与记录功能。代码直接面向Go2硬件平台，利用其底层驱动接口获取IMU、关节状态等实时数据，适用于需要构建训练或测试数据集的机器人学习研究者。 ![GitHub stars](https://img.shields.io/github/stars/ShijieZhao36/unitree_go2_create_dataset?style=social)

- [Robot-ROS2](https://github.com/hgguspet/Robot-ROS2) — 该项目为 Unitree G1 人形机器人提供 ROS2 配置文件和基础接口支持，包含 URDF 模型、控制器配置及传感器话题定义。通过集成 ROS2 控制框架，便于开发者在标准 ROS2 生态中部署运动控制与感知算法。主要面向使用 Unitree G1 进行二次开发的科研与工程用户。 ![GitHub stars](https://img.shields.io/github/stars/hgguspet/Robot-ROS2?style=social)

- [HL-Engine-3](https://github.com/TechMaverik/HL-Engine-3) — HL Engine 3 是一个面向机器人与计算机视觉应用的中间件，提供对 Unitree Go2、Z1 和 G1 等机型的内置支持，简化多平台机器人控制与集成。其通过统一接口实现跨硬件通信，适用于需要快速部署和管理多种 Unitree 机器人的开发者。 ![GitHub stars](https://img.shields.io/github/stars/TechMaverik/HL-Engine-3?style=social)

- [go2_velocity](https://github.com/giangdao1402/go2_velocity) — 该项目旨在将 Unitree Go2 机器人与 MJLab 的速度控制任务进行集成，实现基于强化学习的速度跟踪控制。项目利用 MuJoCo 仿真环境构建 Go2 的动力学模型，并通过自定义奖励函数训练策略网络，支持在仿真中完成前进、转向等基本运动任务。主要面向希望在 Unitree Go2 上快速验证 RL 控制算法的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/giangdao1402/go2_velocity?style=social)

- [unitree-go2-project](https://github.com/Ricky2025-hci/unitree-go2-project) — 该项目为 Unitree Go2 机器人提供 ROS2 环境配置，并集成额外的 LiDAR 与摄像头传感器支持，便于开发者构建感知与导航系统。通过 C++ 实现硬件接口适配，明确面向 Go2 平台扩展感知能力，适用于需要多传感器融合的机器人应用开发。 ![GitHub stars](https://img.shields.io/github/stars/Ricky2025-hci/unitree-go2-project?style=social)

- [unitree-go2-ros2](https://github.com/COMP0244-S25/unitree-go2-ros2) — 该项目为 Unitree Go2 机器人提供 ROS2 接口支持，主要实现机器人状态读取与控制指令发送功能。通过 C++ 编写，利用 Unitree 官方 SDK 与机器人底层通信，适配 ROS2 Humble/Foxy 等版本。适用于需要在 ROS2 生态中集成 Go2 进行导航、SLAM 或自主任务开发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/COMP0244-S25/unitree-go2-ros2?style=social)

- [A-robot-maze-challenge-based-on-genesis](https://github.com/wisdomwxy/A-robot-maze-challenge-based-on-genesis) — 该项目基于Genesis仿真平台实现了Unitree Go2四足机器人的行走控制与可视化演示，并结合迷宫寻路任务展示其导航能力。项目通过Python构建了Go2在仿真环境中的运动控制逻辑，并集成迷宫求解算法，使机器人能自主搜索终点。主要面向对Unitree Go2仿真控制和基础自主导航感兴趣的开发者与研究者。 ![GitHub stars](https://img.shields.io/github/stars/wisdomwxy/A-robot-maze-challenge-based-on-genesis?style=social)

- [unitree-go2-ros2](https://github.com/Chirag-Sharma-04/unitree-go2-ros2) — 该项目为 Unitree Go2 机器人提供 ROS2 接口支持，主要实现机器人状态读取与控制指令下发功能。通过 C++ 编写，利用 Unitree 官方 SDK 与机器人底层通信，适配 ROS2 Humble/Foxy 等版本，便于在 ROS2 生态中集成 Go2 的运动控制与传感器数据。适用于希望在 ROS2 框架下开发 Go2 应用的机器人研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/Chirag-Sharma-04/unitree-go2-ros2?style=social)

- [robodog_perception](https://github.com/davidabasabe/robodog_perception) — 该项目为Unitree Go2机器人提供感知与决策功能，主要实现基于计算机视觉的环境分割和障碍物识别，并结合简单决策逻辑用于导航。代码使用Python开发，直接面向Go2平台进行适配，目标用户为希望在Go2上快速部署视觉感知能力的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/davidabasabe/robodog_perception?style=social)

- [unitree_go](https://github.com/Unitree-Go2-Robot/unitree_go) — 该项目为 Unitree Go2 机器人提供基础的 ROS 驱动与控制接口，主要功能包括硬件通信、状态读取和运动指令下发。通过 CMake 构建系统集成到 ROS 环境，支持实时控制 Go2 的关节与传感器数据流。目标用户为希望在 ROS 生态中开发 Go2 应用的机器人工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Unitree-Go2-Robot/unitree_go?style=social)

- [go2_rviz](https://github.com/Unitree-Go2-Robot/go2_rviz) — 该项目为 Unitree Go2 机器人提供 RViz 可视化配置，便于开发者在 ROS 环境中实时监控机器人状态、传感器数据和运动轨迹。通过集成 ROS 2 和 Unitree 官方 SDK，支持 Go2 的关节状态、IMU 和点云等话题的可视化，适用于基于 ROS 2 的 Go2 应用开发与调试。 ![GitHub stars](https://img.shields.io/github/stars/Unitree-Go2-Robot/go2_rviz?style=social)

- [ROS2-Gazebo-GO2](https://github.com/yanyuze1/ROS2-Gazebo-GO2) — 该项目基于ROS2和Ignition Gazebo构建了Unitree GO2机器人的仿真环境，提供了机器人模型、传感器配置及基本控制接口，便于在Gazebo中进行算法开发与测试。其核心功能包括URDF/SDF模型集成、ROS2控制节点通信以及与GO2硬件接口的初步对齐，适合希望在开源仿真平台中快速部署GO2相关算法的开发者使用。 ![GitHub stars](https://img.shields.io/github/stars/yanyuze1/ROS2-Gazebo-GO2?style=social)

- [isaaclab-Unitree-aws](https://github.com/adferchavarro/isaaclab-Unitree-aws) — 该项目提供了一个基于 Docker 的仿真环境，用于在 Azure 云服务上训练 Unitree G1 机器人，依托 Isaac Lab 仿真平台实现强化学习训练流程。其核心是将 Isaac Lab 与 Unitree G1 模型集成，并通过容器化部署到 AWS/Azure 云基础设施，便于远程大规模训练。主要面向希望利用云端资源进行 Unitree G1 强化学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/adferchavarro/isaaclab-Unitree-aws?style=social)

- [Humanoid-robot-unitree-g1](https://github.com/prathimaAnand/Humanoid-robot-unitree-g1) — 该项目基于ROS2和Gazebo为Unitree G1人形机器人搭建仿真环境，集成LiDAR与摄像头传感器，并利用MoveIt实现运动规划。其核心目标是为G1提供开箱即用的感知与控制仿真框架，适用于研究人形机器人导航与操作任务的开发者。 ![GitHub stars](https://img.shields.io/github/stars/prathimaAnand/Humanoid-robot-unitree-g1?style=social)

- [unitreeGO2_ros_ws](https://github.com/sunqiao0507/unitreeGO2_ros_ws) — 该项目是赵虚左课程的配套代码，基于ROS构建了面向Unitree Go2机器人的开发工作空间，提供了基础控制与通信接口。其核心功能包括机器人状态订阅、命令发布及与Go2底层驱动的集成，适用于学习和二次开发Unitree Go2的ROS应用。目标用户为希望快速上手Unitree Go2 ROS开发的初学者或教育场景使用者。 ![GitHub stars](https://img.shields.io/github/stars/sunqiao0507/unitreeGO2_ros_ws?style=social)

- [BLE-Unitree-GO2-Controller](https://github.com/7emotions/BLE-Unitree-GO2-Controller) — 该项目提供基于蓝牙的宇树Go2机械狗遥控控制功能，使用C++开发，通过BLE协议实现与Unitree Go2的通信，允许用户发送基础运动指令。项目直接面向Unitree Go2硬件，属于轻量级远程操控工具，适合需要快速部署蓝牙控制方案的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/7emotions/BLE-Unitree-GO2-Controller?style=social)

- [Unitree-Go2](https://github.com/JAY-Yaser/Unitree-Go2) — 该项目提供宇树Go2机器人的基础运动控制代码，使用Python实现对Go2的步态和基本动作的驱动逻辑。项目直接面向Unitree Go2硬件，包含底层运动指令封装和简单行为示例，适合希望快速上手Go2运动控制的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/JAY-Yaser/Unitree-Go2?style=social)

- [unitree_go2_description](https://github.com/mlisi1/unitree_go2_description) — 该项目为 Unitree Go2 机器人提供 URDF 描述文件，便于在 ROS 或仿真环境中进行建模与控制开发。其核心功能是定义 Go2 的连杆、关节及物理属性，支持与 Gazebo、RViz 等工具集成。主要面向使用 ROS 开发 Unitree Go2 应用的机器人工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/mlisi1/unitree_go2_description?style=social)

- [Go2-ROS](https://github.com/sharpworks-dev/Go2-ROS) — 该项目为 Unitree Go2 机器人提供了一个 ROS 工作空间，用于支持其毕业设计项目。它集成了 Go2 的 ROS 驱动与控制接口，便于在 ROS 生态中开发感知、导航或控制算法。目标用户为基于 Go2 进行学术或工程开发的 ROS 开发者。 ![GitHub stars](https://img.shields.io/github/stars/sharpworks-dev/Go2-ROS?style=social)

- [unitree_mujoco_ros](https://github.com/EndiRos/unitree_mujoco_ros) — 该项目在MuJoCo仿真环境中实现了Unitree Go2机器人的ROS 2接口，采用类似42 School的项目结构风格。它通过ROS 2与MuJoCo集成，支持对Go2进行仿真控制和算法开发，主要面向希望在高保真物理仿真中测试控制策略的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/EndiRos/unitree_mujoco_ros?style=social)

- [go2_custom_sdk](https://github.com/JHyoonirl/go2_custom_sdk) — 该项目提供 Unitree Go2 机器人的可视化代码，主要用于实时显示机器人状态和传感器数据。通过 Python 实现与 Go2 SDK 的集成，支持关节角度、IMU 数据等关键信息的图形化展示，便于开发者调试和监控机器人运行状态。适用于基于 Unitree Go2 进行二次开发的工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/JHyoonirl/go2_custom_sdk?style=social)

- [Unitree_Go2_Development](https://github.com/kennethPakChungNg/Unitree_Go2_Development) — 该项目为 Unitree Go2-W 提供二次开发支持，主要使用 Python 实现对机器人底层控制接口的封装与扩展。项目聚焦于简化 Go2-W 的运动控制和传感器数据读取，便于开发者快速构建上层应用。目标用户为希望在 Go2-W 平台上进行算法验证或功能拓展的机器人研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/kennethPakChungNg/Unitree_Go2_Development?style=social)

- [unitree-go2-gazebo-ros2](https://github.com/YasiruDEX/unitree-go2-gazebo-ros2) — 该项目为 Unitree Go2 机器人提供 Gazebo 仿真环境与 ROS 2 集成支持，主要功能包括在 Gazebo 中加载 Go2 的 URDF 模型、配置控制器并通过 ROS 2 接口实现基本运动控制。项目基于 C++ 开发，利用 ROS 2 控制框架（如 ros2_control）和 Gazebo Classic 实现硬件抽象与仿真交互，适用于希望在开源仿真环境中开发或测试 Go2 控制算法的开发者。 ![GitHub stars](https://img.shields.io/github/stars/YasiruDEX/unitree-go2-gazebo-ros2?style=social)

- [Mujoco-Unitree-GO2](https://github.com/MateuszJania/Mujoco-Unitree-GO2) — 该项目为 Unitree Go2 机器人提供 MuJoCo 仿真环境下的动力学建模与控制接口，包含 URDF 模型和基础运动控制示例。通过 C++ 实现与 MuJoCo 物理引擎的集成，支持在仿真中测试 Go2 的步态与平衡策略。适用于希望在 MuJoCo 中开发或验证 Unitree Go2 控制算法的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/MateuszJania/Mujoco-Unitree-GO2?style=social)

- [ITU_Unitree_go2_ENRO](https://github.com/TheKhaggard/ITU_Unitree_go2_ENRO) — 该项目为ITU ENRO团队针对Unitree Go2机器人开发的软件与电子系统代码库，主要提供底层硬件驱动和嵌入式控制逻辑。项目使用C++实现，包含与Go2通信接口的定制化模块，适用于需要深度硬件集成的科研或竞赛场景。目标用户为参与ENRO项目的成员及对Go2底层开发感兴趣的工程师。 ![GitHub stars](https://img.shields.io/github/stars/TheKhaggard/ITU_Unitree_go2_ENRO?style=social)

- [unitree_g1_ros2_rviz](https://github.com/louis9RM/unitree_g1_ros2_rviz) — 该项目为 Unitree G1 人形机器人提供 ROS2 环境下的 RViz 可视化支持，主要功能包括机器人状态显示、关节控制界面和传感器数据可视化。通过集成 ROS2 的 URDF 模型与 RViz 插件，实现对 G1 本体的实时监控与交互，便于开发者调试运动控制或感知算法。目标用户为基于 ROS2 开发 Unitree G1 应用的机器人工程师。 ![GitHub stars](https://img.shields.io/github/stars/louis9RM/unitree_g1_ros2_rviz?style=social)

- [Bulan-Unitree-G1-edu-robot](https://github.com/BauyrzhanAskarov/Bulan-Unitree-G1-edu-robot) — 该项目旨在为Unitree G1人形机器人提供教育用途的集成方案，主要功能包括基础控制接口封装与教学示例代码。项目直接面向Unitree-G1硬件平台，通过简化API调用和提供ROS 2兼容的通信框架，降低教育场景下的开发门槛。目标用户为高校师生及机器人教育工作者。 ![GitHub stars](https://img.shields.io/github/stars/BauyrzhanAskarov/Bulan-Unitree-G1-edu-robot?style=social)

- [Unitree_G1_Description](https://github.com/BrennoDom/Unitree_G1_Description) — 该项目为Unitree G1人形机器人的URDF/SDF模型描述文件，提供机器人本体的结构与关节定义，便于在Gazebo、RViz等ROS工具中进行可视化和仿真。其核心价值在于为G1开发者提供标准化的机器人描述基础，支持后续运动控制、SLAM或导航等上层应用开发。目标用户为基于Unitree G1开展算法研究或应用开发的ROS工程师与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/BrennoDom/Unitree_G1_Description?style=social)

- [-Unitree-G1-simulation-with-pybullet](https://github.com/SIMMONA-hub/-Unitree-G1-simulation-with-pybullet) — 该项目基于 PyBullet 物理引擎构建了 Unitree G1 人形机器人的仿真环境，为开发者提供了一个轻量级、开源的模拟平台用于算法开发与测试。其核心功能包括 G1 机器人模型导入、关节控制接口封装以及基础运动示例，便于快速验证控制策略。目标用户为希望在低成本仿真环境中研究 Unitree G1 动力学行为和控制算法的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/SIMMONA-hub/-Unitree-G1-simulation-with-pybullet?style=social)

- [b2_description](https://github.com/Wuhall/b2_description) — 该项目提供 Unitree B2 机器人的 URDF 模型文件，用于在 ROS 或仿真环境中进行运动学与动力学建模。作为基础描述文件，它为基于 B2 的上层控制、规划或仿真开发提供了必要的机器人结构定义。适合需要在自定义仿真或 ROS 应用中集成 Unitree B2 的开发者使用。 ![GitHub stars](https://img.shields.io/github/stars/Wuhall/b2_description?style=social)

- [g1-record-and-replay](https://github.com/meetsitaram/g1-record-and-replay) — 该项目旨在为Unitree G1人形机器人提供动作录制与回放功能，通过Python实现对机器人关节轨迹的记录和重放，便于行为复现与调试。其直接面向Unitree-G1硬件平台，利用官方SDK或底层通信接口获取传感器与执行器数据，适用于需要快速验证运动策略的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/meetsitaram/g1-record-and-replay?style=social)

- [Unitree-H1-Isaac-Sim-Navigation](https://github.com/bobbylammy71446307/Unitree-H1-Isaac-Sim-Navigation) — 该项目旨在为Unitree H1人形机器人提供基于Isaac Sim的导航仿真环境，利用NVIDIA Isaac Sim构建虚拟场景并集成ROS 2接口，支持路径规划与避障算法的开发测试。项目明确针对Unitree-H1型号，通过URDF模型加载和关节控制实现机器人运动仿真，适用于希望在高保真模拟器中验证导航策略的开发者。 ![GitHub stars](https://img.shields.io/github/stars/bobbylammy71446307/Unitree-H1-Isaac-Sim-Navigation?style=social)

- [unitree_go2_voice_control](https://github.com/Gorilla79/unitree_go2_voice_control) — 该项目旨在为 Unitree Go2 机器人提供语音控制功能，通过 Python 实现语音指令识别与机器人动作映射。项目直接面向 Unitree-Go2 型号，利用其 SDK 或 API 接口实现控制指令下发，适用于希望扩展人机交互方式的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Gorilla79/unitree_go2_voice_control?style=social)

- [unitree-go2-development](https://github.com/Violet-Ever86/unitree-go2-development) — 该项目针对宇树科技 Unitree-Go2 机器人进行二次开发，主要提供基于 Python 的控制脚本与接口封装，便于开发者快速实现自定义运动逻辑或高层任务。项目虽尚处早期阶段（无星标），但明确聚焦 Go2 硬件，包含底层通信和运动控制相关代码，适合希望在真实 Go2 平台上进行原型验证的开发者。 ![GitHub stars](https://img.shields.io/github/stars/Violet-Ever86/unitree-go2-development?style=social)

- [go2_hardware](https://github.com/Unitree-Go2-Robot/go2_hardware) — 该项目为 Unitree Go2 机器人提供硬件相关支持，可能包含底层驱动、接口定义或硬件配置文件。作为官方组织 Unitree-Go2-Robot 旗下的仓库，其命名和归属明确指向 Go2 机型的硬件集成，目标用户为需要直接与 Go2 硬件交互的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Unitree-Go2-Robot/go2_hardware?style=social)

- [unitree-g1-public](https://github.com/mkrcek/unitree-g1-public) — 该项目旨在为Unitree G1人形机器人提供公开的控制或开发接口，可能包含底层驱动、运动控制或API封装等核心功能。由于明确以Unitree-G1为命名且仓库专为此型号设立，表明其与该机器人存在直接集成关系。目标用户为基于G1进行二次开发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/mkrcek/unitree-g1-public?style=social)

- [unitree-g1-course-china](https://github.com/Michdo93/unitree-g1-course-china) — 该项目为面向 Unitree G1 人形机器人的中文课程配套代码，主要提供基于 C++ 的基础控制示例和教学材料，帮助开发者快速上手 G1 机器人编程。项目直接针对 Unitree-G1 硬件平台，包含底层接口调用和运动控制逻辑，适用于教育和入门级开发场景。 ![GitHub stars](https://img.shields.io/github/stars/Michdo93/unitree-g1-course-china?style=social)

- [Unitree_go2_human_following](https://github.com/Gorilla79/Unitree_go2_human_following) — 该项目旨在实现 Unitree Go2 机器人的人体跟随功能，利用 Python 编写控制逻辑，通过传感器数据识别人体目标并驱动机器人进行自主跟踪。项目直接面向 Unitree-Go2 平台开发，可能集成其官方 SDK 或 ROS 接口以实现底层运动控制，适用于希望快速部署跟随应用的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Gorilla79/Unitree_go2_human_following?style=social)

- [Voice-Control-Unitree-Go2](https://github.com/romerik/Voice-Control-Unitree-Go2) — 该项目旨在通过语音指令控制 Unitree Go2 机器人，利用 Python 实现语音识别与机器人动作指令的映射。项目直接面向 Unitree-Go2 型号，可能通过官方 SDK 或 ROS 接口与其通信，适用于希望探索人机交互或无障碍控制的开发者。 ![GitHub stars](https://img.shields.io/github/stars/romerik/Voice-Control-Unitree-Go2?style=social)

- [unitree-g1-teleop](https://github.com/lagessiehcs/unitree-g1-teleop) — 该项目旨在为Unitree G1人形机器人提供遥操作（teleoperation）功能，通过Python实现远程控制接口，可能利用动作捕捉设备或手柄输入映射到机器人关节运动。项目直接面向Unitree-G1硬件平台，目标用户为希望快速部署G1遥操作能力的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/lagessiehcs/unitree-g1-teleop?style=social)

- [UnitreeGo2Communication](https://github.com/tiffanymatthe/UnitreeGo2Communication) — 该项目旨在实现与 Unitree Go2 机器人的通信功能，提供基于 Python 的底层接口用于发送控制指令和接收状态数据。项目直接面向 Unitree-Go2 型号，可能涉及官方 SDK 或 UDP/CAN 协议交互，适用于希望快速接入 Go2 进行二次开发的机器人研究人员或工程师。 ![GitHub stars](https://img.shields.io/github/stars/tiffanymatthe/UnitreeGo2Communication?style=social)

- [Unitree-Go2-Automated-Home-Inspector](https://github.com/OGscamp/Unitree-Go2-Automated-Home-Inspector) — 该项目旨在将 Unitree Go2 机器人用于家庭自动巡检任务，通过 Python 实现环境感知与路径规划功能。项目直接面向 Unitree-Go2 平台开发，利用其移动底盘和传感器接口进行室内场景建图与异常检测，适用于智能家居或安防领域的开发者与研究者。 ![GitHub stars](https://img.shields.io/github/stars/OGscamp/Unitree-Go2-Automated-Home-Inspector?style=social)

- [unitree-go2-slam-nav](https://github.com/SHEN00001/unitree-go2-slam-nav) — 该项目旨在为 Unitree Go2 机器人提供 SLAM 与导航功能，基于 C++ 实现，可能集成 ROS 或类似框架以支持定位建图和路径规划。虽然仓库尚无详细描述和星标，但其命名明确指向 Unitree-Go2 的自主导航应用场景，目标用户为希望在 Go2 平台上开发或部署 SLAM 系统的开发者。 ![GitHub stars](https://img.shields.io/github/stars/SHEN00001/unitree-go2-slam-nav?style=social)

- [unitree-go2-slam-toolbox](https://github.com/2473o/unitree-go2-slam-toolbox) — 该项目旨在为 Unitree Go2 机器人提供 SLAM（同步定位与地图构建）功能，基于 C++ 实现，可能集成如 LIO-SAM 或 RTAB-Map 等主流 SLAM 框架以适配 Go2 的传感器配置。项目明确针对 Unitree-Go2 平台开发，目标用户为需要在该机器人上实现自主导航与环境建图的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/2473o/unitree-go2-slam-toolbox?style=social)

- [Unitree-Go2-Navigation-and-Slam](https://github.com/houshoulaopo-crypto/Unitree-Go2-Navigation-and-Slam) — 该项目旨在为Unitree Go2机器人提供导航与SLAM（同步定位与地图构建）功能，可能包含基于ROS或ROS 2的实现，用于在未知环境中进行自主建图与路径规划。项目直接面向Unitree-Go2平台开发，目标用户为希望在其上部署自主导航能力的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/houshoulaopo-crypto/Unitree-Go2-Navigation-and-Slam?style=social)

- [Robot-Locomotion-Navigation-with-Obstacle-Avoidance](https://github.com/JojenJ/Robot-Locomotion-Navigation-with-Obstacle-Avoidance) — 该项目结合 Open Duck 双足运动控制与基于深度强化学习的导航避障系统，并集成了 Unitree GO2 机器人平台，利用 neuPAN 实现感知与导航。项目通过 DRL 算法实现动态环境中的自主移动，适用于 Unitree GO2 的实际部署场景，目标用户为机器人导航与强化学习研究者。 ![GitHub stars](https://img.shields.io/github/stars/JojenJ/Robot-Locomotion-Navigation-with-Obstacle-Avoidance?style=social)

- [maya2mujoco](https://github.com/luckyrobots/maya2mujoco) — 该项目旨在将Autodesk Maya中制作的角色动画导入MuJoCo仿真环境，支持Unitree-G1人形机器人的运动重定向。通过解析Maya动画数据并转换为MuJoCo兼容的XML模型与动作序列，实现高保真动画在物理仿真中的复现。主要面向需要将专业动画工具与机器人仿真结合的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/luckyrobots/maya2mujoco?style=social)

- [biscuit-telemetry-investigation](https://github.com/NayiemW/biscuit-telemetry-investigation) — 该项目旨在调查 Unitree Go2 Pro 机器人在运行过程中是否存在遥测数据收集行为，通过 Python 脚本分析网络流量和系统日志，识别潜在的数据外传证据。项目聚焦于 Go2 Pro 的固件通信机制，帮助用户了解隐私风险。主要面向关注数据安全与隐私的 Unitree 机器人开发者和终端用户。 ![GitHub stars](https://img.shields.io/github/stars/NayiemW/biscuit-telemetry-investigation?style=social)

- [Bluetooth_GamePad-Lora_2_SBUS_Bridge](https://github.com/Corey-Harding/Bluetooth_GamePad-Lora_2_SBUS_Bridge) — 该项目实现了一个蓝牙游戏手柄通过LoRa无线模块向SBUS协议接收设备发送控制信号的桥接功能，明确以Unitree Go2四足机器人为应用示例，使用两块2.4GHz ELRS RC模块（如Radiomaster ER6或LilyGo T3 S3）完成远程遥控。其核心是将Xbox等蓝牙手柄输入转换为SBUS信号，适配支持SBUS的机器人控制器，为Unitree Go2提供了低成本、低延迟的远程操控方案，适合希望扩展Go2遥控方式的开发者或爱好者。 ![GitHub stars](https://img.shields.io/github/stars/Corey-Harding/Bluetooth_GamePad-Lora_2_SBUS_Bridge?style=social)

- [multirobot-sim-ros2](https://github.com/Vipsy-123/multirobot-sim-ros2) — 该项目为Unitree Go2机器人开发了ROS 2兼容的机器人描述模型，基于CHAMP腿式机器人研究仓库进行配置，支持多机器人仿真环境搭建。其核心在于提供URDF/SDF模型及ROS 2接口，便于在Gazebo等仿真器中集成Go2进行运动控制与感知算法测试。主要面向使用ROS 2进行Unitree Go2二次开发的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/Vipsy-123/multirobot-sim-ros2?style=social)

- [Unitree-Go2-Dockerfile](https://github.com/BenCaunt/Unitree-Go2-Dockerfile) — 该项目提供了一个Dockerfile，用于构建支持go2_ros2_sdk的容器环境，便于在隔离环境中开发和部署Unitree Go2机器人的ROS 2应用。它简化了依赖管理与环境配置，特别适合希望快速上手Go2 ROS 2 SDK的开发者。 ![GitHub stars](https://img.shields.io/github/stars/BenCaunt/Unitree-Go2-Dockerfile?style=social)

- [auto_shepherd](https://github.com/LCAS/auto_shepherd) — 该项目是 AutoShepherd 计划的子模块中心，旨在探索牧羊场景中的机器人自动化，明确包含对 Unitree-Go2 的支持。其通过 ROS2 Humble 构建系统，并整合计算机视觉与仿真技术，用于多机器人协同牧羊任务。目标用户为农业自动化及四足机器人应用研究者。 ![GitHub stars](https://img.shields.io/github/stars/LCAS/auto_shepherd?style=social)

- [Unitree-g1-intell-cam](https://github.com/odnokolov/Unitree-g1-intell-cam) — 该项目为Unitree G1机器人搭载的Intel RealSense相机提供QR码识别功能，通过Python实现基于OpenCV的实时二维码检测与解码。项目直接面向G1平台的视觉感知需求，利用RealSense深度相机获取图像流并进行处理，适用于需要视觉导航或目标识别的G1应用场景。 ![GitHub stars](https://img.shields.io/github/stars/odnokolov/Unitree-g1-intell-cam?style=social)

- [Godot_Robot_Simulation](https://github.com/z-mahmud22/Godot_Robot_Simulation) — 该项目提供了一套从ROS的URDF文件中提取关节与连杆信息，并在Godot 4引擎中加载和交互Unitree G1机器人模型的流程指南。通过C#脚本实现URDF解析与Godot场景构建，支持对Unitree-G1的可视化仿真，适用于希望在轻量级游戏引擎中快速原型化Unitree机器人行为的开发者。 ![GitHub stars](https://img.shields.io/github/stars/z-mahmud22/Godot_Robot_Simulation?style=social)

- [RasPi-YOLO-Unitree-Weapons-Detection-Deployment](https://github.com/MaxLangsam/RasPi-YOLO-Unitree-Weapons-Detection-Deployment) — 该项目旨在训练并部署基于YOLO的武器检测模型，运行于树莓派AI相机或AI HAT上，并专为Unitree GO2 Pro机器人平台集成。通过轻量化YOLO模型实现实时目标检测，利用树莓派与GO2 Pro的硬件协同完成边缘端推理，适用于安防巡检等场景。主要面向希望在Unitree机器人上实现智能视觉感知的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/MaxLangsam/RasPi-YOLO-Unitree-Weapons-Detection-Deployment?style=social)

- [tact-go2](https://github.com/bhaptics/tact-go2) — 该项目名为 tact-go2，由 bhaptics 开发，旨在为 Unitree Go2 机器人提供触觉反馈集成支持。通过与 bhaptics 触觉设备（如 TactSuit）联动，项目可能实现机器人运动状态或环境交互的体感映射，使用 Go 语言开发并持续维护至 2025 年。主要面向希望在 Unitree-Go2 上探索沉浸式遥操作或人机交互体验的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/bhaptics/tact-go2?style=social)

- [Unitree_go2_edu_hackathon](https://github.com/SimTheGreat/Unitree_go2_edu_hackathon) — 该项目为 Unitree Go2 机器人提供教育用途的黑客松示例代码，主要面向学生和开发者快速上手 Go2 的基础控制与感知功能。仓库包含基于 Python 的简单控制脚本，可能涉及 ROS 或 SDK 接口调用，适用于教学和原型开发场景。尽管缺乏详细文档，但其明确针对 Unitree-Go2 平台，符合教育类工具定位。 ![GitHub stars](https://img.shields.io/github/stars/SimTheGreat/Unitree_go2_edu_hackathon?style=social)

- [mygo2](https://github.com/exat500g/mygo2) — 该项目旨在为Unitree Go2机器人提供仿真测试环境，使用Python实现基础的模拟功能。项目明确针对Unitree-Go2型号，可能涉及运动控制或传感器仿真的初步验证，适合希望在部署前进行算法测试的开发者。尽管目前缺乏详细文档和社区支持，但其专用性符合Unitree生态工具的基本定位。 ![GitHub stars](https://img.shields.io/github/stars/exat500g/mygo2?style=social)

- [Unitree_go2_waking](https://github.com/katsuchi23/Unitree_go2_waking) — 该项目旨在实现 Unitree Go2 机器人的唤醒控制功能，通过 Python 脚本与机器人底层通信接口交互，完成上电初始化和站立启动流程。项目直接面向 Unitree-Go2 硬件，利用其官方 SDK 或 UDP 控制协议发送运动指令，适用于需要自动化启动四足机器人的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/katsuchi23/Unitree_go2_waking?style=social)

- [go2_ros2_ws](https://github.com/rotematari/go2_ros2_ws) — 该项目是一个基于 ROS 2 的工作空间，旨在为 Unitree Go2 四足机器人提供基础通信与控制接口。通过 Python 实现与 Go2 的底层驱动交互，可能包含状态订阅、命令发布等基本功能，适用于希望在 ROS 2 生态中快速接入 Go2 的开发者。尽管缺乏详细文档，但其命名和结构明确指向 Unitree-Go2 的集成支持。 ![GitHub stars](https://img.shields.io/github/stars/rotematari/go2_ros2_ws?style=social)

- [Unitree-Go2-multi-floor-drive](https://github.com/lsh356812/Unitree-Go2-multi-floor-drive) — 该项目旨在实现 Unitree Go2 机器人在多楼层环境中的自主导航与驱动控制，通过 C++ 开发底层运动逻辑，并可能结合外部定位或地图切换机制以适应不同楼层场景。项目直接面向 Unitree-Go2 硬件平台，目标用户为希望拓展 Go2 在复杂建筑环境中应用的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/lsh356812/Unitree-Go2-multi-floor-drive?style=social)

- [project-unitree-go2-interface](https://github.com/Iftiarchowdhury/project-unitree-go2-interface) — 该项目旨在为Unitree Go2机器人提供Python接口，便于开发者进行控制与交互。虽然仓库目前缺乏详细描述和文档，但其命名明确指向Unitree-Go2的专用接口开发，可能涉及SDK封装或通信协议实现。适合希望用Python快速接入Go2硬件的开发者使用。 ![GitHub stars](https://img.shields.io/github/stars/Iftiarchowdhury/project-unitree-go2-interface?style=social)

- [Isaac-Unitree-Go2](https://github.com/vpraise00/Isaac-Unitree-Go2) — 该项目旨在基于 Isaac Gym 或 Isaac Sim 为 Unitree Go2 机器人搭建强化学习或仿真控制环境，从仓库名称和命名惯例可推断其目标是实现 Go2 在 NVIDIA Isaac 平台上的集成。虽然缺乏详细描述和文档，但其命名明确指向 Unitree-Go2 的仿真支持，可能包含基础运动控制或策略训练框架。主要面向希望在 Isaac 生态中开发 Go2 算法的机器人研究人员或开发者。 ![GitHub stars](https://img.shields.io/github/stars/vpraise00/Isaac-Unitree-Go2?style=social)

- [Unitree_g1](https://github.com/ianzhaoyh/Unitree_g1) — 该项目为Unitree G1人形机器人提供Python接口或控制示例，可能涉及运动控制或通信协议实现。尽管仓库缺乏详细描述，但其命名明确指向Unitree-G1型号，暗示专为其开发的底层交互工具。适合希望直接与G1硬件或仿真环境对接的开发者使用。 ![GitHub stars](https://img.shields.io/github/stars/ianzhaoyh/Unitree_g1?style=social)

- [unitree-g1-fall-prediction](https://github.com/dengXlong/unitree-g1-fall-prediction) — 该项目旨在为Unitree G1人形机器人开发跌倒预测功能，通过传感器数据分析实时判断机器人稳定性状态。虽然仓库目前缺乏详细说明和代码细节，但其命名明确指向Unitree-G1平台，目标是提升该机器人在复杂环境中的安全性和自主恢复能力。适用于关注人形机器人运动安全的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/dengXlong/unitree-g1-fall-prediction?style=social)

- [Unitree_G1_dev](https://github.com/kumar-abhina/Unitree_G1_dev) — 该项目为Unitree G1人形机器人的开发仓库，主要提供基于Python的控制与接口工具。虽然缺乏详细说明，但其命名和主题明确指向Unitree-G1硬件平台，可能包含底层通信、运动控制或API封装等核心功能。适合G1开发者用于二次开发或算法部署。 ![GitHub stars](https://img.shields.io/github/stars/kumar-abhina/Unitree_G1_dev?style=social)

- [unitree_g1_project](https://github.com/Allimpose/unitree_g1_project) — 该项目旨在为Unitree G1人形机器人提供控制或应用开发支持，从仓库名称和所属生态可判断其面向Unitree-G1平台。尽管缺乏详细描述，但命名规范和更新活跃性表明其可能包含G1相关的接口封装、运动控制或示例代码。目标用户为基于Unitree G1进行二次开发的科研或工程人员。 ![GitHub stars](https://img.shields.io/github/stars/Allimpose/unitree_g1_project?style=social)

- [unitree-g1-control-panel](https://github.com/lagessiehcs/unitree-g1-control-panel) — 该项目是一个面向 Unitree G1 人形机器人的控制面板工具，使用 Python 开发，旨在提供对机器人关节状态、运动指令或传感器数据的可视化与交互控制。尽管当前仓库缺乏详细说明和文档，但其命名明确指向 Unitree-G1 型号，表明其专为该平台设计，可能通过官方 SDK 或 ROS 接口实现底层通信。目标用户为希望快速调试或监控 G1 机器人状态的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/lagessiehcs/unitree-g1-control-panel?style=social)

- [unitree-go2](https://github.com/LibraJoy/unitree-go2) — 该项目旨在为 Unitree Go2 机器人提供控制或开发支持，从仓库名称和更新时间来看，可能包含针对该机型的驱动、接口或示例代码。尽管缺乏详细描述和星标，但其命名明确指向 Unitree-Go2，表明专用于此硬件平台。目标用户为希望在 Go2 上进行二次开发或集成新功能的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/LibraJoy/unitree-go2?style=social)

- [unitree_go2_edu](https://github.com/is-buiquocdoanh/unitree_go2_edu) — 该项目旨在为 Unitree Go2 机器人提供教育用途的 Python 控制示例或工具包，可能包含基础运动控制、传感器数据读取或简单行为实现。尽管缺乏详细描述和社区关注（0 stars），但其命名明确指向 Unitree-Go2 教育场景，推测面向学生或初学者开发者进行机器人编程入门。由于直接针对 Unitree Go2 且聚焦教育应用，符合特定集成范畴。 ![GitHub stars](https://img.shields.io/github/stars/is-buiquocdoanh/unitree_go2_edu?style=social)

- [unitree-go2](https://github.com/KosarBehnia/unitree-go2) — 该项目旨在为 Unitree Go2 四足机器人提供 Python 接口或控制工具，从仓库名称和更新时间看可能处于早期开发阶段。虽然缺乏详细描述和星标，但其命名明确指向 Unitree-Go2，暗示直接集成意图。目标用户为希望用 Python 快速开发 Go2 应用的开发者。 ![GitHub stars](https://img.shields.io/github/stars/KosarBehnia/unitree-go2?style=social)

- [Unitree-Go2-Robot.github.io](https://github.com/Unitree-Go2-Robot/Unitree-Go2-Robot.github.io) — 该项目为 Unitree Go2 机器人提供官方文档和资源托管页面，通过 GitHub Pages 展示技术资料与使用指南。虽然当前仓库内容有限且主要使用 Batchfile 脚本，但其域名和组织名称明确指向 Unitree-Go2，属于官方信息分发渠道。适合需要获取 Go2 官方资料的开发者参考。 ![GitHub stars](https://img.shields.io/github/stars/Unitree-Go2-Robot/Unitree-Go2-Robot.github.io?style=social)

- [Unitree-Go2-Control](https://github.com/7Swaize/Unitree-Go2-Control) — 该项目旨在为Unitree Go2四足机器人提供控制相关的Python实现，可能涉及运动控制或底层接口封装。由于仓库缺乏详细描述、文档和星标，其具体功能与技术实现尚不明确，但项目名称直接包含'Unitree-Go2'，表明其目标是面向该机型的控制开发。适合希望基于Python快速实验Go2控制策略的开发者，但需谨慎评估代码成熟度。 ![GitHub stars](https://img.shields.io/github/stars/7Swaize/Unitree-Go2-Control?style=social)

- [Unitree_go2_manuvering](https://github.com/arvijack003/Unitree_go2_manuvering) — 该项目旨在实现 Unitree Go2 机器人的自主机动控制，提供了针对该机型的运动规划与底层控制接口。项目直接面向 Unitree-Go2 硬件，可能涉及 ROS 或 SDK 集成以实现基本移动功能，适合希望在 Go2 上开发自定义行为的个人开发者或研究者。 ![GitHub stars](https://img.shields.io/github/stars/arvijack003/Unitree_go2_manuvering?style=social)

- [go2_webrtc_connect](https://github.com/amznhacker/go2_webrtc_connect) — 该项目旨在通过 WebRTC 技术实现对 Unitree Go2 机器人的远程连接与控制。虽然目前缺乏详细文档和功能说明，但其命名和关键词明确指向 Unitree-Go2 的实时通信集成，可能用于低延迟视频流或指令传输。目标用户为希望基于 WebRTC 构建远程操控系统的 Go2 开发者。 ![GitHub stars](https://img.shields.io/github/stars/amznhacker/go2_webrtc_connect?style=social)

- [Go2RobodogGPT](https://github.com/lthienvu265-coder/Go2RobodogGPT) — 该项目旨在为Unitree Go2机器人提供基于GPT的智能交互或控制功能，可能涉及自然语言指令解析或行为生成。虽然具体实现细节不明确，但其命名直接关联Unitree-Go2，表明专为其设计。目标用户为希望在Go2上集成大语言模型能力的开发者或研究者。 ![GitHub stars](https://img.shields.io/github/stars/lthienvu265-coder/Go2RobodogGPT?style=social)

- [go2](https://github.com/NahinMartinez/go2) — 该项目旨在为 Unitree Go2 机器人提供 C++ 控制接口或驱动支持，可能涉及底层通信协议或运动控制实现。尽管缺乏详细描述和社区关注（0 stars），但其命名和目标平台明确指向 Unitree-Go2，属于硬件适配类项目。适合希望直接通过 C++ 开发 Go2 应用的开发者参考。 ![GitHub stars](https://img.shields.io/github/stars/NahinMartinez/go2?style=social)

- [unitree_go2](https://github.com/alejandrogomezl/unitree_go2) — 该项目旨在为 Unitree Go2 机器人提供 Python 接口或控制工具，从仓库名称和命名惯例可推断其目标是实现对 Go2 的通信、状态读取或运动控制。尽管缺乏详细描述和星标，但其命名明确指向 Unitree-Go2，可能涉及 UDP 通信协议或官方 SDK 的封装。适用于希望用 Python 快速接入 Go2 硬件的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/alejandrogomezl/unitree_go2?style=social)

- [unitree_go2_setup](https://github.com/Gorilla79/unitree_go2_setup) — 该项目旨在为 Unitree Go2 机器人提供系统配置与环境搭建支持，可能包含固件设置、依赖安装或开发环境初始化脚本。尽管缺乏详细描述，但其命名明确指向 Unitree-Go2 的专用配置工具，适用于希望快速部署开发环境的用户。 ![GitHub stars](https://img.shields.io/github/stars/Gorilla79/unitree_go2_setup?style=social)

- [HIMLOCO_GO2](https://github.com/KurehaTian/HIMLOCO_GO2) — 该项目旨在为Unitree Go2机器人提供运动控制或行为策略的实现，从仓库名称'HIMLOCO_GO2'可推断其聚焦于Go2平台的本体运动（locomotion）能力。尽管缺乏详细描述，但命名明确指向Unitree-Go2型号，可能涉及底层控制、步态生成或强化学习策略。目标用户为希望在Go2上开发或测试运动算法的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/KurehaTian/HIMLOCO_GO2?style=social)

- [go2move](https://github.com/SvyatoslavSokolov/go2move) — 该项目旨在为 Unitree Go2 机器人提供运动控制功能，使用 Python 实现与 Go2 的通信和基础移动指令发送。虽然目前缺乏详细文档和功能说明，但其命名和目标明确指向 Unitree-Go2 的直接控制，可能涉及官方 SDK 或 UDP 接口调用。适合希望快速尝试 Go2 基础运动控制的开发者。 ![GitHub stars](https://img.shields.io/github/stars/SvyatoslavSokolov/go2move?style=social)

- [UnitreeG1](https://github.com/taegyuw/UnitreeG1) — 该项目旨在为Unitree G1人形机器人提供控制或开发支持，可能包含接口封装、运动控制或示例代码。尽管仓库目前缺乏详细描述，但其命名明确指向Unitree-G1型号，表明其目标是与该机器人硬件或仿真环境集成。适合G1开发者或研究人员探索基础功能实现。 ![GitHub stars](https://img.shields.io/github/stars/taegyuw/UnitreeG1?style=social)

- [UnitreeG1Platform](https://github.com/CharlesPea/UnitreeG1Platform) — 该项目旨在为Unitree G1人形机器人提供一个基于Python的控制与开发平台，可能包含硬件接口封装、运动控制或感知模块等基础功能。虽然目前仓库缺乏详细描述和文档，但其命名明确指向Unitree-G1专属支持，若完成将有助于开发者快速构建上层应用。目标用户为希望在G1平台上进行算法验证或应用开发的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/CharlesPea/UnitreeG1Platform?style=social)

- [test-unitree-g1](https://github.com/Kibiandkimi/test-unitree-g1) — 该项目旨在测试 Unitree G1 人形机器人的控制或接口功能，从仓库名称和更新时间可推断其针对 Unitree-G1 开发。尽管缺乏详细描述和星标，但其命名明确指向 Unitree G1 机器人，可能包含基础通信、运动控制或 SDK 集成代码。目标用户为希望快速验证 G1 功能的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Kibiandkimi/test-unitree-g1?style=social)

- [unitree_g1_reverse](https://github.com/circuluspibo/unitree_g1_reverse) — 该项目尝试对 Unitree G1 机器人进行逆向工程，主要通过分析其 Android 应用的 Smali 代码来理解通信协议或控制逻辑。虽然缺乏详细文档和功能说明，但其明确针对 Unitree-G1 型号，可能为开发者提供底层接口洞察。目标用户为希望深入理解或扩展 G1 功能的高级开发者。 ![GitHub stars](https://img.shields.io/github/stars/circuluspibo/unitree_g1_reverse?style=social)

- [UNITREE-G1-ROBOT-MODEL](https://github.com/aries444444/UNITREE-G1-ROBOT-MODEL) — 该项目旨在为 Unitree G1 人形机器人提供基础的机器人模型支持，可能包含URDF或SDF格式的描述文件及基本接口。虽然仓库目前缺乏详细说明和文档，但其命名明确指向 Unitree-G1 机型，推测用于仿真环境（如Gazebo、Isaac Sim）或控制开发。适合需要 G1 本体模型进行二次开发的机器人研究人员或工程师。 ![GitHub stars](https://img.shields.io/github/stars/aries444444/UNITREE-G1-ROBOT-MODEL?style=social)

- [g1_sport_mode_ros](https://github.com/Michdo93/g1_sport_mode_ros) — 该项目旨在为Unitree G1人形机器人实现运动模式的ROS控制接口，通过Python开发，可能涉及对G1底层运动控制器的封装与调用。虽然目前缺乏详细描述和社区验证，但其命名明确指向Unitree-G1的特定功能扩展，目标用户为基于ROS开发G1高级运动控制的研究者或工程师。 ![GitHub stars](https://img.shields.io/github/stars/Michdo93/g1_sport_mode_ros?style=social)

- [humanoid_g1_ws](https://github.com/datvu352k4/humanoid_g1_ws) — 该项目是一个针对Unitree G1人形机器人的ROS工作空间，主要用于开发和部署G1相关的控制、感知或导航功能。仓库虽无详细描述，但其命名明确指向Unitree-G1平台，可能包含硬件驱动、运动控制或仿真接口等核心组件。适合G1开发者进行二次开发或算法集成。 ![GitHub stars](https://img.shields.io/github/stars/datvu352k4/humanoid_g1_ws?style=social)

- [unitree_g1](https://github.com/VALHEMSING/unitree_g1) — 该项目为 Unitree G1 人形机器人提供 Python 接口支持，可能用于控制或数据交互。尽管仓库缺乏详细描述和文档，但其命名明确指向 Unitree-G1，暗示与该机器人硬件或 SDK 的直接集成。目标用户为希望使用 Python 开发 G1 应用的开发者。 ![GitHub stars](https://img.shields.io/github/stars/VALHEMSING/unitree_g1?style=social)

- [comp0244-go2](https://github.com/COMP0244-S25/comp0244-go2) — 该项目为伦敦大学学院 COMP0244 课程的实践项目，旨在通过 C++ 开发与 Unitree Go2 机器人交互的控制或感知功能。尽管仓库尚无详细描述，但其命名明确指向 Unitree-Go2，且使用 C++ 实现，可能涉及官方 SDK 或低层通信接口。目标用户为参与该课程的学生及对 Go2 二次开发感兴趣的开发者。 ![GitHub stars](https://img.shields.io/github/stars/COMP0244-S25/comp0244-go2?style=social)

- [Go2Go](https://github.com/ASIG-X/Go2Go) — 该项目名为 Go2Go，主要用途是为 Unitree Go2 机器人提供运动控制或导航相关的功能实现。从项目名称和命名惯例可推测其与 Unitree-Go2 紧密相关，可能涉及底层驱动、步态控制或自主导航等关键技术。目标用户为基于 Go2 进行二次开发的科研人员或工程师。 ![GitHub stars](https://img.shields.io/github/stars/ASIG-X/Go2Go?style=social)

- [go2api](https://github.com/harshit777/go2api) — 该项目是一个用 Go 语言编写的 API 封装，旨在为 Unitree Go2 机器人提供便捷的控制接口。虽然仓库缺乏详细文档和功能说明，但其命名和上下文暗示了与 Unitree-Go2 的直接关联，可能用于发送运动指令或读取状态数据。目标用户为希望使用 Go 语言集成或控制 Go2 机器人的开发者。 ![GitHub stars](https://img.shields.io/github/stars/harshit777/go2api?style=social)

- [Unitree_go2_recognition](https://github.com/it5meyash/Unitree_go2_recognition) — 该项目旨在为Unitree Go2机器人实现目标识别功能，可能结合视觉感知与机器人控制。虽然仓库缺乏详细说明，但其命名明确指向Unitree-Go2平台，推测使用Python进行图像处理或深度学习推理。适合希望在Go2上部署视觉识别能力的开发者参考。 ![GitHub stars](https://img.shields.io/github/stars/it5meyash/Unitree_go2_recognition?style=social)

- [robotics-mcp](https://github.com/sandraschi/robotics-mcp) — 该项目实现多机器人协同系统，支持包括Unitree Go2/G1在内的多种硬件平台，通过共享LIDAR地图、协作式SLAM和射频运动检测实现物理与虚拟机器人的统一协调。其核心功能涵盖实时避障与跨平台通信，主要面向需要异构机器人集群协同作业的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/sandraschi/robotics-mcp?style=social)


---

<a id="related"></a>
## ⭐ 相关 Awesome 列表


---

<div align="center">

## 🤖 自动生成

此列表由 [Awesome-List-Generator](https://github.com/shaoxiang/Awesome-List-Generator) 自动维护。

使用 AI 发现、筛选并组织 Unitree_Robots 相关的高质量资源。

更新时间: 2026-02-04

</div>