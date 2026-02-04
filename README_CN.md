# Awesome Isaac Sim [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)[English](./README.md)
<a id="intro"></a>
## 📝 简介

NVIDIA Isaac Sim 是一个基于 Omniverse 构建的可扩展机器人仿真平台，利用 GPU 加速的多物理场和传感器模拟，为 AI 驱动的机器人开发提供高保真、高效率的虚拟环境。它深度集成 Isaac Lab、Isaac Gym 和新一代 Newton 物理引擎，支持从算法原型到大规模强化学习训练的全流程。本列表精心收录了官方文档、实战教程、开源项目与社区资源，助你快速掌握 Isaac Sim 的核心能力并构建下一代智能机器人系统。 关键关键词：Isaac Sim, Isaac Lab, Isaac Gym, Nvidia Newton。

<a id="scope"></a>
## 🎯 范围

- Isaac Sim 核心功能、架构与工作流
- Isaac Lab（用于机器人学习的模块化框架）
- Isaac Gym（GPU 加速的强化学习训练环境）
- NVIDIA Newton 物理引擎及其在 Isaac Sim 中的应用
- 基于 Isaac Sim 的开源项目、示例与最佳实践

<a id="criteria"></a>
## ✅ 收录标准

- 内容必须直接涉及 Isaac Sim 或其官方子组件（如 Isaac Lab、Isaac Gym、Newton）
- 优先收录官方文档、GitHub 官方仓库及 NVIDIA 技术博客
- 社区项目需具备清晰文档、活跃维护或显著影响力
- 教程或示例需可复现，并体现 Isaac Sim 的关键特性（如 GPU 加速、多传感器模拟、RL 训练等）

<a id="audience"></a>
## 👥 适用人群

面向机器人开发者、AI 研究人员、强化学习工程师以及对 GPU 加速仿真感兴趣的学术与工业界用户。

<a id="toc"></a>
## 📚 目录

- [简介](#intro)- [范围](#scope)- [收录标准](#criteria)- [适用人群](#audience)- [补充资源](#custom)- [论文与研究](#papers)
- [项目](#projects)
- [相关 Awesome 列表](#related)

---

<a id="custom"></a>
## 📌 补充资源

- [Isaac Sim 官方文档](https://docs.isaacsim.omniverse.nvidia.com/) - NVIDIA 官方提供的 Isaac Sim 平台完整技术文档，涵盖安装、核心功能、传感器模拟、机器人建模与强化学习集成等。
- [Isaac Lab 文档](https://isaac-sim.github.io/IsaacLab/) - 专为机器人学习设计的模块化框架，基于 Isaac Sim 构建，支持高性能 RL 训练与仿真。
- [robotsfan](https://www.robotsfan.com) - A blog of Ziqi Fan，包含 Isaac Sim 实战教程、环境配置技巧及机器人仿真项目分享。
- [Isaac Sim Discord 社区](https://discord.gg/wtXUhcDh) - 官方推荐的开发者交流频道，活跃讨论 Isaac Sim 使用、调试与扩展开发。
- [NVIDIA Omniverse Isaac Sim Community Discord](https://discord.gg/nyr6t33v) - 另一个活跃的社区入口，聚焦于 Omniverse 与 Isaac Sim 的集成应用。

### 补充资源

- [Isaac Gym: High-Performance GPU-Based Physics Simulation for RL (Paper)](https://arxiv.org/abs/2108.10470) - NVIDIA 发表的 Isaac Gym 技术论文，介绍其基于 GPU 的并行物理仿真架构，支撑大规模强化学习训练。
- [Isaac Gym Preview Release GitHub](https://github.com/NVIDIA-Omniverse/IsaacGymEnvs) - 官方开源的 Isaac Gym 环境集合，包含多种机器人任务（如 Ant、Humanoid、Allegro Hand）的 RL 示例。
- [NVIDIA Newton Physics Engine Announcement](https://developer.nvidia.com/blog/nvidia-newton-a-new-physics-engine-for-robotics-and-autonomous-machines/) - NVIDIA 官方博客介绍新一代物理引擎 Newton，未来将集成至 Isaac Sim，提供更精确、高效的多体动力学仿真。
- [Isaac Sim Tutorials on NVIDIA Developer](https://developer.nvidia.com/isaac-sim) - 官方开发者平台提供的入门到进阶教程，包括 URDF 导入、ROS/ROS2 桥接、相机/LiDAR 仿真等。
- [Isaac Lab GitHub Repository](https://github.com/isaac-sim/IsaacLab) - Isaac Lab 的开源代码库，包含模块化设计、RL 训练脚本、资产管理和可复现的基准环境。
- [Omniverse Isaac Sim YouTube Channel](https://www.youtube.com/playlist?list=PL5sXyKQg9qkFf9VZl6jJzWbBxYwRmT7dP) - NVIDIA 官方发布的 Isaac Sim 教程视频系列，涵盖环境搭建、机器人部署与 AI 训练流程。

---

<a id="papers"></a>
## 🔥 论文与研究

- ["BTGenBot-2: Efficient Behavior Tree Generation with Small Language Models" (2026)](http://arxiv.org/abs/2602.01870v1) [PDF](https://arxiv.org/pdf/2602.01870v1) — 本文提出BTGenBot-2，一个1B参数的开源小语言模型，能将自然语言任务描述和机器人动作原语直接转换为可执行的XML行为树，支持零样本生成与运行时错误恢复。该工作在NVIDIA Isaac Sim中构建了首个包含52个导航与操作任务的标准化行为树生成基准，并在此平台上完成全部评估实验。其轻量高效特性使其适用于资源受限的真实机器人系统，显著提升部署可行性。

- ["PolicyFlow: Policy Optimization with Continuous Normalizing Flow in Reinforcement Learning" (2026)](http://arxiv.org/abs/2602.01156v1) [PDF](https://arxiv.org/pdf/2602.01156v1) — 本文提出PolicyFlow，一种基于连续归一化流（CNF）的新型on-policy强化学习算法，通过在插值路径上利用速度场变化近似重要性比，避免了CNF全轨迹似然计算的高开销。该方法在IsaacLab等多个环境中验证有效，并引入受布朗运动启发的Brownian正则化器以提升策略多样性。研究展示了PolicyFlow在IsaacLab平台上的成功应用，为复杂策略建模提供了高效稳定的训练方案。

- ["WheelArm-Sim: A Manipulation and Navigation Combined Multimodal Synthetic Data Generation Simulator for Unified Control in Assistive Robotics" (2026)](http://arxiv.org/abs/2601.21129v1) [PDF](https://arxiv.org/pdf/2601.21129v1) — arXiv (Cornell University) — 本文提出WheelArm-Sim，一个基于Isaac Sim构建的合成数据生成仿真框架，用于联合控制轮椅与机械臂的辅助机器人系统。作者在Isaac Sim中开发了包含13项任务、232条轨迹和67,783个样本的多模态数据集，并验证其在统一控制机器学习模型中的可行性。该工作凸显Isaac Sim在构建复杂人机协同仿真环境及高效生成高质量训练数据方面的关键作用，为辅助机器人研究提供重要资源。

- ["A Decentralized Multi-Robot Dataset for Early Deadlock Forecasting in Smart Factory Navigation" (2026)](https://openalex.org/W7126226733) — Zenodo (CERN European Organization for Nuclear Research) — 该论文提出了一个用于多机器人智能工厂环境中早期死锁预测的去中心化数据集，核心贡献在于提供了包含轨迹、事件标签与同步视觉流的丰富模拟数据。研究明确使用 Isaac Sim 作为仿真平台，结合 ROS 2 Humble 和 Nav2 实现两个 Carter 机器人的自主导航，并在其中记录高频率状态与感知数据。该数据集支持从单机器人局部观测中训练死锁预测模型，对提升多机器人系统安全性具有重要应用价值。

- ["Enhancing Control Policy Smoothness by Aligning Actions with Predictions from Preceding States" (2026)](http://arxiv.org/abs/2601.18479v1) [PDF](https://arxiv.org/pdf/2601.18479v1) — 本文提出 ASAP 方法，通过引入“转移诱导相似状态”来对齐动作与前序状态预测，从而有效抑制强化学习策略中的高频振荡。该方法在 Isaac Lab 环境中进行了实验验证，利用真实环境反馈构建状态相似性，无需启发式假设，并结合二阶差分惩罚提升动作平滑性。结果表明 ASAP 在 Isaac Lab 等平台上显著改善了控制策略的平滑度与性能，有助于提升仿真到现实的迁移可靠性。

- ["AION: Aerial Indoor Object-Goal Navigation Using Dual-Policy Reinforcement Learning" (2026)](http://arxiv.org/abs/2601.15614v1) [PDF](https://arxiv.org/pdf/2601.15614v1) — 本文提出AION，一种用于室内空中物体目标导航的端到端双策略强化学习框架，将探索与目标抵达行为解耦为两个专用策略。研究在AI2-THOR基准上训练模型，并在Isaac Sim中使用高保真无人机模型进行实时性能评估，验证了其在探索效率、导航精度和安全性方面的优越性。该工作展示了Isaac Sim作为高保真空中机器人仿真平台在强化学习导航算法验证中的关键作用。

- ["Communication-Free Collective Navigation for a Swarm of UAVs via LiDAR-Based Deep Reinforcement Learning" (2026)](http://arxiv.org/abs/2601.13657v1) [PDF](https://arxiv.org/pdf/2601.13657v1) — arXiv (Cornell University) — 本文提出了一种基于LiDAR的深度强化学习控制器，用于在无通信环境下实现无人机群的集体导航。该方法采用隐式领导者-跟随者框架，仅领导者知晓目标位置，跟随者仅依赖机载LiDAR感知进行决策。核心DRL策略在GPU加速的NVIDIA Isaac Sim中训练，使无人机能通过局部感知学习避障与编队等涌现行为，并成功实现仿真到现实的迁移，在真实五机集群实验中验证了有效性。

- ["Transformable Quadruped Wheelchair: Unified Walking and Wheeled Locomotion via Mode-Conditioned Policy Distillation" (2026)](https://openalex.org/W7124139016) [PDF](https://www.mdpi.com/1424-8220/26/2/566/pdf?version=1768397051) — Sensors — 本文提出一种可变形四足轮椅，通过模式条件策略蒸馏实现行走与轮式运动的统一控制。研究利用NVIDIA Isaac Sim构建高保真仿真环境，采用PPO强化学习分别训练针对崎岖地形的行走策略和适用于平坦路面的轮式策略，并将二者蒸馏为单一模式条件策略。实验通过加速度频谱分析验证了两种模式的稳定性，并在长距离跨地形任务中证明自适应切换显著提升移动效率。

- ["Comprehensive Machine Learning Benchmarking for Fringe Projection Profilometry with Photorealistic Synthetic Data" (2026)](http://arxiv.org/abs/2601.08900v1) [PDF](https://arxiv.org/pdf/2601.08900v1) — arXiv (Cornell University) — 该论文首次构建了面向条纹投影轮廓术（FPP）的开源逼真合成数据集，利用Isaac Sim生成15,600张条纹图像与300组深度重建数据，涵盖50种多样物体。研究在Isaac Sim中精确模拟光学投影与表面反射，为单帧深度重建任务提供标准化基准，并系统评估四种神经网络架构的性能局限。该资源显著推动了基于学习的FPP方法在可控、可复现环境下的开发与比较。

- ["Robot-Assisted Suturing in Surgical Simulation: A Comparative Analysis between NVIDIA's Simulator and an Open Platform" (2026)](https://openalex.org/W7119741193) — Journal of Medical Robotics Research — 该论文构建了基于NVIDIA Isaac Sim的机器人辅助缝合虚拟手术环境，复现了AMBF平台中的场景，包含双机械臂、内窥镜、手术模型及三种线程建模方法，并通过ROS接口实现力反馈设备交互。研究直接以Isaac Sim为核心实验平台，系统评估其在视觉保真度与GPU加速方面的优势，同时对比其在帧率和操作响应延迟上相较AMBF的不足，为外科机器人仿真平台选型提供实证依据。

- ["CoINS: Counterfactual Interactive Navigation via Skill-Aware VLM" (2026)](http://arxiv.org/abs/2601.03956v1) [PDF](https://arxiv.org/pdf/2601.03956v1) — arXiv (Cornell University) — 论文提出CoINS框架，通过技能感知的视觉语言模型实现反事实交互式导航，使机器人能主动清理障碍物以创建可通行路径。作者在Isaac Sim中构建了InterNav数据集并训练InterNav-VLM模型，利用其度量级环境表示与技能约束参数进行反事实推理，判断是否需与物体交互及选择目标。该方法结合基于强化学习的技能库，在Isaac Sim中实现了多样物体的操作与路径疏通，显著提升复杂环境中机器人的自主导航能力。

- ["A Review of Online Diffusion Policy RL Algorithms for Scalable Robotic Control" (2026)](http://arxiv.org/abs/2601.06133v1) [PDF](https://arxiv.org/pdf/2601.06133v1) — 本文首次系统综述并实证评估了在线扩散策略强化学习（Online DPRL）算法在可扩展机器人控制中的表现，提出基于策略改进机制的四类算法新分类法。研究在 NVIDIA Isaac Lab 平台上统一构建了包含12个多样化机器人任务的基准，全面评估算法在任务多样性、并行能力、扩散步长可扩展性等五个维度的性能。该工作揭示了各类方法在样本效率与可扩展性间的根本权衡，为未来高效部署扩散策略于真实机器人系统提供了关键洞见与实践指导。

- ["A Workshop on Planning and Operating Robot Manipulations Using AI and Isaac Sim" (2026)](https://openalex.org/W7126166415) — Learning and analytics in intelligent systems — 该研讨会聚焦于利用AI与Isaac Sim协同进行机器人操作的规划与执行，重点探讨了如何借助Isaac Sim的GPU加速多物理仿真能力构建高保真操作任务环境。会议展示了基于Isaac Sim开发的抓取规划、动作策略学习和闭环控制实验，并强调其在快速原型设计与算法验证中的关键作用。成果为机器人操作研究提供了可复现、可扩展的仿真平台范式。

- ["SCAFusion: A Multimodal 3D Detection Framework for Small Object Detection in Lunar Surface Exploration" (2025)](http://arxiv.org/abs/2512.22503v1) [PDF](https://arxiv.org/pdf/2512.22503v1) — arXiv (Cornell University) — 本文提出SCAFusion，一种面向月面探测中小目标检测的多模态3D检测框架，通过引入认知适配器、对比对齐模块和区域感知坐标注意力机制，显著提升对陨石碎片等小而异形障碍物的检测性能。该方法在基于Isaac Sim构建的模拟月面环境中进行训练与验证，实现了90.93% mAP，较基线提升11.5%，充分验证了其在真实月球任务中的部署潜力。

- ["A Framework for Deploying Learning-based Quadruped Loco-Manipulation" (2025)](http://arxiv.org/abs/2512.18938v1) [PDF](https://arxiv.org/pdf/2512.18938v1) — arXiv (Cornell University) — 该论文提出一个开源框架，用于训练、评估和部署基于强化学习的四足机器人全身控制策略。其核心贡献在于将原本在 Isaac Gym 中训练的策略通过硬件抽象层迁移至 MuJoCo 仿真环境，并成功部署到 Unitree B1 实体机器人上，实现了统一的 sim-to-sim 与 sim-to-real 流程。研究特别分析了 Isaac Gym 与 MuJoCo 接触模型差异对策略性能的影响，并验证了协调全身运动在真实抓取任务中的优势，为可复现的具身智能研究提供了重要工具。

- ["Towards Senior-Robot Interaction: Reactive Robot Dog Gestures" (2025)](http://arxiv.org/abs/2512.17136v2) [PDF](https://arxiv.org/pdf/2512.17136v2) — arXiv (Cornell University) — 该论文提出了一种面向老年人的四足机器人交互系统，通过MediaPipe实现无遥控手势与头部控制，并在Isaac Gym中利用课程式强化学习训练出包括三足平衡和抬腿等高表现力的狗型社交动作。研究在Isaac Sim的Isaac Gym环境中完成95%以上成功率的仿真训练，并将关键动作（如抬爪）部署到Unitree机器人验证其社交表达能力，为老年陪伴机器人提供了可扩展的仿真-现实迁移框架。

- ["Automatic Reward Shaping from Multi-Objective Human Heuristics" (2025)](http://arxiv.org/abs/2512.15120v1) [PDF](https://arxiv.org/pdf/2512.15120v1) — arXiv (Cornell University) — 本文提出MORSE框架，通过双层优化自动融合多个人类启发式奖励为统一奖励函数，并在Isaac Sim环境中验证其在多目标机器人任务中的有效性。作者利用Isaac Sim进行强化学习实验，展示了该方法在无需人工调参的情况下实现与手工设计奖励相当的性能。该工作突显了Isaac Sim作为高性能机器人仿真平台在多目标强化学习研究中的关键作用。

- ["Reinforcement Learning based 6-DoF Maneuvers for Microgravity Intravehicular Docking: A Simulation Study with Int-Ball2 in ISS-JEM" (2025)](http://arxiv.org/abs/2512.13514v1) [PDF](https://arxiv.org/pdf/2512.13514v1) — arXiv (Cornell University) — 该论文提出基于强化学习的六自由度对接控制框架，用于JAXA的Int-Ball2机器人在国际空间站日本实验舱内的自主对接任务。研究在Isaac Sim中构建高保真微重力环境，显式建模推进器拖曳力矩与极性结构，并结合域随机化和观测噪声训练PPO策略，验证了Isaac Sim对复杂空间机器人动力学仿真的有效性。成果为后续基于视觉的端到端对接及sim-to-real迁移奠定基础。

- ["Development of Real-World Implementation Technology for Isaac Sim-Based Autonomous Driving AI Using a Sim2Real Approach" (2025)](https://openalex.org/W7116850167) — Journal of The Korean Society of Manufacturing Technology Engineers — 该论文提出了一种基于Isaac Sim的Sim2Real迁移技术，用于实现自动驾驶AI在真实世界中的部署。作者在Isaac Sim中构建高保真城市场景与传感器模型，生成大规模合成数据，并通过域自适应算法缩小仿真与现实之间的差距。实验表明，所提方法显著提升了感知与控制模块在实车环境中的泛化能力，为高效、低成本的自动驾驶系统开发提供了可行路径。

- ["Entropy-Controlled Intrinsic Motivation Reinforcement Learning for Quadruped Robot Locomotion in Complex Terrains" (2025)](http://arxiv.org/abs/2512.06486v2) [PDF](https://arxiv.org/pdf/2512.06486v2) — 本文提出熵控制内在动机强化学习算法（ECIM），通过结合自适应探索与内在动机机制，有效缓解四足机器人在复杂地形中训练时的早熟收敛问题。研究在Isaac Gym中对六类地形（上下坡、崎岖地面、楼梯等）进行大规模并行仿真实验，显著提升了运动稳定性并降低能耗。该方法在Isaac Sim核心组件Isaac Gym上实现，验证了其作为高效训练平台在具身智能策略开发中的关键作用。

- ["An Integrated System for WEEE Sorting Employing X-ray Imaging, AI-based Object Detection and Segmentation, and Delta Robot Manipulation" (2025)](http://arxiv.org/abs/2512.05599v1) [PDF](https://arxiv.org/pdf/2512.05599v1) — arXiv (Cornell University) — 该论文提出了一种集成X射线成像、AI目标检测与Delta机器人操作的WEEE分拣系统，核心创新在于结合双能X射线成像与YOLO/U-Net模型实现高精度电池识别。作者在Isaac Sim中构建了高度逼真的仿真环境，用于验证整个分拣流程的感知、定位与抓取性能，显著提升了系统在复杂电子废弃物场景下的鲁棒性与安全性。该工作展示了Isaac Sim在闭环机器人分拣系统开发中的关键作用，为危险物品自动化回收提供了可扩展的仿真-现实迁移范式。

- ["Autonomous Planning In-space Assembly Reinforcement-learning free-flYer (APIARY) International Space Station Astrobee Testing" (2025)](http://arxiv.org/abs/2512.03729v1) [PDF](https://arxiv.org/pdf/2512.03729v1) — 该论文提出并验证了首个在轨使用强化学习（RL）控制自由飞行机器人（NASA Astrobee）的实验，其核心6自由度控制策略基于NVIDIA Isaac Lab中的PPO算法训练而成。研究在Isaac Lab中通过随机化目标位姿与质量分布进行仿真训练，显著提升了策略鲁棒性，并成功完成地面测试与国际空间站飞行验证。这项工作展示了Isaac Lab作为高保真、可迁移RL训练平台在空间机器人自主控制中的关键作用，为未来快速部署太空任务行为提供了可行路径。

- ["Autonomous Reinforcement Learning Robot Control with Intel's Loihi 2 Neuromorphic Hardware" (2025)](http://arxiv.org/abs/2512.03911v1) [PDF](https://arxiv.org/pdf/2512.03911v1) — 该论文提出了一种将强化学习训练的ANN策略转换为适用于Intel Loihi 2神经形态硬件的Sigma-Delta脉冲神经网络（SDNN）的端到端流程。研究在NVIDIA Omniverse Isaac Lab中对Astrobee机器人进行闭环控制仿真，验证了转换后SDNN策略的有效性，并与GPU执行性能进行对比。工作直接利用Isaac Lab作为核心仿真平台评估部署效果，为神经形态计算在机器人控制中的应用提供了可复现的仿真验证环境。

- ["RoboWheel: A Data Engine from Real-World Human Demonstrations for Cross-Embodiment Robotic Learning" (2025)](http://arxiv.org/abs/2512.02729v1) [PDF](https://arxiv.org/pdf/2512.02729v1) — arXiv (Cornell University) — 本文提出RoboWheel数据引擎，将人类手部操作视频转化为适用于跨形态机器人学习的训练数据。其核心创新在于利用Isaac Sim构建仿真增强框架，通过多样化的域随机化（包括不同机器人本体、轨迹、物体、背景纹理等）扩展数据分布，同时保持空间关系与物理合理性。该方法在Isaac Sim中生成大量接触丰富的可执行轨迹，显著降低对遥操作的依赖，为视觉-语言-动作模型提供高质量监督信号。

- ["CostNav: A Navigation Benchmark for Real-World Economic-Cost Evaluation of Physical AI Agents" (2025)](http://arxiv.org/abs/2511.20216v2) [PDF](https://arxiv.org/pdf/2511.20216v2) — 本文提出CostNav，首个面向物理AI智能体的经济成本导航基准，通过整合SEC财报、AIS事故报告等真实商业数据与Isaac Sim中的碰撞和货物动力学仿真，实现对自主配送系统商业价值的量化评估。研究利用Isaac Sim精确模拟物理交互与任务执行过程，揭示当前导航方法（如Nav2）在经济上不可行，推动社区关注真实部署场景下的成本效益优化。该基准为机器人导航研究提供了从任务成功到商业可行性的关键桥梁。

- ["Digital twins as decision-support tools for automation in agriculture: A case study on robotic vaccination" (2025)](https://openalex.org/W4416642291) — Smart Agricultural Technology — 本文提出了一种基于数字孪生的农业机器人疫苗接种系统框架，利用NVIDIA Isaac Sim构建高保真仿真环境，集成Franka Emika Panda机械臂与自定义操作器，结合Detectron2模型实现牛颈部肌肉精准分割，并通过强化学习优化注射位点定位。Isaac Sim被用作核心开发与测试平台，支持在动态、逼真的虚拟牧场环境中验证系统的位置精度与控制鲁棒性，为畜牧业自动化提供可扩展、低成本的部署前验证方案。

- ["A Study on Bridging the Gap With Reinforcement Learning: TD3 Optimization for Sim-to-real Transfer from Gazebo to Isaac Sim" (2025)](https://openalex.org/W7104761584) — Journal of Institute of Control Robotics and Systems — 该论文研究了从Gazebo到Isaac Sim的仿真到现实（sim-to-real）迁移问题，提出基于TD3强化学习算法的优化策略以缩小域差距。作者在Isaac Sim中构建了与Gazebo对应的机器人控制环境，并利用其GPU加速的物理仿真能力进行策略训练和迁移实验，验证了优化后TD3在Isaac Sim中训练的策略能更高效地部署到真实机器人上。这项工作突显了Isaac Sim作为高保真、高性能训练平台在强化学习迁移中的关键作用。

- ["Multi-Agent Deep Reinforcement Learning for Collision-Free Posture Control of Multi-Manipulators in Shared Workspaces" (2025)](https://openalex.org/W4415999376) [PDF](https://www.mdpi.com/1424-8220/25/22/6822/pdf?version=1762524575) — Sensors — 该论文提出了一种基于多智能体深度强化学习（MADRL）的实时无碰撞姿态控制框架，用于共享工作空间中的多机械臂协同操作。作者在 NVIDIA Isaac Sim 中实现并验证了该方法，利用其高保真物理仿真能力构建重叠工作空间场景，并采用线段表示法高效计算机械臂连杆间距离以指导避障。实验表明，该方法相比传统状态表示具有更快的收敛速度和更高的计算效率，在 Isaac Sim 中成功实现了协作抓取任务，显著缩短任务完成时间，为密集工业环境下的多机器人协调提供了实用解决方案。

- ["Isaac Lab: A GPU-Accelerated Simulation Framework for Multi-Modal Robot Learning" (2025)](http://arxiv.org/abs/2511.04831v1) [PDF](https://arxiv.org/pdf/2511.04831v1) — 本文提出了Isaac Lab，作为Isaac Gym的继任者，它是一个面向多模态机器人学习的GPU加速仿真框架。该框架深度集成Isaac Sim的核心能力，包括高保真GPU并行物理、逼真渲染、多频率传感器仿真及域随机化工具，并明确规划与Nvidia Newton可微分物理引擎的整合。其模块化架构支持大规模强化与模仿学习实验，在全身控制、灵巧操作等任务中展现价值，为下一代机器人学习研究提供统一平台。

- ["Learning Spatial Awareness for Laparoscopic Surgery with AI Assisted Visual Feedback" (2025)](http://arxiv.org/abs/2511.02233v1) [PDF](https://arxiv.org/pdf/2511.02233v1) — arXiv (Cornell University) — 该论文提出了一种AI辅助的腹腔镜手术训练框架，通过在NVIDIA Isaac Sim中构建混合现实环境，将标准2D内窥镜画面与同步的3D视觉反馈相结合。系统利用Isaac Sim实现高保真手术场景仿真，并集成AI模块实时定位器械、检测器械-组织交互，在检测到空间误判时动态叠加3D提示，从而提升受训者对深度、接触和器械朝向的感知能力。该方法显著增强了传统2D训练中的空间意识，具有临床教学与技能评估的应用潜力。

- ["Reinforcement Learning for 12-DoF Ant Robot Locomotion in One-File Isaac Sim" (2025)](https://openalex.org/W7117505902) — 该论文提出了一种在单文件中实现的强化学习方法，用于训练12自由度蚂蚁机器人的运动控制策略。作者直接在Isaac Sim中构建了高保真机器人模型并利用其GPU加速的物理引擎进行高效训练，显著提升了样本效率和运动性能。该工作展示了Isaac Sim作为端到端RL训练平台在复杂多足机器人控制中的实用价值。

- ["Real-DRL: Teach and Learn in Reality" (2025)](http://arxiv.org/abs/2511.00112v1) [PDF](https://arxiv.org/pdf/2511.00112v1) — 本文提出Real-DRL框架，通过DRL-Student、PHY-Teacher与Trigger三组件协同，在真实物理系统中实现安全优先的深度强化学习。研究在NVIDIA Isaac Gym中对四足机器人进行仿真实验，利用其GPU加速物理引擎验证算法在Sim2Real迁移中的安全性与有效性，并与真实机器人实验对比，凸显Isaac Gym作为关键仿真平台的作用。该工作为安全关键型自主系统提供了可验证、可迁移的训练范式。

- ["Towards Reinforcement Learning Based Log Loading Automation" (2025)](http://arxiv.org/abs/2510.26363v1) [PDF](https://arxiv.org/pdf/2510.26363v1) — 该研究提出了一种基于强化学习的林业集材车全自动装木系统，将任务从先前的抓取扩展至完整的装载流程，包括定位、抓取、运输和卸放。作者在 NVIDIA Isaac Gym 中构建了拖车式集材车仿真模型与典型装木场景虚拟环境，并采用课程学习策略训练智能体，在随机初始条件下实现94%的成功率。该成果为林业机械自动化提供了可部署的强化学习解决方案，并验证了 Isaac Gym 在复杂机器人操作任务中的高效训练能力。

- ["Towards An Adaptive Locomotion Strategy For Quadruped Rovers: Quantifying When To Slide Or Walk On Planetary Slopes" (2025)](http://arxiv.org/abs/2510.18678v1) [PDF](https://arxiv.org/pdf/2510.18678v1) — arXiv (Cornell University) — 该论文提出一种自适应四足行星巡视器运动策略，通过比较行走与躯干滑行在不同坡度、摩擦和速度下的运输成本（CoT），确定两者切换的阈值条件。研究核心依赖 Isaac Sim 进行高保真物理仿真，结合 ANSYS-Rocky 验证颗粒相互作用，为行星松散斜坡环境提供能耗优化的混合运动方案。该方法有望提升腿式机器人在复杂地外地形中的能效与安全性。

- ["GaussGym: An open-source real-to-sim framework for learning locomotion from pixels" (2025)](http://arxiv.org/abs/2510.15352v1) [PDF](https://arxiv.org/pdf/2510.15352v1) — 该论文提出 GaussGym，一种将 3D Gaussian Splatting 作为即插即用渲染器集成到 Isaac Gym 中的高保真、高吞吐量仿真框架。作者在 Isaac Gym 环境中实现超过每秒 10 万步的训练速度，并利用 iPhone 扫描、ARKit 和 GrandTour 等真实场景数据构建数千个逼真训练环境，显著提升基于像素的机器人运动策略学习效果。该工作直接以 Isaac Gym 为核心仿真平台，推动了可扩展、视觉丰富的 sim-to-real 机器人学习。

- ["DeGrip: A Compact Cable-driven Robotic Gripper for Desktop Disassembly" (2025)](http://arxiv.org/abs/2510.16231v1) [PDF](https://arxiv.org/pdf/2510.16231v1) — arXiv (Cornell University) — 本文提出DeGrip——一种专为拆解废旧台式电脑设计的紧凑型缆绳驱动三自由度机械夹爪，其解耦腕部与夹爪驱动的设计适用于狭小空间作业。作者在Isaac Sim中构建了完整的废旧桌面拆解仿真环境，用于评估DeGrip在任意位姿下执行复杂拆解任务的能力，并验证其在受限空间中的操作性能。该工作展示了Isaac Sim作为硬件-算法协同验证平台在可持续机器人应用中的实用价值。

- ["UrbanVerse: Scaling Urban Simulation by Watching City-Tour Videos" (2025)](http://arxiv.org/abs/2510.15018v1) [PDF](https://arxiv.org/pdf/2510.15018v1) — 本文提出UrbanVerse，一个从城市游览视频自动生成高保真、物理感知的城市场景仿真系统，并在Isaac Sim中构建了160个高质量场景及10个艺术家设计的基准测试环境。系统包含10万+带语义与物理属性的3D资产库和自动场景生成管线，显著提升导航策略的泛化能力，在零样本sim-to-real迁移中成功率提升30.1%。该工作直接以Isaac Sim作为核心仿真平台，为城市机器人训练提供可扩展、真实感强的虚拟环境。

- ["EdgeNavMamba: Mamba Optimized Object Detection for Energy Efficient Edge Devices" (2025)](http://arxiv.org/abs/2510.14946v1) [PDF](https://arxiv.org/pdf/2510.14946v1) — 本文提出EdgeNavMamba，一种基于Mamba架构的高效目标检测模型，用于资源受限边缘设备上的自主导航。该方法在IsaacLab模拟器中进行训练与评估，验证了其在保持高检测精度的同时减少31%参数量的有效性。通过将检测结果作为强化学习策略的输入，系统在Jetson Orin Nano等设备上实现高达73%的能耗降低，显著提升边缘端导航系统的能效与实用性。

- ["Adaptive Obstacle-Aware Task Assignment and Planning for Heterogeneous Robot Teaming" (2025)](http://arxiv.org/abs/2510.14063v1) [PDF](https://arxiv.org/pdf/2510.14063v1) — 本文提出OATH框架，通过障碍物感知的自适应Halton序列地图和聚类-拍卖-选择机制，提升异构机器人团队在复杂环境中的任务分配与规划性能。研究在NVIDIA Isaac Sim中实现并验证了该方法，利用其GPU加速的多物理仿真能力进行动态障碍环境下的大规模多智能体实验，显著优于现有MATP方法。该工作展示了Isaac Sim作为高保真、可扩展机器人协同算法测试平台的关键价值。

- ["Benchmarking Digital Twins for Tower Cranes: Isaac Sim vs. Gazebo" (2025)](https://openalex.org/W4415969566) — 该论文系统性地对比了Isaac Sim与Gazebo在塔式起重机数字孪生建模中的性能表现，重点评估了物理仿真精度、实时性及传感器模拟能力。作者在Isaac Sim中构建了高保真塔吊模型，利用其GPU加速的多物理引擎进行动力学仿真，并与Gazebo结果进行定量比较。研究表明Isaac Sim在复杂负载摆动仿真和视觉传感器渲染方面显著优于传统CPU-based仿真器，为建筑机器人数字孪生提供了高效验证平台。

- ["Population-Coded Spiking Neural Networks for High-Dimensional Robotic Control" (2025)](http://arxiv.org/abs/2510.10516v1) [PDF](https://arxiv.org/pdf/2510.10516v1) — 本文提出了一种结合群体编码脉冲神经网络（SNN）与深度强化学习（DRL）的新框架，用于高维机器人控制，在保持控制性能的同时显著降低能耗。作者在 Isaac Gym 平台上利用 PixMC 基准对 Franka 机械臂进行训练和评估，展示了其 Population-coded Spiking Actor Network（PopSAN）在复杂操作任务中的有效性，实现了比传统人工神经网络高达 96.10% 的能耗节省。该方法为资源受限的机器人系统提供了高效、稳定的控制策略，具有重要的实际部署价值。

- ["Integration of the TIAGo Robot into Isaac Sim with Mecanum Drive Modeling and Learned S-Curve Velocity Profiles" (2025)](http://arxiv.org/abs/2510.10273v2) [PDF](https://arxiv.org/pdf/2510.10273v2) — 本文首次将PAL Robotics的TIAGo++ Omni机器人集成到Isaac Sim中，重点建模其全向麦卡纳姆轮底盘动力学。作者开发了两种驱动控制模型：一种高保真物理模型复现真实轮系行为，另一种轻量级速度模型适配学习算法，并通过少量轨迹数据学习真实机器人的S型速度曲线。该Isaac Sim模型为研究人员提供了高效、逼真的仿真平台，支持在复杂环境中开展基于学习的移动操作控制研究。

- ["PolySim: Bridging the Sim-to-Real Gap for Humanoid Control via Multi-Simulator Dynamics Randomization" (2025)](http://arxiv.org/abs/2510.01708v3) [PDF](https://arxiv.org/pdf/2510.01708v3) — 本文提出PolySim，一种通过多仿真器动力学随机化来缩小人形机器人控制中仿真到现实差距的训练平台。该方法在单次训练中并行集成包括Isaac Sim在内的多个异构仿真引擎，实现跨仿真器的动力学域随机化，从而降低单一仿真器的归纳偏置。实验表明，PolySim显著优于仅使用Isaac Sim的基线，在MuJoCo上提升52.8%的成功率，并实现零样本迁移到真实Unitree G1机器人。

- ["Data-Efficient Multitask DAgger" (2025)](http://arxiv.org/abs/2509.25466v1) [PDF](https://arxiv.org/pdf/2509.25466v1) — 本文提出了一种数据高效的多任务DAgger框架，通过性能感知的调度策略动态分配专家演示数据，显著提升多任务策略的整体成功率。该方法在IsaacLab中构建了多样化的抽屉开启任务套件进行验证，利用其GPU加速的物理仿真能力训练视觉策略，并成功实现零样本迁移到真实机器人。这项工作凸显了IsaacLab作为高效、可迁移机器人学习平台的价值。

- ["A Framework for Scalable Heterogeneous Multi-Agent Adversarial Reinforcement Learning in IsaacLab" (2025)](http://arxiv.org/abs/2510.01264v1) [PDF](https://arxiv.org/pdf/2510.01264v1) — 该论文提出一个支持可扩展异构多智能体对抗强化学习的框架，核心贡献是扩展IsaacLab以实现高保真物理仿真中的对抗策略训练。作者在IsaacLab中构建了多个具有非对称目标与能力的异构对抗环境，并集成了基于PPO的HAPPO算法变体，实现了高效、高吞吐量的对抗策略训练与评估。该工作显著拓展了Isaac Sim生态在安全、追逃和竞争性操作等现实对抗场景中的应用能力。

- ["DreamerNav: learning-based autonomous navigation in dynamic indoor environments using world models" (2025)](https://openalex.org/W4414525330) [PDF](https://www.frontiersin.org/journals/robotics-and-ai/articles/10.3389/frobt.2025.1655171/pdf) (Citations: 1) — Frontiers in Robotics and AI — 本文提出DreamerNav，一种基于世界模型的机器人无关导航框架，通过在NVIDIA Isaac Sim中进行高保真、逼真的仿真训练，实现了动态室内环境下的鲁棒自主导航。系统利用Isaac Sim逐步提升任务复杂度，结合深度图像与局部占用地图，在RSSM中学习动态障碍物的潜在表征，显著提升样本效率与泛化能力。该方法在仿真中训练后可直接部署于四足机器人，验证了Isaac Sim作为训练平台对真实世界迁移的有效支撑。

- ["CGA-ASNet: an RGB-D amodal segmentation network for restoring occluded tomato regions" (2025)](https://openalex.org/W4414448697) [PDF](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2025.1664718/pdf) — Frontiers in Plant Science — 本文提出CGA-ASNet，一种用于恢复被遮挡番茄区域的RGB-D无模态分割网络，并利用NVIDIA Isaac Sim的Replicator Composer构建了高保真合成番茄数据集Tomato-sim，用于训练模型。该方法通过上下文与全局注意力模块提升对遮挡区域形态的重建能力，在未使用显式域自适应的情况下，借助Isaac Sim模拟多样光照条件以缩小仿真与现实之间的域差距。该工作展示了Isaac Sim在农业机器人视觉感知任务中生成逼真训练数据的关键作用，具有重要的表型研究应用价值。

- ["DyDexHandover: Human-like Bimanual Dynamic Dexterous Handover using RGB-only Perception" (2025)](http://arxiv.org/abs/2509.17350v2) [PDF](https://arxiv.org/pdf/2509.17350v2) — arXiv (Cornell University) — 本文提出DyDexHandover框架，首次实现仅使用RGB视觉输入的双臂动态空中传递任务，通过多智能体强化学习训练端到端策略，并引入人类动作先验正则化以提升动作自然性与泛化能力。研究在Isaac Sim中构建了完整的双臂机器人仿真环境，用于策略训练与评估，成功率达99%（已见物体）和75%（未见物体）。该工作展示了Isaac Sim在高保真多臂协同操作仿真中的关键作用，为基于视觉的灵巧操作提供了可扩展的训练平台。

- ["RL-augmented Adaptive Model Predictive Control for Bipedal Locomotion over Challenging Terrain" (2025)](http://arxiv.org/abs/2509.18466v1) [PDF](https://arxiv.org/pdf/2509.18466v1) — 该论文提出一种强化学习增强的模型预测控制（RL-augmented MPC）框架，专门用于双足机器人在崎岖与低摩擦地形上的鲁棒行走。作者在 NVIDIA Isaac Lab 中构建了包含楼梯、踏脚石和滑面等多种挑战性地形的仿真环境，对基于单刚体动力学的MPC三个关键组件——系统动力学、摆动腿控制器和步态频率——进行端到端参数化训练。实验表明，该方法显著优于纯MPC或纯RL基线，为复杂地形下的双足运动控制提供了高适应性解决方案。

- ["Robotic Skill Diversification via Active Mutation of Reward Functions in Reinforcement Learning During a Liquid Pouring Task" (2025)](http://arxiv.org/abs/2509.18463v1) [PDF](https://arxiv.org/pdf/2509.18463v1) — arXiv (Cornell University) — 本文提出了一种通过在强化学习中主动对奖励函数权重施加高斯噪声来实现机器人技能多样化的框架，并以液体倾倒任务为案例进行验证。研究在 NVIDIA Isaac Sim 中构建了包含 Franka Emika Panda 机械臂与液体物理仿真的高保真环境，利用 PPO 算法训练策略，展示了不同奖励权重变异如何催生包括清洗容器边缘、搅拌和浇水等新颖技能。该方法为机器人在 Isaac Sim 平台中实现任务内技能泛化与跨任务迁移提供了新路径。

- ["Design and Implementation of Digital Twin System of OCS Maintenance Robot" (2025)](https://openalex.org/W4414345490) — Journal of Advanced Computational Intelligence and Intelligent Informatics — 该论文提出了一种基于Isaac Sim构建的接触网维护机器人数字孪生系统，用于在川藏线高寒缺氧环境下辅助维修作业。研究利用Isaac Sim搭建虚拟维护环境，集成VR技术对机械臂维修过程进行仿真与错误修正，并通过rviz实现虚实联动的实际维修操作。该系统显著提升了高原恶劣气候下接触网维护的可行性与安全性。

- ["VIRTUS-FPP: Virtual Sensor Modeling for Fringe Projection Profilometry in NVIDIA Isaac Sim" (2025)](http://arxiv.org/abs/2509.22685v1) [PDF](https://arxiv.org/pdf/2509.22685v1) — arXiv (Cornell University) — 本文提出VIRTUS-FPP，首个基于NVIDIA Isaac Sim构建的条纹投影轮廓术（FPP）物理虚拟传感器建模框架。该工作充分利用Isaac Sim的物理渲染与可编程感知能力，完整复现FPP从标定到三维重建的全流程，并通过与真实系统对比验证其数字孪生精度。该框架显著提升FPP系统在配置灵活性、环境鲁棒性及原型开发效率方面的性能，为高精度3D传感提供高效仿真平台。

- ["Scalable Multi-Objective Robot Reinforcement Learning through Gradient Conflict Resolution" (2025)](http://arxiv.org/abs/2509.14816v1) [PDF](https://arxiv.org/pdf/2509.14816v1) — 本文提出GCR-PPO方法，通过多头评论家将策略更新分解为各目标的梯度，并基于目标优先级解决梯度冲突，有效提升多目标强化学习的可扩展性。该方法在Isaac Lab的标准操作与运动控制基准上进行评估，展示了在高冲突任务中优于并行PPO的性能，且无显著计算开销。研究成果为复杂机器人任务中的多目标优化提供了高效、稳定的训练方案。

- ["Dynamic Scene 3D Reconstruction of an Uncooperative Resident Space Object" (2025)](http://arxiv.org/abs/2509.07932v1) [PDF](https://arxiv.org/pdf/2509.07932v1) — arXiv (Cornell University) — 该论文提出利用Isaac Sim构建高保真仿真环境，生成在真实轨道光照条件下翻滚卫星的物理精确2D图像序列，用于评估动态场景3D重建算法的性能。研究以Neuralangelo在静态场景中的重建结果为基线，验证了所生成3D网格与原始CAD模型高度一致，能保留任务规划所需的关键细节。该工作凸显了Isaac Sim在空间目标数字建模与在轨服务仿真中的关键支撑作用。

- ["Performance Characterization of the LEAP Hand: Control Interface and Digital Twin Integration" (2025)](https://openalex.org/W4415398891) — 本文系统表征了低成本灵巧手LEAP Hand的控制性能，并开发了支持用户自定义运动控制的调试接口。关键贡献在于将该控制接口与GPU加速的Isaac Sim物理仿真器深度集成，构建了高保真数字孪生系统，用于部署和验证复杂手势。通过长达4小时的连续运动实验，评估了精度、动态跟踪与热特性，为基于Isaac Sim的灵巧手强化学习训练和真实-仿真迁移提供了可靠平台。

- ["Real-Time Buoyancy Estimation for AUV Simulations Using Convex Hull-Based Submerged Volume Calculation" (2025)](http://arxiv.org/abs/2509.03804v1) [PDF](https://arxiv.org/pdf/2509.03804v1) — 本文提出一种基于凸包的实时水下体积计算方法，用于在NVIDIA Isaac Sim中实现高保真AUV浮力模拟。作者从Isaac Sim环境中提取AUV网格几何，沿z轴动态计算与水面相交的浸没体积，并通过横截面积扩展策略降低计算开销，支持实时响应姿态、深度及波浪扰动。该方法无需预计算流体模型，显著提升了Isaac Sim在水下机器人仿真中的物理真实性与实用性。

- ["Learning to Coordinate: Distributed Meta-Trajectory Optimization Via Differentiable ADMM-DDP" (2025)](http://arxiv.org/abs/2509.01630v2) [PDF](https://arxiv.org/pdf/2509.01630v2) — 本文提出Learning to Coordinate（L2C）框架，通过元学习自动调节分布式ADMM-DDP优化中的超参数，实现多智能体系统的高效协同。该方法在Isaac Sim中进行高保真仿真，成功生成四旋翼协同运输任务的动态可行轨迹，并支持在狭小空间内安全重构编队以操作6自由度负载。实验利用Isaac Sim验证了L2C对不同团队规模和任务条件的强适应性，显著提升梯度计算效率。

- ["Pallet Detection and Pose Estimation System Based on Synthetic Data from Isaac Sim" (2025)](https://openalex.org/W4415883711) — 该论文提出了一种基于合成数据的托盘检测与位姿估计系统，利用Isaac Sim生成高保真、带精确标注的RGB-D合成数据集，有效解决了真实场景中托盘数据稀缺和标注成本高的问题。作者在Isaac Sim中构建了多样化的仓储环境，并通过域随机化增强模型泛化能力，训练出的检测网络在真实世界测试中表现出高精度。该工作展示了Isaac Sim作为合成数据生成平台在物流机器人感知任务中的关键价值。

- ["Language-Enhanced Mobile Manipulation for Efficient Object Search in Indoor Environments" (2025)](http://arxiv.org/abs/2508.20899v1) [PDF](https://arxiv.org/pdf/2508.20899v1) — arXiv (Cornell University) — 该论文提出了一种语言增强的分层导航框架GODHS，利用大语言模型进行场景语义推理并指导移动操作机器人高效搜索目标物体。研究在Isaac Sim中构建了完整的室内环境仿真系统，对GODHS的语义感知、空间推理与启发式运动规划模块进行了端到端验证，显著优于传统非语义搜索策略。该工作展示了Isaac Sim在支持复杂语义-动作闭环任务中的强大能力，为家庭和服务机器人应用提供了可复现的仿真基准。

- ["The Metaverse in Smart Industrial Environments: from Vision to Proof-of-Concept" (2025)](https://openalex.org/W4415034459) — 该论文提出了一种面向工业元宇宙的云边协同架构，并基于NVIDIA Isaac Sim与Omniverse构建了具体验证原型，实现了与真实ROS机器人系统的集成。研究利用Isaac Sim作为核心仿真平台，支撑数字孪生、实时数据交互与沉浸式可视化，验证了其在工业操作、协作与决策中的可行性。该工作展示了Isaac Sim在构建工业元宇宙应用中的关键作用，为智能工厂提供了可扩展的仿真-现实融合范式。

- ["HumanoidVerse: A Versatile Humanoid for Vision-Language Guided Multi-Object Rearrangement" (2025)](http://arxiv.org/abs/2508.16943v1) [PDF](https://arxiv.org/pdf/2508.16943v1) — 本文提出 HumanoidVerse 框架，实现基于视觉-语言指令的通用人形机器人多物体长程重排任务。该方法在 Isaac Gym 中构建包含350个多物体任务的大规模数据集，并采用多阶段课程学习与双教师蒸馏策略训练策略，无需环境重置即可流畅执行连续子任务。实验表明其在任务成功率和空间精度上显著优于现有方法，为具身智能体在真实感知约束下执行复杂序列操作提供了可行路径。

- ["Mind and Motion Aligned: A Joint Evaluation IsaacSim Benchmark for Task Planning and Low-Level Policies in Mobile Manipulation" (2025)](http://arxiv.org/abs/2508.15663v1) [PDF](https://arxiv.org/pdf/2508.15663v1) — arXiv (Cornell University) — 该论文提出了Kitchen-R基准，首次在Isaac Sim中构建厨房数字孪生环境，统一评估任务规划与底层控制策略。研究利用Isaac Sim实现高保真物理仿真，支持500余条复杂语言指令和移动机械臂操作，并提供基于视觉语言模型的规划器与扩散策略控制器作为基线。该基准通过三种评估模式推动语言引导机器人系统的整体性能评测，为具身智能提供更真实、集成的测试平台。

- ["Isaac Sim-to-Real: Reinforcement Learning based Locomotion for Quadrupeds" (2025)](https://openalex.org/W4414432529) — 该论文提出一种基于强化学习的四足机器人运动控制方法，利用 Isaac Sim 构建高保真仿真环境进行策略训练，并通过域随机化和系统辨识技术缩小 sim-to-real 鸿沟。研究在 Isaac Sim 中实现了完整的训练-部署流程，最终将策略成功迁移到真实 Unitree A1 机器人上，验证了 Isaac Sim 在复杂动力学仿真与机器人学习中的关键作用。

- ["Simulation-To-Reality Hyperparameter Optimization of MPPI Controllers via Bayesian Optimization in NVIDIA Omniverse Isaac Sim" (2025)](https://openalex.org/W4414432302) — 该论文提出一种基于贝叶斯优化的仿真到现实（Sim2Real）超参数调优方法，专门用于优化模型预测路径积分（MPPI）控制器在真实机器人上的性能。作者在 NVIDIA Omniverse Isaac Sim 中构建高保真仿真环境，利用其 GPU 加速的多物理引擎对四足机器人进行大规模并行仿真，并将优化后的 MPPI 超参数直接迁移到实体机器人上验证。该工作凸显了 Isaac Sim 作为 Sim2Real 研究核心平台的能力，为复杂控制策略的高效部署提供了实用范式。

- ["Sem-Geo-Nav: A Semantically and Geometrically Aware Navigation Framework for Legged Robots" (2025)](https://openalex.org/W4415598523) — 本文提出Sem-Geo-Nav框架，通过融合2D占据栅格、语义类别图、地面高程图和障碍物净空图，实现对腿式机器人可穿越性的统一评估。该框架在Omniverse Isaac Sim中构建包含可穿越障碍（如窗帘、桌子、木板）的室内仿真环境，并验证了其导航性能——机器人平均探索率达99.15%，显著优于基线方法。研究直接依赖Isaac Sim进行高保真物理仿真与场景交互实验，凸显其在复杂地形导航算法开发中的关键作用。

- ["Fully Spiking Actor-Critic Neural Network for Robotic Manipulation" (2025)](http://arxiv.org/abs/2508.12038v1) [PDF](https://arxiv.org/pdf/2508.12038v1) — 该论文提出一种基于全脉冲神经网络（SNN）的混合课程强化学习框架，用于9自由度机械臂的目标抓取任务。作者在Isaac Gym仿真平台上开展实验，利用其GPU加速的物理引擎验证了所提方法在真实物理约束下的优越性能，并通过能量消耗建模定量比较SNN与传统ANN的能效。该工作凸显了Isaac Gym作为高保真、高效机器人策略训练平台的关键作用，为低功耗神经形态控制在现实机器人系统中的部署提供了可行路径。

- ["GBC: Generalized Behavior-Cloning Framework for Whole-Body Humanoid Imitation" (2025)](http://arxiv.org/abs/2508.09960v1) [PDF](https://arxiv.org/pdf/2508.09960v1) — 本文提出通用行为克隆框架GBC，通过可微分IK网络实现人体动作数据到任意人形机器人的自动重定向，并结合新型DAgger-MMPPO算法与MMTransformer架构学习高保真模仿策略。该框架完全基于Isaac Lab构建，提供开源、可配置的端到端训练平台，支持多形态人形机器人策略训练与迁移。其在Isaac Lab中的集成使社区能高效复现和部署通用人形控制流程，显著提升仿人机器人开发的通用性与实用性。

- ["Fusion Robotics: Analysing Mobility Modes of an End-Over-End Walking Manipulator for Maintenance and Decommissioning" (2025)](https://openalex.org/W4413325946) — Lecture notes in computer science — 该论文提出并分析了一种用于维护与退役任务的端对端翻滚式行走机械臂的多种移动模式。研究在 NVIDIA Isaac Sim 中构建了高保真仿真环境，利用其 GPU 加速的多物理引擎对机械臂的翻滚步态、稳定性及地形适应性进行了系统评估，并生成了关键运动数据集。该工作展示了 Isaac Sim 在复杂移动操作机器人开发中的价值，为核设施等危险环境下的自主作业提供了仿真验证基础。

- ["CleanUpBench: Embodied Sweeping and Grasping Benchmark" (2025)](http://arxiv.org/abs/2508.05543v1) [PDF](https://arxiv.org/pdf/2508.05543v1) — 该论文提出了CleanUpBench，一个面向移动清洁机器人的新型具身智能基准，用于评估扫地与抓取双模态任务性能。该基准基于NVIDIA Isaac Sim构建，模拟配备扫地装置和六自由度机械臂的服务机器人，在手工设计及程序生成的室内环境中执行多目标清理任务，并提供涵盖任务完成率、空间效率等维度的综合评测体系。其在Isaac Sim中实现的高保真物理交互与可扩展场景为具身智能算法提供了贴近现实的测试平台。

- ["UniFucGrasp: Human-Hand-Inspired Unified Functional Grasp Annotation Strategy and Dataset for Diverse Dexterous Hands" (2025)](http://arxiv.org/abs/2508.03339v2) [PDF](https://arxiv.org/pdf/2508.03339v2) — 本文提出UniFucGrasp，一种受人手启发的通用功能性抓取标注策略与数据集，支持多种灵巧手结构。该方法基于仿生学将人类自然动作映射到不同机械手，并在Isaac Sim中进行仿真验证，利用其GPU加速的多物理场模拟能力评估抓取的功能性与稳定性。实验表明该方法显著提升跨手型的功能操作准确率与泛化能力，降低标注成本，为灵巧操作提供高质量数据基础。

- ["Learning stable bipedal locomotion skills for quadrupedal robots on challenging terrains with automatic fall recovery" (2025)](https://openalex.org/W4412840387) [PDF](https://www.nature.com/articles/s44182-025-00043-2.pdf) (Citations: 3) — npj Robotics — 该论文提出了一种基于强化学习的方法，用于在复杂地形上为四足机器人学习稳定的双足运动技能并实现自动跌倒恢复。研究在 NVIDIA Isaac Sim 中构建高保真仿真环境，利用其 GPU 加速的多物理引擎进行大规模并行训练，并生成包含崎岖地形和扰动的多样化训练场景。该方法显著提升了机器人在真实世界中的运动鲁棒性和恢复能力。

- ["Benchmarking Massively Parallelized Multi-Task Reinforcement Learning for Robotics Tasks" (2025)](http://arxiv.org/abs/2507.23172v2) [PDF](https://arxiv.org/pdf/2507.23172v2) — 该论文提出了MTBench，一个大规模并行多任务强化学习基准，包含50个操作任务和20个移动任务，专门在Isaac Gym（Isaac Sim的GPU加速仿真环境）中实现。作者整合了四种基础RL算法与七种前沿MTRL方法，系统评估了高并行化下on-policy算法的性能优势。该基准显著加速了多任务策略训练与评估，为机器人通用智能体研究提供了可复现、高效率的实验平台。

- ["Digital Twin Robotics: Immersive Software-in-the-Loop Testing with OpenUSD, Isaac Sim, and ROS" (2025)](https://openalex.org/W4412900330) [PDF](https://dl.acm.org/doi/pdf/10.1145/3721251.3734066?download=true) — 该论文提出了一种基于数字孪生的沉浸式软件在环测试框架，核心贡献在于集成 OpenUSD、Isaac Sim 和 ROS 实现高保真机器人仿真与验证。作者将 Isaac Sim 作为主要仿真平台，利用其 GPU 加速的多物理场模拟能力构建动态一致的虚拟环境，并通过 ROS 接口实现真实机器人软件栈的无缝对接。该方法显著提升了测试效率与真实性，适用于复杂场景下的机器人算法验证与部署。

- ["Shared Control of Holonomic Wheelchairs through Reinforcement Learning" (2025)](http://arxiv.org/abs/2507.17055v1) [PDF](https://arxiv.org/pdf/2507.17055v1) — arXiv (Cornell University) — 本文提出一种基于强化学习的共享控制方法，用于全向轮椅的智能导航，将用户2D输入映射为3D运动指令，在保障安全的同时降低认知负荷。该方法在Isaac Gym中完成训练，并在Gazebo中进行仿真测试，系统比较了不同RL架构与奖励函数对用户舒适度和操作流畅性的影响。研究成功实现了从仿真到现实的迁移，展示了首个基于RL的全向轮椅共享控制真实部署，凸显Isaac Sim（Isaac Gym）在高效策略训练中的关键作用。

- ["Digital Twin-Enabled Adaptive Robotics: Leveraging Large Language Models in Isaac Sim for Unstructured Environments" (2025)](https://openalex.org/W4415775569) (Citations: 2) — Machines — 该论文提出一个融合数字孪生、本地大语言模型与实时感知的自适应机器人框架，用于非结构化环境中的协作任务。系统以 Isaac Sim 为核心仿真平台，实现物理 YuMi 机器人与其虚拟环境的双向同步，并通过 RealSense 相机和 Mistral 7B 模型支持语音交互与环境理解。在医院显微镜载玻片分拣任务中，Isaac Sim 确保了98.11%的关节运动同步精度，验证了其在高保真机器人数字孪生中的关键作用。

- ["Probabilistic Human Intent Prediction for Mobile Manipulation: An Evaluation with Human-Inspired Constraints" (2025)](http://arxiv.org/abs/2507.10131v1) [PDF](https://arxiv.org/pdf/2507.10131v1) — arXiv (Cornell University) — 本文提出GUIDER框架，通过双阶段概率推理实现对人类导航与操作意图的实时识别。研究在Isaac Sim中构建了包含25次人机交互试验的评估环境，利用其高保真物理仿真和传感器模拟能力，验证了GUIDER在重定向和几何约束场景下显著优于基线方法的稳定性（提升31.4%–39.5%）。该工作展示了Isaac Sim作为人机协作算法验证平台的有效性，为移动操作机器人提供了可部署的意图预测解决方案。

- ["Automated Behaviour-Driven Acceptance Testing of Robotic Systems" (2025)](http://arxiv.org/abs/2507.05125v1) [PDF](https://arxiv.org/pdf/2507.05125v1) — arXiv (Cornell University) — 该论文提出一种基于行为驱动开发（BDD）的自动化验收测试框架，用于机器人系统的规范验证。研究通过领域特定语言和知识图谱建模生成可执行测试，并将 Isaac Sim 作为核心仿真环境，与 BDD 框架和模型转换模块集成，实现对抓取放置任务中不同智能体与环境配置的自动化测试与评估。该方法显著提升了机器人系统验证的严谨性与可靠性。

- ["A multimodal digital twin for autonomous micro-drilling in scientific exploration" (2025)](https://openalex.org/W4411701295) [PDF](https://link.springer.com/content/pdf/10.1007/s11548-025-03465-3.pdf) — International Journal of Computer Assisted Radiology and Surgery — 该论文提出了一种多模态数字孪生系统，用于自主微钻颅骨窗口手术的模拟与训练。其核心创新在于将AMBF仿真器与Isaac Sim结合，利用Isaac Sim提供逼真的视觉渲染，生成高保真合成图像，并与深度音频生成模型协同工作，产生真实的钻孔声音。实验表明，基于Isaac Sim生成的合成图像训练的CNN在真实蛋壳图像上达到70.2 mAP，验证了该平台在多模态机器人训练中的实用价值。

- ["Bridging the Sim-to-Real Gap for Athletic Loco-Manipulation" (2025)](https://openalex.org/W4414050931) [PDF](https://doi.org/10.15607/rss.2025.xxi.125) (Citations: 2) — 该论文提出了一种结合强化学习与系统辨识的方法，以缩小仿真到现实的差距，实现高动态的运动-操作任务。作者在 Isaac Sim 中构建了高保真四足机器人模型，并利用其 GPU 加速的物理引擎进行大规模并行训练，生成了可迁移至真实 Unitree Go2 机器人的策略。研究展示了 Isaac Sim 在复杂动态任务中的仿真能力及其对现实部署的有效支撑。

- ["ViTaSCOPE: Visuo-tactile Implicit Representation for In-hand Pose and Extrinsic Contact Estimation" (2025)](https://openalex.org/W4414050430) [PDF](https://doi.org/10.15607/rss.2025.xxi.054) (Citations: 3) — 该论文提出了ViTaSCOPE方法，通过融合视觉与触觉信息构建隐式表示，用于估计手内物体的姿态及外部接触点。研究在Isaac Sim中搭建了高保真多模态仿真环境，利用其GPU加速的物理引擎生成带精确接触力和视觉数据的合成数据集，并在其中进行端到端训练与验证。该工作展示了Isaac Sim在复杂交互感知任务中的关键作用，为具身智能提供了可扩展的仿真训练范式。

- ["GRADE: Generating Realistic and Dynamic Environments for robotics research with Isaac Sim" (2025)](https://openalex.org/W4411616910) (Citations: 1) — The International Journal of Robotics Research — 本文提出GRADE框架，基于NVIDIA Isaac Sim构建高保真、动态且可定制的机器人仿真环境，用于生成富含物理信息与视觉细节的合成数据。该框架深度利用Isaac Sim的渲染能力、物理引擎及底层API，支持主动SLAM、多机器人协同等复杂场景的在线/离线评估，并引入新颖的实验复现机制，可在保持物理一致性的前提下对环境与任务进行灵活变体。其产出的高质量合成视频数据集显著推动了视觉感知与自主机器人研究的发展。

- ["Robotic Simulation Systems and Intelligent Offline Teaching for Urban Rail Transit Maintenance" (2025)](https://openalex.org/W4411352922) [PDF](https://www.mdpi.com/2079-9292/14/12/2431/pdf?version=1749896318) — Electronics — 该研究提出了一种面向城轨检修机器人的仿真系统与离线示教方法，核心贡献在于结合Gazebo与Isaac Sim构建多保真度开发流程。其中，Isaac Sim被明确用于复杂大规模场景下的高保真渲染与鲁棒物理仿真，支撑底盘检修机器人的传感器配置、环境建模及离线编程验证。实验表明，基于该系统的单次机械臂运动编程仅需30秒，显著提升教学效率，为轨道交通智能运维提供高效、安全的部署方案。

- ["SGN-CIRL: Scene Graph-based Navigation with Curriculum, Imitation, and Reinforcement Learning" (2025)](http://arxiv.org/abs/2506.04505v1) [PDF](https://arxiv.org/pdf/2506.04505v1) — arXiv (Cornell University) — 本文提出SGN-CIRL框架，结合3D场景图、课程学习、模仿学习与强化学习，实现无地图的机器人导航。该方法在Isaac Sim环境中进行训练与评估，利用其GPU加速的多物理仿真能力构建部分可观测的3D场景，并通过场景图显式建模物体间空间关系，显著提升复杂导航任务的成功率。研究成果为语义感知导航提供了高效可扩展的仿真训练范式。

- ["Bridging Virtual and Physical Robotics: An AI-Driven Educational Platform Using NVIDIA Omniverse Isaac Sim and Jetson Orin Nano" (2025)](https://openalex.org/W4413918282) — 该论文提出一个融合虚拟与实体机器人的AI教育平台，核心采用NVIDIA Omniverse Isaac Sim构建高保真仿真环境，并通过Jetson Orin Nano实现真实机器人控制。作者在Isaac Sim中开发了完整的教学实验流程，包括传感器模拟、强化学习训练和实时部署，显著降低了机器人教育的硬件门槛。该平台为高校和研究机构提供了可扩展、低成本的AI机器人教学与开发解决方案。

- ["Model-Based System Engineering Framework for Verification and Validation of Cyber-Physical Vehicle Systems" (2025)](https://openalex.org/W4414494115) — ASME Letters in Translational Robotics — 该论文提出了一种基于数字孪生的元建模框架，用于自动驾驶车辆系统的模块化建模、验证与确认。研究明确将 Isaac Sim 作为三大核心仿真环境之一，用于在自定义越野地形上对路径规划算法进行快速原型设计与性能评估，并结合 System Composer 实现需求可追溯的验证流程。该工作展示了 Isaac Sim 在复杂越野场景下支持多方案路径规划器对比实验的能力，为自主系统开发提供了高效、可扩展的仿真验证平台。

- ["FastTD3: Simple, Fast, and Capable Reinforcement Learning for Humanoid Control" (2025)](http://arxiv.org/abs/2505.22642v3) [PDF](https://arxiv.org/pdf/2505.22642v3) — 本文提出FastTD3算法，通过并行仿真、大批次更新、分布式的评论家网络和精细调参，在IsaacLab等平台上显著加速人形机器人控制任务的训练。作者在IsaacLab环境中验证了该方法可在单张A100 GPU上3小时内完成HumanoidBench多项任务，且训练过程稳定。该工作为基于Isaac Sim生态的强化学习研究提供了高效、轻量的实现方案。

- ["IndustryEQA: Pushing the Frontiers of Embodied Question Answering in Industrial Scenarios" (2025)](http://arxiv.org/abs/2505.20640v1) [PDF](https://arxiv.org/pdf/2505.20640v1) — arXiv (Cornell University) — 该论文提出了IndustryEQA，首个面向工业场景的具身问答（EQA）基准，专注于仓库环境中安全关键任务的感知与推理能力评估。研究基于NVIDIA Isaac Sim平台构建高保真仿真环境，生成包含动态人类、工业设备及危险情境的 episodic 视频，并提供1344个涵盖六类安全与认知维度的问题-答案对。该基准为开发适用于真实工业场景的安全感知具身智能体提供了重要数据支撑和评估标准。

- ["Omni-Perception: Omnidirectional Collision Avoidance for Legged Locomotion in Dynamic Environments" (2025)](http://arxiv.org/abs/2505.19214v2) [PDF](https://arxiv.org/pdf/2505.19214v2) — arXiv (Cornell University) — 本文提出Omni-Perception，一种端到端的四足机器人运动策略，通过直接处理原始LiDAR点云实现全向避障。其核心是PD-RiskNet感知模块，并开发了高保真LiDAR仿真工具包，明确支持Isaac Gym等平台用于高效策略训练和sim-to-real迁移。该方法在动态复杂环境中展现出优于基于中间地图方法的鲁棒性，为真实机器人部署提供实用价值。

- ["GenPO: Generative Diffusion Models Meet On-Policy Reinforcement Learning" (2025)](http://arxiv.org/abs/2505.18763v4) [PDF](https://arxiv.org/pdf/2505.18763v4) — 本文提出GenPO框架，将生成式扩散模型与on-policy强化学习结合，通过精确扩散逆映射和双虚拟动作机制解决扩散策略下状态-动作对数似然不可计算的问题。该方法在Isaac Lab的八个机器人基准任务（包括四足、人形行走与灵巧操作）上进行训练与验证，充分利用其GPU加速并行仿真能力。研究成果显著提升了on-policy算法在复杂机器人控制中的探索效率与稳定性，为Isaac Sim生态提供了新型可扩展的策略优化方案。

- ["H2-COMPACT: Human-Humanoid Co-Manipulation via Adaptive Contact Trajectory Policies" (2025)](http://arxiv.org/abs/2505.17627v1) [PDF](https://arxiv.org/pdf/2505.17627v1) — 本文提出H2-COMPACT框架，通过分层策略学习实现人形机器人与人类基于触觉线索的协同搬运。其底层策略在Isaac Gym中利用随机负载（0–3 kg）和摩擦条件进行深度强化学习训练，生成稳定、负载自适应的全身关节轨迹，并在MuJoCo和真实Unitree G1机器人上验证。该方法首次将学习到的触觉引导与全身腿式控制融合，实现流畅的人-人形机器人协同操作，具有高实用性与部署价值。

- ["RoboRAN: A Unified Robotics Framework for Reinforcement Learning-Based Autonomous Navigation" (2025)](http://arxiv.org/abs/2505.14526v2) [PDF](https://arxiv.org/pdf/2505.14526v2) — arXiv (Cornell University) — 本文提出RoboRAN，一个支持多域机器人强化学习导航的统一框架，其核心贡献之一是发布了首个开源API，用于将Isaac Lab中训练的策略部署到真实机器人上，实现轻量级推理与快速实地验证。该框架在Isaac Lab中构建训练环境，并通过统一的评估测试平台支持水下、陆地和太空等多介质导航任务，显著提升仿真到现实的迁移效率与跨平台可比性。

- ["Composing Dextrous Grasping and In-Hand Manipulation via Scoring with a Reinforcement Learning Critic" (2025)](https://openalex.org/W4413945820) [PDF](https://arxiv.org/pdf/2505.13253) (Citations: 1) — 该论文提出利用在手操作强化学习策略的Critic网络对初始抓取姿态进行评分与选择，从而桥接稳定抓取与后续操作目标之间的鸿沟。研究在Isaac Sim中构建了完整的抓取-操作仿真环境，用于训练和评估策略，并将所学策略成功迁移到真实机器人系统，实现了对复杂物体的自主抓取与重定向。该方法显著提升在手操作成功率，且无需额外训练，在Isaac Sim平台上的高效仿真是其关键支撑。

- ["Depth Transfer: Learning to See Like a Simulator for Real-World Drone Navigation" (2025)](http://arxiv.org/abs/2505.12428v1) [PDF](https://arxiv.org/pdf/2505.12428v1) — 该论文提出一种基于变分自编码器的深度迁移方法，通过域自适应对齐仿真与真实深度数据的潜在空间，实现无需微调的策略迁移。研究在 Isaac Gym 中训练无人机避障策略，并利用其生成的立体深度数据成功迁移到 AvoidBench 和真实环境，显著提升避障成功率。该工作凸显了 Isaac Gym 作为高效 RL 训练平台在视觉驱动无人机导航中的关键作用。

- ["Learning to Walk with Hybrid Serial-Parallel Linkages: a Case Study on the Kangaroo Robot" (2025)](https://openalex.org/W4414969711) — HAL (Le Centre pour la Communication Scientifique Directe) — 本文提出了一种端到端强化学习训练流程，用于控制具有混合串并联腿部结构的72自由度袋鼠机器人Kangaroo实现行走，未对复杂运动学进行简化。研究核心依赖Isaac Lab框架，并充分利用Isaac Sim内置的约束建模能力来准确模拟并联机构的动力学行为。通过在Isaac Sim中训练并在MuJoCo中验证，展示了策略在跨仿真器部署中的鲁棒性，为高保真仿人机器人控制提供了实用范例。

- ["PROBE: Proprioceptive Obstacle Detection and Estimation while Navigating in Clutter" (2025)](http://arxiv.org/abs/2505.11848v1) [PDF](https://arxiv.org/pdf/2505.11848v1) — 本文提出PROBE方法，利用机器人本体感知（如关节扭矩与全身运动）通过Transformer网络推断被遮挡的矩形障碍物的尺寸与SE(2)位姿，无需依赖视觉。该方法在Isaac Gym中构建的模拟环境中进行训练与评估，并在真实Unitree Go1四足机器人上验证有效性。研究展示了Isaac Gym作为高保真、GPU加速仿真平台在复杂导航任务中的关键作用，为视觉受限场景下的自主导航提供了实用解决方案。

- ["Surgical Robotics Environment in NVIDIA Isaac Sim for Robot-Assisted Suturing" (2025)](https://openalex.org/W4411272480) — 该论文构建了一个基于NVIDIA Isaac Sim的外科手术机器人仿真环境，专门用于机器人辅助缝合任务。作者利用Isaac Sim的GPU加速物理引擎和高保真渲染能力，开发了包含柔性组织形变、缝合针交互及力反馈的多物理场仿真系统，并生成了用于训练强化学习策略的合成数据集。该环境为手术机器人算法的快速迭代与安全验证提供了可扩展、高保真的测试平台。

- ["Web2Grasp: Learning Functional Grasps from Web Images of Hand-Object Interactions" (2025)](http://arxiv.org/abs/2505.05517v2) [PDF](https://arxiv.org/pdf/2505.05517v2) — 本文提出Web2Grasp方法，从网络图像中提取人类手-物交互信息以学习功能性抓取策略，避免依赖昂贵的机器人演示。作者利用IsaacGym进行物理仿真，将基于网络数据初步训练的抓取策略用于生成大量物理可行且保持功能性的抓取样本，显著提升模型在已见与未见物体上的成功率和功能性评分。该工作展示了IsaacGym在扩展低成本抓取数据集和验证抓取策略中的关键作用，为多指灵巧手的功能性操作提供了高效训练范式。

- ["MULE: Multi-terrain and Unknown Load Adaptation for Effective Quadrupedal Locomotion" (2025)](http://arxiv.org/abs/2505.00488v1) [PDF](https://arxiv.org/pdf/2505.00488v1) — 该论文提出一种自适应强化学习框架MULE，使四足机器人能动态适应不同负载与复杂地形。研究在Isaac Gym中进行大规模仿真训练和验证，结合真实Unitree Go1机器人部署，展示了无需预设步态即可在斜坡、楼梯等场景下稳健执行任务的能力。该工作凸显了Isaac Gym作为高效RL训练平台在机器人运动控制中的关键作用。

- ["Compound Koopman data-driven control for an inchworm robot: validation through virtual experiments" (2025)](https://openalex.org/W4410506136) — Robotica — 本文提出一种结合分数阶PID控制与Koopman算子理论的复合数据驱动控制方法，用于解决尺蠖机器人高度非线性动力学带来的控制难题。作者在NVIDIA Isaac Sim中构建虚拟实验环境，利用深度神经网络学习Koopman算子以实现非线性系统线性化，并在此基础上设计FPID控制器，显著提升了轨迹跟踪精度与运动效率。该工作展示了Isaac Sim作为高保真仿真平台在生物启发机器人控制验证中的关键作用。

- ["Efficient trajectory planning for a 4-DOF robotic arm with curve interpolation and Gaussian process inference for pick-and-place manipulation tasks" (2025)](https://openalex.org/W4410412228) — Robotica — 本文提出了一种结合贝塞尔曲线插值与高斯过程推理的高效轨迹规划方法，用于4自由度机械臂的抓取放置任务。作者在Nvidia Isaac Sim中构建仿真环境，对所提方法进行验证，利用自定义指标评估轨迹偏差与平滑性，并通过高斯过程结合先验与平滑因子优化可行轨迹。该方法显著降低了计算复杂度，为实时机器人控制提供了高效、平滑的轨迹生成方案。

- ["High-Performance Reinforcement Learning on Spot: Optimizing Simulation Parameters with Distributional Measures" (2025)](http://arxiv.org/abs/2504.17857v3) [PDF](https://arxiv.org/pdf/2504.17857v3) — 该论文提出了一种基于分布度量优化仿真参数的高性能强化学习方法，首次实现了端到端RL策略在Boston Dynamics Spot机器人上的部署。作者明确使用NVIDIA IsaacLab作为训练平台，利用Wasserstein距离和最大均值差异量化仿真与真实数据的分布差异，并以此指导CMA-ES算法优化未知物理参数。所训练策略支持多种步态（含腾空相），实现超5.2m/s的高速运动，显著超越Spot默认控制器性能，为四足机器人高敏捷控制提供了可复现的开源方案。

- ["Performance Analysis of a Mass-Spring-Damper Deformable Linear Object Model in Robotic Simulation Frameworks" (2025)](http://arxiv.org/abs/2504.13659v1) [PDF](https://arxiv.org/pdf/2504.13659v1) — 该论文提出基于质量-弹簧-阻尼器（MSD）模型的可变形线性物体（DLO）仿真方法，用于机器人操作任务中的力数据采集。研究明确使用 Isaac Sim 作为核心仿真平台之一，结合域随机化技术系统评估模型参数变化对 DLO 动力学行为的影响，并与 Gazebo 进行对比验证。该工作为在 Isaac Sim 中训练处理柔性物体的机器人策略提供了关键数据和方法支持。

- ["Reducing the Sim2Real gap for vacuum grasping in Isaac Sim" (2025)](https://openalex.org/W4410298109) — 本文提出了一种用于真空抓取的新型接触计算模型，明确集成到NVIDIA Isaac Sim平台中，以缩小仿真与现实之间的差距。该模型通过准静态弹簧模拟吸盘形变，并引入五项密封形成条件及表面缺陷检测规则，显著提升了对复杂几何物体抓取过程中密封失效的仿真精度。实验表明，相比Isaac Sim默认的Surface Gripper，该方法在存在孔洞、凸起等表面不连续性时更准确地复现真实抓取行为，为高保真机器人抓取仿真提供了关键工具。

- ["Learning Dual-Arm Coordination for Grasping Large Flat Objects" (2025)](http://arxiv.org/abs/2504.03500v1) [PDF](https://arxiv.org/pdf/2504.03500v1) — 本文提出一种基于模型无关深度强化学习的双臂协同抓取框架，用于抓取大型平面物体。作者在Isaac Gym中构建高保真仿真环境，利用大规模抓取姿态检测模型提取图像特征作为强化学习状态输入，并采用共享Actor-Critic结构的CNN-PPO算法训练双臂协调策略。该方法在Isaac Gym中完成端到端训练后可零样本迁移到真实机器人，无需微调即实现对未见物体的高效抓取，显著优于基线方法。

- ["Bench2FreeAD: A Benchmark for Vision-based End-to-end Navigation in Unstructured Robotic Environments" (2025)](http://arxiv.org/abs/2503.12180v2) [PDF](https://arxiv.org/pdf/2503.12180v2) — 本文提出首个面向非结构化场景端到端机器人导航的基准 Bench2FreeAD，并构建了 FreeWorld 数据集，其中包含使用 Isaac Sim 生成的合成数据。作者利用 Isaac Sim 模拟器搭建非结构化道路环境（如辅路、校园和室内），生成高保真视觉数据用于训练和验证 VAD 模型。该工作显著提升了端到端导航模型在服务与物流机器人中的适应性与性能，为真实世界部署提供了仿真-现实协同的数据基础。

- ["MarineGym: A High-Performance Reinforcement Learning Platform for Underwater Robotics" (2025)](http://arxiv.org/abs/2503.09203v1) [PDF](https://arxiv.org/pdf/2503.09203v1) — arXiv (Cornell University) — 本文提出了MarineGym，一个专为水下机器人强化学习设计的高性能平台，其核心创新在于集成了基于Isaac Sim开发的GPU加速流体动力学插件，实现在单块RTX 3060 GPU上每秒25万帧的 rollout 速度。该平台利用Isaac Sim作为底层仿真引擎，提供五种无人水下航行器模型、多种推进系统及标准化任务，并结合域随机化工具提升Sim2Real迁移能力。MarineGym显著提升了训练效率与策略鲁棒性，为水下机器人RL研究提供了高效、可复现的基准环境。

- ["Multitask Reinforcement Learning for Quadcopter Attitude Stabilization and Tracking using Graph Policy" (2025)](http://arxiv.org/abs/2503.08259v1) [PDF](https://arxiv.org/pdf/2503.08259v1) — 该论文提出一种基于图卷积网络的多任务强化学习框架，用于四旋翼飞行器的姿态稳定与跟踪控制。作者利用 Isaac Gym 进行大规模并行仿真，训练多任务 Soft Actor-Critic 策略，在统一架构下高效处理两种不同控制任务。所学策略仅含两层24神经元网络，成功部署于 Pixhawk 飞控实现400 Hz实时控制，验证了 Isaac Sim 平台在高样本效率机器人策略开发中的实用价值。

- ["Safe Distributed Learning-Enhanced Predictive Control for Multiple Quadrupedal Robots" (2025)](http://arxiv.org/abs/2503.05836v1) [PDF](https://arxiv.org/pdf/2503.05836v1) — 该论文提出了一种用于多足机器人编队控制的分布式学习增强预测控制框架，结合控制李雅普诺夫函数与控制屏障函数保障稳定性和安全性，并设计了SAPIE编码机制以适应动态团队结构。研究在NVIDIA Omniverse Isaac Sim中进行了高保真仿真验证，利用其GPU加速的多物理场模拟能力评估编队稳定性、实时协调性与避障性能，为大规模四足机器人协同部署提供了可靠方案。

- ["Hierarchical Reinforcement Learning for Quadrupedal Robots: Efficient Object Manipulation in Constrained Environments" (2025)](https://openalex.org/W4408133349) [PDF](https://www.mdpi.com/1424-8220/25/5/1565/pdf?version=1741072866) (Citations: 1) — Sensors — 该论文提出了一种面向四足机器人物体操作任务的分层强化学习框架，通过新颖的基于传感器观测的奖励函数提升在密集障碍环境中的决策能力。研究在 NVIDIA Isaac Sim 中使用 ANYbotics 四足机器人进行仿真训练与测试，实现了平均 11 厘米的定位精度和高效路径规划。该工作展示了 Isaac Sim 在复杂物理交互与机器人策略部署中的关键支撑作用，具有实际应用潜力。

- ["Aerial Gym Simulator: A Framework for Highly Parallelized Simulation of Aerial Robots" (2025)](http://arxiv.org/abs/2503.01471v1) [PDF](https://arxiv.org/pdf/2503.01471v1) — 本文提出了Aerial Gym Simulator，一个基于NVIDIA Isaac Gym构建的高并行化、模块化空中机器人仿真框架，支持欠驱动、全驱动和过驱动多旋翼平台的仿真。该框架集成了并行几何控制器和自定义GPU加速的光线投射渲染系统，可生成深度、分割及顶点级环境标注，并成功实现了基于强化学习的深度导航策略及其sim2real迁移。其与Isaac Sim生态紧密集成，为无人机控制、规划与感知研究提供了高效工具。

- ["Runtime Learning of Quadruped Robots in Wild Environments" (2025)](http://arxiv.org/abs/2503.04794v2) [PDF](https://arxiv.org/pdf/2503.04794v2) — 本文提出一种四足机器人在野外环境中的运行时学习框架，核心包含高性能DRL代理（HP-Student）与高保障物理模型控制器（HA-Teacher）的协同机制。该框架在Nvidia Isaac Gym中进行仿真实验，利用其GPU加速的多物理场模拟能力验证了方法在动态复杂地形下的安全性与适应性。实验基于Unitree Go2机器人平台，展示了相较现有安全DRL方法的优越性能，为真实世界部署提供了可靠仿真基础。

- ["Multi-Keypoint Affordance Representation for Functional Dexterous Grasping" (2025)](http://arxiv.org/abs/2502.20018v2) [PDF](https://arxiv.org/pdf/2502.20018v2) — 该论文提出多关键点可供性表示方法（CMKA）与基于关键点的抓取矩阵变换（KGT），通过人类抓握图像弱监督和大视觉模型提取细粒度可供性特征，实现任务驱动的灵巧抓取。研究在Isaac Gym仿真环境中进行大量实验，验证了方法在抓取姿态一致性、未见工具泛化能力及可供性定位精度上的显著提升。该工作直接利用Isaac Gym作为核心仿真平台，支撑算法训练与评估，对基于物理仿真的灵巧操作研究具有重要应用价值。

- ["Wheeled Lab: Modern Sim2Real for Low-cost, Open-source Wheeled Robotics" (2025)](http://arxiv.org/abs/2502.07380v2) [PDF](https://arxiv.org/pdf/2502.07380v2) — 本文提出Wheeled Lab，一个面向低成本开源轮式机器人的现代Sim2Real生态系统，其核心是将实体小车与Isaac Lab深度集成，用于端到端强化学习策略开发。作者基于Isaac Lab构建了高保真仿真环境，并成功训练出三种零样本迁移策略：可控漂移、越障行驶和视觉导航，全部在真实RC小车上实现零样本部署。该工作显著降低了机器人学习的硬件与软件门槛，为教育和研究提供了可复现、开放且经济的Isaac Sim应用范例。

- ["Value-Based Deep RL Scales Predictably" (2025)](http://arxiv.org/abs/2502.04327v2) [PDF](https://arxiv.org/pdf/2502.04327v2) — 该论文提出价值型离策略深度强化学习方法具有可预测的扩展规律，通过更新数据比（UTD）构建数据与计算资源的帕累托前沿，并据此优化超参数分配以最大化给定预算下的性能。研究在IsaacGym等平台上验证了SAC、BRO和PQL算法在数据、算力或性能外推时的可预测性，明确将IsaacGym作为核心实验环境之一。该工作为高效利用Isaac Sim生态中的GPU加速RL训练提供了理论指导和实践框架。

- ["ASAP: Aligning Simulation and Real-World Physics for Learning Agile Humanoid Whole-Body Skills" (2025)](http://arxiv.org/abs/2502.01143v3) [PDF](https://arxiv.org/pdf/2502.01143v3) — 本文提出ASAP框架，通过两阶段方法解决仿真与现实之间的动力学差异问题，显著提升人形机器人全身敏捷运动能力。该方法在IsaacGym中预训练运动跟踪策略，并利用真实世界数据训练残差动作模型，再将该模型集成回仿真器进行微调；特别地，论文明确将Isaac Sim作为关键迁移目标之一（IsaacGym → IsaacSim），验证了其在GPU加速多物理仿真平台上的有效性。该工作为基于Isaac Sim的高保真机器人技能迁移提供了实用范式。

- ["Real Case Studies in Industry 5.0: The Example of Nvidia" (2025)](https://openalex.org/W4406825094) (Citations: 1) — 该研究探讨了英伟达在推动Industry 5.0转型中的关键技术贡献，重点分析了Isaac平台在人形机器人开发中的作用。论文明确指出Isaac Sim被用于构建高保真仿真环境，以模拟人类行为并与GR00T模型和Jetson Thor芯片协同实现安全高效的人机协作。这一应用凸显了Isaac Sim作为核心仿真工具在下一代协作机器人研发中的关键价值。

- ["Sim-to-Real Transfer for Mobile Robots with Reinforcement Learning: from NVIDIA Isaac Sim to Gazebo and Real ROS 2 Robots" (2025)](http://arxiv.org/abs/2501.02902v1) [PDF](https://arxiv.org/pdf/2501.02902v1) (Citations: 2) — arXiv (Cornell University) — 该论文提出了一种基于NVIDIA Isaac Sim的端到端强化学习框架，用于移动机器人的局部路径规划与避障，重点解决以外感知（exteroception）为基础的策略可复现性问题。作者在Isaac Sim中训练自定义机器人策略，并成功实现零样本迁移到Gazebo仿真及真实ROS 2机器人，验证了策略的泛化能力。实验表明其性能与Nav2导航栈相当，为定制机器人平台快速部署先进局部规划器提供了可行路径。

- ["Choosing the Arena: A Systematic Review of Simulators for Deep Reinforcement Learning in Mobile Robot Navigation" (2025)](https://openalex.org/W7118007974) [PDF](https://thesai.org/Downloads/Volume16No12/Paper_62-Choosing_the_Arena_A_Systematic_Review_of_Simulators.pdf) — International Journal of Advanced Computer Science and Applications — 该论文通过系统性文献综述提出了一种基于实证的机器人仿真器分类框架，将仿真平台划分为三类原型。其中，第三类（Archetype III）明确将 NVIDIA Isaac Sim 作为 GPU 原生引擎的代表，用于大规模、感知密集型的深度强化学习任务，强调其在逼真渲染和并行仿真方面的优势，以支持零样本迁移。研究为 Isaac Sim 在高保真、数据驱动的移动机器人导航研究中的战略应用提供了理论依据和选型指导。

- ["Isaac Sim Integrated Digital Twin for Feasibility Checks in Skill-Based Engineering" (2025)](https://openalex.org/W4413869787) — Mechanisms and machine science — 该论文提出了一种将Isaac Sim集成到数字孪生系统中的方法，用于在基于技能的工程中进行可行性验证。作者利用Isaac Sim构建高保真机器人操作仿真环境，通过实时物理仿真与传感器模拟，对自动化任务序列进行虚拟验证，显著提升工程部署前的可靠性评估效率。该方法为智能制造中的快速原型设计和技能模块验证提供了高效、可扩展的仿真平台。

- ["Automatic Docking of Modules of Modular Robots: Development and Evaluation of an Automatic Docking Method in Isaac Sim" (2025)](https://openalex.org/W7115909426) [PDF](https://www.jstage.jst.go.jp/article/jrsj/43/10/43_43_1012/_pdf) — Journal of the Robotics Society of Japan — 该论文提出了一种模块化机器人自动对接方法，并在 Isaac Sim 中完整实现了对接系统的仿真环境与控制策略。作者利用 Isaac Sim 的高保真物理引擎和传感器模拟功能，对磁吸式对接机构的运动规划、视觉引导和容错控制进行了系统性开发与评估。实验结果验证了该方法在复杂扰动下的鲁棒性，为模块化机器人自主组装提供了可复现的仿真基准。

- ["Adaptive Multi-Robot Exploration for Unknown Environments Using Edge-Weighted Path Planning" (2025)](https://openalex.org/W4411472236) (Citations: 1) — IEEE Access — 本文提出了一种可扩展的自适应多机器人探索算法，通过动态更新基于访问次数、路径预留和障碍物信息的边权重，优化路径分配并实现100%区域覆盖。研究在Isaac Sim中构建了高保真3D环境，并通过ROS集成进行算法验证，展示了其在探索效率与实时适应性方面的优势。该方法为实际多机器人系统在未知环境中的协同探索提供了高效可行的解决方案。

- ["Realistic Simulation of Urban Air Mobility Scenarios" (2025)](https://openalex.org/W7126737649) — 该论文提出了一种基于Isaac Sim构建的高保真城市空域仿真工具，用于模拟符合欧盟U-space法规的大量无人机在城市环境中的飞行。作者充分利用Isaac Sim的GPU加速多物理引擎和并行任务执行能力，实现超现实的空域冲突预测与系统验证，显著降低真实部署前的开发与测试成本。该工作直接将Isaac Sim作为核心仿真平台，支撑整个UAM场景的建模与分析。

- ["Digital Twin-Enabled Robotic Automation of Electrolyzer Assemblies for Power-to-X Solutions" (2025)](https://openalex.org/W4413882120) — Mechanisms and machine science — 该论文提出了一种基于数字孪生的机器人自动化系统，用于电解槽组件的高精度装配，以支持Power-to-X能源解决方案。作者在Isaac Sim中构建了完整的电解槽装配产线数字孪生环境，利用其GPU加速的多物理仿真能力对机械臂运动规划、夹具交互和装配容差进行高保真验证。该工作展示了Isaac Sim在工业级绿色能源设备自动化中的关键作用，为复杂精密装配任务提供了可扩展的虚拟调试平台。

- ["ORB-SLAM2 System Enhanced With SiaT-Hough Module on Mars Digital Twin Platform: For Rock Counting and 3D Reconstruction in Martian Environments" (2025)](https://openalex.org/W4412030352) — IEEE Access — 本文提出了一种基于NVIDIA Isaac Sim构建的火星数字孪生平台，通过程序化地形生成与资产管理创建具有多尺度精细地貌特征的随机火星环境，并在此平台上集成SiaT-Hough模块增强ORB-SLAM2系统，实现火星岩石的语义分割、3D重建与计数。Isaac Sim作为核心仿真平台，提供了高保真物理渲染与可编程场景生成能力，支撑了轻量级Siamese Transformer与Hough变换联合模型的训练与验证。该系统在火星仿真数据集上达到87.86%分割精度和57.34 FPS处理速度，为行星探测任务中的实时感知与建图提供了可行方案。

- ["Performance Analysis of a Mass-Spring-Damper Deformable Linear Object Model in Robotic Simulation Frameworks" (2025)](https://openalex.org/W4410514945) [PDF](https://arxiv.org/pdf/2504.13659) — Springer proceedings in advanced robotics — 该论文系统评估了质量-弹簧-阻尼器模型在多种机器人仿真框架中模拟可变形线性物体（DLO）的性能表现。研究明确将 Isaac Sim 作为核心实验平台之一，与 PyBullet 和 MuJoCo 进行对比，利用其 GPU 加速的多物理场仿真能力实现高保真 DLO 动态模拟，并提供了详细的性能指标和参数配置。该工作为在 Isaac Sim 中开展柔性物体操作任务提供了重要基准和实践指导。

- ["GOME-NGU: Visual Navigation Under Sparse Reward via Goal-Oriented Memory Encoder With Never Give Up" (2025)](https://openalex.org/W4409049667) — IEEE Access — 本文提出GOME-NGU算法，通过结合Never Give Up（NGU）的充分探索与目标导向记忆编码器（GOME）的高效利用，提升稀疏奖励下视觉导航性能。研究在NVIDIA Isaac Gym中完成训练，并将策略迁移至Isaac Sim进行验证，还在Husky机器人平台上测试了算法在真实感仿真环境中的路径优化能力。该工作凸显了Isaac Sim在强化学习策略迁移验证中的关键作用，为机器人导航提供了高保真评估平台。

- ["Learning an Adaptive Fall Recovery Controller for Quadrupeds on Complex Terrains" (2024)](http://arxiv.org/abs/2412.16924v1) [PDF](https://arxiv.org/pdf/2412.16924v1) — 本文提出了一种自适应跌倒恢复（AFR）控制器，利用深度强化学习使四足机器人在岩石、陡坡等复杂地形中高效恢复站立。研究在 Isaac Gym 中基于 Go1 机器人进行训练，并成功将策略直接迁移到 Spot 和 ANYmal 等真实平台，在 Gazebo 中也验证了有效性。该方法显著提升了恢复成功率与速度，展示了 Isaac Sim 在高保真、可迁移机器人控制策略开发中的关键作用。

- ["RoboMIND: Benchmark on Multi-embodiment Intelligence Normative Data for Robot Manipulation" (2024)](http://arxiv.org/abs/2412.13877v3) [PDF](https://arxiv.org/pdf/2412.13877v3) (Citations: 2) — arXiv (Cornell University) — 本文提出了RoboMIND数据集，包含107k条多机器人平台的操作演示轨迹，并在Isaac Sim中构建了对应数字孪生环境，精确复现真实任务与资产。该仿真环境支持低成本生成额外训练数据并高效评估策略，显著提升视觉-语言-动作模型的泛化能力与操作成功率。这项工作为基于Isaac Sim的机器人模仿学习和多具身智能研究提供了高质量基准资源。

- ["АУТОНОМНА НАВИГАЦИЈА РОБОТА МЕЂУ РЕДОВИМА ПОЉОПРИВРЕДНИХ ЗАСАДА" (2024)](https://openalex.org/W4405171754) [PDF](https://www.ftn.uns.ac.rs/ojs/index.php/zbornik/article/download/3733/3349) — Zbornik radova Fakulteta tehničkih nauka u Novom Sadu — 该论文提出并比较了基于传统图像处理与YOLOv8机器学习的两种农田行间自主导航方法，重点解决作物行末端识别与跨行转向问题。研究在NVIDIA Isaac Sim中构建高保真农田仿真环境，生成带语义标注的数据集用于训练YOLOv8模型，并在ROS 2框架下集成RTK-GPS与NAV2 PurePursuit路径跟踪器。该工作展示了Isaac Sim在农业机器人感知模型训练和系统验证中的关键作用，为低成本、可扩展的田间自主导航提供了实用方案。

- ["InfiniteWorld: A Unified Scalable Simulation Framework for General Visual-Language Robot Interaction" (2024)](http://arxiv.org/abs/2412.05789v1) [PDF](https://arxiv.org/pdf/2412.05789v1) (Citations: 1) — arXiv (Cornell University) — 本文提出InfiniteWorld，一个基于NVIDIA Isaac Sim构建的统一可扩展仿真框架，专为通用视觉-语言机器人交互设计。该框架整合了生成驱动的3D资产构建、Real2Sim迁移、自动化标注与统一资产处理流程，并在Isaac Sim中实现了四个新型通用基准任务，包括场景图协同探索与开放世界社交移动操作。这些基准全面评估具身智能体在环境理解、任务规划与多智能体交互方面的能力，为大规模具身AI研究提供标准化平台。

- ["NaVILA: Legged Robot Vision-Language-Action Model for Navigation" (2024)](http://arxiv.org/abs/2412.04453v2) [PDF](https://arxiv.org/pdf/2412.04453v2) — 本文提出NaVILA，一种用于足式机器人视觉-语言导航的两层框架，通过将视觉语言模型与运动技能解耦，先生成含空间信息的中层语言指令（如“前进75cm”），再由基于视觉的强化学习策略执行低层关节控制。该方法在IsaacLab中构建的新基准上进行了验证，利用其高保真物理仿真和低层控制接口，实现了更贴近现实的复杂场景导航，并支持真实机器人迁移。研究显著提升了现有VLA方法在具身导航任务中的性能与泛化能力。

- ["Learning Dual-Arm Push and Grasp Synergy in Dense Clutter" (2024)](http://arxiv.org/abs/2412.04052v2) [PDF](https://arxiv.org/pdf/2412.04052v2) — 该论文提出了一种目标导向的分层深度强化学习框架，用于在密集杂乱环境中学习双臂推-抓协同策略。作者在Isaac Gym中开发并训练了该系统，利用预训练视觉主干网络和基于CNN的PPO算法DRL模型，结合新颖的模糊奖励函数，有效映射视觉输入到6自由度双臂推抓动作。该方法显著提升了在复杂场景中对目标物体的成功抓取率，并在仿真与真实机器人上验证了其有效性。

- ["Robotic Path Planning Algorithms for Additive Manufacturing Using Advanced Simulation Tools" (2024)](https://openalex.org/W7123379658) [PDF](https://iconline.ipleiria.pt/bitstreams/c40ee2aa-2645-4fb2-ab4f-e2d53f631f8b/download) — IC-Online (Scientific Information of the Polytechnic Institute of Leiria) — 该论文提出并评估了用于机器人增材制造的路径规划算法MotionGen与模型预测控制（MPC），核心实验在NVIDIA Isaac Sim中进行，结合ROS2、MoveIt2和cuRobo库构建仿真测试平台。研究利用Isaac Sim实现动态障碍物环境下的轨迹生成与性能对比，结果表明MotionGen在能耗、时间效率和轨迹平滑性方面优于MPC，适用于实时增材制造场景。该工作展示了Isaac Sim作为高性能仿真平台在优化机器人AM控制算法中的关键作用。

- ["Bimanual Grasp Synthesis for Dexterous Robot Hands" (2024)](http://arxiv.org/abs/2411.15903v1) [PDF](https://arxiv.org/pdf/2411.15903v1) — 本文提出BimanGrasp算法，通过优化能量函数生成稳定可行的双手灵巧抓取姿态，并利用Isaac Gym物理仿真引擎对超过15万组抓取进行验证，构建了首个大规模双手灵巧抓取数据集BimanGrasp-Dataset。基于该数据集训练的扩散模型BimanGrasp-DDPM显著提升抓取生成速度与成功率。该工作直接依赖Isaac Sim（Isaac Gym）作为核心验证平台，为数据驱动的双手机器人操作提供高质量仿真基础。

- ["A Benchmark Dataset for Collaborative SLAM in Service Environments" (2024)](http://arxiv.org/abs/2411.14775v1) [PDF](https://arxiv.org/pdf/2411.14775v1) (Citations: 2) — IEEE Robotics and Automation Letters — 该论文提出了一个面向多机器人协同SLAM（C-SLAM）的新基准数据集CSE，专门针对医院、办公室和仓库等多样化室内服务场景。作者利用Isaac Sim构建高保真仿真环境，生成包含动态物体、同质化区域等真实挑战的多模态数据，包括精确时间同步的双目RGB、深度图像、IMU及真值位姿，并通过三台机器人模拟真实服务行为。该数据集为C-SLAM算法在复杂服务环境中的评估与开发提供了高质量、可复现的仿真平台。

- ["A systemic survey of the Omniverse platform and its applications in data generation, simulation and metaverse" (2024)](https://openalex.org/W4404509220) (Citations: 4) — Frontiers in Computer Science — 本文系统综述了NVIDIA Omniverse平台在多领域中的应用，重点探讨了Isaac Sim及其Isaac Gym和SDK在机器人仿真中的核心作用。论文详细分析了Isaac Sim如何支持高保真、GPU加速的物理模拟，并作为合成数据生成与强化学习训练的关键工具。该研究为理解Isaac Sim在Omniverse生态中的技术定位及实际应用价值提供了全面参考。

- ["Utilisation of Vision Systems and Digital Twin for Maintaining Cleanliness in Public Spaces" (2024)](http://arxiv.org/abs/2411.05964v1) [PDF](https://arxiv.org/pdf/2411.05964v1) — arXiv (Cornell University) — 该论文提出结合视觉系统与数字孪生技术管理公共场所清洁度，核心贡献在于利用Nvidia Omniverse Isaac Sim构建火车站的高保真虚拟环境，用于模拟和测试清洁策略。研究在Isaac Sim中实现了垃圾检测、垃圾桶填充识别、污渍分割及人员（含清洁工）行为分析等模块，并通过初步评估验证了系统的可行性。该工作展示了Isaac Sim作为清洁机器人算法开发与部署前验证平台的应用价值。

- ["TacEx: GelSight Tactile Simulation in Isaac Sim -- Combining Soft-Body and Visuotactile Simulators" (2024)](http://arxiv.org/abs/2411.04776v1) [PDF](https://arxiv.org/pdf/2411.04776v1) — arXiv (Cornell University) — 本文提出TacEx，一个模块化触觉仿真框架，通过将软体接触模拟器GIPC与视觉触觉模拟器Taxim和FOTS集成到Isaac Sim中，实现了对GelSight Mini传感器的高保真仿真。作者在Isaac Lab中构建了多个强化学习环境（如推物、抓取和杆平衡），利用Isaac Sim生成的凝胶形变与RGB图像作为高维观测输入，验证了策略训练的可行性与仿真稳定性。该工作显著增强了Isaac Sim在精细触觉交互任务中的能力，为接触密集型机器人操作提供了可扩展的仿真基础。

- ["Learning Generalizable Policy for Obstacle-Aware Autonomous Drone Racing" (2024)](http://arxiv.org/abs/2411.04246v1) [PDF](https://arxiv.org/pdf/2411.04246v1) — 该论文提出一种基于域随机化的深度强化学习方法，用于训练可泛化的障碍感知无人机竞速策略。作者在 Isaac Gym 环境中构建高保真无人机动力学模型，并通过在每次 rollout 前对赛道布局和障碍物配置进行随机化，结合并行经验采集，显著提升了策略在未见过的复杂环境中的泛化能力。实验中无人机在 Isaac Sim 支持的 GPU 加速仿真中达到 70 km/h 的高速，验证了方法的有效性，为真实世界障碍密集场景下的自主导航提供了可行路径。

- ["Evaluating PyBullet and Isaac Sim in the Scope of Robotics and Reinforcement Learning" (2024)](https://openalex.org/W4405709846) (Citations: 4) — 该论文系统评估了PyBullet与Isaac Sim在机器人学和强化学习任务中的性能差异，重点对比了两者在物理仿真精度、训练速度及可扩展性方面的表现。作者在Isaac Sim中实现了多个标准RL基准环境，并利用其GPU加速的并行仿真能力进行大规模策略训练，显著提升了样本效率。研究为选择高保真、高效率的机器人仿真平台提供了实证依据。

- ["The Role of Domain Randomization in Training Diffusion Policies for Whole-Body Humanoid Control" (2024)](http://arxiv.org/abs/2411.01349v1) [PDF](https://arxiv.org/pdf/2411.01349v1) — 本文研究扩散策略（Diffusion Policies）在全身人形机器人控制中的应用，重点探讨数据集多样性与规模对策略性能的影响。作者在Isaac Gym仿真环境中，通过在不同域随机化条件下训练对抗运动先验（AMP）智能体，生成多样化的合成演示数据，并系统评估了扩散策略在行走任务中的表现。研究表明，相比操作任务，人形机器人运动控制需要更大、更多样化的数据集才能实现稳定策略，为基于Isaac Sim的高保真仿真实验提供了重要参考。

- ["In-Simulation Testing of Deep Learning Vision Models in Autonomous Robotic Manipulators" (2024)](http://arxiv.org/abs/2410.19277v2) [PDF](https://arxiv.org/pdf/2410.19277v2) (Citations: 2) — 该论文提出MARTENS框架，通过集成NVIDIA Isaac Sim的逼真仿真环境与进化搜索算法，主动发现深度学习视觉模型在自主机械臂系统中的关键失效场景。Isaac Sim被用作核心测试平台，生成多样化、高保真的合成数据以优化目标检测模型并揭示系统设计缺陷。该方法在两个工业案例中显著提升故障检出率和多样性，训练修复后的模型在真实图像上达到0.91和0.82的mAP，验证了其从仿真到现实的有效迁移能力。

- ["NavRL: Learning Safe Flight in Dynamic Environments" (2024)](http://arxiv.org/abs/2409.15634v2) [PDF](https://arxiv.org/pdf/2409.15634v2) — arXiv (Cornell University) — 本文提出NavRL框架，一种基于PPO算法的深度强化学习导航方法，通过精心设计的状态与动作表示实现无人机在动静态障碍物环境中的安全飞行，并结合速度障碍启发的安全屏蔽机制提升可靠性。研究利用NVIDIA Isaac Sim构建并行训练环境，同时驱动数千架四旋翼无人机进行高效仿真训练，显著加速策略收敛，并成功实现零样本迁移到真实飞行。该方法为复杂动态场景下的自主导航提供了高安全性与强泛化能力的解决方案。

- [" High fidelity Mars Rover simulation platform based on digital twin and machine learning integration: Innovation and application of ISMRS " (2024)](https://openalex.org/W4402359048) [PDF](https://www.researchsquare.com/article/rs-4851864/latest.pdf) — 该论文提出了基于数字孪生与机器学习融合的高保真火星车仿真平台ISMRS，其核心构建于NVIDIA Isaac Sim之上，用于生成逼真火星地形并支持多类火星车能力测试。平台利用Isaac Sim实现ROS2兼容的自主导航与障碍规避，并通过合成数据训练YOLOv8模型进行岩石实例分割，验证了仿真环境的高保真度，显著提升模型在真实场景中的迁移性能，为地外机器人开发提供高效训练与验证手段。

- ["Learning to Singulate Objects in Packed Environments using a Dexterous Hand" (2024)](http://arxiv.org/abs/2409.00643v2) [PDF](https://arxiv.org/pdf/2409.00643v2) — 本文提出SOPE框架，通过基于位移的状态表示和多阶段强化学习方法，使16自由度Allegro灵巧手能在高密度杂乱环境中完成目标物体的分离任务。研究在Isaac Gym中进行大量仿真实验，并将训练策略直接迁移到实体机器人，在250次真实试验中达到79.2%的成功率，显著优于基线方法。该工作凸显了Isaac Gym作为高保真、可迁移灵巧操作训练平台的关键作用。

- ["Advancing Humanoid Locomotion: Mastering Challenging Terrains with Denoising World Model Learning" (2024)](https://openalex.org/W4402703212) [PDF](https://arxiv.org/pdf/2408.14472) (Citations: 1) — arXiv (Cornell University) — 本文提出去噪世界模型学习（DWL）框架，实现了人形机器人在雪地、斜坡、楼梯及极不平整地形上的零样本sim-to-real迁移控制。研究依托Isaac Sim构建高保真物理仿真环境，利用其GPU加速多物理场模拟能力训练统一神经网络策略，显著提升人形机器人在复杂真实场景中的鲁棒性与泛化能力。该成果展示了Isaac Sim在高难度人形机器人控制任务中的关键支撑作用。

- ["TacSL: A Library for Visuotactile Sensor Simulation and Learning" (2024)](https://openalex.org/W4402426888) [PDF](https://arxiv.org/pdf/2408.06506) — arXiv (Cornell University) — 本文提出TacSL库，实现了基于GPU的视觉触觉传感器仿真与学习，显著提升触觉图像生成和接触力分布提取速度（超200倍于现有方法），并深度集成于Isaac Sim平台。该库提供多种传感器模型、高接触强度训练环境及在线/离线算法，支持高效策略学习；作者还提出新型在线强化学习算法AACD，促进仿真到现实的触觉策略迁移。其在Isaac Sim中的原生集成使大规模触觉数据生成与机器人操作训练成为可能，具有重要应用价值。

- ["Learning to Walk with Adaptive Feet" (2024)](https://openalex.org/W4400941985) [PDF](https://www.mdpi.com/2218-6581/13/8/113/pdf?version=1721986738) (Citations: 2) — Robotics — 该论文提出了一种端到端强化学习控制策略，专门用于利用自适应足端提供的地形信息实现四足机器人动态行走。研究在 Isaac Sim 中构建高保真仿真环境，对不同强化学习算法训练的策略进行评估，验证了自适应足端与数据驱动控制结合的有效性。该工作展示了 Isaac Sim 在复杂感知-运动耦合任务中的训练与测试能力，为具身智能体开发提供了可复现平台。

- ["Random Latent Exploration for Deep Reinforcement Learning" (2024)](http://arxiv.org/abs/2407.13755v3) [PDF](https://arxiv.org/pdf/2407.13755v3) — 本文提出随机潜在探索（RLE）策略，通过在潜在空间中采样随机目标来促进智能体深度探索。该方法在包括Isaac Gym在内的连续控制任务中验证了有效性，作为即插即用模块显著提升现有强化学习算法的探索能力。实验表明RLE在保持简洁性的同时优于传统噪声或奖励奖励机制，适用于GPU加速的机器人仿真训练场景。

- ["Autonomous robotic 3D scanning for smart factory planning" (2024)](https://openalex.org/W4399423245) (Citations: 2) — 本文提出了一种用于智能工厂规划的自主移动地面机器人3D扫描系统，以克服传统扫描方法依赖人工操作的局限性。作者在NVIDIA Isaac Sim中构建并仿真了该机器人系统，利用其GPU加速的多物理场模拟能力高效开发、原型化和测试大规模工业扫描框架。该工作展示了Isaac Sim作为工业机器人3D扫描系统验证平台的重要价值。

- ["Soft body simulation of fish in fish processing factories" (2024)](https://openalex.org/W4400949143) [PDF](http://www.scs-europe.net/dlib/2024/ecms2024acceptedpapers/0150_dtsm_ecms2024_0021.pdf) — 该论文提出了一种基于NVIDIA Omniverse和Isaac Sim的软体鱼仿真方法，用于鱼加工产线的设计与优化。作者在Isaac Sim中构建了具备软体物理特性的数字鱼模型，并搭建了完整的鱼处理生产线仿真环境，通过与真实物理产线的对比验证了其行为真实性。该工作展示了Isaac Sim在复杂生物材料操作场景中的高保真多物理仿真能力，为食品加工自动化提供了可扩展的虚拟验证平台。

- ["A Robust Strategy for UAV Autonomous Landing on a Moving Platform under Partial Observability" (2024)](https://openalex.org/W4399173563) [PDF](https://www.mdpi.com/2504-446X/8/6/232/pdf?version=1717064560) (Citations: 8) — Drones — 本文提出一种结合LSTM与改进PPO的强化学习算法RPO-LSTM，用于解决UAV在部分可观测条件下对移动平台的自主降落问题。研究在Isaac Sim中构建高保真仿真环境，利用其GPU加速的多物理引擎模拟传感器噪声、数据闪烁等挑战性场景，并通过端到端训练实现无需特征工程的鲁棒控制策略。该方法在成功率上显著优于传统PPO和Lee-EKF，在复杂干扰下提升高达74%，为无人机在真实世界受限感知条件下的安全着陆提供了可靠解决方案。

- ["Learning Quadruped Locomotion Policies Using Logical Rules" (2024)](https://openalex.org/W4399176222) [PDF](https://ojs.aaai.org/index.php/ICAPS/article/download/31470/33630) (Citations: 3) — Proceedings of the International Conference on Automated Planning and Scheduling — 该论文提出基于奖励机（Reward Machines）的四足步态学习方法RMLL，通过少量逻辑规则（如前后脚交替移动）实现高效、多样化的步态策略学习，无需依赖运动先验。研究在Isaac Sim中进行仿真训练，验证了所学步态在多种地形下的稳定性、能效及样本效率，并成功迁移到真实四足机器人。该工作展示了Isaac Sim作为高保真、GPU加速仿真平台在复杂运动策略开发中的关键作用。

- ["Maximum Entropy Reinforcement Learning via Energy-Based Normalizing Flow" (2024)](http://arxiv.org/abs/2405.13629v2) [PDF](https://arxiv.org/pdf/2405.13629v2) — 本文提出了一种基于能量函数的归一化流（EBFlow）的最大熵强化学习框架，将策略评估与改进整合为单一目标优化过程，避免了蒙特卡洛近似并支持多模态动作分布建模。该方法在Omniverse Isaac Gym模拟的高维机器人任务中进行了实验验证，展示了优于主流基线的性能。研究直接利用Isaac Sim旗下的Omniverse Isaac Gym作为核心仿真平台，凸显其在复杂机器人控制任务中的训练效率与可扩展性价值。

- ["Going into Orbit: Massively Parallelizing Episodic Reinforcement Learning" (2024)](http://arxiv.org/abs/2405.11512v1) [PDF](https://arxiv.org/pdf/2405.11512v1) — arXiv (Cornell University) — 本文详细实现了基于NVIDIA Orbit框架的推箱子强化学习任务，该框架直接构建于Isaac Sim之上，利用其GPU加速的多物理仿真能力实现大规模并行训练。作者通过与CPU实现对比，展示了Orbit在样本生成效率上的显著优势，并通过超参调优进一步提升了性能。这项工作突显了Isaac Sim作为高性能机器人学习仿真平台在加速强化学习研究中的核心作用。

- ["Task and Domain Adaptive Reinforcement Learning for Robot Control" (2024)](http://arxiv.org/abs/2404.18713v3) [PDF](https://arxiv.org/pdf/2404.18713v3) — 本文提出一种任务与领域自适应的强化学习智能体，通过迁移学习实现策略在不同任务和环境条件下的动态调整。该方法在基于Isaac Gym构建的高并行自定义飞艇模拟器中训练，并成功实现零样本迁移到真实飞艇完成多种任务。研究展示了Isaac Sim（Isaac Gym）在复杂机器人控制仿真与真实部署中的关键作用，为多任务自适应机器人控制提供了高效训练平台。

- ["Humanoid-Gym: Reinforcement Learning for Humanoid Robot with Zero-Shot Sim2Real Transfer" (2024)](http://arxiv.org/abs/2404.05695v2) [PDF](https://arxiv.org/pdf/2404.05695v2) (Citations: 5) — arXiv (Cornell University) — 该论文提出了 Humanoid-Gym，一个基于 NVIDIA Isaac Gym 的强化学习框架，专门用于训练人形机器人运动技能，并实现零样本仿真到现实（sim2real）迁移。作者直接利用 Isaac Gym 作为核心训练环境，通过其 GPU 加速的并行物理模拟能力高效训练策略，并在 RobotEra 的 XBot-S 和 XBot-L 真实人形机器人上验证了零样本迁移效果。该工作凸显了 Isaac Sim 生态在高保真、可迁移机器人策略开发中的关键作用，为具身智能研究提供了实用工具链。

- ["Benchmarking Population-Based Reinforcement Learning across Robotic Tasks with GPU-Accelerated Simulation" (2024)](http://arxiv.org/abs/2404.03336v5) [PDF](https://arxiv.org/pdf/2404.03336v5) (Citations: 1) — arXiv (Cornell University) — 本文提出并评估了一种基于种群的强化学习（PBRL）方法，利用GPU加速仿真显著提升策略探索效率。研究在Isaac Gym中对Anymal Terrain、Shadow Hand、Humanoid和Franka Nut Pick四个任务进行系统性实验，通过动态调整超参数并分析种群规模与变异机制的影响，证明PBRL在累积奖励上优于PPO、SAC和DDPG等基线算法，并首次成功将PBRL训练的策略部署到真实Franka机器人上，验证了其sim-to-real迁移能力。

- ["Adaptive Energy Regularization for Autonomous Gait Transition and Energy-Efficient Quadruped Locomotion" (2024)](http://arxiv.org/abs/2403.20001v2) [PDF](https://arxiv.org/pdf/2403.20001v2) — 该论文提出一种基于自适应能量正则化的强化学习奖励策略，使四足机器人能在不同速度下自主切换步态并提升能效。研究在 Isaac Gym 中进行大规模仿真训练，利用其GPU加速的物理模拟高效优化策略，并成功迁移到 ANYmal-C 和 Unitree Go1 真机验证。该工作凸显了 Isaac Sim（Isaac Gym）作为高保真、可扩展训练平台对能量高效运动控制研究的关键支撑作用。

- ["Arm-Constrained Curriculum Learning for Loco-Manipulation of the Wheel-Legged Robot" (2024)](http://arxiv.org/abs/2403.16535v2) [PDF](https://arxiv.org/pdf/2403.16535v2) — 本文提出一种臂约束课程学习架构，用于解决轮腿机器人搭载机械臂后的控制不稳定性问题。作者在Isaac Gym中训练强化学习策略，通过臂约束算法保障控制安全性，并设计奖励感知的课程学习方法协调机械臂与底盘的奖励差异。训练好的策略成功迁移到实体机器人，完成了开门、拨动风扇及接力棒抓取等动态抓取任务，验证了方法在复杂loco-manipulation场景中的有效性。

- ["Digital Twin and Deep Reinforcement Learning-Driven Robotic Automation System for Confined Workspaces: A Nozzle Dam Replacement Case Study in Nuclear Power Plants" (2024)](https://openalex.org/W4392914637) [PDF](https://link.springer.com/content/pdf/10.1007/s40684-023-00593-6.pdf) (Citations: 16) — International Journal of Precision Engineering and Manufacturing-Green Technology — 该研究提出了一种结合数字孪生与深度强化学习的机器人自动化系统，用于核电厂狭窄空间内的喷嘴封堵器更换任务。论文明确使用 Isaac Sim 构建高保真数字孪生环境，以训练基于近端策略优化（PPO）算法的自主移动机械臂，并在其中进行全流程仿真验证。该工作展示了 Isaac Sim 在高风险工业场景中实现安全、高效机器人部署的关键作用。

- ["MultiGripperGrasp: A Dataset for Robotic Grasping from Parallel Jaw Grippers to Dexterous Hands" (2024)](http://arxiv.org/abs/2403.09841v2) [PDF](https://arxiv.org/pdf/2403.09841v2) — arXiv (Cornell University) — 本文提出了大规模多夹爪抓取数据集MultiGripperGrasp，包含11种夹爪对345个物体的3040万条抓取样本。所有抓取均在Isaac Sim中进行物理仿真验证，并记录物体脱落时间作为抓取质量指标。该数据集通过统一手掌位姿对齐不同夹爪，支持跨夹爪抓取迁移，显著提升各夹爪的成功抓取数量，为通用抓取规划与迁移研究提供重要资源。

- ["Sim-to-Real gap in RL: Use Case with TIAGo and Isaac Sim/Gym" (2024)](http://arxiv.org/abs/2403.07091v2) [PDF](https://arxiv.org/pdf/2403.07091v2) (Citations: 1) — arXiv (Cornell University) — 本文研究了基于强化学习的策略在TIAGo移动操作机器人上的仿真到现实（sim-to-real）迁移问题，核心贡献在于系统比较并实际应用NVIDIA的Isaac Gym与Isaac Sim作为训练平台。作者在两个仿真环境中训练RL策略，并重点优化无碰撞运动控制架构，最终在真实机器人上成功复现了仿真中学习到的行为。该工作验证了Isaac Sim/Gym在高保真机器人仿真与策略迁移中的有效性，为复杂操作任务提供了可复现的sim-to-real流程。

- ["GenNBV: Generalizable Next-Best-View Policy for Active 3D Reconstruction" (2024)](http://arxiv.org/abs/2402.16174v3) [PDF](https://arxiv.org/pdf/2402.16174v3) — 本文提出GenNBV，一种端到端可泛化的主动3D重建Next-Best-View策略，采用强化学习框架并扩展至5D自由动作空间，使无人机能在未知几何体上自主扫描。研究在Isaac Gym中构建仿真基准，利用Houses3K和OmniObject3D数据集进行训练与评估，显著提升跨数据集泛化能力。该方法在未见建筑级物体上分别达到98.26%和97.12%的覆盖率，验证了Isaac Sim作为高保真、可扩展机器人感知仿真平台的关键作用。

- ["Tiny Reinforcement Learning for Quadruped Locomotion using Decision Transformers" (2024)](http://arxiv.org/abs/2402.13201v1) [PDF](https://arxiv.org/pdf/2402.13201v1) — 该论文提出一种面向资源受限四足机器人Bittle的轻量化决策Transformer模仿学习方法，通过将控制策略建模为条件序列生成任务，并结合量化与剪枝压缩模型。研究在Isaac Gym中进行仿真训练与评估，验证了4比特量化和剪枝可在模型体积减少约30%的同时保持高性能步态，显著提升部署可行性。该工作展示了Isaac Gym作为高效强化学习仿真平台在低功耗机器人策略开发中的关键作用。

- ["<i>OmniDrones:</i> An Efficient and Flexible Platform for Reinforcement Learning in Drone Control" (2024)](https://openalex.org/W4391019623) (Citations: 33) — IEEE Robotics and Automation Letters — 本文提出了OmniDrones，一个基于NVIDIA Omniverse Isaac Sim构建的高效灵活的无人机强化学习平台。该平台利用Isaac Sim的GPU并行仿真能力，提供4种无人机模型、5类传感器、4种控制模式及10余项基准任务，并集成多种主流RL算法基线。通过在Isaac Sim中实现高保真物理与传感器仿真，OmniDrones为无人机控制研究提供了可扩展、开源的实验环境，显著降低算法开发与验证门槛。

- ["A Multiarm Robotic Platform for Scientific Exploration: Its Design, Digital Twins, and Validation" (2024)](https://openalex.org/W4390874093) [PDF](https://ieeexplore.ieee.org/ielx7/100/4600619/10399868.pdf) (Citations: 11) — IEEE Robotics & Automation Magazine — 该论文提出了一种用于科学探索的多臂AI机器人平台，重点展示了其在类器官研究中执行颅窗制备等精细操作的能力。作者利用Isaac Sim构建了该平台的高保真数字孪生系统，用于仿真验证和遥操作控制算法开发，并通过peg transfer、纱布切割及全球首次双人遥操作颅骨钻孔等实验验证了系统性能。该工作为生物医学研究提供了可复现、开源的机器人实验框架，具有重要科研应用价值。

- ["Visual-Language Decision System Through Integration of Foundation Models for Service Robot Navigation" (2024)](https://openalex.org/W4391695313) (Citations: 5) — 本文提出了一种视觉-语言决策（VLD）系统，通过融合CLIP、OFA和PaddleOCR三种视觉语言模型与GPT-3大语言模型，使服务机器人能在未知环境中自主理解语义并进行导航决策。作者在Isaac Sim中构建了高保真仿真环境，用于训练和验证VLD系统的感知与决策能力，并将该系统部署到真实TurtleBot3机器人上完成实地导航实验。该工作展示了Isaac Sim作为关键仿真平台在连接多模态AI模型与机器人实际应用中的价值。

- ["General-Purpose Sim2Real Protocol for Learning Contact-Rich Manipulation With Marker-Based Visuotactile Sensors" (2024)](https://openalex.org/W4390776907) [PDF](https://ieeexplore.ieee.org/ielx7/8860/4359257/10388459.pdf) (Citations: 18) — IEEE Transactions on Robotics — 该论文提出了一种通用的Sim2Real协议，用于基于标记式视觉触觉传感器的接触密集型操作策略学习。为提升仿真保真度，作者采用基于有限元方法（FEM）的物理仿真器以精确模拟传感器弹性形变，并在Isaac Sim中实现该高保真触觉仿真环境。其提出的触觉特征提取网络直接处理标记点像素坐标，并结合自监督预训练策略，显著提升了强化学习策略的效率与泛化能力，在插孔、插头调节和开锁等任务中验证了有效性，为触觉驱动的机器人操作提供了可复现、开源的仿真到现实迁移框架。

- ["Automation in Unstructured Production Environments Using Isaac Sim: A Flexible Framework for Dynamic Robot Adaptability" (2024)](https://openalex.org/W4404789713) (Citations: 7) — Procedia CIRP — 该论文提出了一种在非结构化生产环境中实现机器人自动化的灵活框架，核心在于利用 Isaac Sim 构建高保真、动态变化的虚拟产线场景，以训练和验证机器人的实时适应能力。作者在 Isaac Sim 中集成了物理精确的多物体交互模型与传感器仿真，并通过域随机化生成多样化训练数据，显著提升了策略在真实工业环境中的迁移性能。该工作展示了 Isaac Sim 作为工业自动化开发平台的关键价值。

- ["Stabilization of a Quintuple Inverted Pendulum System in Isaac Sim" (2024)](https://openalex.org/W4405821495) — Lecture notes on data engineering and communications technologies — 该论文提出了一种针对五级倒立摆系统的稳定控制策略，并在 Isaac Sim 中构建了高保真物理仿真环境进行验证。作者利用 Isaac Sim 的 GPU 加速多物理引擎精确模拟了复杂非线性动力学特性，实现了对多关节串联不稳定系统的实时状态反馈与控制。该工作展示了 Isaac Sim 在高维欠驱动系统建模与控制算法验证中的强大能力，为复杂机器人控制研究提供了可靠仿真平台。

- ["Enhancement of Control Performance for Degraded Robot Manipulators Using Digital Twin and Proximal Policy Optimization" (2024)](https://openalex.org/W4391305596) [PDF](https://ieeexplore.ieee.org/ielx7/6287639/6514899/10415386.pdf) (Citations: 7) — IEEE Access — 该论文提出一种结合数字孪生与近端策略优化（PPO）强化学习的方法，用于提升性能退化机械臂的控制精度。作者在Isaac Sim中构建六自由度机械臂的数字孪生模型，通过调节物理引擎参数逼近真实退化机器人的不稳定动力学特性，并利用域随机化在仿真中训练鲁棒策略，最终部署到实体机器人上，使位置误差相比内置控制器和PID分别降低63%和39%。该工作凸显了Isaac Sim作为高保真、可调参仿真平台在机器人退化补偿中的关键作用。

- ["Sim-to-Real Gap in RL: Use Case with TIAGo and Isaac Sim/Gym" (2024)](https://openalex.org/W4405927045) (Citations: 2) — Springer proceedings in advanced robotics — 该论文以TIAGo机器人为案例，系统研究强化学习中仿真到现实（sim-to-real）的迁移差距问题。作者在Isaac Sim/Gym中构建高保真仿真环境，用于训练机器人控制策略，并通过对比真实机器人实验分析性能差异。研究揭示了Isaac Sim中物理建模与渲染细节对策略迁移效果的关键影响，为提升仿真真实性提供了实证依据。

- ["Reinforcement learning for quadruped robot locomotion control" (2024)](https://openalex.org/W7112725633) — The HKU Scholars Hub (University of Hong Kong) — 该论文提出结合模型预测控制（MPC）与强化学习（RL）的方法，用于四足机器人在复杂地形中的运动控制。作者在Isaac Gym平台上构建仿真环境，利用其GPU加速的并行物理模拟能力高效训练RL策略，并通过真实四足机器人验证了所学策略的有效性。该工作展示了Isaac Gym作为高保真、高效率训练平台在四足机器人控制中的关键作用，为现实世界部署提供了可行路径。

- ["Automated Hyperparameter Tuning in Reinforcement Learning for Quadrupedal Robot Locomotion" (2023)](https://openalex.org/W4390266979) [PDF](https://www.mdpi.com/2079-9292/13/1/116/pdf?version=1703674774) (Citations: 7) — Electronics — 本文提出了一种自动调整四足机器人强化学习中主导奖励函数尺度的方法，通过定义反映步态稳定性的“步态分数”来评估并选择最优策略。研究在 Isaac Sim 中构建了两个不同尺寸与形态的四足机器人仿真环境，利用其 GPU 加速的多物理引擎高效执行大量训练与评估实验。该方法显著减少了人工调参成本，为复杂机器人系统的自适应奖励设计提供了可扩展的解决方案。

- ["MEP-SEG DATASET : SYNTHETIC IMAGES GENERATED FROM BUILDING INFORMATION MODELING (BIM)" (2023)](https://openalex.org/W4392686425) — HAL (Le Centre pour la Communication Scientifique Directe) — 该论文提出了MEP-SEG数据集，通过将Autodesk Revit中的三个建筑信息模型（BIM）导入NVIDIA Isaac Sim生成8751组合成图像及其对应的语义分割掩码和标签文件，涵盖13类建筑构件。Isaac Sim在此作为核心渲染与合成数据生成平台，利用其高保真物理仿真和GPU加速能力实现逼真的室内场景模拟。该数据集为建筑环境中的语义分割任务提供了高质量训练资源，具有显著的工程应用价值。

- ["Learning and Reusing Quadruped Robot Movement Skills from Biological Dogs for Higher-Level Tasks" (2023)](https://openalex.org/W4390007869) [PDF](https://www.mdpi.com/1424-8220/24/1/28/pdf?version=1703059553) (Citations: 3) — Sensors — 该论文提出了一种分层强化学习框架，使四足机器人能从生物狗的运动数据中学习基础运动技能，并在此基础上高效训练高层任务。研究在Isaac Sim中构建仿真环境，利用其GPU加速的物理引擎和域随机化技术训练策略，实现无需微调即可迁移到实体机器人。该方法显著提升了四足机器人动作的仿生性与任务适应性，展示了Isaac Sim在高保真机器人学习中的关键作用。

- ["DARLEI: Deep Accelerated Reinforcement Learning with Evolutionary Intelligence" (2023)](http://arxiv.org/abs/2312.05171v1) [PDF](https://arxiv.org/pdf/2312.05171v1) — DARLEI 提出了一种结合进化算法与并行强化学习的框架，用于高效训练和演化 UNIMAL 智能体群体。该方法以 Isaac Gym 作为核心仿真平台，利用其 GPU 加速能力，在单个工作站上实现比以往基于 CPU 集群方法快 20 倍以上的训练速度，并通过开启智能体间碰撞模拟多智能体交互对形态演化的影响。这项工作展示了 Isaac Gym 在大规模具身智能体协同进化研究中的关键作用，为未来构建共演化平台和探索涌现行为提供了高效基础。

- ["Multi Actor-Critic DDPG for Robot Action Space Decomposition: A Framework to Control Large 3D Deformation of Soft Linear Objects" (2023)](https://openalex.org/W4389501449) [PDF](https://arxiv.org/pdf/2312.04308) (Citations: 2) — arXiv (Cornell University) — 本文提出MultiAC6框架，通过双Actor-Critic深度强化学习代理分解机器人动作空间，实现对可变形线性物体（DLO）的大尺度3D形变控制。该方法在Isaac Sim中构建高保真物理仿真环境进行训练，并成功弥合了sim-to-real差距，在真实世界中实现高达40厘米的精准操控。实验表明其成功率比单智能体方法高66%，且无需重训练即可泛化至不同材质与长度的DLO，为柔性物体操作提供了高效可靠的解决方案。

- ["PolyFit: A Peg-in-hole Assembly Framework for Unseen Polygon Shapes via Sim-to-real Adaptation" (2023)](https://openalex.org/W4389421688) [PDF](https://arxiv.org/pdf/2312.02531) (Citations: 1) — arXiv (Cornell University) — 本文提出PolyFit，一种基于力/力矩（F/T）的监督学习框架，用于5自由度未知多边形形状的插孔装配任务。研究在Isaac Sim中构建了包含多样几何形状、外部位姿及其对应接触F/T数据的大规模仿真训练集，并采用多点接触策略提升位姿估计精度。通过仿真到现实的配对数据实现高效sim-to-real迁移，在真实环境中对未见形状达到85.0%的成功率，显著提升了插孔任务的泛化能力与鲁棒性。

- ["Robust Conformal Prediction for STL Runtime Verification under Distribution Shift" (2023)](http://arxiv.org/abs/2311.09482v2) [PDF](https://arxiv.org/pdf/2311.09482v2) — arXiv (Cornell University) — 该论文提出了一种面向信号时序逻辑（STL）任务的鲁棒预测性运行时验证（RPRV）算法，用于在分布偏移下对随机信息物理系统进行故障预测。作者在 NVIDIA Isaac Sim 环境中使用 Franka 机械臂进行实验，利用其轨迹预测模型结合鲁棒保形预测方法，在已知部署与设计阶段分布间 f-散度上界的前提下，提供具有统计有效性的概率保证。该方法首次在 STL 运行时验证中实现对分布偏移的显式建模与量化，为基于 Isaac Sim 的机器人系统安全验证提供了新工具。

- ["MetaGraspNetV2: All-in-One Dataset Enabling Fast and Reliable Robotic Bin Picking via Object Relationship Reasoning and Dexterous Grasping" (2023)](https://openalex.org/W4388407473) [PDF](https://ieeexplore.ieee.org/ielx7/8856/4358066/10309974.pdf) (Citations: 22) — IEEE Transactions on Automation Science and Engineering — 本文提出MetaGraspNetV2，一个面向机器人料箱抓取的全能型数据集，包含通过物理仿真合成的29.6万张逼真图像和3200张真实世界测试图像，提供包括遮挡推理、6自由度位姿估计和双夹具抓取在内的全标注。该数据集明确使用Isaac Sim作为物理引擎，在其“metaverse synthesis”流程中生成高保真、多任务对齐的合成数据。这一基于Isaac Sim构建的数据资源显著提升了感知与抓取系统的整体性能，为高速、高可靠性的杂乱场景抓取提供了关键基础。

- ["A ROS 2 and TwinCAT Based Digital Twin Framework for Mechatronics Systems" (2023)](https://openalex.org/W4390485878) (Citations: 8) — 本文提出了一种基于ROS 2与TwinCAT的数字孪生框架，用于机电系统的自主控制开发。其核心创新在于将NVIDIA Isaac Sim作为虚拟环境模块，与TwinCAT 3实时控制系统和ROS 2中间件集成，构建了可扩展的闭环仿真架构。该框架在起重机负载操作案例中验证了有效性，为复杂机电系统提供了高保真、GPU加速的数字孪生平台基础。

- ["Software Framework of Autonomous Mobile Robots on Isaac Sim and ROS" (2023)](https://openalex.org/W4390481090) (Citations: 2) — 该论文提出了一种基于Isaac Sim与ROS集成的自主移动机器人软件框架，重点实现AI驱动的运动控制、多传感器融合以及目标检测与编队控制。研究在Isaac Sim中构建了完整的AMR仿真环境，用于验证从起始点到目标点再返回的闭环导航任务，并通过精确的位姿序列执行展示了平台对复杂工厂场景的模拟能力。该工作凸显了Isaac Sim作为高保真、GPU加速仿真平台在军事与工业AMR开发中的实用价值。

- ["RANS: Highly-Parallelised Simulator for Reinforcement Learning based Autonomous Navigating Spacecrafts" (2023)](http://arxiv.org/abs/2310.07393v1) [PDF](https://arxiv.org/pdf/2310.07393v1) — 该论文提出RANS——一个基于NVIDIA Isaac Gym构建的高并行化仿真库，专为强化学习驱动的航天器自主导航任务设计。作者充分利用Isaac Gym的GPU加速物理仿真与策略训练一体化架构，实现了数千个航天器实例的并行仿真，支持姿态、位置和速度控制等关键机动任务，可用于着陆、对接和交会等复杂空间场景的验证。该工作填补了航天器RL训练缺乏专用高并行仿真平台的空白，显著提升了数据生成效率与算法迭代速度。

- ["Terrain-adaptive Central Pattern Generators with Reinforcement Learning for Hexapod Locomotion" (2023)](http://arxiv.org/abs/2310.07744v1) [PDF](https://arxiv.org/pdf/2310.07744v1) — 本文提出一种将深度强化学习（DRL）与中枢模式发生器（CPG）结合的地形自适应六足机器人运动控制方法，其中CPG生成基础步态信号，DRL动态调整CPG映射参数以提升复杂地形下的适应性。研究在Isaac Gym仿真环境中进行训练与评估，验证了该方法在地形适应性、收敛速度和奖励设计简化方面的优势。该工作展示了Isaac Gym作为高效、可扩展的GPU加速仿真平台在腿式机器人控制策略开发中的关键作用。

- ["OmniDrones: An Efficient and Flexible Platform for Reinforcement Learning in Drone Control" (2023)](http://arxiv.org/abs/2309.12825v1) [PDF](https://arxiv.org/pdf/2309.12825v1) (Citations: 1) — arXiv (Cornell University) — 本文提出了OmniDrones，一个基于NVIDIA Omniverse Isaac Sim构建的高效灵活的无人机强化学习平台。该平台利用Isaac Sim的GPU并行仿真能力，提供4种无人机模型、5种传感器模态、4种控制模式及10余项基准任务，并集成多种主流RL算法基线。通过在Isaac Sim中实现高保真物理与传感器仿真，OmniDrones为无人机控制研究提供了可扩展、开源的实验环境，显著降低算法开发与验证门槛。

- ["NeuroMechFly v2, simulating embodied sensorimotor control in adult <i>Drosophila</i>" (2023)](https://openalex.org/W4386819513) [PDF](https://www.biorxiv.org/content/biorxiv/early/2023/10/09/2023.09.18.556649.full.pdf) (Citations: 15) — 该论文提出了NeuroMechFly v2，一个用于模拟果蝇感觉运动控制的神经机械框架，新增视觉与嗅觉感知、上行运动反馈及复杂地形导航能力。研究在Isaac Sim中构建了生物启发的闭环控制器，利用强化学习实现多模态导航，并结合连接组约束的视觉网络进行仿生行为模拟。该工作展示了Isaac Sim作为高保真神经机器人仿真平台在理解神经系统机制和开发自主智能体方面的关键作用。

- ["OmniLRS: A Photorealistic Simulator for Lunar Robotics" (2023)](http://arxiv.org/abs/2309.08997v1) [PDF](https://arxiv.org/pdf/2309.08997v1) — arXiv (Cornell University) — 本文提出OmniLRS，一个基于Isaac Sim构建的高保真月球机器人仿真平台，支持快速程序化环境生成、多机器人协同及面向机器学习的合成数据流水线。该系统深度集成Isaac Sim的GPU加速物理与渲染能力，并提供ROS1/ROS2接口以控制机器人与环境；通过在合成数据上训练YOLOv8模型，在岩石实例分割任务中实现接近真实数据训练的性能，微调后甚至提升14%平均精度，验证了其在地外机器人感知算法开发中的实用价值。

- ["Bridging Locomotion and Manipulation Using Reconfigurable Robotic Limbs via Reinforcement Learning" (2023)](https://openalex.org/W4385805393) [PDF](https://www.mdpi.com/2313-7673/8/4/364/pdf?version=1691989509) (Citations: 13) — Biomimetics — 该论文提出了一种通过强化学习统一机器人运动与操作（loco-manipulation）的方法，利用可重构的过约束机械肢在多足行走与多指抓取之间切换，并采用共享策略进行联合训练。研究在 Isaac Sim 中构建高保真仿真环境，对基于MLP和图神经网络的策略进行训练与验证，并成功实现Sim2Real迁移。该工作为运动与操作技能的内在关联提供了数据驱动证据，展示了Isaac Sim在复杂机器人行为联合学习中的关键作用。

- ["Towards Building AI-CPS with NVIDIA Isaac Sim: An Industrial Benchmark and Case Study for Robotics Manipulation" (2023)](http://arxiv.org/abs/2308.00055v1) [PDF](https://arxiv.org/pdf/2308.00055v1) (Citations: 23) — arXiv (Cornell University) — 本文提出了一个面向AI驱动机器人操作的公开基准，核心贡献是构建了包含八项典型操作任务和多种AI控制器的标准化评估体系。该基准明确以NVIDIA Omniverse Isaac Sim作为唯一仿真平台，利用其GPU加速的多物理引擎进行大规模实验，并开发了首个兼容Isaac Sim的 falsification 框架，将传统验证方法与现代物理仿真结合。该工作为AI-CPS系统的可靠性评估提供了可复现、可扩展的工业级测试环境，显著提升了在Isaac Sim中验证AI控制器鲁棒性的能力。

- ["Parallel $Q$-Learning: Scaling Off-policy Reinforcement Learning under Massively Parallel Simulation" (2023)](http://arxiv.org/abs/2307.12983v1) [PDF](https://arxiv.org/pdf/2307.12983v1) — 本文提出并实现了Parallel Q-Learning（PQL），一种专为大规模GPU并行仿真设计的高效异策强化学习框架。作者在Isaac Gym中构建了数万个并行环境，通过同时并行化数据收集、策略学习与价值学习，在单个工作站上显著缩短了训练时间，并优于PPO等同策方法。该工作展示了Q-learning在Isaac Sim核心组件Isaac Gym上的可扩展性，为复杂机器人任务提供了高样本效率与快速收敛的训练范式。

- ["Sampling-based Model Predictive Control Leveraging Parallelizable Physics Simulations" (2023)](http://arxiv.org/abs/2307.09105v3) [PDF](https://arxiv.org/pdf/2307.09105v3) (Citations: 6) — arXiv (Cornell University) — 该论文提出一种基于采样的模型预测控制方法，核心创新在于将Isaac Gym（Isaac Sim的高性能GPU并行仿真组件）作为MPPI控制器的前向动力学模型，无需显式建模机器人动力学与接触。通过利用Isaac Gym的大规模并行仿真能力，该方法高效处理高维、接触密集的任务，如移动导航避障、非抓取操作和全身控制，并在仿真与真实环境中验证了有效性。此工作显著提升了复杂机器人任务的可扩展性与实用性。

- ["Application of Reinforcement Learning to UR10 Positioning for Prioritized Multi-Step Inspection in NVIDIA Omniverse" (2023)](https://openalex.org/W4385830952) (Citations: 6) — 本文研究了在大规模定制背景下，利用强化学习解决UR10机器人多步骤检测中的定位问题。作者在NVIDIA Omniverse的Isaac Sim环境中实现了DDPG、TD3、TRPO和PPO等先进强化学习算法，并通过实验发现TRPO在定位精度方面表现最优。该工作展示了Isaac Sim作为高保真、GPU加速仿真平台在自动化检测系统开发中的关键作用。

- ["SynTable: A Synthetic Data Generation Pipeline for Unseen Object Amodal Instance Segmentation of Cluttered Tabletop Scenes" (2023)](http://arxiv.org/abs/2307.07333v3) [PDF](https://arxiv.org/pdf/2307.07333v3) (Citations: 4) — arXiv (Cornell University) — 本文提出SynTable，一个基于Isaac Sim Replicator Composer构建的合成数据生成管道，专门用于生成杂乱桌面场景中未见物体的全模态实例分割数据集。该工具利用Isaac Sim的渲染能力自动生成包含遮挡、材质、深度图及全模态/模态掩码等丰富标注的高保真图像，无需人工标注，并成功用于训练UOAIS-Net模型，在OSD-Amodal数据集上实现优异的Sim-to-Real迁移性能。该工作凸显了Isaac Sim在高质量机器人视觉合成数据生成中的核心作用。

- ["A Planning Framework for Robotic Insertion Tasks via Hydroelastic Contact Model" (2023)](https://openalex.org/W4384525704) [PDF](https://www.mdpi.com/2075-1702/11/7/741/pdf?version=1689652461) (Citations: 6) — Machines — 该论文提出了一种结合双层优化的运动规划框架，利用水弹性接触模型提升机器人插装任务的力交互精度与计算效率。作者在Isaac Sim中实现并验证了该框架，通过Dynamic Movement Primitives参数化轨迹，并集成Black-Box Optimization进行策略优化，同时利用Isaac Sim的GPU加速多物理仿真能力高效生成带视觉不确定性的模拟数据。实验以经典的Peg-in-Hole任务为基准，在Isaac Sim中复现并验证了接触力响应的准确性，显著缩小了sim-to-real差距，为高保真、低成本的机器人技能训练提供了实用方案。

- ["Pegasus Simulator: An Isaac Sim Framework for Multiple Aerial Vehicles Simulation" (2023)](http://arxiv.org/abs/2307.05263v2) [PDF](https://arxiv.org/pdf/2307.05263v2) (Citations: 23) — arXiv (Cornell University) — 本文提出了Pegasus Simulator，一个基于NVIDIA Isaac Sim构建的模块化框架，用于多架多旋翼飞行器的实时高保真仿真。该框架深度集成Isaac Sim，支持与PX4-Autopilot和ROS2开箱即用的对接，并通过其图形界面实现直观操作；作者在Isaac Sim中实现了非线性控制器并展示了两架无人机执行高动态机动的仿真结果。该工作显著提升了基于Isaac Sim的空中机器人算法开发效率与可复现性。

- ["IndustReal: Transferring Contact-Rich Assembly Tasks from Simulation to Reality" (2023)](https://openalex.org/W4385430467) [PDF](https://doi.org/10.15607/rss.2023.xix.039) (Citations: 36) — 该论文提出IndustReal框架，通过强化学习在仿真中训练机器人完成高精度接触式装配任务，并成功迁移到现实世界。研究明确使用NVIDIA Isaac Sim（基于Factory基准）作为核心仿真平台，开发了仿真感知策略更新、符号距离场奖励和基于采样的课程学习等方法，并结合策略级动作整合器提升现实部署性能。该工作为Isaac Sim在工业装配场景中的应用提供了可复现的算法与系统工具链。

- ["Rotating without Seeing: Towards In-hand Dexterity through Touch" (2023)](https://openalex.org/W4385430564) [PDF](https://doi.org/10.15607/rss.2023.xix.036) (Citations: 69) — 该论文提出了一种仅依赖触觉信息实现多指灵巧手在手内旋转物体的方法，无需视觉输入。作者在仿真中使用密集分布的二值力传感器覆盖整个手掌与手指表面，并基于强化学习训练策略；其仿真环境明确采用 Isaac Sim 进行多物理场模拟，以支持高保真触觉交互和策略训练。该方法显著缩小了 Sim2Real 差距，可在真实机器人上直接部署并成功操作未见过的物体，为无视觉灵巧操作提供了实用解决方案。

- ["AnyTeleop: A General Vision-Based Dexterous Robot Arm-Hand Teleoperation System" (2023)](https://openalex.org/W4385430618) [PDF](https://doi.org/10.15607/rss.2023.xix.015) (Citations: 72) — 该论文提出了AnyTeleop，一种通用的基于视觉的灵巧机器人臂-手遥操作系统，能够在真实和仿真环境中实现高性能操作。研究在Isaac Sim中进行仿真实验，利用其GPU加速的多物理场模拟能力训练和验证系统，并证明AnyTeleop在该平台上的模仿学习性能优于专为该仿真器设计的先前系统。该工作展示了Isaac Sim作为遥操作与模仿学习联合开发平台的有效性，为通用机器人控制提供了可扩展方案。

- ["Sampling-based Exploration for Reinforcement Learning of Dexterous Manipulation" (2023)](https://openalex.org/W4385403828) [PDF](https://doi.org/10.15607/rss.2023.xix.020) (Citations: 25) — 本文提出一种基于采样探索的强化学习方法，用于实现无被动支撑表面下的灵巧操作。作者在Isaac Sim中构建高保真多物理仿真环境，利用其GPU加速能力高效生成符合动力学约束的重置分布，并训练模型无关的控制策略。该方法显著提升了复杂物体操作任务的成功率，并验证了从Isaac Sim到真实机器人（如Allegro Hand）的有效迁移能力。

- ["Integrated Object Deformation and Contact Patch Estimation from Visuo-Tactile Feedback" (2023)](https://openalex.org/W4385416139) [PDF](https://doi.org/10.15607/rss.2023.xix.080) (Citations: 7) — 本文提出神经形变接触场（NDCF），通过视觉-触觉反馈联合建模柔性物体的形变与接触区域，利用隐式表示实现对复杂接触面的统一预测，并在训练中融入物理先验约束。作者使用Isaac Sim生成高保真模拟数据训练NDCF模型，并验证其无需微调即可直接迁移到真实机器人系统，在模拟和现实任务中均优于点云基线方法。该工作凸显了Isaac Sim在生成用于触觉感知研究的高质量多模态仿真数据方面的关键作用。

- ["LAGOON: Language-Guided Motion Control" (2023)](https://openalex.org/W4381557820) [PDF](https://arxiv.org/pdf/2306.10518) (Citations: 3) — arXiv (Cornell University) — 本文提出LAGOON方法，通过多阶段强化学习实现语言指令驱动的机器人运动控制。其关键步骤包括利用预训练模型生成人体动作、在仿真中训练控制策略以模仿该动作，并借助域随机化将策略迁移到四足机器人。论文明确使用Isaac Sim作为核心仿真平台进行策略训练和物理模拟，支撑了从语言到真实机器人行为的可靠迁移，为具身智能体提供了高效开发框架。

- ["DeXtreme: Transfer of Agile In-hand Manipulation from Simulation to Reality" (2023)](https://openalex.org/W4383108265) (Citations: 83) — 本文提出了一种基于深度强化学习的灵巧手内操作策略，通过在Isaac Gym中进行大规模GPU加速仿真训练，实现了从仿真到真实世界的高效迁移。研究利用Isaac Gym构建高保真、高并发的多指操作环境，训练出能适应多种扰动条件的鲁棒策略和视觉姿态估计器，在Allegro Hand上完成物体重定向任务，性能优于现有基于视觉的方法。该工作验证了Isaac Gym在灵巧操作sim-to-real中的关键作用，并为低成本机器人平台提供了可复现方案。

- ["Aerial Gym -- Isaac Gym Simulator for Aerial Robots" (2023)](http://arxiv.org/abs/2305.16510v1) [PDF](https://arxiv.org/pdf/2305.16510v1) — 该论文提出了 Aerial Gym，一个基于 Isaac Gym 的高并行空中机器人仿真平台，支持数百万多旋翼飞行器同时仿真，并集成了 SE(3) 几何控制器用于姿态、速度与位置跟踪。系统利用 Isaac Gym 的 GPU 加速能力，提供带障碍物随机化的复杂环境，以及模拟 RGB、深度、分割和光流图像的机载相机功能，显著提升导航策略的训练效率。该工作填补了大规模并行空中机器人仿真的空白，为强化学习驱动的自主飞行研究提供了开源工具。

- ["DexPBT: Scaling up Dexterous Manipulation for Hand-Arm Systems with Population Based Training" (2023)](http://arxiv.org/abs/2305.12127v1) [PDF](https://arxiv.org/pdf/2305.12127v1) (Citations: 20) — 本文提出DexPBT算法，利用Isaac Gym这一GPU加速的并行物理仿真器，训练单臂或双臂灵巧手系统完成重抓取、抓抛和物体重新定向等高难度操作任务。作者设计了一种去中心化的基于种群的训练（PBT）方法，显著提升了深度强化学习的探索能力，成功生成了鲁棒的控制策略。该工作展示了Isaac Gym在大规模灵巧操作策略训练中的关键作用，为复杂手-臂协同控制提供了可扩展的仿真训练范式。

- ["A Fast 6DOF Visual Selective Grasping System Using Point Clouds" (2023)](https://openalex.org/W4381679720) [PDF](https://www.mdpi.com/2075-1702/11/5/540/pdf?version=1683769569) (Citations: 2) — Machines — 该论文提出了一种基于点云的快速6自由度视觉选择性抓取系统，核心贡献是设计了名为Point Encoder Convolution (PEC)的深度学习网络用于物体分类，并结合几何基元与侧向曲率估计抓取区域。作者在Isaac Sim中构建高保真仿真环境生成训练数据集，利用其GPU加速的多物理场模拟能力确保点云数据的真实性与多样性。该系统在真实机器人上实现了94%的成功率和4毫秒的推理速度，适用于低成本硬件或实时抓取任务。

- ["Deep Learning for Ultrasound Speed-of-Sound Reconstruction: Impacts of Training Data Diversity on Stability and Robustness" (2023)](https://openalex.org/W4376878291) (Citations: 12) — The Journal of Machine Learning for Biomedical Imaging — 该论文提出了一种基于乳腺断层合成图像的新仿真方法，用于生成更逼真的超声波速重建深度学习训练数据，并与简化几何模型结合以提升数据多样性。研究在Isaac Sim中构建了高保真多物理场仿真环境，系统评估了网络对散射体数量、噪声和几何结构等参数的敏感性，验证了多样化训练数据对模型在真实测量数据上稳定性和鲁棒性的提升作用，为医学超声定量成像提供了可靠的数据生成与验证平台。

- ["Enhancing Efficiency of Quadrupedal Locomotion over Challenging Terrains with Extensible Feet" (2023)](http://arxiv.org/abs/2305.01998v1) [PDF](https://arxiv.org/pdf/2305.01998v1) — 本文提出一种基于深度强化学习的四足机器人运动策略，通过在膝关节与足端之间引入可伸缩的棱柱关节提升复杂地形下的运动效率。研究在 NVIDIA Isaac Gym 仿真环境中完成策略训练与评估，利用运输成本（CoT）指标对比带与不带棱柱关节的机器人性能。结果表明，新增执行自由度显著增强了机器人穿越高难度地形的能力，并大幅降低能耗，验证了Isaac Gym在高效策略开发中的关键作用。

- ["Digital Twin of a Multi-Arm Robot Platform based on Isaac Sim for Synthetic Data Generation" (2023)](https://openalex.org/W4393538722) — Zenodo (CERN European Organization for Nuclear Research) — 该论文构建了一个基于Isaac Sim的多臂机器人平台数字孪生系统，专门用于生成大规模合成数据集，以支持机器人视觉与控制任务的预训练。作者在Isaac Sim中精确建模了多臂机器人的物理结构、传感器配置及环境交互，并利用其GPU加速的渲染与物理引擎高效生成带标注的RGB-D图像和状态数据。该数据集已公开发布，可显著降低真实世界数据采集成本，提升机器人学习算法的泛化能力。

- ["DribbleBot: Dynamic Legged Manipulation in the Wild" (2023)](https://openalex.org/W4362599025) [PDF](https://arxiv.org/pdf/2304.01159) (Citations: 1) — arXiv (Cornell University) — 该论文提出 DribbleBot，一个能在真实野外环境中用四足机器人运球的系统，通过在仿真中使用强化学习训练策略并迁移到现实世界。研究明确采用 Isaac Sim 作为核心仿真平台，利用其 GPU 加速的多物理场模拟能力来建模复杂地形下的球体动力学和机器人-球交互，并生成用于策略训练的高保真数据。该工作展示了 Isaac Sim 在动态全身控制与感知联合训练中的关键作用，为腿式机器人灵巧操作提供了可复现的仿真到现实迁移范式。

- ["Multi-Task Reinforcement Learning in Continuous Control with Successor Feature-Based Concurrent Composition" (2023)](http://arxiv.org/abs/2303.13935v2) [PDF](https://arxiv.org/pdf/2303.13935v2) — 该论文提出一种基于后继特征（Successor Features）的多任务强化学习方法，通过统一SF-GPI与值组合框架，在连续控制中实现无需额外训练即可组合策略分布。作者在Isaac Gym上构建了Pointmass和Pointer两个并行化基准环境，利用其大规模仿真能力高效验证多任务迁移性能，所提方法在保持与SAC相当单任务性能的同时，成功泛化至未见任务，为机器人在线学习提供高样本效率解决方案。

- ["GRADE: Generating Realistic And Dynamic Environments for Robotics Research with Isaac Sim" (2023)](http://arxiv.org/abs/2303.04466v3) [PDF](https://arxiv.org/pdf/2303.04466v3) (Citations: 2) — arXiv (Cornell University) — 本文提出GRADE框架，基于NVIDIA Isaac Sim构建高度可定制的动态仿真环境，用于机器人视觉感知研究。作者利用Isaac Sim的渲染能力与底层API，实现对动态场景的精确控制、真值数据采集，并支持实验的可重复性。通过在Isaac Sim中生成带丰富标注的无人机视角合成视频数据集，训练的人体检测与分割模型有效缩小了合成到真实（sim-to-real）的差距，为V-SLAM等动态环境下的机器人感知任务提供高质量仿真平台。

- ["Cutaneous Feedback Interface for Teleoperated In-Hand Manipulation" (2023)](http://arxiv.org/abs/2303.03250v1) [PDF](https://arxiv.org/pdf/2303.03250v1) — 本文提出了一种基于五连杆机构的皮肤触觉反馈接口，用于增强遥操作中的手内操作能力，通过在食指和拇指提供两个接触点传递抓取力、剪切力、摩擦及物体位姿信息。研究在Isaac Sim中构建了被动枢转任务的数值仿真环境，定量评估该接口对操作性能的提升效果。该工作展示了Isaac Sim作为高保真遥操作人机交互验证平台的应用价值。

- ["A Multi-Layered 3D NDT Scan-Matching Method for Robust Localization in Logistics Warehouse Environments" (2023)](https://openalex.org/W4322743802) [PDF](https://www.mdpi.com/1424-8220/23/5/2671/pdf?version=1677594334) (Citations: 4) — Sensors — 本文提出了一种多层3D NDT扫描匹配方法，通过在高度方向分层处理点云并基于各层协方差不确定性动态选择最优层，提升物流仓库等动态环境中的定位鲁棒性。研究利用Nvidia Omniverse Isaac Sim构建仿真环境，对所提方法进行了系统验证，生成了包含货架、货箱等典型仓库元素的高保真场景数据。该方法为移动机器人在遮挡严重、布局频繁变化的仓储环境中实现稳定导航提供了有效解决方案。

- ["Trend of Robot Simulators for the Development of Intelligent Robots: A Review" (2023)](https://openalex.org/W4324336845) (Citations: 1) — Journal of Korean institute of intelligent systems — 本文综述了五种主流机器人仿真器在智能机器人开发中的应用，重点分析了Isaac Sim在GPU内同时执行物理仿真与深度强化学习的优势。文中专门考察了11篇使用Isaac Sim的研究，突出其在缓解CPU-GPU数据瓶颈、加速训练过程以及支持可变形物体仿真方面的关键作用。该综述为选择高性能机器人仿真平台提供了实证参考，尤其强调Isaac Sim在AI驱动机器人快速迭代中的应用价值。

- ["Reinforcement Learning Based Pushing and Grasping Objects from Ungraspable Poses" (2023)](https://openalex.org/W4322716936) [PDF](https://arxiv.org/pdf/2302.13328) (Citations: 1) — arXiv (Cornell University) — 该论文提出了一种基于深度强化学习的推-抓协同策略，用于处理处于不可抓取姿态的物体。研究在 Isaac Sim 中构建高保真仿真环境，利用其 GPU 加速的多物理引擎进行大量交互式训练，并通过 CycleGAN 实现从 Isaac Sim 到真实机器人的无微调迁移。该方法显著提升了训练效率与泛化能力，为复杂物体操作提供了可部署的解决方案。

- ["Orbit: A Unified Simulation Framework for Interactive Robot Learning Environments" (2023)](http://arxiv.org/abs/2301.04195v2) [PDF](https://arxiv.org/pdf/2301.04195v2) (Citations: 181) — IEEE Robotics and Automation Letters — 本文提出了Orbit，一个基于NVIDIA Isaac Sim构建的统一、模块化机器人学习仿真框架。Orbit利用Isaac Sim的GPU加速多物理场仿真能力，支持高保真刚体与可变形体模拟，并集成了16种机器人平台、4类传感器、10种运动生成器及20余项基准任务，可高效训练强化学习策略或采集专家示范数据。该框架显著降低了在逼真环境中开发和测试交互式机器人算法的门槛，为机器人学习研究提供了强大工具。


---

<a id="projects"></a>
## 🔧 项目

- [IsaacLab](https://github.com/isaac-sim/IsaacLab) — IsaacLab 是一个基于 NVIDIA Isaac Sim 构建的统一机器人学习框架，专为强化学习、模仿学习等任务设计。它深度集成 Isaac Sim 的 GPU 加速物理仿真能力，提供模块化环境、传感器模型和训练工具链，支持快速开发与部署机器人策略。该项目面向机器人学习研究者与开发者，是 Isaac Sim 生态中的核心高级框架。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/IsaacLab?style=social)

- [IsaacGymEnvs](https://github.com/isaac-sim/IsaacGymEnvs) — 该项目提供基于Isaac Gym的强化学习环境集合，专为GPU加速的机器人仿真训练设计。它紧密集成NVIDIA Isaac Sim生态，利用其高性能物理引擎和并行仿真能力，支持多种机器人任务（如Ant、Humanoid、ShadowHand等）的RL算法开发与测试。目标用户为从事机器人强化学习研究与应用的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/IsaacGymEnvs?style=social)

- [legged_gym](https://github.com/leggedrobotics/legged_gym) — 该项目为足式机器人提供基于 Isaac Gym 的强化学习训练环境，专为在 Isaac Sim 的 GPU 加速物理仿真框架下高效训练四足、双足等腿式机器人策略而设计。它利用 Isaac Gym 的 RL 环境接口和 PhysX 引擎，实现高并发、低延迟的仿真训练，并与 Isaac Sim 生态深度集成。主要面向机器人学习研究者和开发者，用于快速开发和验证腿式机器人的运动控制算法。 ![GitHub stars](https://img.shields.io/github/stars/leggedrobotics/legged_gym?style=social)

- [IsaacSim](https://github.com/isaac-sim/IsaacSim) — NVIDIA Isaac Sim 是一个基于 Omniverse 的开源平台，用于在逼真虚拟环境中开发、仿真和测试 AI 驱动的机器人。它深度集成 GPU 加速的多物理仿真、传感器模拟和强化学习支持，专为机器人研究人员和开发者设计，提供与 Isaac Gym、Isaac Lab 等 NVIDIA 机器人工具链的原生兼容性。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/IsaacSim?style=social)

- [OmniIsaacGymEnvs](https://github.com/isaac-sim/OmniIsaacGymEnvs) — 该项目提供了一系列面向Omniverse Isaac Gym的强化学习环境，专为在Isaac Sim中训练机器人策略而设计。它基于Isaac Gym的GPU加速物理仿真能力，实现了多种机器人任务（如Ant、Humanoid、ShadowHand等）的RL训练环境，并与Isaac Sim深度集成，支持通过RL算法（如PPO）进行高效训练。目标用户为使用Isaac Sim进行机器人强化学习研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/OmniIsaacGymEnvs?style=social)

- [TienKung-Lab](https://github.com/Open-X-Humanoid/TienKung-Lab) — TienKung-Lab 是一个专为足式机器人设计的强化学习训练框架，直接基于 Isaac Lab 构建，提供完整的仿真到仿真的迁移（sim2sim）工作流。项目深度集成 Isaac Sim 的物理引擎与传感器模拟功能，利用其 GPU 加速多智能体并行能力，实现高效的人形机器人运动控制策略训练。目标用户为从事具身智能与人形机器人研究的开发者和科研人员。 ![GitHub stars](https://img.shields.io/github/stars/Open-X-Humanoid/TienKung-Lab?style=social)

- [IsaacSim-dockerfiles](https://github.com/NVIDIA-Omniverse/IsaacSim-dockerfiles) — 该项目提供官方的 Isaac Sim Docker 镜像构建文件，用于在容器化环境中部署和运行 NVIDIA Isaac Sim。通过 Dockerfile 封装了 Isaac Sim 的依赖与运行时环境，便于用户在不同系统上快速启动一致的仿真环境。适用于需要在 CI/CD、云平台或本地机器上高效部署 Isaac Sim 的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/NVIDIA-Omniverse/IsaacSim-dockerfiles?style=social)

- [awesome-isaac-sim](https://github.com/sjtuyinjie/awesome-isaac-sim) — 该项目是一个精选的 NVIDIA Isaac Sim 相关资源集合，涵盖教程、工具、示例和项目，旨在帮助开发者更高效地使用 Isaac Sim 进行机器人仿真与 AI 训练。内容明确聚焦于 Isaac Sim 生态，包括环境搭建、传感器模拟、强化学习集成等核心主题。目标用户为机器人研发人员、AI 工程师及科研人员。 ![GitHub stars](https://img.shields.io/github/stars/sjtuyinjie/awesome-isaac-sim?style=social)

- [isaacsim-app-template](https://github.com/isaac-sim/isaacsim-app-template) — 该项目是 NVIDIA Isaac Sim 的官方应用模板，用于快速创建基于 Kit 框架的自定义仿真应用。它提供了标准项目结构、配置文件和启动脚本，便于开发者集成传感器、机器人模型和物理场景，并与 Isaac Sim 的 Omniverse 后端无缝协作。目标用户为希望在 Isaac Sim 生态中构建专用仿真工具或扩展功能的机器人研发人员。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/isaacsim-app-template?style=social)

- [awesome-isaac-sim](https://github.com/shaoxiang/awesome-isaac-sim) — 该项目是一个精选的 NVIDIA Isaac Sim 资源集合，汇集了教程、工具和项目，旨在帮助开发者高效利用 Isaac Sim 进行机器人与自主系统的 GPU 加速多物理仿真。内容聚焦于 Isaac Sim 的核心功能，包括传感器模拟、强化学习训练和机器人建模，直接服务于该平台的用户社区。目标用户为从事 AI 驱动机器人研发的工程师与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/shaoxiang/awesome-isaac-sim?style=social)

- [isaac_lab_rl](https://github.com/austinchao886/isaac_lab_rl) — 该项目为ANYmal四足机器人提供基于Isaac Lab（Isaac Sim 4.5）的强化学习框架，使用RSL-RL PPO算法实现训练，并采用清晰的环境/智能体/训练模块分离设计。项目包含完整的Docker容器化配置，确保训练与测试的可复现性，适用于在Isaac Sim中开展高性能机器人强化学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/austinchao886/isaac_lab_rl?style=social)

- [Isaac-GR00T](https://github.com/NVIDIA/Isaac-GR00T) — NVIDIA Isaac GR00T N1.6 是一个面向通用机器人的基础模型，旨在通过统一的神经架构支持多任务、多机器人策略学习。该项目与 Isaac Sim 紧密集成，利用其高保真物理仿真和传感器模拟能力进行大规模行为训练与验证，支持在 Isaac Sim 中部署和测试 GR00T 模型。核心技术包括模仿学习、强化学习与世界模型，目标用户为机器人 AI 研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/NVIDIA/Isaac-GR00T?style=social)

- [rsl_rl](https://github.com/leggedrobotics/rsl_rl) — rsl_rl 是一个专为机器人控制设计的轻量级强化学习库，主要实现PPO等算法，支持与Isaac Sim和Isaac Gym无缝集成，利用其GPU加速的物理仿真环境进行高效训练。项目采用PyTorch实现，提供模块化策略和优化器，适用于四足机器人等高动态系统的策略开发。目标用户为使用NVIDIA Isaac平台进行机器人学习研究的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/leggedrobotics/rsl_rl?style=social)

- [ASAP](https://github.com/LeCAR-Lab/ASAP) — ASAP 是一个用于学习敏捷人形机器人全身技能的强化学习框架，通过物理对齐方法缩小仿真与现实之间的差距。项目明确基于 Isaac Sim 构建仿真环境，利用其 GPU 加速的多物理引擎进行高保真人形机器人训练，并提供与 Isaac Lab 的集成接口。该框架面向从事人形机器人强化学习研究的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/LeCAR-Lab/ASAP?style=social)

- [ProtoMotions](https://github.com/NVlabs/ProtoMotions) — ProtoMotions 是一个用于训练物理仿真数字人和人形机器人的 GPU 加速仿真与学习框架，支持强化学习与高保真角色动画。该项目由 NVIDIA 研究团队开发，明确支持在 Isaac Sim 中运行，利用其 PhysX 物理引擎和 Omniverse 架构实现高保真人体动力学仿真。它提供了与 Isaac Sim 深度集成的示例和工具链，适用于机器人学、虚拟角色控制等领域的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/NVlabs/ProtoMotions?style=social)

- [NavRL](https://github.com/Zhefan-Xu/NavRL) — NavRL 是一个基于强化学习的机器人导航框架，专注于动态环境中的安全飞行与避障。项目原生集成 NVIDIA Isaac Sim 作为核心仿真平台，利用其 GPU 加速的多物理场模拟能力训练策略，并支持 ROS1/ROS2 接口。该框架适用于需要在高保真仿真中开发和验证自主导航算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Zhefan-Xu/NavRL?style=social)

- [skrl](https://github.com/Toni-SM/skrl) — skrl 是一个模块化的强化学习库，支持 PyTorch、JAX 和 NVIDIA Warp 后端，明确提供对 NVIDIA Isaac Lab 和 Isaac Sim 环境的集成支持。它通过统一接口兼容 Gymnasium 等多种仿真平台，并利用 GPU 加速实现高效训练，适用于机器人控制等场景。该项目面向希望在 Isaac Sim 生态中开发和部署强化学习算法的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Toni-SM/skrl?style=social)

- [HOVER](https://github.com/NVlabs/HOVER) — HOVER 是一个用于生成高质量、物理精确的机器人仿真数据集的框架，主要支持在 Isaac Sim 中进行大规模虚拟环境构建与数据采集。它利用 Isaac Sim 的 GPU 加速多物理引擎，实现逼真的传感器模拟（如 RGB-D、LiDAR）和动态物体交互，适用于训练和验证机器人感知与导航模型。该项目由 NVIDIA 研究团队开发，专为 Isaac Sim 生态设计，目标用户为机器人学习与仿真领域的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/NVlabs/HOVER?style=social)

- [robot_lab](https://github.com/fan-ziqi/robot_lab) — 该项目是一个基于 Isaac Lab 的机器人强化学习扩展库，提供模块化组件和工具链，用于快速构建和训练机器人策略。它深度集成 Isaac Lab 的仿真环境与 RL 框架，利用其 GPU 加速的物理模拟能力，支持多种机器人任务的开发与评估。主要面向使用 Isaac Sim 生态进行机器人学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/fan-ziqi/robot_lab?style=social)

- [awesome-isaac-gym](https://github.com/robotlearning123/awesome-isaac-gym) — 该项目是一个精选的 Awesome 列表，汇集了面向 NVIDIA Isaac Gym 的强化学习框架、研究论文、软件工具和学习资源。它明确聚焦于 Isaac Gym 生态，涵盖环境实现、算法示例和机器人学习教程，帮助研究人员和开发者快速上手基于 GPU 加速的机器人仿真与训练。目标用户为从事机器人强化学习的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/robotlearning123/awesome-isaac-gym?style=social)

- [go2_omniverse](https://github.com/abizovnuralem/go2_omniverse) — 该项目为Unitree Go2和G1人形机器人提供对NVIDIA Isaac Lab（包括Isaac Gym和Isaac Sim）的官方支持，实现了在Omniverse平台上的高保真仿真与强化学习训练。通过集成Isaac Lab的Orbit框架，项目提供了完整的机器人URDF模型、传感器配置及任务环境，便于研究人员快速开展基于GPU加速物理仿真的机器人控制算法开发。目标用户为从事人形机器人学习与仿真的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/abizovnuralem/go2_omniverse?style=social)

- [holosoma](https://github.com/amazon-far/holosoma) — Holosoma 是一个用于生成合成数据的框架，主要支持在 Isaac Sim 中创建逼真的 3D 场景以训练机器人感知模型。它利用 Omniverse 和 Isaac Sim 的渲染与物理模拟能力，提供场景配置、传感器模拟和数据标注功能。该项目面向需要大规模高质量合成数据的机器人视觉与 AI 训练开发者。 ![GitHub stars](https://img.shields.io/github/stars/amazon-far/holosoma?style=social)

- [ReKep](https://github.com/huangwl18/ReKep) — ReKep 是一个用于机器人操作的时空关系关键点约束推理框架，主要通过视觉语言模型解析任务指令并生成关键点约束，引导机器人完成复杂操作。该项目明确支持在 Isaac Sim 中进行仿真训练与部署，利用其 GPU 加速物理引擎实现高保真交互，并提供了与 Isaac Lab 的集成示例。目标用户为从事具身智能与仿真训练的机器人研究人员。 ![GitHub stars](https://img.shields.io/github/stars/huangwl18/ReKep?style=social)

- [unitree_rl_lab](https://github.com/unitreerobotics/unitree_rl_lab) — 该项目基于 Isaac Lab 实现了针对宇树（Unitree）机器人的强化学习算法，提供了完整的训练环境与策略部署流程。它深度集成 Isaac Sim 的物理仿真与 GPU 加速能力，利用 Isaac Lab 的模块化框架构建四足机器人控制任务。目标用户为从事四足机器人强化学习研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/unitreerobotics/unitree_rl_lab?style=social)

- [PegasusSimulator](https://github.com/PegasusSimulator/PegasusSimulator) — PegasusSimulator 是一个基于 NVIDIA Isaac Sim 构建的无人机仿真框架，提供对 PX4 飞控系统的原生支持，并集成多旋翼动力学模型与传感器模拟。它利用 Isaac Sim 的 Omniverse Kit 扩展机制，实现高保真、GPU 加速的 UAV 仿真环境，适用于无人机算法开发与自主飞行测试。 ![GitHub stars](https://img.shields.io/github/stars/PegasusSimulator/PegasusSimulator?style=social)

- [aerial_gym_simulator](https://github.com/ntnu-arl/aerial_gym_simulator) — 该项目是一个专为飞行机器人设计的强化学习仿真框架，基于Isaac Gym构建，利用其GPU加速的物理模拟能力实现高吞吐量的多智能体训练。它提供了针对多旋翼无人机的动力学模型、传感器模拟和任务环境，并深度集成Isaac Gym的API以支持大规模并行仿真。主要面向从事空中机器人自主控制与强化学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/ntnu-arl/aerial_gym_simulator?style=social)

- [isaac_ros_nvblox](https://github.com/NVIDIA-ISAAC-ROS/isaac_ros_nvblox) — 该项目提供基于NVIDIA GPU加速的3D场景重建与Nav2局部代价地图生成功能，利用nvblox库实现实时稠密建图。它专为Isaac ROS设计，可无缝集成到Isaac Sim仿真环境或真实机器人系统中，支持Jetson平台部署。主要面向使用ROS 2 Humble开发自主导航机器人的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/NVIDIA-ISAAC-ROS/isaac_ros_nvblox?style=social)

- [LeggedLab](https://github.com/Hellod035/LeggedLab) — LeggedLab 提供面向足式机器人的 Isaac Lab 直接工作流，基于 Isaac Sim 构建高性能仿真环境，支持四足和双足机器人控制策略的快速开发与测试。项目深度集成 Isaac Lab 的 RL 框架和 PhysX 物理引擎，利用 GPU 加速实现大规模并行训练。主要面向足式机器人研究者与开发者，适用于强化学习与运动控制算法验证。 ![GitHub stars](https://img.shields.io/github/stars/Hellod035/LeggedLab?style=social)

- [HDMI](https://github.com/LeCAR-Lab/HDMI) — HDMI 是一个用于高维多模态强化学习的框架，主要支持在 Isaac Sim 和 Isaac Gym 环境中进行机器人策略训练。该项目提供了与 Isaac Sim 深度集成的接口，利用其 GPU 加速的物理仿真能力来高效生成多模态感知数据（如 RGB-D、点云和关节状态）。目标用户为从事具身智能与仿真训练的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/LeCAR-Lab/HDMI?style=social)

- [NaVILA](https://github.com/AnjieCheng/NaVILA) — NaVILA 是一个面向足式机器人的视觉-语言-动作导航模型，支持在仿真环境中进行端到端导航任务。项目明确使用 Isaac Sim 作为主要仿真平台，利用其 GPU 加速的多物理场模拟能力构建高保真训练环境，并集成了 ROS 2 和 Isaac Sim 的通信接口。该仓库为研究具身智能与多模态机器人控制的研究人员提供了可复现的 Isaac Sim 集成方案。 ![GitHub stars](https://img.shields.io/github/stars/AnjieCheng/NaVILA?style=social)

- [OmniDrones](https://github.com/btx0424/OmniDrones) — OmniDrones 是一个基于强化学习的多无人机仿真框架，专为 NVIDIA Isaac Sim（Omniverse 平台）构建，利用其 GPU 加速的物理引擎和传感器模拟能力实现高保真无人机集群训练。项目通过 Isaac Sim 的 USD 场景和 PhysX 物理系统实现逼真的多机动力学与环境交互，支持大规模并行 RL 训练。主要面向机器人强化学习研究者和无人机自主系统开发者。 ![GitHub stars](https://img.shields.io/github/stars/btx0424/OmniDrones?style=social)

- [isaac-go2-ros2](https://github.com/Zhefan-Xu/isaac-go2-ros2) — 该项目提供了一个基于 NVIDIA Isaac Sim 的 Unitree Go2 机器人仿真平台，用于测试导航、决策与自主任务。它通过 ROS 2 Humble 实现与 Isaac Sim 的深度集成，支持相机、LiDAR 等传感器仿真，并利用 Isaac ROS 和 Isaac Lab 工具链构建高性能机器人算法开发环境。目标用户为使用 Unitree Go2 进行 AI 驱动机器人研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Zhefan-Xu/isaac-go2-ros2?style=social)

- [HumanoidVerse](https://github.com/LeCAR-Lab/HumanoidVerse) — HumanoidVerse 是一个专注于人形机器人仿真的开源框架，主要基于 Isaac Sim 构建，提供高保真物理模拟和传感器仿真能力。项目利用 Isaac Sim 的 GPU 加速多物理引擎支持复杂人形机器人的运动控制、感知与交互实验，并集成了 ROS 2 和常用强化学习接口。该框架面向机器人研究人员和开发者，旨在加速人形机器人算法在逼真虚拟环境中的开发与验证。 ![GitHub stars](https://img.shields.io/github/stars/LeCAR-Lab/HumanoidVerse?style=social)

- [legged-loco](https://github.com/yang-zj1026/legged-loco) — 该项目专注于在 Isaac Lab 中训练四足机器人底层运动控制策略，利用其强化学习框架和 GPU 加速物理仿真能力，实现高效、稳定的步态学习。项目基于 Isaac Lab 的环境接口和传感器抽象，采用 PPO 等算法进行端到端策略优化，适用于希望在 Isaac Sim 生态中开发高性能腿式机器人控制器的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/yang-zj1026/legged-loco?style=social)

- [OceanSim](https://github.com/umfieldrobotics/OceanSim) — OceanSim 是一个面向水下机器人感知任务的 GPU 加速仿真框架，专为高保真水下视觉与传感器模拟设计。该项目基于 Isaac Sim 构建，利用其 PhysX 物理引擎和 RTX 渲染能力，实现逼真的水下光学效果、浑浊介质散射及动态流体交互。目标用户为从事水下机器人感知、SLAM 和自主导航研究的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/umfieldrobotics/OceanSim?style=social)

- [humanoid_amp](https://github.com/linden713/humanoid_amp) — 该项目基于Isaac Lab实现Unitree G1人形机器人的AMP（Adversarial Motion Priors）运动控制，利用Isaac Sim的GPU加速物理仿真环境训练高动态全身动作策略。项目集成了Isaac Lab的任务框架与资产加载系统，并针对G1机器人定制了URDF模型和奖励函数，适用于人形机器人强化学习研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/linden713/humanoid_amp?style=social)

- [pace-sim2real](https://github.com/leggedrobotics/pace-sim2real) — PACE 提供了一套系统化方法，用于腿式机器人从仿真到现实的迁移，通过标准关节编码器识别执行器与关节动力学特性。该项目明确支持在 Isaac Sim 中进行高保真仿真，并提供了与 Isaac Lab 的集成示例，利用其 GPU 加速物理引擎和传感器模拟能力。目标用户为从事腿式机器人 sim2real 研究的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/leggedrobotics/pace-sim2real?style=social)

- [unitree_sim_isaaclab](https://github.com/unitreerobotics/unitree_sim_isaaclab) — 该项目基于 Isaac Lab 构建了 Unitree 机器人的仿真环境，专为四足机器人控制与强化学习研究设计。它利用 Isaac Lab 的 GPU 加速物理仿真能力，提供高保真、高性能的 Unitree 机器人（如 Go1、H1）模拟接口，并集成了传感器模型与运动控制示例。目标用户为使用 Isaac Sim 生态进行四足机器人算法开发与训练的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/unitreerobotics/unitree_sim_isaaclab?style=social)

- [FALCON](https://github.com/LeCAR-Lab/FALCON) — FALCON 是一个用于学习力自适应人形机器人移动-操作（loco-manipulation）的框架，主要在 Isaac Sim 中构建高保真仿真环境以训练和验证策略。项目利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能，实现复杂接触交互与动态任务的闭环训练。其核心基于强化学习与力控策略，目标用户为研究人形机器人灵巧操作与全身运动控制的科研人员。 ![GitHub stars](https://img.shields.io/github/stars/LeCAR-Lab/FALCON?style=social)

- [NaVILA-Bench](https://github.com/yang-zj1026/NaVILA-Bench) — NaVILA-Bench 是一个面向视觉-语言导航（Vision-Language Navigation）的基准测试平台，专为 Isaac Lab 构建，用于评估智能体在复杂3D环境中根据自然语言指令进行导航的能力。项目基于 Isaac Sim 的高性能物理与渲染引擎，利用其 GPU 加速的多智能体仿真能力，提供逼真的室内场景和交互式任务设置。该基准适用于机器人导航、具身智能及多模态 AI 研究人员。 ![GitHub stars](https://img.shields.io/github/stars/yang-zj1026/NaVILA-Bench?style=social)

- [dexterity-aha-guide](https://github.com/Wu-Fisher/dexterity-aha-guide) — 该项目提供从零开始构建灵巧手仿真的教程和代码，主要基于 Isaac Sim 平台实现高保真物理模拟。它利用 Isaac Sim 的 GPU 加速多物理引擎和 ROS 2 集成功能，展示如何搭建灵巧手模型、配置传感器并实现闭环控制。目标用户为希望在 Isaac Sim 中开发灵巧操作任务的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Wu-Fisher/dexterity-aha-guide?style=social)

- [isaacLab.manipulation](https://github.com/NathanWu7/isaacLab.manipulation) — 该项目是一个基于 Isaac Lab 的独立扩展，专注于机器人操作任务，提供对机械臂和灵巧手的支持。它利用 Isaac Sim 的 GPU 加速物理仿真能力，构建了适用于强化学习的 manipulation 环境，并与 Isaac Lab 的框架深度集成。目标用户为从事机器人操作研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/NathanWu7/isaacLab.manipulation?style=social)

- [IsaacLabExtensionTemplate](https://github.com/isaac-sim/IsaacLabExtensionTemplate) — 该项目是一个基于 Isaac Lab 的外部扩展模板，用于快速创建与 Isaac Sim 兼容的自定义扩展模块。它提供了标准项目结构、构建脚本和示例代码，支持通过 Omniverse Kit 扩展机制集成到 Isaac Sim 中，便于开发者复用 Isaac Lab 的机器人仿真能力。目标用户为希望在 Isaac Sim 生态中开发专用工具或插件的机器人研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/IsaacLabExtensionTemplate?style=social)

- [isaac_berkeley_humanoid](https://github.com/HybridRobotics/isaac_berkeley_humanoid) — 该项目提供了在 Isaac Sim 中仿真伯克利人形机器人的完整框架，包含 URDF 模型、控制器和任务配置，专为基于 Isaac Sim 的人形机器人运动控制与强化学习研究设计。它深度集成 Isaac Sim 的 PhysX 物理引擎和 ROS 2 接口，支持高保真动力学仿真与传感器模拟。主要面向人形机器人算法开发人员和具身智能研究人员。 ![GitHub stars](https://img.shields.io/github/stars/HybridRobotics/isaac_berkeley_humanoid?style=social)

- [Isaac-RL-Two-wheel-Legged-Bot](https://github.com/jaykorea/Isaac-RL-Two-wheel-Legged-Bot) — 该项目实现了一个两轮腿式机器人的强化学习训练框架，专为 Isaac Lab 设计。它利用 Isaac Sim 的 GPU 加速物理仿真能力，在 Isaac Gym 环境中构建了自定义的双足-轮式混合机器人模型，并集成了 RL 训练流程。目标用户是希望在 Isaac Sim 生态中开发新型移动机器人控制策略的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/jaykorea/Isaac-RL-Two-wheel-Legged-Bot?style=social)

- [IsaacLab-Arena](https://github.com/isaac-sim/IsaacLab-Arena) — Isaac Lab - Arena 是一个专为 NVIDIA Isaac Lab 设计的机器人仿真框架，通过提供可组合、可扩展的系统，支持快速构建多样化的仿真环境并评估机器人学习策略。它深度集成 Isaac Lab，允许用户灵活配置机器人本体、物体和场景，适用于强化学习与具身智能研究。目标用户为使用 Isaac Sim 生态进行机器人算法开发与验证的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/IsaacLab-Arena?style=social)

- [IsaacSim-ros_workspaces](https://github.com/isaac-sim/IsaacSim-ros_workspaces) — 该项目提供专为 Isaac Sim 设计的 ROS 工作空间配置，用于简化机器人操作系统（ROS/ROS2）与 Isaac Sim 的集成。它包含预配置的包和依赖项，支持通过 ROS Bridge 实现 Isaac Sim 与外部 ROS 节点的通信，并兼容 ROS1 Noetic 和 ROS2 Humble。目标用户是需要在 Isaac Sim 中开发或测试 ROS 驱动机器人应用的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/IsaacSim-ros_workspaces?style=social)

- [WheeledLab](https://github.com/UWRobotLearning/WheeledLab) — WheeledLab 提供面向轮式移动机器人的开源环境、资产与工作流，专为 Isaac Lab 深度集成而设计。项目基于 Python 实现，利用 Isaac Lab 的 GPU 加速物理仿真能力，支持机器人导航、控制与强化学习算法的快速开发与测试。主要面向从事移动机器人研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/UWRobotLearning/WheeledLab?style=social)

- [isaac_ros_cumotion](https://github.com/NVIDIA-ISAAC-ROS/isaac_ros_cumotion) — isaac_ros_cumotion 是 NVIDIA 提供的 ROS 2 软件包，专为机械臂运动规划与控制提供 GPU 加速支持，基于 CUDA 实现高效轨迹生成与优化。该项目深度集成 Isaac Sim 生态，可与 Isaac Lab 和 Isaac Gym 协同使用，实现高保真仿真到真实机器人的无缝迁移。其核心功能包括与 MoveIt 2 兼容的运动规划接口，适用于在 Jetson 平台上开发高性能机器人操作应用的开发者。 ![GitHub stars](https://img.shields.io/github/stars/NVIDIA-ISAAC-ROS/isaac_ros_cumotion?style=social)

- [kinova_isaaclab_sim2real](https://github.com/louislelay/kinova_isaaclab_sim2real) — 该项目专注于在 Isaac Lab 中训练 Kinova Gen3 机械臂，实现从仿真到现实（sim2real）的策略迁移，并支持 ROS/ROS2 部署。它利用 PPO 强化学习算法，在 Isaac Sim 提供的 GPU 加速物理仿真环境中训练策略，最终将控制策略部署到真实 Kinova 机器人上。项目为使用 Isaac Sim 和 Isaac Lab 进行机器人强化学习研究与应用的开发者提供了完整工作流。 ![GitHub stars](https://img.shields.io/github/stars/louislelay/kinova_isaaclab_sim2real?style=social)

- [IsaacAutomator](https://github.com/isaac-sim/IsaacAutomator) — IsaacAutomator 是一个用于在主流云平台（AWS、Azure、GCP、阿里云）上自动化部署和运行 Isaac Sim 与 Isaac Lab 的工具。它通过 Python 脚本实现跨云环境的一键配置，简化了 GPU 加速机器人仿真环境的搭建流程。该项目直接面向 Isaac Sim 生态，为需要在云端扩展仿真的开发者和研究人员提供关键基础设施支持。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/IsaacAutomator?style=social)

- [MobilityGen](https://github.com/NVlabs/MobilityGen) — MobilityGen 是一个用于生成移动性数据的流水线工具，主要支持在 Isaac Sim 中创建高保真、物理真实的行人和群体运动数据集。该项目利用 Isaac Sim 的 GPU 加速多智能体仿真能力，结合行为模型与环境交互，生成可用于训练和验证机器人导航系统的多样化轨迹数据。目标用户为从事具身智能、服务机器人或自主导航研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/NVlabs/MobilityGen?style=social)

- [synthetic-manipulation-motion-generation](https://github.com/NVIDIA-Omniverse-blueprints/synthetic-manipulation-motion-generation) — 该项目提供了一个参考工作流，用于从少量人类演示中生成大量机器人操作的合成运动轨迹。它基于 NVIDIA Omniverse 构建，明确支持在 Isaac Sim 中进行运动数据生成与仿真，利用其 PhysX 物理引擎和 USD 场景表示实现高保真操作任务模拟。目标用户为需要大规模合成操作数据以训练机器人策略的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/NVIDIA-Omniverse-blueprints/synthetic-manipulation-motion-generation?style=social)

- [isaac_sim_grasping](https://github.com/IRVLUTD/isaac_sim_grasping) — 该项目提供了一套用于机器人抓取仿真的工具包，专为MultiGripperGrasp数据集设计，基于Isaac Sim构建。它利用Isaac Sim的GPU加速物理引擎和传感器模拟功能，实现多夹爪抓取策略的高效仿真与评估。主要面向从事机器人操作与抓取研究的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/IRVLUTD/isaac_sim_grasping?style=social)

- [arnold](https://github.com/arnold-benchmark/arnold) — ARNOLD 是一个面向语言引导机器人操作的基准平台，支持在逼真3D场景中处理连续物体状态。该项目明确将 Isaac Sim 作为其官方支持的仿真后端之一，利用其GPU加速的物理和渲染能力构建高保真交互环境。通过集成 Isaac Sim，ARNOLD 实现了对复杂指令-动作映射任务的高效训练与评估，适用于具身智能与多模态机器人学习研究者。 ![GitHub stars](https://img.shields.io/github/stars/arnold-benchmark/arnold?style=social)

- [isaac_so_arm101](https://github.com/MuammerBay/isaac_so_arm101) — 该项目为SO-ARM100/101机械臂提供Isaac Lab外部集成支持，基于Isaac Sim构建强化学习训练环境。通过Omniverse平台实现高保真物理仿真，并利用Isaac Lab的模块化框架配置机器人任务与奖励函数。主要面向使用NVIDIA Isaac Sim进行机器人控制算法开发的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/MuammerBay/isaac_so_arm101?style=social)

- [LEAP_Hand_Sim](https://github.com/leap-hand/LEAP_Hand_Sim) — 该项目是专为LEAP Hand V1设计的Isaac Gym仿真环境，基于NVIDIA Isaac Sim平台实现高保真手部灵巧操作模拟。它利用GPU加速的物理引擎支持大规模并行强化学习训练，提供完整的机器人手模型、控制接口和任务示例。主要面向从事灵巧手控制与强化学习研究的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/leap-hand/LEAP_Hand_Sim?style=social)

- [InternManip](https://github.com/InternRobotics/InternManip) — InternManip 是一个集成了多种机器人操作学习任务的训练与评估套件，支持多数据集和基准测试。项目明确提供对 Isaac Sim 的原生支持，利用其 GPU 加速的物理仿真能力进行策略模型训练，并通过 Isaac Lab 进行任务配置与环境搭建。该工具适合从事机器人学习研究的开发者和研究人员使用。 ![GitHub stars](https://img.shields.io/github/stars/InternRobotics/InternManip?style=social)

- [OmniLRS](https://github.com/OmniLRS/OmniLRS) — Omniverse Lunar Robotics Simulator（OmniLRS）是一个基于NVIDIA Omniverse构建的月球机器人仿真平台，专为在高保真月面环境中测试和开发机器人系统而设计。该项目深度集成Isaac Sim，利用其GPU加速的物理引擎和传感器模拟功能，支持轮式/足式机器人在复杂月壤地形中的运动规划与感知算法验证。目标用户为从事地外机器人研发的科研机构与航天工程师。 ![GitHub stars](https://img.shields.io/github/stars/OmniLRS/OmniLRS?style=social)

- [MetaIsaacGrasp](https://github.com/YitianShi/MetaIsaacGrasp) — 该项目是一个基于 Isaac Lab 构建的抓取学习测试平台，专注于强化学习环境下的抓取检测与策略训练。它利用 Isaac Sim 的 GPU 加速物理仿真能力，提供可扩展的机械臂抓取任务框架，支持自定义物体与传感器配置。主要面向机器人抓取研究者和 Isaac Sim 开发生态用户。 ![GitHub stars](https://img.shields.io/github/stars/YitianShi/MetaIsaacGrasp?style=social)

- [isaac_drone_racer](https://github.com/kousheekc/isaac_drone_racer) — Isaac Drone Racer 是一个基于 Isaac Lab 构建的强化学习框架，专为高速自主无人机竞速任务设计。项目利用 Isaac Sim 的 GPU 加速物理仿真能力，实现高保真无人机动力学模拟与传感器建模，并集成了 RL 训练流程以优化竞速策略。该框架面向从事空中机器人与自主竞速研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/kousheekc/isaac_drone_racer?style=social)

- [orbit-surgical](https://github.com/orbit-surgical/orbit-surgical) — ORBIT-Surgical 是一个面向手术机器人增强灵巧性学习的开源仿真框架，基于 Isaac Sim 构建，利用其 GPU 加速的多物理场模拟能力实现高保真手术场景模拟。项目集成了 Isaac Sim 的传感器、渲染和物理引擎接口，并提供专门针对微创手术操作的工具模型与任务环境。主要面向医疗机器人研究者和 AI 手术自动化开发者。 ![GitHub stars](https://img.shields.io/github/stars/orbit-surgical/orbit-surgical?style=social)

- [gz-omni](https://github.com/gazebosim/gz-omni) — gz-omni 是一个连接 Gazebo 与 NVIDIA Isaac Sim 的桥接工具，通过 Omniverse Connector 实现两个仿真平台间的数据同步与互操作。该项目利用 C++ 开发，支持在 Isaac Sim 中可视化和交互 Gazebo 仿真场景，便于开发者在统一环境中结合两者优势进行机器人算法开发与测试。主要面向需要跨仿真平台协作的机器人研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/gazebosim/gz-omni?style=social)

- [GarmentLab](https://github.com/GarmentLab/GarmentLab) — GarmentLab 是一个面向服装操作任务的统一仿真与基准测试平台，主要支持在 Isaac Sim 中进行高保真布料物理模拟。项目利用 NVIDIA PhysX 和 OmniGraph 实现服装的动态交互，并提供标准化的任务接口和评估指标。该平台专为机器人操作服装的研究人员和开发者设计，深度集成 Isaac Sim 的 GPU 加速多物理场仿真能力。 ![GitHub stars](https://img.shields.io/github/stars/GarmentLab/GarmentLab?style=social)

- [DreamControl](https://github.com/GenRobo/DreamControl) — DreamControl 是一个基于引导扩散模型的人形机器人全身控制框架，旨在实现受人类启发的场景交互行为。该项目通过在 Isaac Sim 中构建高保真人形机器人仿真环境，利用其 GPU 加速的物理引擎进行动作生成与验证，并支持与场景物体的复杂交互。关键技术包括扩散策略、运动重定向和物理约束优化，主要面向人形机器人控制与具身智能研究者。 ![GitHub stars](https://img.shields.io/github/stars/GenRobo/DreamControl?style=social)

- [GenManip](https://github.com/InternRobotics/GenManip) — GenManip 是一个基于大语言模型（LLM）驱动的机器人操作仿真框架，旨在实现可泛化的指令跟随操作。该项目明确构建于 NVIDIA Isaac Sim 之上，利用其 GPU 加速的多物理仿真能力来生成多样化、语义丰富的操作任务场景。通过与 Isaac Sim 深度集成，系统能将自然语言指令转化为仿真环境中的具体动作序列，适用于机器人学习与泛化研究社区。 ![GitHub stars](https://img.shields.io/github/stars/InternRobotics/GenManip?style=social)

- [mjcf2usd](https://github.com/LightwheelAI/mjcf2usd) — 该项目是一个专为Isaac Sim开发的扩展工具，用于将MuJoCo的MJCF格式文件转换为通用场景描述（USD）格式，便于在Isaac Sim中直接加载和使用机器人模型。其核心功能基于Python实现，利用Isaac Sim的USD支持能力，简化了从MuJoCo到NVIDIA仿真平台的迁移流程。该工具主要面向使用Isaac Sim进行具身智能与机器人仿真的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/LightwheelAI/mjcf2usd?style=social)

- [X-MOBILITY](https://github.com/NVlabs/X-MOBILITY) — X-MOBILITY 是一个用于机器人移动性研究的开源框架，主要支持在复杂地形上进行运动规划与控制算法开发。该项目明确集成了 Isaac Sim 作为其核心仿真平台，利用其 GPU 加速的多物理场模拟能力来验证足式与轮式机器人的穿越性能。项目包含预构建的 Isaac Sim 场景和传感器配置，适用于机器人感知-行动闭环研究，目标用户为从事野外移动机器人研发的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/NVlabs/X-MOBILITY?style=social)

- [MarineGym](https://github.com/Marine-RL/MarineGym) — MarineGym 是一个面向水下机器人强化学习的高性能平台，基于 Isaac Sim 构建，利用其 GPU 加速的多物理场仿真能力实现逼真的海洋环境模拟。项目集成了流体动力学、传感器噪声模型和实时控制接口，支持复杂水下任务的策略训练与验证。主要面向水下机器人研究者和自主系统开发者。 ![GitHub stars](https://img.shields.io/github/stars/Marine-RL/MarineGym?style=social)

- [DexGarmentLab](https://github.com/wayrise/DexGarmentLab) — DexGarmentLab 是一个面向灵巧服装操作的仿真环境，支持可泛化策略训练。该项目基于 Isaac Sim 构建，利用其 GPU 加速的多物理场仿真能力实现高保真布料动力学模拟，并集成了 ROS 2 和 Franka 机械臂模型。主要面向机器人学习与可穿戴机器人领域的研究人员。 ![GitHub stars](https://img.shields.io/github/stars/wayrise/DexGarmentLab?style=social)

- [IsaacLabEureka](https://github.com/isaac-sim/IsaacLabEureka) — IsaacLabEureka 是一个基于 Isaac Lab 的强化学习智能体自动课程生成框架，利用大语言模型（LLM）自动生成奖励函数和训练课程，显著降低在 Isaac Sim 中开发复杂机器人控制策略的门槛。该项目深度集成 Isaac Lab 的 API，支持 GPU 加速的并行仿真环境，适用于需要高效自动化 RL 训练流程的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/IsaacLabEureka?style=social)

- [isaac-sim-mcp](https://github.com/omni-mcp/isaac-sim-mcp) — 该项目为Isaac Sim提供了MCP（Multi-Client Protocol）扩展与服务器实现，允许外部客户端通过标准化协议与Isaac Sim仿真环境进行实时交互和控制。它深度集成Isaac Sim的OmniKit架构，利用Python构建通信接口，支持多智能体协同仿真与远程指令调度。主要面向需要将Isaac Sim接入分布式AI训练或远程操作系统的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/omni-mcp/isaac-sim-mcp?style=social)

- [isaac-launchable](https://github.com/isaac-sim/isaac-launchable) — 该项目利用 NVIDIA Brev 的 Launchable 功能，为学习者提供预配置的 Isaac Sim 与 Isaac Lab 开发环境，包含 VSCode 实例、Kit App Streaming 客户端等组件。通过 Docker 容器化部署，简化了 Isaac Sim 生态工具链的搭建流程，特别适合希望快速上手 NVIDIA 机器人仿真平台的新用户和教育场景。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/isaac-launchable?style=social)

- [OmniIsaacGymEnvs-UR10Reacher](https://github.com/j3soon/OmniIsaacGymEnvs-UR10Reacher) — 该项目为UR10机械臂提供了一个基于强化学习的Reacher任务环境，专为NVIDIA Omniverse Isaac Gym/Sim设计，支持Sim2Real迁移。它利用Isaac Sim的GPU加速物理仿真能力，构建高保真UR10操作场景，并集成到Isaac Gym的RL训练框架中。目标用户是希望在Isaac Sim中开发或测试UR系列机器人强化学习算法的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/j3soon/OmniIsaacGymEnvs-UR10Reacher?style=social)

- [TacEx](https://github.com/DH-Ng/TacEx) — 该项目为Isaac Sim和Isaac Lab提供触觉感知扩展功能，通过集成高保真触觉传感器模拟，支持在GPU加速的物理仿真环境中进行机器人触觉交互研究。其基于Python实现，可无缝接入NVIDIA Isaac生态，适用于需要精细接触反馈的机器人学习与控制任务。目标用户为从事具身智能与触觉感知研究的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/DH-Ng/TacEx?style=social)

- [isaac-ros2-control-sample](https://github.com/hijimasa/isaac-ros2-control-sample) — 该项目提供了一系列实用工具，旨在简化 Isaac Sim 与 ROS 2 控制系统的集成，支持 ros2_control 操作、自动传感器生成及传感器数据发布。通过 Python 脚本实现 Isaac Sim 中仿真传感器的自动化配置与 ROS 2 Humble 环境下的数据通信，显著降低机器人控制开发门槛。主要面向使用 Isaac Sim 进行机器人仿真的 ROS 2 开发者。 ![GitHub stars](https://img.shields.io/github/stars/hijimasa/isaac-ros2-control-sample?style=social)

- [RLRoverLab](https://github.com/abmoRobotics/RLRoverLab) — 该项目提供了面向火星车和太空任务的强化学习环境，专为 Isaac Sim 和 Isaac Lab 构建，利用其 GPU 加速的物理仿真能力实现高保真机器人训练。通过集成 Isaac Lab 的 RL 框架，支持基于 PhysX 的多体动力学与传感器模拟，适用于航天机器人算法研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/abmoRobotics/RLRoverLab?style=social)

- [isaac-marl-mobile-manipulation](https://github.com/TIERS/isaac-marl-mobile-manipulation) — 该项目利用多智能体强化学习（MARL）在 NVIDIA Isaac Sim 中实现移动操作任务，通过 Isaac Sim 提供的高保真物理仿真和 GPU 加速环境训练多个协作机器人。项目基于 Isaac Sim 的 Python API 构建任务场景，并集成 RLlib 等框架进行策略训练，适用于研究多机器人协同操作的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/TIERS/isaac-marl-mobile-manipulation?style=social)

- [SurgicalGym](https://github.com/SamuelSchmidgall/SurgicalGym) — SurgicalGym 是一个基于 GPU 加速的高性能仿真平台，专为手术机器人强化学习任务设计。项目明确集成 Isaac Gym 和 Isaac Sim，利用其物理引擎与并行模拟能力构建逼真的手术操作环境，支持可扩展的 RL 训练流程。目标用户为医疗机器人领域的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/SamuelSchmidgall/SurgicalGym?style=social)

- [Lightwheel_Kitchen](https://github.com/LightwheelAI/Lightwheel_Kitchen) — 该项目提供了一个由 Lightwheel 设计的完整厨房场景，专为在 Isaac Sim 中进行仿真与交互而构建。场景支持具身智能（embodied AI）任务，包含高保真环境资产和物理交互配置，可直接加载到 Isaac Sim 中用于机器人操作、任务规划等研究。目标用户为使用 Isaac Sim 开发家庭服务机器人或具身智能算法的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/LightwheelAI/Lightwheel_Kitchen?style=social)

- [synthetic_data_generation_training_workflow](https://github.com/NVIDIA-AI-IOT/synthetic_data_generation_training_workflow) — 该项目提供了一个端到端的工作流，用于在 Isaac Sim 中生成合成数据并训练计算机视觉模型，特别聚焦于仓储场景下的物体检测任务。它利用 Omniverse 和 Isaac Sim 构建逼真仿真环境，结合 ROS 2 接口与 Jetson 部署支持，实现从数据生成、标注到模型微调和迁移学习的完整流程。目标用户为需要高效构建机器人感知系统的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/NVIDIA-AI-IOT/synthetic_data_generation_training_workflow?style=social)

- [SpdrBot](https://github.com/Indystrycc/SpdrBot) — 该项目使用NVIDIA Isaac Sim和Isaac Lab对四足蜘蛛机器人SpdrBot进行仿真，提供了完整的机器人建模、控制策略和强化学习训练流程。项目基于Isaac Lab框架构建环境，利用其GPU加速的物理仿真能力实现高效训练，并包含URDF模型与任务配置。主要面向希望在Isaac Sim生态中开发或研究四足机器人控制算法的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/Indystrycc/SpdrBot?style=social)

- [SWAGGER](https://github.com/nvidia-isaac/SWAGGER) — SWAGGER 是一个用于高效路径规划的稀疏路点图生成工具，主要面向机器人导航与运动控制。该项目由 NVIDIA Isaac 团队开发，明确支持在 Isaac Sim 中进行仿真集成，利用其 GPU 加速的物理和传感器模拟能力验证路径规划算法。核心技术基于 Python 实现，适用于需要在复杂环境中进行实时导航的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/nvidia-isaac/SWAGGER?style=social)

- [WBC-AGILE](https://github.com/nvidia-isaac/WBC-AGILE) — 该项目提供面向人形机器人的全身控制（WBC）框架AGILE，专为在Isaac Sim中实现高动态运动而设计。它利用Isaac Sim的GPU加速物理仿真能力，结合优化控制算法，支持复杂地形上的实时平衡与步态生成。目标用户为从事人形机器人运动控制研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/nvidia-isaac/WBC-AGILE?style=social)

- [COMPASS](https://github.com/NVlabs/COMPASS) — COMPASS 是一个基于残差强化学习与技能合成的跨具身移动策略框架，主要用于训练通用机器人导航策略。该项目明确支持在 Isaac Sim 中进行仿真训练和部署，利用其 GPU 加速的多物理引擎实现高保真环境交互，并提供与 Isaac Lab 的集成接口。目标用户为从事具身智能与自主导航研究的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/NVlabs/COMPASS?style=social)

- [bipedal_locomotion_isaaclab](https://github.com/Andy-xiong6/bipedal_locomotion_isaaclab) — 该项目为双足机器人在 Isaac Lab 中提供了一系列强化学习驱动的运动控制任务，包括站立、行走和奔跑等基础及进阶动作。它基于 Isaac Lab 框架构建，利用其 GPU 加速的物理仿真与 RL 训练能力，实现了高效、可扩展的双足运动策略开发。项目包含完整的任务定义、奖励函数设计和训练脚本，适合从事人形或双足机器人仿真的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/Andy-xiong6/bipedal_locomotion_isaaclab?style=social)

- [robotis_lab](https://github.com/ROBOTIS-GIT/robotis_lab) — 该项目提供基于ROBOTIS机器人的强化学习与模仿学习教程，并支持Sim2Real策略部署。明确集成Isaac Lab和Isaac Sim作为核心仿真平台，利用其GPU加速物理引擎和传感器模拟功能，实现从仿真训练到真实机器人迁移的完整流程。目标用户为使用NVIDIA Isaac生态进行机器人学习研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/ROBOTIS-GIT/robotis_lab?style=social)

- [nav-suite](https://github.com/leggedrobotics/nav-suite) — 该项目是专为 Isaac Lab 设计的导航套件，提供用于足式机器人在复杂环境中实现自主导航的模块化工具链。它深度集成 Isaac Sim 的传感器仿真与物理引擎，支持基于 ROS 2 的导航栈部署，并利用 GPU 加速实现高保真环境感知与路径规划。主要面向使用 Isaac Lab 进行四足或双足机器人导航算法开发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/leggedrobotics/nav-suite?style=social)

- [go2_isaac_ros2](https://github.com/CLeARoboticsLab/go2_isaac_ros2) — 该项目在Isaac Sim中实现Unitree Go2四足机器人的仿真，通过ROS 2接口进行底层关节控制。它利用Isaac Sim的PhysX物理引擎和ROS 2通信框架，构建了机器人状态发布与命令订阅的闭环控制链路。适用于希望在Isaac Sim中开发或测试Go2机器人运动控制算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/CLeARoboticsLab/go2_isaac_ros2?style=social)

- [OmniIsaacGymEnvs-DofbotReacher](https://github.com/j3soon/OmniIsaacGymEnvs-DofbotReacher) — 该项目为Dofbot机械臂提供了一个基于强化学习的Reacher任务环境，专为NVIDIA Omniverse Isaac Gym/Sim设计，支持Sim2Real迁移。它利用Isaac Sim的GPU加速物理仿真能力，构建了可直接用于训练和部署的机器人控制环境，并包含与真实Dofbot硬件对接的接口。目标用户是从事机器人强化学习研究与Sim2Real应用开发的工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/j3soon/OmniIsaacGymEnvs-DofbotReacher?style=social)

- [robo_imitate](https://github.com/MarijaGolubovic/robo_imitate) — 该项目基于生成式扩散模型实现端到端机器人控制，利用 Isaac Sim 进行高保真仿真环境下的数据生成与策略训练。通过模仿学习从遥操作数据中学习控制策略，并集成 ROS 2 实现真实机器人部署。项目明确使用 Isaac Sim 作为核心仿真平台，适用于希望在 GPU 加速物理仿真中开发学习型机器人控制算法的研究人员。 ![GitHub stars](https://img.shields.io/github/stars/MarijaGolubovic/robo_imitate?style=social)

- [TabletopGen](https://github.com/D-Robotics-AI-Lab/TabletopGen) — TabletopGen 是一个支持从文本或单张图像生成实例级可交互3D桌面场景的工具，主要用于机器人操作任务的仿真环境构建。项目明确支持导出至 Isaac Sim，并提供与 Isaac Sim 兼容的 USD 格式场景和物理属性配置，便于在 NVIDIA 的 GPU 加速仿真平台中进行机器人感知与操作训练。其核心技术基于扩散模型与3D重建，目标用户为从事具身智能和桌面操作仿真的研究人员。 ![GitHub stars](https://img.shields.io/github/stars/D-Robotics-AI-Lab/TabletopGen?style=social)

- [bcr_arm](https://github.com/blackcoffeerobotics/bcr_arm) — bcr_arm 是一个7自由度机械臂的仿真项目，集成了 ROS2 Control 和 MoveIt2 进行运动规划，并明确支持 NVIDIA Isaac Sim 作为仿真后端之一。项目同时兼容 Gazebo（GZ Fortress/Harmonic）和多个 ROS2 版本（Humble/Jazzy），通过统一接口实现跨仿真平台部署。其 Isaac Sim 支持使开发者能在 GPU 加速的多物理场环境中测试机器人控制与规划算法，适用于 ROS2 机器人开发人员和 Isaac Sim 用户。 ![GitHub stars](https://img.shields.io/github/stars/blackcoffeerobotics/bcr_arm?style=social)

- [LearningHumanoidArmMotion-RAL2025-Code](https://github.com/hojae-io/LearningHumanoidArmMotion-RAL2025-Code) — 该项目为 RA-L 2025 论文《Learning Humanoid Arm Motion》提供开源实现，主要用途是学习和生成人形机器人手臂运动策略。代码基于 Isaac Sim 构建仿真环境，利用其 GPU 加速的物理引擎进行高保真动作训练与验证，并集成 RL 框架实现端到端策略学习。目标用户为从事人形机器人运动控制与强化学习研究的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/hojae-io/LearningHumanoidArmMotion-RAL2025-Code?style=social)

- [urdf-importer-extension](https://github.com/isaac-sim/urdf-importer-extension) — 该项目是一个专为 Isaac Sim 开发的 URDF 导入器扩展，用于将机器人 URDF 文件高效加载到 Isaac Sim 场景中。它基于 C++ 实现，利用 Omniverse Kit 的底层 API 与 PhysX 物理引擎深度集成，支持关节、连杆、碰撞体和视觉网格的自动解析与实例化。主要面向使用 Isaac Sim 进行机器人仿真与强化学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/urdf-importer-extension?style=social)

- [IsaacLabEvalTasks](https://github.com/isaac-sim/IsaacLabEvalTasks) — 该项目用于在 Isaac Lab 中对 GR00T N1 策略进行基准测试，提供标准化的评估任务和环境配置。它直接基于 Isaac Lab 构建，利用其 GPU 加速的物理仿真和机器人学习框架，实现高效、可复现的策略评估。目标用户为使用 Isaac Sim/Isaac Lab 进行具身智能与机器人策略研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/IsaacLabEvalTasks?style=social)

- [PhysRL](https://github.com/benjaminegger/PhysRL) — PhysRL 是一个高性能强化学习研究框架，专为利用 NVIDIA Isaac Gym 物理仿真引擎而设计。它通过紧密集成 Isaac Gym 的 GPU 加速并行仿真能力，实现高效的策略训练与环境交互，采用 Python 编写并优化了数据流水线和训练循环。该框架主要面向机器人控制和物理交互任务的强化学习研究人员。 ![GitHub stars](https://img.shields.io/github/stars/benjaminegger/PhysRL?style=social)

- [VolleyBots](https://github.com/thu-uav/VolleyBots) — VolleyBots 是一个用于多无人机排球对抗的测试平台，结合了运动控制与策略决策。项目基于 Isaac Sim 构建高保真物理仿真环境，利用其 GPU 加速的多智能体动力学模拟能力实现无人机集群的实时交互与训练。该框架为研究复杂动态环境中多机器人协同与博弈提供了可扩展的 Isaac Sim 集成方案，适用于机器人学习与自主系统研究人员。 ![GitHub stars](https://img.shields.io/github/stars/thu-uav/VolleyBots?style=social)

- [relic](https://github.com/bdaiinstitute/relic) — 该项目为论文《Versatile Loco-Manipulation through Flexible Interlimb Coordination》提供补充代码，主要实现四足机器人在Isaac Sim中的loco-manipulation仿真环境与控制策略。其核心基于Isaac Sim构建高保真物理模拟，并利用GPU加速实现多肢体协调任务训练。目标用户为研究腿臂协同操作的机器人学习研究者。 ![GitHub stars](https://img.shields.io/github/stars/bdaiinstitute/relic?style=social)

- [LocoTouch](https://github.com/linchangyi1/LocoTouch) — LocoTouch 是一个面向四足机器人动态运输任务的感知学习框架，专为 Isaac Lab 环境开发，利用触觉传感提升运动控制性能。项目基于 Isaac Sim 的物理仿真与传感器模拟能力，在 Isaac Lab 中实现端到端强化学习训练，并集成高保真触觉反馈机制。该仓库为研究具身智能与多模态感知在腿式机器人中的应用提供了可复现的基准，适用于机器人学习研究人员。 ![GitHub stars](https://img.shields.io/github/stars/linchangyi1/LocoTouch?style=social)

- [sru-navigation-sim](https://github.com/leggedrobotics/sru-navigation-sim) — 该项目是为Isaac Lab开发的SRU强化学习导航扩展，主要用于在Isaac Sim环境中训练和测试腿式机器人或移动平台的自主导航策略。它基于Isaac Lab框架构建，利用其GPU加速的物理仿真和RL训练能力，集成了传感器模拟、任务定义和奖励函数等模块。目标用户为从事机器人导航研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/leggedrobotics/sru-navigation-sim?style=social)

- [collab-sim](https://github.com/NVlabs/collab-sim) — 该项目是一个用于模型预测控制（MPC）与VR遥操作的研究工具包，专为Isaac Sim和cuRobo集成而设计。它利用Isaac Sim的高保真物理仿真能力与cuRobo的GPU加速运动规划，实现低延迟、高精度的远程机器人操控。主要面向机器人学习与人机协作领域的研究人员。 ![GitHub stars](https://img.shields.io/github/stars/NVlabs/collab-sim?style=social)

- [isaac-auv-env](https://github.com/warplab/isaac-auv-env) — 该项目为IsaacLab构建了一个基于WarpAUV/CUREE的强化学习环境，专为ICRA 2025发布设计，利用Isaac Sim的GPU加速物理仿真能力实现水下自主航行器（AUV）的高保真训练。它直接集成Isaac Lab框架，使用Python开发，支持Warp驱动的多体动力学与传感器模拟。目标用户为从事水下机器人强化学习研究的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/warplab/isaac-auv-env?style=social)

- [IsaacLab-Quadruped-Tasks](https://github.com/felipemohr/IsaacLab-Quadruped-Tasks) — 该项目基于 Isaac Lab 构建四足机器人任务扩展，提供针对四足机器人的强化学习训练环境和任务配置。它直接利用 Isaac Lab 的框架结构，实现了如站立、行走等典型四足控制任务，并支持与 Isaac Sim 的物理仿真后端集成。适用于希望在 Isaac Sim 生态中快速开发和测试四足机器人策略的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/felipemohr/IsaacLab-Quadruped-Tasks?style=social)

- [basic-locomotion-dls-isaaclab](https://github.com/iit-DLSLab/basic-locomotion-dls-isaaclab) — 该项目是一个基于 Isaac Lab 的扩展，专为多款四足机器人提供基础运动控制任务支持，包含从仿真到仿真（sim-to-sim）及仿真到现实（sim-to-real）的完整迁移流程，并集成多种强化学习优化技巧。其核心功能紧密依赖 Isaac Lab 的物理仿真与 RL 训练框架，适用于希望在 Isaac Sim 生态中快速开发和部署四足机器人运动策略的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/iit-DLSLab/basic-locomotion-dls-isaaclab?style=social)

- [PolySim](https://github.com/EmboMaster/PolySim) — PolySim 旨在通过多仿真器动力学随机化缩小人形机器人控制的仿真到现实差距，明确支持在 Isaac Sim 中进行训练和部署。项目利用 Isaac Sim 的 GPU 加速物理引擎与域随机化技术，结合其他仿真平台实现跨仿真器策略迁移。其核心方法包括动态参数扰动和多仿真一致性优化，主要面向人形机器人控制研究者与 Isaac Sim 开发者。 ![GitHub stars](https://img.shields.io/github/stars/EmboMaster/PolySim?style=social)

- [IsaacLabTutorial](https://github.com/isaac-sim/IsaacLabTutorial) — 该项目是 Isaac Lab 的官方配套教程，提供基于 Python 的示例代码和文档，帮助用户快速上手 Isaac Sim 中的机器人仿真与强化学习训练。内容涵盖环境搭建、传感器配置、物理交互及策略训练等核心功能，紧密集成 Isaac Sim 和 Isaac Gym 的底层接口。主要面向希望利用 NVIDIA Isaac 平台开发 AI 驱动机器人的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/IsaacLabTutorial?style=social)

- [GBC](https://github.com/sjtu-mvasl-robotics/GBC) — GBC 是一个面向全身人形机器人模仿学习的通用行为克隆框架，明确支持在 Isaac Sim 中进行高保真仿真训练与部署。项目利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟能力，实现从人类动作捕捉数据到机器人全身控制策略的端到端学习。其核心基于 PyTorch 和 Isaac Sim 的 Python API 构建，适用于人形机器人研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/sjtu-mvasl-robotics/GBC?style=social)

- [RC2026_SIM](https://github.com/Kuriharamio/RC2026_SIM) — 该项目为 ROBOCON2026 提供基于 Isaac Lab 的专用仿真环境，集成重庆邮电大学 HXC 战队的 3D 机器人模型，支持在 Isaac Sim 中进行机器人控制算法开发与任务测试。利用 Isaac Lab 的 GPU 加速物理仿真能力，实现高保真、高性能的竞赛场景模拟，适用于参赛队伍快速迭代和验证策略。 ![GitHub stars](https://img.shields.io/github/stars/Kuriharamio/RC2026_SIM?style=social)

- [nlp-pnp-robotic-arm](https://github.com/sahilrajpurkar03/nlp-pnp-robotic-arm) — 该项目是一个基于ROS2 Humble的智能抓取放置系统SPARC，集成了MoveIt、YOLOv8-OBB和Isaac Sim，支持Franka Panda与UR5机械臂的实时物体检测、运动规划及自然语言控制。其通过Ollama驱动的聊天机器人实现人机交互，并在Isaac Sim中进行仿真验证，利用GPU加速物理模拟提升训练效率。适用于希望结合大语言模型与Isaac Sim进行机器人操作研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/sahilrajpurkar03/nlp-pnp-robotic-arm?style=social)

- [the-bimo-project](https://github.com/mekion/the-bimo-project) — Bimo 是一个开源双足机器人平台，提供 Python API 并支持全 3D 打印，其核心亮点是包含基于 Isaac Lab 的仿真环境实现，并已验证 sim-to-real 迁移能力。项目通过 Isaac Lab 构建训练和测试场景，利用 GPU 加速物理仿真进行策略开发，最终部署到真实硬件。该平台面向希望在 Isaac Sim 生态中研究双足运动控制与迁移学习的机器人开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/mekion/the-bimo-project?style=social)

- [torobo_isaac_lab](https://github.com/TokyoRobotics/torobo_isaac_lab) — 该项目提供了基于 Isaac Lab 的 Torobo 机器人强化学习示例，利用 Isaac Sim 的 GPU 加速物理仿真能力，实现高性能机器人控制策略训练。项目直接构建于 Isaac Lab 框架之上，包含针对 Torobo 机械臂的环境配置、任务定义和训练脚本，采用 Python 实现并与 Isaac Sim 的传感器、执行器和物理引擎深度集成。适用于希望在 Isaac Sim 生态中开发或测试机器人强化学习算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/TokyoRobotics/torobo_isaac_lab?style=social)

- [SynTable](https://github.com/ngzhili/SynTable) — SynTable 是一个用于生成杂乱桌面场景中未见物体的全模态实例分割合成数据的流水线，明确利用 NVIDIA Isaac Sim 进行高保真渲染与相机采样。项目通过 Isaac Sim 的 PhysX 物理引擎和 RTX 渲染器实现逼真的物体遮挡、材质和光照效果，支持机器人抓取与感知任务。目标用户为从事机器人视觉、合成数据生成及遮挡感知研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/ngzhili/SynTable?style=social)

- [isaac_sim_motion_generator](https://github.com/Auromix/isaac_sim_motion_generator) — 该项目提供了一个基于 cuRobo 的运动生成功能框架，专为 Isaac Sim 设计，支持正向/逆向运动学计算与轨迹生成。它深度集成 Isaac Sim 环境，利用 CUDA 加速实现实时机器人运动规划，适用于需要在仿真与真实机器人之间无缝迁移的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Auromix/isaac_sim_motion_generator?style=social)

- [tbai_isaac](https://github.com/tbai-lab/tbai_isaac) — 该项目旨在提升仿人机器人的运动智能，基于 Isaac Sim 构建高保真仿真环境，用于训练和测试动态行走与敏捷动作策略。它利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能，结合强化学习算法实现复杂地形下的实时运动控制。主要面向机器人学习与仿人运动控制领域的研究人员。 ![GitHub stars](https://img.shields.io/github/stars/tbai-lab/tbai_isaac?style=social)

- [ReasonNav](https://github.com/ReasonNav/ReasonNav) — ReasonNav 是一个实现类人导航的智能体系统，主要面向真实人类环境中的具身推理任务。该项目基于 NVIDIA Isaac Sim 构建仿真环境，利用其 GPU 加速的多物理场模拟能力进行导航策略训练与评估。项目集成了 Isaac Sim 的传感器模拟和场景交互功能，目标用户为机器人导航与具身 AI 领域的研究人员。 ![GitHub stars](https://img.shields.io/github/stars/ReasonNav/ReasonNav?style=social)

- [rl-vs-gc](https://github.com/PratikKunapuli/rl-vs-gc) — 该项目复现并对比经典控制器与强化学习控制器在四旋翼轨迹跟踪任务中的性能，主要基于 Isaac Sim 构建高保真仿真环境，并利用其 GPU 加速物理引擎进行大规模策略评估。代码集成了 Isaac Sim 的 Python API 实现传感器模拟与动力学仿真，为机器人控制研究者提供可复现的基准平台。 ![GitHub stars](https://img.shields.io/github/stars/PratikKunapuli/rl-vs-gc?style=social)

- [sage](https://github.com/isaac-sim2real/sage) — SAGE 是一个用于量化机器人关节运动中仿真到现实（sim-to-real）差距的框架，明确支持 Isaac Sim 进行物理仿真，并结合真实硬件数据与统计分析。项目通过在 Isaac Sim 中模拟多种人形机器人关节行为，与实机采集数据对比，帮助研究人员识别和缩小仿真偏差。其核心功能包括 Isaac Sim 仿真集成、多机器人支持及自动化评估流程，主要面向机器人学习与 sim-to-real 迁移领域的开发者和研究者。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim2real/sage?style=social)

- [gearboxAssembly](https://github.com/rocochallenge/gearboxAssembly) — 该项目基于 Isaac Lab 构建，用于在 Galaxea R1 机器人平台上模拟齿轮箱装配任务。它利用 Isaac Lab 的强化学习和物理仿真能力，提供完整的任务环境、奖励函数和训练脚本，支持策略训练与评估。目标用户为从事机器人操作、强化学习或工业自动化研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/rocochallenge/gearboxAssembly?style=social)

- [LEAP_Hand_Isaac_Lab](https://github.com/leap-hand/LEAP_Hand_Isaac_Lab) — 该项目为LEAP Hand V1灵巧手在Isaac Lab中的官方支持仓库，提供了完整的机器人模型、控制器和任务配置，专为在Isaac Sim环境中进行灵巧操作仿真与强化学习训练而设计。它基于Isaac Lab框架构建，利用其GPU加速的物理仿真和传感器模拟能力，实现高保真手部交互。目标用户为从事灵巧手控制、触觉感知和具身智能研究的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/leap-hand/LEAP_Hand_Isaac_Lab?style=social)

- [isaaclab_door_open](https://github.com/soom1017/isaaclab_door_open) — 该项目是一个基于 Isaac Lab 的移动操作扩展模板，专注于门开启任务，提供了完整的任务配置、奖励函数和场景搭建。它直接利用 Isaac Lab 的强化学习框架和 PhysX 物理引擎，实现了机械臂与移动底盘协同操作的仿真环境。目标用户为研究移动操作或人机交互的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/soom1017/isaaclab_door_open?style=social)

- [isaac_sim_ws](https://github.com/flexivrobotics/isaac_sim_ws) — 该项目将 Flexiv 机器人集成到 Isaac Sim 中，支持通过 Flexiv Elements Studio 或 RDK 进行控制，并复用真实机器人上的力/力矩控制器。它利用 Isaac Sim 的 USD 和 PhysX 引擎实现高保真仿真，使用户能在虚拟环境中测试与实际硬件一致的控制策略。主要面向使用 Flexiv 机械臂并希望在 Isaac Sim 中进行算法开发和验证的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/flexivrobotics/isaac_sim_ws?style=social)

- [isaaclab_ur_reach_sim2real](https://github.com/louislelay/isaaclab_ur_reach_sim2real) — 该项目提供了一个ROS2控制器，用于UR机械臂执行sim-to-real抓取任务，直接利用Isaac Lab中训练好的策略模型。它通过ROS2接口将Isaac Lab的强化学习策略部署到真实UR10机器人上，实现了从仿真到现实的迁移。关键技术包括Isaac Lab策略集成、ROS2通信及UR驱动适配，适用于希望在真实机器人上验证Isaac Lab训练成果的研究者和工程师。 ![GitHub stars](https://img.shields.io/github/stars/louislelay/isaaclab_ur_reach_sim2real?style=social)

- [int-ball2_isaac_sim](https://github.com/open-space-robotics/int-ball2_isaac_sim) — 该项目是专为国际空间站（ISS）设计的Int-Ball2球形无人机在Isaac Sim中的高保真仿真环境，基于NVIDIA Isaac Sim构建，支持ROS/Space ROS接口，用于空间机器人算法的开发与测试。它利用Isaac Sim的GPU加速多物理场模拟能力，复现微重力条件下的飞行动力学，并提供传感器和控制模块的虚拟集成。主要面向空间机器人研究者和航天任务开发者。 ![GitHub stars](https://img.shields.io/github/stars/open-space-robotics/int-ball2_isaac_sim?style=social)

- [zed-isaac-sim](https://github.com/stereolabs/zed-isaac-sim) — 该项目为ZED SDK提供NVIDIA Isaac Sim集成，通过Omniverse Kit扩展将Stereo Labs的ZED相机功能引入Isaac Sim仿真环境。它支持在Isaac Sim中直接使用ZED相机的深度、RGB和姿态数据，便于开发和测试基于真实感视觉输入的机器人感知算法。目标用户为需要在Isaac Sim中集成ZED相机进行机器人仿真与AI训练的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/stereolabs/zed-isaac-sim?style=social)

- [LabUtopia](https://github.com/Rui-li023/LabUtopia) — LabUtopia 是一个面向科学具身智能体的高保真仿真与分层基准平台，明确支持 Isaac Sim 作为其核心仿真引擎之一，利用其 GPU 加速的多物理场模拟能力构建复杂实验环境。项目通过 Isaac Sim 实现高精度传感器模拟和动态交互，为科研人员提供可扩展的机器人任务基准。 ![GitHub stars](https://img.shields.io/github/stars/Rui-li023/LabUtopia?style=social)

- [Matterix](https://github.com/AccelerationConsortium/Matterix) — Matterix 是一个面向机器人辅助化学实验自动化的数字孪生平台，明确支持 Isaac Sim 和 Isaac Lab，用于构建高保真化学实验室仿真环境。项目集成了液体、粉末等粒子物理模拟，并结合语义引擎与状态机实现复杂实验工作流建模，支持 sim2real 迁移。其目标用户为材料科学与自动化化学领域的研究人员及开发者。 ![GitHub stars](https://img.shields.io/github/stars/AccelerationConsortium/Matterix?style=social)

- [foxglove-isaac-sim](https://github.com/foxglove/foxglove-isaac-sim) — 该项目是一个Isaac Sim扩展，用于将Isaac Sim中的仿真数据实时连接到Foxglove可视化平台。它通过Omniverse Kit Extension机制实现，支持发布传感器数据、机器人状态等话题至Foxglove，便于远程监控与调试。主要面向使用Isaac Sim进行机器人开发并希望利用Foxglove进行高效数据可视化的工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/foxglove/foxglove-isaac-sim?style=social)

- [rebot](https://github.com/yuffish/rebot) — ReBot 是一个用于机器人学习的框架，通过真实-仿真-真实（real-to-sim-to-real）的视频合成方法扩展数据规模。项目明确将 Isaac Sim 作为其核心仿真平台，利用其 GPU 加速的多物理场模拟能力生成高保真合成视频，并实现策略迁移。该工具面向希望利用 Isaac Sim 进行大规模机器人视觉策略训练的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/yuffish/rebot?style=social)

- [isaacsim_typings](https://github.com/work-r-labs/isaacsim_typings) — 该项目为 Isaac Sim 4.5 提供 VSCode 和 Cursor 编辑器的智能提示（IntelliSense）与 AI 上下文支持，通过类型定义文件（typings）增强开发体验。它专门针对 Isaac Sim 的 Python API 进行类型注解，提升代码自动补全、错误检查和文档提示能力。目标用户是使用 Isaac Sim 进行机器人仿真与 AI 开发的工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/work-r-labs/isaacsim_typings?style=social)

- [himloco_lab](https://github.com/IsaacZH/himloco_lab) — 该项目用于在 Isaac Lab 环境中训练、导出和部署 HimLoco 强化学习策略，专为 Unitree Go2 四足机器人设计。它深度集成 Isaac Lab 的仿真与训练框架，利用其 GPU 加速的物理引擎和 RL 工具链实现高效策略开发。目标用户为基于 Isaac Sim 生态进行四足机器人控制研究的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/IsaacZH/himloco_lab?style=social)

- [Isaac_Lab_UR5e_Peg_in_Hole](https://github.com/JonasFano/Isaac_Lab_UR5e_Peg_in_Hole) — 该项目利用强化学习在 Isaac Lab 中控制 UR5e 机械臂完成高精度的插孔（peg-in-hole）任务，采用微分逆运动学（differential IK）进行末端执行器控制，并结合域随机化提升策略泛化能力。项目基于 Isaac Sim 的底层物理引擎和机器人仿真框架构建，专为研究精密装配任务的 AI 训练而设计，适用于机器人学习研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/JonasFano/Isaac_Lab_UR5e_Peg_in_Hole?style=social)

- [isaac_ros_nitros_bridge](https://github.com/NVIDIA-ISAAC-ROS/isaac_ros_nitros_bridge) — 该项目提供了一个基于NITROS加速的ROS 2桥接工具，用于在Isaac ROS与标准ROS 2节点间高效传输数据。它通过零拷贝内存共享和GPU加速优化通信性能，专为Isaac Sim及Isaac ROS生态设计，显著提升机器人感知与控制流水线的实时性。主要面向使用Isaac Sim进行仿真并部署到ROS 2系统的开发者。 ![GitHub stars](https://img.shields.io/github/stars/NVIDIA-ISAAC-ROS/isaac_ros_nitros_bridge?style=social)

- [UR5-Object-Alignment](https://github.com/sahilrajpurkar03/UR5-Object-Alignment) — 该项目提供了一个完整的模仿学习流程，用于在NVIDIA Isaac Sim中实现UR5机械臂的杆件对齐任务。它集成了游戏手柄手动采集数据、LeRobot格式的数据集组织、扩散策略训练以及通过ROS2部署策略，充分利用Isaac Sim的高保真仿真环境进行机器人操作学习。目标用户为从事机器人模仿学习与仿真训练的研究者和工程师。 ![GitHub stars](https://img.shields.io/github/stars/sahilrajpurkar03/UR5-Object-Alignment?style=social)

- [cumotion](https://github.com/nvidia-isaac/cumotion) — cuMotion 是一个面向机器人领域的 GPU 加速运动生成库，提供逆运动学、轨迹优化和运动规划等核心功能。该项目由 NVIDIA Isaac 团队开发，明确支持与 Isaac Sim 集成，利用 CUDA 实现高性能并行计算，适用于复杂操作任务的实时运动控制。目标用户为使用 Isaac Sim 进行机器人仿真与算法开发的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/nvidia-isaac/cumotion?style=social)

- [GCR-PPO](https://github.com/humphreymunn/GCR-PPO) — GCR-PPO 是一种面向多目标机器人强化学习的PPO改进算法，通过多头评论家结构计算各奖励项的优势函数，并采用优先级感知的梯度手术（类似PCGrad）保护任务目标免受正则化干扰。该项目专为在 Isaac Lab 环境中与 RSL-RL 框架集成而设计，支持GPU大规模并行训练，适用于需要高效多目标优化的机器人仿真研究者。 ![GitHub stars](https://img.shields.io/github/stars/humphreymunn/GCR-PPO?style=social)

- [Isaac_Lab_UR5e_Lift_Cube_Project_AI](https://github.com/JonasFano/Isaac_Lab_UR5e_Lift_Cube_Project_AI) — 该项目在 Isaac Lab 中实现了基于 Stable-Baselines3 的 PPO、DDPG 和 TD3 强化学习算法，用于训练 UR5e 或 Franka 机械臂完成抓取并提升立方体至目标位姿的任务。支持差分逆运动学（IK）控制和关节位置控制两种策略，代码结构清晰且适配 Isaac Lab 的仿真环境。适用于希望在 Isaac Sim 生态中快速开展机器人操作任务研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/JonasFano/Isaac_Lab_UR5e_Lift_Cube_Project_AI?style=social)

- [Manipulators-simulation-workshop-roscon-es-2024](https://github.com/DarK404/Manipulators-simulation-workshop-roscon-es-2024) — 该项目为 ROSCon ES 2024 提供了使用 NVIDIA Isaac Sim 和 ROS 2 模拟 Universal Robots 机械臂的完整教程与代码资源。它通过 Isaac Sim 的 PhysX 物理引擎和 ROS 2 接口实现高保真机械臂仿真，包含 URDF 加载、控制节点和传感器集成等关键技术。目标用户为希望在 Isaac Sim 中快速上手工业机械臂仿真的 ROS 开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/DarK404/Manipulators-simulation-workshop-roscon-es-2024?style=social)

- [isaac-sim-jetson-hil-course-doc](https://github.com/NVIDIA-AI-IOT/isaac-sim-jetson-hil-course-doc) — 该项目是 NVIDIA 提供的 Isaac Sim 与 Jetson 硬件在环（HIL）实操课程的官方文档站点，专为开发者和研究人员设计，详细指导如何将 Isaac Sim 仿真环境与 Jetson 边缘计算设备集成，实现机器人控制算法的实时测试与验证。内容涵盖 Isaac Sim 的传感器模拟、ROS 2 接口配置及与 Jetson 平台的低延迟通信设置，适用于希望在真实硬件上部署仿真训练成果的机器人工程师。 ![GitHub stars](https://img.shields.io/github/stars/NVIDIA-AI-IOT/isaac-sim-jetson-hil-course-doc?style=social)

- [IsaacLab](https://github.com/Marine-RL/IsaacLab) — 该项目是一个基于 NVIDIA Isaac Sim 构建的统一机器人学习框架，专为强化学习和仿真训练设计。它深度集成 Isaac Sim 的 GPU 加速物理引擎与传感器模拟功能，提供模块化环境、任务配置和训练流程，支持快速开发和部署机器人策略。目标用户为从事机器人强化学习研究与应用的开发者和科研人员。 ![GitHub stars](https://img.shields.io/github/stars/Marine-RL/IsaacLab?style=social)

- [isaac-sim-mini-projects](https://github.com/v-xchen-v/isaac-sim-mini-projects) — 该项目提供一系列轻量级小项目，用于探索 NVIDIA Isaac Sim 中的特定功能或工作流，如场景搭建、机器人控制、操作任务及强化/模仿学习集成。每个示例均聚焦 Isaac Sim 的核心能力，采用模块化设计便于复现和快速原型开发，适合希望高效学习或验证 Isaac Sim 功能的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/v-xchen-v/isaac-sim-mini-projects?style=social)

- [Sim2RealLab](https://github.com/zachoines/Sim2RealLab) — Sim2RealLab 是一个模块化的仿真到现实（sim-to-real）工具包，作为 Isaac Lab 的扩展，提供端到端的资产处理、物理绑定、强化学习环境、域随机化和部署工具，专为移动与多机器人平台的策略训练与迁移设计。项目深度集成 Isaac Lab，利用其 GPU 加速的物理仿真能力，支持高效开发可迁移的机器人控制策略。目标用户为使用 Isaac Sim 生态进行机器人强化学习研究与部署的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/zachoines/Sim2RealLab?style=social)

- [isaac_underwater](https://github.com/leonlime/isaac_underwater) — 该项目专注于在 NVIDIA Isaac Sim 中实现水下环境的物理仿真与测试，利用 Omniverse 平台构建逼真的水体和流体交互场景。通过自定义材质、流体动力学参数及传感器模型，支持水下机器人在 Isaac Sim 中的感知与控制算法验证。目标用户为从事水下机器人研发与仿真的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/leonlime/isaac_underwater?style=social)

- [ArenaSim](https://github.com/EquGamer/ArenaSim) — ArenaSim 是一个基于 Isaac Sim 构建的机器人竞技场模拟框架，主要用于开发和测试多智能体对抗策略。项目深度集成 Isaac Sim 的 GPU 加速物理引擎与传感器仿真能力，利用其 Python API 实现自定义环境和智能体交互逻辑。目标用户为研究多智能体强化学习与机器人博弈算法的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/EquGamer/ArenaSim?style=social)

- [ur5_isaac_simulation](https://github.com/caiobarrosv/ur5_isaac_simulation) — 该项目提供UR5机械臂在Isaac Sim中的仿真环境，基于Python构建，利用Isaac Sim的PhysX物理引擎和ROS 2接口实现高保真机器人控制与感知模拟。项目包含URDF模型加载、关节控制及传感器集成，适用于需要在Isaac Sim中开发和测试UR5操作任务的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/caiobarrosv/ur5_isaac_simulation?style=social)

- [RL-Navigation](https://github.com/sahars93/RL-Navigation) — 该项目基于 OmniIsaacGymEnvs 扩展，利用2D LiDAR数据在Isaac Sim中实现移动机器人导航的强化学习训练。它直接复用并修改了NVIDIA官方Isaac Gym环境，构建了面向导航任务的自定义RL场景，支持GPU加速的并行仿真。主要面向希望在Isaac Sim生态中研究基于LiDAR的自主导航算法的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/sahars93/RL-Navigation?style=social)

- [isaac_manager](https://github.com/KyleM73/isaac_manager) — isaac_manager 是一个简化 Isaac Sim 开发环境配置与管理的工具，通过 Makefile 脚本自动化处理依赖安装、容器构建和仿真启动等流程。该项目专为 Isaac Sim 用户设计，提供一键式工作流以降低使用门槛，特别适合需要频繁切换或部署 Isaac Sim 环境的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/KyleM73/isaac_manager?style=social)

- [TactSim-IsaacLab](https://github.com/yuanqing-ai/TactSim-IsaacLab) — 该项目基于 Isaac Lab 构建，专注于触觉感知的机器人仿真，利用 Isaac Sim 的 GPU 加速物理引擎实现高保真触觉传感器模拟。它集成了自定义触觉渲染模块，并支持与 Isaac Lab 的任务框架和 RL 训练流程无缝对接。主要面向从事具身智能与触觉交互研究的科研人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/yuanqing-ai/TactSim-IsaacLab?style=social)

- [GRADE-RR](https://github.com/eliabntt/GRADE-RR) — GRADE-RR 是一个用于生成逼真动态机器人仿真环境的框架，专门面向 Isaac Sim 平台构建，支持在 Omniverse 中创建包含动态人类和动物行为的复杂场景。项目利用 Isaac Sim 的 GPU 加速物理与渲染能力，结合 ROS 集成，实现高保真数据生成，适用于需要动态交互环境的机器人研究。目标用户为使用 Isaac Sim 进行具身智能或人机交互研究的科研人员。 ![GitHub stars](https://img.shields.io/github/stars/eliabntt/GRADE-RR?style=social)

- [Safe-Multi-Agent-Isaac-Gym](https://github.com/chauncygu/Safe-Multi-Agent-Isaac-Gym) — 该项目提供了一个面向安全多智能体强化学习研究的基准测试平台，基于Isaac Gym构建，实现了多个具有安全约束的多机器人协作与竞争任务。它利用Isaac Gym的GPU加速物理仿真能力，支持高效并行训练，并集成了安全策略评估指标。主要面向从事安全强化学习与多智能体系统研究的科研人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/chauncygu/Safe-Multi-Agent-Isaac-Gym?style=social)

- [piper_isaac_sim](https://github.com/agilexrobotics/piper_isaac_sim) — 该项目为 AgileX Robotics 的 Piper 机器人提供 Isaac Sim 仿真支持，包含在 Isaac Sim 中运行该机器人的 URDF 模型、传感器配置及控制接口。通过集成 Isaac Sim 的 PhysX 物理引擎和 ROS 2 工具链，实现高保真运动仿真与算法验证。主要面向使用 Isaac Sim 开发四足机器人应用的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/agilexrobotics/piper_isaac_sim?style=social)

- [AdaVLN](https://github.com/dillonloh/AdaVLN) — 该项目为 Isaac Sim 开发了一个扩展插件，用于在 Matterport3D 环境中动态添加和控制交互对象，支持 AdaVLN（Adaptive Vision-and-Language Navigation）研究。它通过 Isaac Sim 的 API 实现物理逼真的动态物体行为，并与视觉-语言导航任务集成，使研究人员能在高保真仿真环境中训练和测试智能体。目标用户为从事具身智能、机器人导航及多模态学习的研究人员。 ![GitHub stars](https://img.shields.io/github/stars/dillonloh/AdaVLN?style=social)

- [nvidia-isaac-summary](https://github.com/j3soon/nvidia-isaac-summary) — 该项目是对 NVIDIA Isaac 生态系统的非官方汇总，系统梳理了包括 Isaac Sim、Isaac Gym、Isaac ROS 和 Isaac SDK 等核心组件的功能与关系。它明确涵盖 Isaac Sim 作为关键组成部分，提供架构概览和资源链接，帮助用户快速理解其在机器人仿真与训练中的作用。目标用户为希望入门或整合 Isaac Sim 及相关工具的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/j3soon/nvidia-isaac-summary?style=social)

- [openarm_isaac_lab](https://github.com/enactic/openarm_isaac_lab) — 该项目为 OpenArm 机械臂提供基于 Isaac Lab 的仿真环境，利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能，实现高保真机器人控制与强化学习训练。项目包含 URDF 模型集成、任务配置及与 Isaac Lab 核心 API 的深度适配，支持快速开发和部署机械臂智能控制策略。主要面向使用 Isaac Lab 进行机器人仿真的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/enactic/openarm_isaac_lab?style=social)

- [isaacsim_vla_ws](https://github.com/MyLovelyAxe/isaacsim_vla_ws) — 该项目是一个ROS工作空间，专为在笔记本端部署视觉-语言-动作（VLA）流水线而设计，明确支持与Isaac Sim的集成。它包含ROS包、Bash脚本和配置文件，用于连接Isaac Sim仿真环境并处理感知与控制数据流，基于Python实现。目标用户是希望在Isaac Sim中开发或测试VLA驱动机器人应用的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/MyLovelyAxe/isaacsim_vla_ws?style=social)

- [IsaacSimZMQ](https://github.com/isaac-sim/IsaacSimZMQ) — IsaacSimZMQ 是一个专为 Isaac Sim 开发的扩展插件，通过 ZeroMQ（ZMQ）协议实现仿真环境与外部应用程序的高效通信。该工具利用 Python 编写，支持在 Isaac Sim 运行时实时交换数据，适用于需要与外部控制系统、AI 模型或远程客户端交互的机器人仿真场景。目标用户为使用 Isaac Sim 进行机器人开发与测试的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/IsaacSimZMQ?style=social)

- [lerobot_so101_teleop](https://github.com/liorbenhorin/lerobot_so101_teleop) — 该项目为 LeRobot SO-101 机器人在 Isaac Lab 中提供了一个示例仿真环境，用于通过遥操作收集演示数据。它利用 Isaac Lab 的 GPU 加速物理仿真能力，实现了与 SO-101 机器人的集成，并支持通过键盘或手柄进行实时控制以生成训练数据。主要面向希望在 Isaac Sim 生态中开发模仿学习或行为克隆应用的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/liorbenhorin/lerobot_so101_teleop?style=social)

- [rb_isaac_edu](https://github.com/kimsooyoung/rb_isaac_edu) — 该项目是一个面向教育用途的 Isaac Sim 教程仓库，提供基于 Python 的示例代码和教学材料，帮助初学者快速上手 NVIDIA Isaac Sim 平台。内容涵盖机器人仿真基础、传感器配置及与 Isaac Gym 的集成方法，强调 GPU 加速物理仿真的实践应用。目标用户为高校学生、研究人员及希望学习 Isaac Sim 机器人仿真的开发者。 ![GitHub stars](https://img.shields.io/github/stars/kimsooyoung/rb_isaac_edu?style=social)

- [tools-OmniNxtSimulator](https://github.com/UAV-Swarm/tools-OmniNxtSimulator) — 该项目是一个基于 Isaac Lab 构建的 OmniNxt 无人机群仿真工具，主要用于在 Isaac Sim 环境中模拟多无人机协同任务。它利用 Isaac Lab 的强化学习和物理仿真能力，提供可扩展的 UAV Swarm 训练与测试框架，适用于机器人研究人员和自主系统开发者。 ![GitHub stars](https://img.shields.io/github/stars/UAV-Swarm/tools-OmniNxtSimulator?style=social)

- [robots](https://github.com/work-r-labs/robots) — 该项目提供了一个开源的工业机器人模型库，专为 NVIDIA Isaac Sim 设计，支持以 URDF 格式导入 ABB 等主流厂商的机器人模型，并集成到 Omniverse 平台中。通过与 Isaac Sim 深度兼容，用户可直接在 GPU 加速的多物理仿真环境中进行机器人部署、测试和控制算法开发。目标用户为使用 Isaac Sim 进行工业自动化仿真的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/work-r-labs/robots?style=social)

- [isaac_demo](https://github.com/NVIDIA-AI-IOT/isaac_demo) — 该项目提供了一系列演示示例，用于将 Isaac ROS 与 Isaac Sim 集成，展示如何在 Isaac Sim 的高保真仿真环境中运行基于 ROS 的机器人应用。项目通过 Python 脚本实现传感器数据模拟、机器人控制和可视化，便于开发者快速验证 ROS 节点在 Isaac Sim 中的兼容性与性能。主要面向希望结合 Isaac ROS 和 Isaac Sim 进行机器人算法开发与测试的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/NVIDIA-AI-IOT/isaac_demo?style=social)

- [Sim-Suction-API](https://github.com/junchengli1/Sim-Suction-API) — Sim-Suction-API 提供了一个用于生成机器人吸盘抓取合成数据并训练模型的仿真框架，特别针对杂乱环境中的操作任务。该项目基于 Isaac Sim 构建，利用其 GPU 加速的物理引擎和传感器模拟能力，实现高保真吸盘抓取场景生成。目标用户为从事机器人抓取研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/junchengli1/Sim-Suction-API?style=social)

- [Sim-Grasp](https://github.com/junchengli1/Sim-Grasp) — Sim-Grasp 是一个用于生成合成数据并训练机器人二指抓取模型的仿真框架，专注于杂乱环境中的抓取任务。该项目基于 Isaac Sim 构建，利用其 GPU 加速的物理引擎和传感器模拟能力生成逼真的抓取场景与标注数据。目标用户为从事机器人抓取感知与学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/junchengli1/Sim-Grasp?style=social)

- [nvidia_isaac-sim_ros2_docker](https://github.com/arambarricalvoj/nvidia_isaac-sim_ros2_docker) — 该项目提供了一个预配置的 Docker 容器，用于在隔离环境中运行 NVIDIA Isaac Sim，并集成了 ROS 2 Humble 及 Isaac Sim 与 ROS 2 之间的桥接功能。通过容器化方式简化了 Isaac Sim 与 ROS 2 的联合开发环境搭建，利用 NVIDIA 官方镜像和 ROS 2 bridge 实现传感器数据和控制命令的双向通信。适用于希望快速部署 Isaac Sim 与 ROS 2 集成环境的机器人开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/arambarricalvoj/nvidia_isaac-sim_ros2_docker?style=social)

- [MimicKit_IsaacLab](https://github.com/NathanWu7/MimicKit_IsaacLab) — 该项目为MimicKit提供Isaac Lab支持，使其能够在NVIDIA Isaac Sim的Isaac Lab框架中运行。通过集成Isaac Lab的强化学习和机器人仿真环境，项目实现了对MimicKit行为克隆与模仿学习功能的适配，利用其基于PyTorch和RLlib的架构。主要面向希望在Isaac Sim生态中开展模仿学习研究的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/NathanWu7/MimicKit_IsaacLab?style=social)

- [Tac-Man-Simulation](https://github.com/YuyangLee/Tac-Man-Simulation) — 该项目为论文《Tac-Man: Tactile-Informed Prior-Free Manipulation of Articulated Objects》提供仿真研究支持，主要基于 Isaac Sim 构建触觉感知驱动的铰接物体操作环境。它利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟能力，实现高保真触觉反馈与交互，适用于机器人操作研究社区。 ![GitHub stars](https://img.shields.io/github/stars/YuyangLee/Tac-Man-Simulation?style=social)

- [UrbanVerse](https://github.com/OatmealLiu/UrbanVerse) — UrbanVerse 旨在构建无限规模的物理合理城市仿真环境，通过结合 Isaac Sim 的高保真物理资产与真实世界城市布局，实现可扩展的城市场景模拟。项目明确基于 Isaac Sim 构建，利用其 GPU 加速多物理引擎生成逼真的城市级仿真数据，支持具身智能体在复杂城市场景中的训练与测试。目标用户为从事城市级机器人仿真、自动驾驶或具身 AI 研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/OatmealLiu/UrbanVerse?style=social)

- [gentle-humanoid-training](https://github.com/Axellwppr/gentle-humanoid-training) — 该项目实现了一个全身运动跟踪与柔顺控制的人形机器人训练框架，主要基于Isaac Sim和Isaac Gym构建强化学习环境。它利用GPU加速的物理仿真对人形机器人进行端到端策略训练，支持高保真动力学与接触建模。目标用户为从事人形机器人运动控制与强化学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Axellwppr/gentle-humanoid-training?style=social)

- [intro-to-omniverse-isaac-supp](https://github.com/j3soon/intro-to-omniverse-isaac-supp) — 该项目为题为“Omniverse 与 Isaac 机器人平台入门”的演讲提供补充材料，包含演示代码、配置示例和教程资源，重点展示如何在 Isaac Sim 中构建和仿真机器人场景。内容涵盖 USD 场景搭建、传感器配置及与 Isaac Gym 的集成方法，基于 NVIDIA Omniverse 生态实现 GPU 加速的物理仿真。适合希望快速上手 Isaac Sim 进行机器人开发与 AI 训练的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/j3soon/intro-to-omniverse-isaac-supp?style=social)

- [newton-isaac-sim](https://github.com/TheNewtonCapstone/newton-isaac-sim) — 该项目基于NVIDIA Isaac Sim构建Newton项目的仿真环境，主要用于开发和测试AI驱动的机器人应用。它利用Isaac Sim的GPU加速多物理场仿真能力，提供与Newton平台集成的定制化模拟场景和工具链。目标用户为参与Newton项目或希望在Isaac Sim中部署类似机器人系统的开发者。 ![GitHub stars](https://img.shields.io/github/stars/TheNewtonCapstone/newton-isaac-sim?style=social)

- [Limo-Isaac-Sim](https://github.com/agilexrobotics/Limo-Isaac-Sim) — 该项目为 AgileX Limo 机器人提供 Isaac Sim 仿真支持，通过 Python 脚本实现机器人模型导入、传感器配置（如激光雷达和摄像头）及运动控制接口，利用 Isaac Sim 的 PhysX 物理引擎和 ROS 2 集成功能构建高保真仿真环境。主要面向使用 Limo 机器人进行导航、SLAM 或自主算法开发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/agilexrobotics/Limo-Isaac-Sim?style=social)

- [ETRI-Dual-Hand-Arm-Robot](https://github.com/DonghyungKim/ETRI-Dual-Hand-Arm-Robot) — 该项目提供了ETRI双手机器人的USD文件和ROS2软件包，专为在Isaac Sim中进行操作技能学习而设计。通过与Isaac Sim深度集成，支持GPU加速的多物理仿真，便于开发和训练灵巧操作策略。目标用户为使用Isaac Sim进行人形或双臂机器人 manipulation 研究的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/DonghyungKim/ETRI-Dual-Hand-Arm-Robot?style=social)

- [Reinforcement-Learning-Isaac-Lab-Projects](https://github.com/nicolaloi/Reinforcement-Learning-Isaac-Lab-Projects) — 该项目提供多个基于 Isaac Lab 的强化学习实验环境，专注于无人机和足式机器人等应用场景。通过自定义任务和奖励函数，利用 Isaac Lab 的 GPU 加速物理仿真能力进行高效训练。适合希望在 Isaac Sim 生态中快速开发和测试机器人强化学习算法的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/nicolaloi/Reinforcement-Learning-Isaac-Lab-Projects?style=social)

- [nova_carter_sm_library](https://github.com/robosoft-ai/nova_carter_sm_library) — 该项目提供了一套基于SMACC2状态机的应用程序，专为Isaac Sim中的NOVA Carter机器人设计，集成ROS2、Nav2及Isaac ROS组件，并利用IsaacROSDev容器实现Jetson平台的便捷部署。其核心功能围绕在Isaac Sim环境中构建和运行复杂导航行为，适用于需要在NVIDIA Isaac Sim中开发和测试自主移动机器人行为的开发者。 ![GitHub stars](https://img.shields.io/github/stars/robosoft-ai/nova_carter_sm_library?style=social)

- [i4h-sensor-simulation](https://github.com/isaac-for-healthcare/i4h-sensor-simulation) — 该项目为医疗健康领域提供传感器仿真功能，基于Isaac Sim构建，利用其GPU加速的物理和渲染引擎模拟医疗设备中的各类传感器数据。项目通过Isaac Sim的扩展接口实现高保真传感器建模，支持如内窥镜、超声等医疗场景的虚拟感知测试。主要面向医疗机器人开发者与研究人员，用于在安全可控环境中验证感知算法。 ![GitHub stars](https://img.shields.io/github/stars/isaac-for-healthcare/i4h-sensor-simulation?style=social)

- [zero-to-slam](https://github.com/Caian/zero-to-slam) — 该项目提供了一个容器化的 ROS2 SLAM 与导航解决方案，专为在 NVIDIA Omniverse Isaac Sim 中运行而设计。通过 Docker 封装 ROS2、SLAM 工具链及 Isaac Sim 通信接口，实现开箱即用的机器人建图与定位功能。目标用户为希望在 Isaac Sim 高保真仿真环境中快速部署和测试 SLAM 算法的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/Caian/zero-to-slam?style=social)

- [whole-body-mimic-lab](https://github.com/wenconggan/whole-body-mimic-lab) — 该项目是一个基于 Isaac Sim 的全身动作模仿框架，利用 Isaac Lab 提供的强化学习环境和 PhysX 物理引擎，实现高保真人体运动生成。它通过端到端策略训练虚拟角色复现参考运动数据，支持自定义角色与任务，并深度集成 Isaac Sim 的传感器、资产加载和渲染管线。主要面向机器人学与具身智能研究者，用于开发类人运动控制算法。 ![GitHub stars](https://img.shields.io/github/stars/wenconggan/whole-body-mimic-lab?style=social)

- [UR_Isaac-sim](https://github.com/DarK404/UR_Isaac-sim) — 该项目提供UR3e机器人在Isaac Sim中的仿真配置，结合MoveIt2实现运动规划与控制。通过ROS 2 Humble和ros2-control集成，支持在Isaac Sim环境中测试UR机械臂的轨迹执行与任务仿真。主要面向使用Universal Robots与Isaac Sim进行机器人算法开发的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/DarK404/UR_Isaac-sim?style=social)

- [isaaclab_sim_to_real](https://github.com/XMebius/isaaclab_sim_to_real) — 该项目利用 Isaac Lab 训练四足机器人 Aliengo 在复杂粗糙地形中的运动策略，并实现从仿真到真实机器人的部署。它基于 Isaac Sim 的 GPU 加速物理仿真能力，结合强化学习算法训练鲁棒控制器，关键技术包括域随机化和策略迁移。目标用户为从事四足机器人仿真到现实迁移研究的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/XMebius/isaaclab_sim_to_real?style=social)

- [IsaacRobotics](https://github.com/mschweig/IsaacRobotics) — 该项目提供面向 Isaac Sim 和 Isaac Lab 的机器人应用示例，涵盖强化学习训练、机械臂控制和移动机器人仿真等场景。代码基于 Python 实现，利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能，并与 Isaac Lab 的模块化 RL 框架集成。主要面向希望快速上手 NVIDIA 机器人仿真平台的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/mschweig/IsaacRobotics?style=social)

- [isaac-xr-teleop-sample-client-apple](https://github.com/isaac-sim/isaac-xr-teleop-sample-client-apple) — 该项目是一个基于 Swift 开发的 Apple 平台客户端示例应用，用于通过扩展现实（XR）设备实现对 Isaac Sim 中机器人的远程操作（teleoperation）。它直接与 Isaac Sim 集成，利用其 XR 通信协议实现实时姿态传输与控制指令下发，适用于希望在 iOS 或 visionOS 设备上开发沉浸式机器人遥操作界面的开发者。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/isaac-xr-teleop-sample-client-apple?style=social)

- [isaac-sim-3d-lidar-odometry-mapping](https://github.com/taherfattahi/isaac-sim-3d-lidar-odometry-mapping) — 该项目利用 Nvidia Isaac Sim 与 MOLA 框架实现高精度的 3D LiDAR 里程计与建图功能，通过 ROS 2 接口在 Isaac Sim 仿真环境中生成和处理激光雷达数据。其核心在于将 MOLA 的 SLAM 算法与 Isaac Sim 的高保真传感器仿真深度集成，支持实时位姿估计与地图构建。适用于需要在 Isaac Sim 中开发或验证激光雷达导航算法的机器人研究人员。 ![GitHub stars](https://img.shields.io/github/stars/taherfattahi/isaac-sim-3d-lidar-odometry-mapping?style=social)

- [isaac_ur5](https://github.com/prajapatisarvesh/isaac_ur5) — 该项目在 NVIDIA Isaac Sim 中实现了 UR5 机械臂的仿真模型，并通过 ROS 桥接与 MoveIt 集成，支持运动规划与控制。其利用 Isaac Sim 的 PhysX 物理引擎和 ROS 通信接口，使用户能在高保真 GPU 加速环境中开发和测试 UR5 的机器人应用。适用于希望在 Isaac Sim 中快速部署 UR5 并结合 ROS/MoveIt 进行算法验证的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/prajapatisarvesh/isaac_ur5?style=social)

- [isaac-sim-mobile-robot-rtab-map](https://github.com/taherfattahi/isaac-sim-mobile-robot-rtab-map) — 该项目在NVIDIA Isaac Sim中实现移动机器人SLAM建图与导航，集成RTAB-Map、Navigation2和RViz2，通过ROS 2桥接实现传感器数据同步与实时可视化。利用Isaac Sim的Omniverse环境构建高保真仿真场景，支持激光雷达与深度相机输入，适用于需要GPU加速物理仿真与SLAM算法验证的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/taherfattahi/isaac-sim-mobile-robot-rtab-map?style=social)

- [MT_Isaac_sim](https://github.com/MetaToolEU/MT_Isaac_sim) — 该项目利用 NVIDIA Isaac Sim 构建双臂 Universal Robots 的数字孪生环境，支持实时控制、碰撞检测与路径规划。通过 Isaac Sim 的 GPU 加速物理仿真和机器人 SDK，实现高保真多机械臂协同操作，适用于需要复杂操作任务验证的机器人研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/MetaToolEU/MT_Isaac_sim?style=social)

- [NVIDIA-Isaac-Sim-and-Isaac-ROS-Integration-on-Jetson-Orin-Nano](https://github.com/kabilankb/NVIDIA-Isaac-Sim-and-Isaac-ROS-Integration-on-Jetson-Orin-Nano) — 该项目提供在 Jetson Orin Nano 上集成 NVIDIA Isaac Sim 与 Isaac ROS 的详细指南，基于 JetPack 6 实现高效的 AprilTag 检测与可视化。通过将 Isaac Sim 的仿真能力与 Isaac ROS 的感知模块结合，支持机器人在仿真与真实硬件间无缝衔接。主要面向使用 NVIDIA Jetson 平台开发机器人感知系统的开发者。 ![GitHub stars](https://img.shields.io/github/stars/kabilankb/NVIDIA-Isaac-Sim-and-Isaac-ROS-Integration-on-Jetson-Orin-Nano?style=social)

- [marladona-isaac-lab](https://github.com/leggedrobotics/marladona-isaac-lab) — 该项目是一个基于 Isaac Lab 的外部扩展模板，旨在为用户提供标准化的项目结构和开发框架，便于快速构建与 Isaac Lab 兼容的机器人仿真模块。它封装了 Isaac Lab 的核心接口，支持自定义任务、传感器和控制器的集成，采用 Python 实现并遵循 Isaac Sim 的扩展机制。目标用户为希望在 Isaac Sim 生态中开发可复用、模块化机器人仿真的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/leggedrobotics/marladona-isaac-lab?style=social)

- [RL_Dog](https://github.com/pietrodardano/RL_Dog) — 该项目提供针对四足机器人（如AlienGo和Unitree）的强化学习实现，支持PPO、DDPG和TD3算法，主要用于行走与停止控制。项目明确包含Isaac Lab和Isaac Sim的集成示例，利用SKRL和Stable Baselines3在NVIDIA Isaac Sim环境中训练策略。目标用户为希望在Isaac Sim中开发或测试四足机器人运动控制算法的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/pietrodardano/RL_Dog?style=social)

- [StrideSim](https://github.com/AuTURBO/StrideSim) — StrideSim 是一个基于 NVIDIA Isaac Sim 构建的四足机器人仿真平台，提供高保真物理环境并原生支持 ROS 2 Humble。项目利用 Isaac Sim 的 GPU 加速多物理引擎实现逼真的机器人运动模拟，并通过 ROS 2 接口实现传感器数据发布与控制指令接收。其核心功能紧密集成 Isaac Sim 的渲染与仿真能力，专为四足机器人开发者和研究人员设计。 ![GitHub stars](https://img.shields.io/github/stars/AuTURBO/StrideSim?style=social)

- [IsaacSim-Autonomous-Forklift](https://github.com/iminolee/IsaacSim-Autonomous-Forklift) — 该项目基于 Isaac Sim 构建了一个自主叉车仿真系统，通过集成 ROS 实现仓库环境中的自动导航、托盘检测与精准对接功能。利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟，结合 Python 编写的控制逻辑，支持实时监控与交互。主要面向机器人开发者和物流自动化研究人员，用于测试和验证自主叉车算法。 ![GitHub stars](https://img.shields.io/github/stars/iminolee/IsaacSim-Autonomous-Forklift?style=social)

- [isaacsim_openvla](https://github.com/RiccardoBianco/isaacsim_openvla) — 该项目旨在将 OpenVLA（开源视觉-语言-动作模型）与 NVIDIA Isaac Sim 集成，用于在仿真环境中实现具身智能机器人的感知与控制。通过利用 Isaac Sim 的 GPU 加速物理仿真和传感器模拟能力，项目提供了一个端到端的框架，支持在虚拟环境中训练和部署基于视觉语言模型的机器人策略。主要面向希望在高保真仿真中开发和测试具身 AI 系统的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/RiccardoBianco/isaacsim_openvla?style=social)

- [GenTact](https://github.com/HIRO-group/GenTact) — GenTact 为 Isaac Sim 提供触觉仿真扩展功能，通过自定义传感器模型和物理交互逻辑，实现高保真触觉数据生成。项目基于 Python 开发，紧密集成 Isaac Sim 的传感器与物理引擎接口，支持机器人抓取、操作等任务中的接触力反馈模拟。适用于需要在 Isaac Sim 中进行触觉感知研究或开发的机器人研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/HIRO-group/GenTact?style=social)

- [ogmp_isaac](https://github.com/DRCL-USC/ogmp_isaac) — 该项目实现了面向人形机器人的Oracle引导多模态策略（OGMP），专为Isaac Lab环境开发，利用其GPU加速的物理仿真能力进行复杂动作策略训练。代码基于Isaac Lab构建，直接依赖其任务框架和传感器接口，支持高保真人形机器人控制研究。主要面向使用Isaac Sim/Isaac Lab进行高级机器人学习的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/DRCL-USC/ogmp_isaac?style=social)

- [g1-isaac-groot-n1](https://github.com/Jalil32/g1-isaac-groot-n1) — 该项目旨在微调并部署 NVIDIA 的 Isaac GR00T N1 模型到 Unitree G1 人形机器人，利用 Isaac Sim 提供的仿真环境进行训练与验证。项目通过 Isaac Sim 与 Isaac Lab 集成，实现基于 GPU 加速的物理仿真和策略迁移，支持端到端的机器人行为学习。主要面向希望在真实人形机器人上部署生成式机器人模型的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/Jalil32/g1-isaac-groot-n1?style=social)

- [isaacsim_ros2_drone](https://github.com/SasaKuruppuarachchi/isaacsim_ros2_drone) — 该项目提供了一系列工具，用于简化在Isaac Sim中开发无人机应用的流程，包括与ros2_control的集成、自动传感器生成及传感器数据发布功能。它通过Docker容器化部署，支持ROS 2 Humble，并兼容QGroundControl地面站，便于开发者快速构建和测试基于Isaac Sim的无人机仿真系统。目标用户为使用Isaac Sim进行无人机算法开发与验证的机器人工程师。 ![GitHub stars](https://img.shields.io/github/stars/SasaKuruppuarachchi/isaacsim_ros2_drone?style=social)

- [manager_isaacsim_link](https://github.com/SevenFo/manager_isaacsim_link) — 该项目是一个用于为 Isaac Sim 的 Python 包创建符号链接的工具，通过将 site-packages 目录链接到 Isaac Sim 安装路径，显著提升 VSCode 等 IDE 中的代码自动补全与类型提示能力。它直接针对 Isaac Sim 的模块导入问题提供解决方案，利用操作系统符号链接技术绕过 IDE 对非标准包路径的识别限制。主要面向使用 Isaac Sim 进行机器人仿真开发的 Python 开发者。 ![GitHub stars](https://img.shields.io/github/stars/SevenFo/manager_isaacsim_link?style=social)

- [semu.robotics.ros_bridge](https://github.com/Toni-SM/semu.robotics.ros_bridge) — 该项目是一个专为 NVIDIA Omniverse Isaac Sim 开发的外部扩展，实现了与 ROS（Robot Operating System）的双向通信桥接。它基于 OmniGraph 和 Python 构建，允许用户在 Isaac Sim 中发布和订阅 ROS 消息，从而将仿真环境无缝集成到现有机器人软件栈中。该工具主要面向使用 ROS 生态并希望利用 Isaac Sim 高保真仿真的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/Toni-SM/semu.robotics.ros_bridge?style=social)

- [Go2_Isaac_ros2](https://github.com/sallu-786/Go2_Isaac_ros2) — 该项目实现了Unitree Go2四足机器人的仿真，基于NVIDIA Isaac Lab/Isaac Sim平台，并通过ROS 2接口支持导航等任务。项目利用Isaac Sim的GPU加速物理仿真能力，结合ROS 2通信框架，为机器人算法开发提供闭环测试环境。主要面向使用Isaac Sim进行四足机器人研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/sallu-786/Go2_Isaac_ros2?style=social)

- [OmniIsaacGymEnvs-KukaReacher](https://github.com/j3soon/OmniIsaacGymEnvs-KukaReacher) — 该项目为Kuka KR120机械臂提供了一个基于强化学习的Sim2Real环境，专为NVIDIA Omniverse Isaac Gym/Sim平台构建。它复用了Isaac Gym的API结构，实现了与Isaac Sim深度集成的机器人控制任务，支持GPU加速的并行仿真。目标用户是希望在Isaac Sim中开发或迁移Kuka机械臂强化学习算法的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/j3soon/OmniIsaacGymEnvs-KukaReacher?style=social)

- [BDX-R-IsaacLab](https://github.com/BDX-R/BDX-R-IsaacLab) — 该项目为BDX-R四足机器人在Isaac Lab环境中实现强化学习训练，提供完整的任务配置、奖励函数和运动控制策略。它基于Isaac Sim的GPU加速物理仿真能力，利用Isaac Lab框架构建训练流程，并集成了机器人URDF模型与传感器模拟。主要面向希望在Isaac Sim生态中开发或测试四足机器人RL算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/BDX-R/BDX-R-IsaacLab?style=social)

- [booster_train](https://github.com/BoosterRobotics/booster_train) — 该项目为 Booster 机器人提供了一套基于 Isaac Lab 的强化学习训练任务，利用 Isaac Sim 的 GPU 加速物理仿真能力构建高保真训练环境。通过与 Isaac Lab 框架深度集成，实现了机器人运动控制、感知和决策策略的端到端训练。主要面向使用 NVIDIA Isaac Sim 生态进行机器人强化学习研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/BoosterRobotics/booster_train?style=social)

- [isaac_sim_pointcloud_full_publisher](https://github.com/REGATTE/isaac_sim_pointcloud_full_publisher) — 该项目是一个C++工具，用于在Isaac Sim中完整发布点云数据（PCD格式），通过ROS话题输出全量点云信息，便于机器人感知与环境建模。它专为Isaac Sim设计，直接与其传感器仿真系统集成，支持高保真点云流传输。适用于需要在Isaac Sim中进行点云处理、SLAM或3D感知算法开发的机器人研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/REGATTE/isaac_sim_pointcloud_full_publisher?style=social)

- [orbit_envs](https://github.com/pascal-roth/orbit_envs) — 该项目为Omniverse Isaac Sim提供Matterport和Unreal Engine扩展，主要用于构建高保真室内仿真环境。它通过集成Matterport3D数据集与Unreal Engine资产，支持在Isaac Sim中快速部署逼真的机器人训练场景，并利用USD格式实现与Omniverse生态的无缝对接。目标用户为需要真实室内环境进行导航、交互或感知算法研究的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/pascal-roth/orbit_envs?style=social)

- [husky_demo](https://github.com/NVIDIA-AI-IOT/husky_demo) — 该项目提供Husky机器人在Isaac Sim中的仿真及硬件在环（HIL）测试功能，并通过Isaac ROS实现与真实硬件的集成。它利用Isaac Sim的GPU加速物理引擎和传感器模拟能力，结合ROS 2接口，支持在Jetson Orin等边缘设备上部署控制算法。主要面向使用Isaac Sim进行移动机器人开发与验证的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/NVIDIA-AI-IOT/husky_demo?style=social)

- [Isaac-ur_rtde](https://github.com/Steigner/Isaac-ur_rtde) — 该项目实现了 NVIDIA Omniverse Isaac Sim 与 Universal Robots 机器人之间的 RTDE 通信，允许在 Isaac Sim 中实时控制和监控 UR 机器人。它通过 Python 封装 UR 的 RTDE 接口，支持在仿真环境中与真实 UR 机器人同步数据，适用于需要硬件在环（HIL）或数字孪生的机器人开发场景。目标用户为使用 Isaac Sim 进行 UR 机器人仿真的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/Steigner/Isaac-ur_rtde?style=social)

- [Reach](https://github.com/mobinajamali/Reach) — 该项目是一个基于强化学习的机器人抓取目标位姿训练流程，专为UR10机械臂设计。它明确使用Isaac Lab和Isaac Sim构建仿真环境，利用其GPU加速的物理引擎和RL训练框架实现高效策略学习。适用于希望在Isaac Sim生态中开发机械臂控制算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/mobinajamali/Reach?style=social)

- [mjcf-importer-extension](https://github.com/isaac-sim/mjcf-importer-extension) — 该项目是一个用于NVIDIA Isaac Sim的MJCF（MuJoCo XML格式）导入器扩展，允许用户将MuJoCo模型直接导入Isaac Sim中进行仿真。它通过C++实现，利用Isaac Sim的USD（Universal Scene Description）架构完成模型转换与集成，支持物理属性和关节结构的映射。该工具主要面向需要在Isaac Sim中复用MuJoCo机器人模型的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/mjcf-importer-extension?style=social)

- [ur10e_2f140_topic_based_ros2_control](https://github.com/qdeyna/ur10e_2f140_topic_based_ros2_control) — 该项目提供UR10e机械臂与Robotiq 2F140夹爪在Isaac Sim中的集成方案，支持两种ROS 2控制策略：mock组件模式和基于话题的ros2_control工作流。通过自定义C++节点实现与Isaac Sim的通信，利用其GPU加速物理仿真能力进行机器人控制测试。主要面向使用Isaac Sim进行机器人算法开发与验证的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/qdeyna/ur10e_2f140_topic_based_ros2_control?style=social)

- [isaac_ros2_utils](https://github.com/hijimasa/isaac_ros2_utils) — 该项目是一个ROS 2工具包，旨在简化Isaac Sim的使用，提供与ros2_control的集成、自动传感器生成及传感器数据发布功能。它通过Python实现，支持在Isaac Sim中快速配置和仿真各类传感器，并与ROS 2控制系统无缝对接。主要面向使用Isaac Sim进行机器人仿真的ROS 2开发者。 ![GitHub stars](https://img.shields.io/github/stars/hijimasa/isaac_ros2_utils?style=social)

- [uosm.isaac.px4_bridge](https://github.com/limshoonkit/uosm.isaac.px4_bridge) — 该项目是一个 Omniverse 扩展，用于在 Isaac Sim 中集成 PX4 自动驾驶仪，支持通过 ROS 2 与仿真环境通信。它利用 Isaac Sim 的多物理场仿真能力，为无人机和自主飞行器提供高保真测试平台，主要面向基于 PX4 和 ROS 2 开发的机器人研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/limshoonkit/uosm.isaac.px4_bridge?style=social)

- [IsaacNPC](https://github.com/Renforce-Dynamics/IsaacNPC) — IsaacNPC 是一个轻量级的非玩家角色（NPC）框架，专为 Isaac Lab 设计，使机器人能作为自主环境实体运行，支持预训练策略或基于规则的控制器。该项目直接集成于 Isaac Lab 生态，利用其仿真与强化学习能力，为多智能体交互和复杂场景构建提供基础。适用于需要在 Isaac Sim 中开发动态、交互式虚拟环境的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/Renforce-Dynamics/IsaacNPC?style=social)

- [torobo_usd_models](https://github.com/TokyoRobotics/torobo_usd_models) — 该项目提供专为 NVIDIA Isaac Sim 优化的 TOROBO 机器人 USD 模型，包含完整的关节、碰撞体和视觉外观定义，支持在 Isaac Sim 中直接加载用于仿真与控制开发。模型基于 Universal Scene Description (USD) 格式构建，确保与 Isaac Sim 的 PhysX 和 Omniverse 引擎无缝集成。主要面向使用 Isaac Sim 进行机器人算法验证和仿真的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/TokyoRobotics/torobo_usd_models?style=social)

- [Isaacsim-Franka](https://github.com/jmSNU/Isaacsim-Franka) — 该项目基于NVIDIA Isaac Sim构建了一个面向Franka Panda机械臂的视觉强化学习环境，利用Isaac Sim的GPU加速物理仿真与传感器模拟能力，实现了RGB图像输入的RL任务。代码采用Python编写，集成了Isaac Sim的API以控制机器人并获取视觉观测，适用于研究视觉引导的机器人操作策略的科研人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/jmSNU/Isaacsim-Franka?style=social)

- [isaac-crowd-sim](https://github.com/SCAI-Lab/isaac-crowd-sim) — 该项目用于在Isaac Sim中模拟多样化的人群场景，支持自主导航算法的开发与测试。它通过集成Isaac Sim的物理引擎和传感器仿真能力，构建动态、逼真的行人交互环境，适用于机器人避障与路径规划研究。目标用户为从事自主移动机器人或智能体导航研发的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/SCAI-Lab/isaac-crowd-sim?style=social)

- [isaaclab_kangaroo](https://github.com/hucebot/isaaclab_kangaroo) — 该项目为袋鼠机器人（Kangaroo robot）在 Isaac Lab 中实现了一系列运动控制任务，基于 Isaac Sim 的强化学习框架构建，利用其 GPU 加速的物理仿真能力进行训练。项目包含针对该仿生机器人的定制化任务定义、奖励函数和观察空间设计，适用于研究复杂动态运动策略的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/hucebot/isaaclab_kangaroo?style=social)

- [hit_omniverse](https://github.com/shaosb/hit_omniverse) — 该项目实现了解耦式模仿学习框架，用于全身体人形机器人的自然步态控制。它基于 Isaac Lab 构建，利用其强化学习和仿真环境进行训练与部署，采用 PyTorch 实现策略网络，并依赖 Omniverse 提供的高保真物理模拟。主要面向人形机器人运动控制研究者和 Isaac Sim 开发者。 ![GitHub stars](https://img.shields.io/github/stars/shaosb/hit_omniverse?style=social)

- [robot_usds](https://github.com/fiveages-sim/robot_usds) — 该项目提供面向 ROS2 Control 的 Isaac Sim USD 资源，主要用于在 Isaac Sim 中加载和控制移动操作机器人模型。通过定义符合 ROS2 控制规范的 USD 场景文件，实现与 Isaac Sim 的深度集成，支持关节状态反馈和命令接口。目标用户为使用 Isaac Sim 进行机器人仿真并希望与 ROS2 生态系统对接的开发者。 ![GitHub stars](https://img.shields.io/github/stars/fiveages-sim/robot_usds?style=social)

- [isaac_rover_2.0](https://github.com/abmoRobotics/isaac_rover_2.0) — 该项目实现了基于 Isaac Gym/Sim 的火星车 2.0 仿真系统，利用 NVIDIA Isaac Sim 提供的 GPU 加速物理引擎对火星车进行动力学建模与控制策略测试。项目通过 URDF 导入机器人模型，并集成强化学习训练流程，适用于希望在高保真仿真环境中开发行星探测机器人控制算法的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/abmoRobotics/isaac_rover_2.0?style=social)

- [IsaacLab_AMP_rl-games](https://github.com/Gudegi/IsaacLab_AMP_rl-games) — 该项目在 Isaac Lab 框架中实现了对抗运动先验（AMP）算法，结合 rl_games 强化学习库用于训练人形机器人运动策略。它利用 Isaac Sim 的 GPU 加速物理仿真能力，通过对抗性判别器引导智能体生成自然运动，适用于需要高保真运动控制的机器人研究。目标用户为基于 Isaac Lab 开发高级运动技能的强化学习研究者。 ![GitHub stars](https://img.shields.io/github/stars/Gudegi/IsaacLab_AMP_rl-games?style=social)

- [DEAS-Isaac-GR00T](https://github.com/csmile-1006/DEAS-Isaac-GR00T) — 该项目结合DEAS、Isaac-GR00T与RoboCasa，构建基于视觉-语言-动作模型（VLA）的机器人强化学习框架。其核心在于利用Isaac Sim提供的高保真仿真环境训练具身智能体，并通过GR00T架构实现多模态指令到动作的映射。项目面向希望在Isaac Sim生态中开发VLA驱动机器人的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/csmile-1006/DEAS-Isaac-GR00T?style=social)

- [isaac-quad-loco](https://github.com/dyumanaditya/isaac-quad-loco) — 该项目利用强化学习与模型预测控制（MPC）实现四足机器人运动控制，专为NVIDIA Isaac Sim平台构建，基于Isaac Gym环境进行GPU加速的并行仿真训练。代码集成了Isaac Sim的物理引擎和传感器模拟功能，支持端到端策略学习与部署。适用于希望在Isaac Sim中研究四足机器人运动控制的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/dyumanaditya/isaac-quad-loco?style=social)

- [Isaaclab-arm-learning](https://github.com/BBBig-z/Isaaclab-arm-learning) — 该项目基于Isaac Lab框架构建了六自由度机械臂的强化学习训练系统，支持多种操作任务与控制策略，并集成WandB用于实验跟踪。其核心功能紧密依托Isaac Lab的仿真与RL环境，专为在Isaac Sim生态中开发和测试机械臂智能控制算法的研究者与工程师设计。 ![GitHub stars](https://img.shields.io/github/stars/BBBig-z/Isaaclab-arm-learning?style=social)

- [husky_ur5_isaacsim](https://github.com/ppppplus/husky_ur5_isaacsim) — 该项目提供了一个基于 Isaac Sim 的仿真环境，集成了 Husky 移动底盘、UR5 机械臂和 Robotiq 2F-140 夹爪，用于构建移动操作机器人系统。通过 Isaac Sim 的 GPU 加速物理引擎实现高保真动力学模拟，并支持传感器配置与任务场景搭建。适用于需要在 Isaac Sim 中开发或测试移动机械臂协同控制算法的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/ppppplus/husky_ur5_isaacsim?style=social)

- [LightManager](https://github.com/worv-ai/LightManager) — LightManager 是一个面向 Omniverse Isaac Sim 的高级扩展，用于动态管理和实时动画化场景光照，提升仿真视觉表现力与交互性。该工具通过 Python 实现，深度集成 Isaac Sim 的渲染管线，支持用户在机器人和自主系统仿真中灵活调整光照条件。适用于需要高保真视觉效果的 Isaac Sim 开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/worv-ai/LightManager?style=social)

- [summit_arm_drone](https://github.com/RAICAM-EU-Project/summit_arm_drone) — 该项目在 Isaac Sim 中设计并仿真了一个搭载机械臂的移动机器人与无人机协同作业系统，利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟能力，实现多智能体协同控制与环境交互。项目基于 Python 构建，集成了机器人运动学、无人机动力学及任务调度逻辑，适用于研究异构机器人系统在 Isaac Sim 平台上的联合仿真与算法开发。 ![GitHub stars](https://img.shields.io/github/stars/RAICAM-EU-Project/summit_arm_drone?style=social)

- [Robot-action-simulation-with-GR00T-integration](https://github.com/saha0073/Robot-action-simulation-with-GR00T-integration) — 该项目展示了如何将 NVIDIA 的通用机器人基础模型 GR00T 集成到 Isaac Sim 中，用于控制灵巧手、机械臂和双足机器人等多种平台。通过 Python 脚本实现 GR00T 模型与 Isaac Sim 仿真环境的对接，利用其 GPU 加速物理引擎执行动作生成与仿真。主要面向希望在 Isaac Sim 中测试或部署 GR00T 控制策略的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/saha0073/Robot-action-simulation-with-GR00T-integration?style=social)

- [isaac-sim-colab](https://github.com/j3soon/isaac-sim-colab) — 该项目提供在 Google Colab 上无头运行 NVIDIA Isaac Sim 的非官方指南，通过 Jupyter Notebook 实现远程访问和 GPU 加速仿真。它解决了 Isaac Sim 在云端 Colab 环境中的部署难题，利用虚拟显示和容器化技术绕过图形界面依赖。主要面向希望在无本地高性能硬件条件下快速尝试或教学演示 Isaac Sim 功能的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/j3soon/isaac-sim-colab?style=social)

- [bdx_walk_rl](https://github.com/benoit-robotics/bdx_walk_rl) — 该项目提供了一个基于Isaac Sim的强化学习训练环境，专门用于训练BDX双足机器人行走。它利用Isaac Lab框架构建仿真场景，集成GPU加速的物理模拟与RL训练流程，支持高效的策略开发与测试。目标用户为使用Isaac Sim进行仿人机器人运动控制研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/benoit-robotics/bdx_walk_rl?style=social)

- [autonomous-navigation-pipeline-FAST-LIO-LIO-SAM-Nav2-Isaac-Sim-](https://github.com/Shareefbaba/autonomous-navigation-pipeline-FAST-LIO-LIO-SAM-Nav2-Isaac-Sim-) — 该项目构建了一个无地图自主导航流水线，整合了ROS2 Nav2、FAST-LIO和LIO-SAM，并在NVIDIA Isaac Sim中实现2D/3D LiDAR与IMU的紧耦合里程计、SLAM实验及实时避障功能。通过Isaac Sim提供高保真仿真环境，支持LiDAR–IMU传感器数据融合与本地路径规划器测试，适用于机器人导航算法开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Shareefbaba/autonomous-navigation-pipeline-FAST-LIO-LIO-SAM-Nav2-Isaac-Sim-?style=social)

- [omni-farm-isaac](https://github.com/j3soon/omni-farm-isaac) — 该项目提供用于在 Omniverse Farm 上运行 Isaac Sim 工作负载的工具和脚本，支持批量调度与分布式执行 Isaac Sim、Isaac Gym 和 Isaac Lab 任务。通过 Shell 脚本封装了 Omniverse Farm 的作业提交流程，简化了大规模仿真训练的部署。主要面向需要在集群环境中高效运行 NVIDIA Isaac Sim 仿真的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/j3soon/omni-farm-isaac?style=social)

- [Isaaclab-Gripper-Drone-Pickplace](https://github.com/uiseoklee/Isaaclab-Gripper-Drone-Pickplace) — 该项目基于Isaac Sim构建了一个无人机操作框架，利用深度强化学习和高精度物理仿真训练四旋翼无人机自主抓取与搬运物体。它直接集成Isaac Lab环境，采用GPU加速的多物理场模拟实现逼真的抓取动力学，并提供完整的训练与部署流程。适用于希望在Isaac Sim中开发空中机器人操作任务的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/uiseoklee/Isaaclab-Gripper-Drone-Pickplace?style=social)

- [Synthesis-Assets-Explorer](https://github.com/Extwin-Synthesis/Synthesis-Assets-Explorer) — Synthesis Asset Explorer 是一个专为 Isaac Sim 和 Omniverse 设计的扩展工具，用于加载高质量开源 USD 资源，包括可动仿真的拟真资产、建筑模型、3D Gaussian Splatting 模型及真实世界比例的交互式仿真场景。该工具深度集成 Isaac Sim 的物理仿真与 SimReady 标准，支持快速构建数字孪生和合成数据生成环境，适用于机器人仿真、人形机器人开发及 sim2real 迁移研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Extwin-Synthesis/Synthesis-Assets-Explorer?style=social)

- [RL_UR5_IsaacLab](https://github.com/aparame/RL_UR5_IsaacLab) — 该项目基于Isaac Lab平台，开发了一个视觉驱动的强化学习智能体，用于在人机协作环境中控制UR5机械臂。它利用PPO算法与PyTorch实现，结合RGB图像输入进行端到端策略学习，并强调安全性设计。项目直接构建于Isaac Lab之上，适用于需要在高保真物理仿真中研究人机协同操作的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/aparame/RL_UR5_IsaacLab?style=social)

- [isaac-sim-surgical-robotics-challenge](https://github.com/surgical-robotics-ai/isaac-sim-surgical-robotics-challenge) — 该项目在Isaac Sim中实现了约翰霍普金斯大学LCSR实验室开发的AMBF外科机器人挑战，利用Isaac Sim的GPU加速物理仿真能力复现手术机器人任务环境。通过USD场景构建和Python脚本控制，支持高保真器械交互与软组织模拟，为外科机器人AI算法提供训练与测试平台。主要面向医疗机器人研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/surgical-robotics-ai/isaac-sim-surgical-robotics-challenge?style=social)

- [scout_v2_isaac](https://github.com/leonlime/scout_v2_isaac) — 该项目为Agilex Scout V2机器人提供NVIDIA Isaac Sim仿真支持，基于Omniverse平台构建，包含机器人模型、传感器配置及控制接口，便于在Isaac Sim中进行移动机器人算法开发与测试。主要面向使用Isaac Sim进行地面机器人仿真的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/leonlime/scout_v2_isaac?style=social)

- [IsaacOrbit-Quadruped-RL](https://github.com/felipemohr/IsaacOrbit-Quadruped-RL) — 该项目提供了基于Isaac Orbit的四足机器人强化学习训练环境，专为在Isaac Sim生态中开发和测试四足运动控制策略而设计。它利用Isaac Orbit框架构建高保真仿真场景，支持GPU加速的物理模拟与RL训练流程。目标用户为从事四足机器人AI控制研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/felipemohr/IsaacOrbit-Quadruped-RL?style=social)

- [isaac-b2-ros2](https://github.com/HuangZihaooo/isaac-b2-ros2) — 该项目为Unitree B2四足机器人提供基于Isaac Sim的ROS 2（Humble）仿真接口，利用Isaac Sim的PhysX物理引擎和ROS 2通信框架实现高保真运动控制与传感器模拟。通过自定义USD资产和ROS 2节点集成，支持在Isaac Sim中部署B2机器人的感知、导航与强化学习算法，主要面向使用NVIDIA Isaac Sim进行四足机器人开发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/HuangZihaooo/isaac-b2-ros2?style=social)

- [AerialManipulation](https://github.com/PratikKunapuli/AerialManipulation) — 该项目旨在探索使用强化学习（RL）控制二自由度空中机械臂的方法，专为 Isaac Lab 平台开发。它利用 Isaac Sim 的 GPU 加速物理仿真能力，在 Isaac Lab 框架下构建了完整的 RL 训练环境与任务定义。项目包含自定义机器人模型、传感器配置及奖励函数设计，适用于希望在 Isaac Sim 生态中研究空中操作与强化学习结合的科研人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/PratikKunapuli/AerialManipulation?style=social)

- [IsaacImitationLearning](https://github.com/tsnz/IsaacImitationLearning) — 该项目为 Isaac Lab 提供模仿学习（Imitation Learning）的实现框架，支持从专家演示数据中训练机器人策略。它基于 Isaac Lab 的强化学习环境构建，利用其 GPU 加速的物理仿真能力进行高效策略学习，包含行为克隆和 GAIL 等算法示例。主要面向希望在 Isaac Sim 生态中开展模仿学习研究的机器人开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/tsnz/IsaacImitationLearning?style=social)

- [isaac_sim_how_to_make_pick_and_place_demo](https://github.com/hijimasa/isaac_sim_how_to_make_pick_and_place_demo) — 该项目提供了一个完整的教程，展示如何在 Isaac Sim 中创建 USD 场景并编写 Python 脚本实现抓取与放置（pick-and-place）任务。内容涵盖资产建模、场景搭建及基于 Isaac Sim API 的控制逻辑实现，适合希望快速上手 Isaac Sim 机器人操作仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/hijimasa/isaac_sim_how_to_make_pick_and_place_demo?style=social)

- [UR5e_IsaacLab_SCUT](https://github.com/OwenCaleb/UR5e_IsaacLab_SCUT) — 该项目基于 Isaac Lab 框架，为 UR5e 机械臂提供了完整的仿真环境与控制接口，支持在 Isaac Sim 中进行强化学习和运动规划任务。它复用了 UR5 的 Isaac Lab 配置并针对 UR5e 型号进行了适配，包含机器人模型、传感器配置及任务定义。主要面向使用 NVIDIA Isaac Sim 进行机器人算法开发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/OwenCaleb/UR5e_IsaacLab_SCUT?style=social)

- [noetix_e1_lab](https://github.com/Noetix-Robotics/noetix_e1_lab) — 该项目是一个基于Isaac Lab的强化学习框架，专门用于训练E1人形机器人。它利用Isaac Lab提供的GPU加速物理仿真和RL环境接口，实现了针对人形机器人的运动控制策略训练。目标用户为从事人形机器人强化学习研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/Noetix-Robotics/noetix_e1_lab?style=social)

- [isaaclab_g1](https://github.com/ARC-KIST/isaaclab_g1) — 该项目旨在使用强化学习（RL）在 Isaac Lab 中训练 G1 机器人，直接基于 Isaac Sim 的 Isaac Lab 框架构建，利用其 GPU 加速的物理仿真和 RL 训练能力。项目包含针对人形机器人 G1 的任务定义、奖励函数和训练配置，适用于希望在 Isaac Sim 生态中开发或测试人形机器人控制策略的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/ARC-KIST/isaaclab_g1?style=social)

- [Isaacsim-vlm-arm](https://github.com/K-Dyson/Isaacsim-vlm-arm) — 该项目实现了一个基于视觉语言模型（VLM）的智能机械臂智能体，能够理解自然语言指令并结合图像感知执行操作。项目利用 Isaac Sim 构建高保真仿真环境，集成 VLM 与机器人控制策略，通过 GPU 加速的物理模拟实现端到端的指令-动作映射。主要面向研究具身智能、人机交互及多模态机器人控制的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/K-Dyson/Isaacsim-vlm-arm?style=social)

- [isaac-sim-people-cycle-sim](https://github.com/dillonloh/isaac-sim-people-cycle-sim) — 该项目是对NVIDIA Isaac Sim中"anim.people"测试扩展的修改版，通过循环复用"people"图元（prims）高效模拟高密度人流场景。它针对Isaac Sim的动画与场景管理机制进行优化，利用其USD架构和GPU加速能力实现大规模人群仿真。适用于需要在Isaac Sim中构建复杂人流动态环境的机器人导航或社会交互研究者。 ![GitHub stars](https://img.shields.io/github/stars/dillonloh/isaac-sim-people-cycle-sim?style=social)

- [LatencyNodes](https://github.com/worv-ai/LatencyNodes) — Latency-Nodes 是一个专为 Isaac Sim 开发的 OmniGraph 扩展，用于在机器人仿真中模拟通信延迟，通过自定义节点实现对传感器或控制信号传输延迟的建模。该工具直接集成于 Isaac Sim 的 OmniGraph 系统，利用 Python 编写，支持构建更贴近真实网络环境的机器人测试场景。适用于需要评估通信延迟对机器人性能影响的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/worv-ai/LatencyNodes?style=social)

- [x-trainer](https://github.com/embodied-dobot/x-trainer) — X-Trainer 是一个协作机械臂平台，支持 VR/手柄遥操作数据采集，并提供 NVIDIA GPU 加速的仿真功能。项目明确集成了 Isaac Sim 作为其核心仿真环境，利用其多物理场和传感器模拟能力进行机器人训练。该平台面向需要高精度（±0.05 mm）操作与仿真实训结合的机器人学习研究者。 ![GitHub stars](https://img.shields.io/github/stars/embodied-dobot/x-trainer?style=social)

- [runai-isaac](https://github.com/j3soon/runai-isaac) — 该项目提供在 Run:ai 平台上运行 Isaac Sim 工作负载所需的工具和脚本，主要通过 Dockerfile 实现环境封装与调度集成。它明确支持 Isaac Sim、Isaac Gym 和 Isaac Lab，利用 Run:ai 的资源管理能力优化 GPU 加速的机器人仿真任务。目标用户为希望在 Kubernetes 集群上高效调度 Isaac Sim 仿真的 AI 与机器人研发团队。 ![GitHub stars](https://img.shields.io/github/stars/j3soon/runai-isaac?style=social)

- [isaac-ppo](https://github.com/dyumanaditya/isaac-ppo) — 该项目实现了近端策略优化（PPO）强化学习算法，专为 Isaac Sim Orbit 框架设计，用于在 GPU 加速的物理仿真环境中训练机器人策略。代码基于 PyTorch 构建，与 Orbit 的任务接口和环境封装紧密集成，便于在 Isaac Sim 中快速部署和测试 RL 算法。适用于希望在 Isaac Sim 生态中开发或验证强化学习控制策略的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/dyumanaditya/isaac-ppo?style=social)

- [Turtlebot3_Lime_IsaacSim_Humble](https://github.com/momoiorg-repository/Turtlebot3_Lime_IsaacSim_Humble) — 该项目提供了一套 Docker 配置和脚本，用于搭建集成 NVIDIA Isaac Sim 4.5.0 与 ROS 2 Humble 的开发环境，并包含 TurtleBot3 Lime 的演示案例。通过容器化方式简化了 Isaac Sim 与 ROS 2 的协同部署，利用 Python 脚本实现仿真场景的自动化配置。主要面向希望在 Isaac Sim 中快速测试 TurtleBot3 机器人应用的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/momoiorg-repository/Turtlebot3_Lime_IsaacSim_Humble?style=social)

- [IsaacLab_Locomotion_H1](https://github.com/NirajPudasaini/IsaacLab_Locomotion_H1) — 该项目是基于 Isaac Lab 的 Unitree H1 人形机器人在复杂地形上的运动控制扩展，利用 Isaac Sim 的 GPU 加速物理仿真能力实现高动态步态训练。它集成了 Isaac Lab 的强化学习框架，采用 PPO 算法进行策略优化，并针对粗糙地形设计了专用奖励函数和观测空间。主要面向使用 Isaac Sim 进行人形机器人运动控制研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/NirajPudasaini/IsaacLab_Locomotion_H1?style=social)

- [IsaacLab_Locomotion_H1-2](https://github.com/NirajPudasaini/IsaacLab_Locomotion_H1-2) — 该项目是基于 Isaac Lab 开发的 Unitree H1-2 人形机器人在平坦与粗糙地形上的运动控制扩展，利用 Isaac Sim 的强化学习和物理仿真能力实现高动态步态训练。项目集成了 Isaac Lab 的任务框架与环境配置，采用 PPO 算法进行策略优化，适用于研究人形机器人在复杂地形下的稳定行走。主要面向使用 Isaac Sim 进行机器人强化学习研究的开发者与科研人员。 ![GitHub stars](https://img.shields.io/github/stars/NirajPudasaini/IsaacLab_Locomotion_H1-2?style=social)

- [Quadrupeds_Climbing](https://github.com/leo01110111/Quadrupeds_Climbing) — 该项目是一个基于 Isaac Lab 的强化学习任务，专门训练 Unitree Go2 四足机器人在陡峭地形上攀爬。它利用 Isaac Sim 提供的 GPU 加速物理仿真环境，结合 RL 算法实现复杂地形下的运动控制，适用于机器人学习与仿真的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/leo01110111/Quadrupeds_Climbing?style=social)

- [LocoLab](https://github.com/syw-robotics/LocoLab) — LocoLab 是一套面向 Isaac Lab 的运动控制任务训练与评估的入门环境套件，专为四足和双足机器人设计。它基于 Isaac Lab 构建，提供模块化的任务配置、奖励函数和观测空间定义，支持快速实验迭代。项目利用 Isaac Sim 的 GPU 加速物理仿真能力，目标用户为从事机器人强化学习研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/syw-robotics/LocoLab?style=social)

- [OmniIsaacGymEnvs-HiwinReacher](https://github.com/j3soon/OmniIsaacGymEnvs-HiwinReacher) — 该项目为Hiwin RA620机械臂提供了基于强化学习的Sim2Real仿真环境，专为NVIDIA Omniverse Isaac Gym/Sim构建。它利用Isaac Sim的GPU加速物理仿真能力，实现了机械臂到达任务的训练与部署，并支持从仿真到真实机器人的迁移。目标用户是从事机器人强化学习研究与应用的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/j3soon/OmniIsaacGymEnvs-HiwinReacher?style=social)

- [rm_65_dh95_isaac](https://github.com/Kassra-sinaei/rm_65_dh95_isaac) — 该项目在NVIDIA Isaac Sim中实现了Realman双臂机器人RM-65与DH95夹爪的仿真，提供了完整的URDF模型导入、关节控制和场景配置示例。通过Isaac Sim的PhysX物理引擎和ROS 2接口，支持机器人运动学与抓取任务的可视化测试，适用于需要在高保真GPU加速环境中开发多臂协作策略的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Kassra-sinaei/rm_65_dh95_isaac?style=social)

- [isaacsim_standalone_examples](https://github.com/cpnota/isaacsim_standalone_examples) — 该项目提取了 NVIDIA Isaac Sim 官方 standalone_examples 中的 Python 脚本，去除冗余安装包，便于 pip 用户直接使用代码。它依赖已安装的 Isaac Sim 环境运行，保留了原始示例的核心功能，如机器人控制、传感器仿真等，适用于希望快速访问和复用 Isaac Sim 示例脚本的开发者。 ![GitHub stars](https://img.shields.io/github/stars/cpnota/isaacsim_standalone_examples?style=social)

- [Isaac-sim-go2-with-arm](https://github.com/nayon007/Isaac-sim-go2-with-arm) — 该项目基于 NVIDIA Isaac Sim 4.5 实现了 Go2 四足机器人带机械臂的全身 PD 控制，支持稳定爬行、小跑及可调步态，并通过 ROS 2 主题提供实时关节空间反馈。代码采用模块化 Python 架构，专为基于仿真的腿式机器人研究与教学设计，深度集成 Isaac Sim 与 ROS 2 生态。 ![GitHub stars](https://img.shields.io/github/stars/nayon007/Isaac-sim-go2-with-arm?style=social)

- [physical-ai-humanoid-robotics-textbook](https://github.com/ZohaibCodez/physical-ai-humanoid-robotics-textbook) — 该项目是一本完整的物理AI与人形机器人开源教材，包含87个交互式课程、RAG聊天机器人及ROS 2实践项目，并明确集成NVIDIA Isaac Sim作为核心仿真平台。内容通过Docusaurus构建，结合Python机器人编程和多物理仿真，面向教育者、学生及机器人开发者，旨在提供基于Isaac Sim的系统性学习资源。 ![GitHub stars](https://img.shields.io/github/stars/ZohaibCodez/physical-ai-humanoid-robotics-textbook?style=social)

- [Unitree-Go2-EDU-RL-Training-and-Deployment-Tutorial](https://github.com/TheX1an/Unitree-Go2-EDU-RL-Training-and-Deployment-Tutorial) — 该项目提供 Unitree Go2 EDU 机器人的强化学习训练与部署教程，重点展示了如何在 Isaac Sim 中构建仿真环境并集成 RL 训练流程。项目利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能，实现从仿真到真机的策略迁移。目标用户为希望在 Isaac Sim 平台上开发四足机器人控制策略的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/TheX1an/Unitree-Go2-EDU-RL-Training-and-Deployment-Tutorial?style=social)

- [fhi.isaac.grippers](https://github.com/fraunhofer-italia/fhi.isaac.grippers) — 该项目旨在减少NVIDIA Isaac Sim中抓取任务的仿真到现实（sim2real）差距，提供针对Isaac Sim优化的夹爪模型与抓取策略。通过高保真物理参数校准和传感器模拟，提升仿真环境中机械手抓取的现实迁移能力。主要面向机器人抓取研究者与Isaac Sim开发者。 ![GitHub stars](https://img.shields.io/github/stars/fraunhofer-italia/fhi.isaac.grippers?style=social)

- [wandelbots-isaacsim-extension](https://github.com/wandelbotsgmbh/wandelbots-isaacsim-extension) — 该项目是官方提供的 NVIDIA Isaac Sim 扩展，用于与 Wandelbots NOVA 平台进行通信，使用户能在 Isaac Sim 中直接控制和编程工业机器人。该扩展基于 Omniverse Kit 构建，利用 Python 实现与 NOVA 的 API 集成，支持在高保真仿真环境中部署和测试机器人工作流程。主要面向使用 Wandelbots 生态系统的工业自动化开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/wandelbotsgmbh/wandelbots-isaacsim-extension?style=social)

- [sim2real-3d-printed-quadruped](https://github.com/shaheenbharwani/sim2real-3d-printed-quadruped) — 该项目实现了一个完整的四足机器人从仿真到现实的AI工作流，使用Isaac Lab进行强化学习训练，并通过ROS2部署到3D打印的物理硬件上。其核心在于利用Isaac Lab的GPU加速仿真环境训练运动控制策略，并通过自定义接口与ROS2通信，最终在真实机器人上验证性能。适用于希望探索Isaac Sim生态中sim2real迁移的机器人研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/shaheenbharwani/sim2real-3d-printed-quadruped?style=social)

- [Multi-Agent-Robotics-System-using-ROS2-Isaac-Sim](https://github.com/YousefSamm/Multi-Agent-Robotics-System-using-ROS2-Isaac-Sim) — 该项目构建了一个基于ROS 2和NVIDIA Isaac Sim的多智能体机器人系统，集成了行为树、强化学习运动控制器及Nav2导航栈，支持移动机械臂、叉车和Spot机器人在仓库场景中的自主导航与操作。通过Isaac Sim实现高保真GPU加速仿真，并利用Isaac ROS桥接ROS 2节点，为多机器人协同任务提供端到端开发与测试环境。适用于研究多智能体协调、自主物流和机器人强化学习的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/YousefSamm/Multi-Agent-Robotics-System-using-ROS2-Isaac-Sim?style=social)

- [wlr-competition-2025-IsaacLab](https://github.com/leggedrobotics/wlr-competition-2025-IsaacLab) — 该项目是为2025年腿式机器人竞赛（WLR）基于Isaac Lab构建的官方框架，提供标准化的仿真环境、任务定义和评估接口。它深度集成Isaac Sim的PhysX物理引擎与RL训练流程，支持四足机器人运动控制策略的快速开发与测试。目标用户为参与该竞赛的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/leggedrobotics/wlr-competition-2025-IsaacLab?style=social)

- [RM_Isaac](https://github.com/bu-air-lab/RM_Isaac) — 该项目利用奖励机（Reward Machines）在Isaac Gym中训练四足机器人运动策略，通过形式化奖励结构提升策略学习的可解释性与效率。它直接基于Isaac Gym的强化学习环境构建，使用PyTorch实现策略网络，并与NVIDIA的GPU加速物理仿真深度集成。适用于研究形式化方法与强化学习结合的机器人控制研究人员。 ![GitHub stars](https://img.shields.io/github/stars/bu-air-lab/RM_Isaac?style=social)

- [ARCH](https://github.com/Jiankai-Sun/ARCH) — ARCH 是一个面向长时程、高接触复杂度机器人装配任务的分层混合学习框架。该项目在 Isaac Sim 中构建了高保真装配仿真环境，并利用其 GPU 加速物理引擎进行大规模并行训练，实现了策略从仿真到实体机械臂的有效迁移。关键技术包括基于 Isaac Gym 的强化学习与模仿学习融合架构，适用于需要精细接触建模的机器人操作研究者。 ![GitHub stars](https://img.shields.io/github/stars/Jiankai-Sun/ARCH?style=social)

- [RLxUSD](https://github.com/dorado-daniel/RLxUSD) — RLxUSD 提出了一种用于在通用场景描述（USD）格式中记录强化学习训练片段的轻量级标准，特别适配 Isaac Sim 的 USD 原生环境。该项目定义了 RL 数据（如观测、动作、奖励）如何嵌入 USD 时间采样属性，便于与 Isaac Sim 的物理仿真和可视化无缝集成。目标用户为在 Isaac Sim 中开发或调试强化学习算法的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/dorado-daniel/RLxUSD?style=social)

- [roger-reach](https://github.com/work-r-labs/roger-reach) — 该项目是一个面向制造单元设计的交互式可达性分析工具，专为 Isaac Sim 构建，用于可视化和验证机器人工作空间覆盖范围。它利用 OpenUSD 和 URDF 格式集成机器人模型，在 Isaac Sim 环境中实现实时可达性仿真与人机交互评估。目标用户为使用 Isaac Sim 进行产线布局和机器人部署的工程师与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/work-r-labs/roger-reach?style=social)

- [zivid-isaac-sim](https://github.com/zivid/zivid-isaac-sim) — 该项目是Zivid官方为NVIDIA Isaac Sim开发的扩展插件，用于在Isaac Sim中集成Zivid 3D相机的仿真与数据接入功能。它通过Python实现，支持在Isaac Sim的GPU加速多物理仿真环境中模拟Zivid相机的点云输出和传感器特性，便于开发者在机器人感知和抓取任务中进行高保真视觉系统测试。主要面向使用Zivid硬件并基于Isaac Sim构建机器人应用的工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/zivid/zivid-isaac-sim?style=social)

- [isaac-orbit-container](https://github.com/roboticsleeds/isaac-orbit-container) — 该项目提供了一个 Singularity 容器，用于封装 Isaac Sim 与 Isaac Orbit，并集成 ROS Noetic 环境，便于在高性能计算集群中部署和运行基于 Isaac Sim 的机器人仿真任务。容器通过 Shell 脚本自动化构建流程，解决了依赖冲突和环境配置难题，特别适合需要在多用户 HPC 系统上使用 Isaac Sim 与 ROS 协同开发的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/roboticsleeds/isaac-orbit-container?style=social)

- [nvidia-isaac-sim](https://github.com/alvgaona/nvidia-isaac-sim) — 该项目提供了一组用于 NVIDIA Isaac Sim 的 Docker 镜像，简化了 Isaac Sim 及其相关组件（如 Isaac Lab）在不同环境下的部署与运行。通过 Docker 容器化封装，解决了依赖复杂性和环境配置难题，特别适合需要快速搭建 Isaac Sim 开发或测试环境的机器人研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/alvgaona/nvidia-isaac-sim?style=social)

- [IsaacSim_ROS2_HelloWorld](https://github.com/AydinLT00/IsaacSim_ROS2_HelloWorld) — 该项目提供在 Windows 11 上通过 WSL2（Ubuntu 24.04）连接 NVIDIA Isaac Sim 与 ROS 2 Jazzy 的详细配置指南和兼容性解决方案。重点解决 Isaac Sim 与 ROS 2 在跨平台环境下的通信问题，利用 Docker 和网络桥接技术实现传感器数据互通。适用于希望在开发主机上集成 Isaac Sim 高保真仿真与 ROS 2 机器人中间件的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/AydinLT00/IsaacSim_ROS2_HelloWorld?style=social)

- [JeffrinSam_MTS](https://github.com/ISRIndustrial/JeffrinSam_MTS) — 该项目利用Isaac Lab通过模仿学习为Unitree H1/G1机器人生成合成关节数据，并在Isaac Sim中进行仿真与可视化。结合Cosmos提升视觉真实感，并融合遥操作数据微调Gr00t N1.5模型，最终在Isaac Sim中完成抓取放置任务的推理验证。目标用户为使用Isaac Sim进行人形机器人训练与仿真的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/ISRIndustrial/JeffrinSam_MTS?style=social)

- [learning_based_robot_navigation](https://github.com/ritwikrohan/learning_based_robot_navigation) — 该项目提供了一个端到端的学习型机器人导航流程，从在 NVIDIA Isaac Sim 中生成合成数据，到使用 PyTorch 训练导航策略，并最终通过 ROS 2 部署 TensorRT 优化模型。其核心依赖 Isaac Sim 进行高保真仿真数据生成，是 Isaac Sim 在具身智能训练中的典型应用，适用于机器人学习研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/ritwikrohan/learning_based_robot_navigation?style=social)

- [VLM-dataset-generator](https://github.com/katherinejin12/VLM-dataset-generator) — 该项目提供了一套基于 NVIDIA Isaac Sim 的工具，用于生成多样化的合成数据集，包含多种环境、对象及智能体（如机器人、人类、叉车和无人机），并支持丰富的运动轨迹。其核心功能依赖 Isaac Sim 的 GPU 加速多物理仿真能力，可为视觉语言模型和 AI 机器人代理的训练与评估提供逼真数据。主要面向需要大规模、可控合成数据的机器人学习研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/katherinejin12/VLM-dataset-generator?style=social)

- [isaacLab-learning](https://github.com/HaoranZhangumich/isaacLab-learning) — 该项目是面向 Isaac Lab 的自学文档资源，系统整理了 Isaac Lab 的核心概念、环境配置与强化学习训练流程。内容涵盖从基础入门到高级仿真实践，特别聚焦于 Isaac Sim 与 Isaac Gym 的集成使用及 GPU 加速物理仿真。适合希望快速上手 NVIDIA Isaac 平台进行机器人强化学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/HaoranZhangumich/isaacLab-learning?style=social)

- [legged-gym-in-isaac-lab](https://github.com/CMUYUY/legged-gym-in-isaac-lab) — 该项目将基于 Isaac Gym 的 legged_gym 迁移至 NVIDIA Isaac Lab 框架，支持在复杂地形上对 ANYmal-C 四足机器人进行强化学习训练。通过适配 Isaac Lab 的仿真与 RL 接口，实现了与 Isaac Sim 底层物理引擎和传感器模拟的深度集成。主要面向使用 Isaac Sim 生态进行四足机器人控制算法研究的科研人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/CMUYUY/legged-gym-in-isaac-lab?style=social)

- [isaaclab-pixi](https://github.com/AtharvaBhorpe/isaaclab-pixi) — 该项目提供了一个基于 Pixi 包管理器的 Isaac Lab 可复现开发环境，用于简化机器人仿真设置流程。它通过声明式配置确保依赖一致性，直接面向 Isaac Sim 生态中的 Isaac Lab 框架，利用 Pixi 实现跨平台、可复现的 GPU 加速仿真环境部署。适用于希望快速搭建标准化 Isaac Lab 开发与实验环境的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/AtharvaBhorpe/isaaclab-pixi?style=social)

- [extreme-quadruped-parkour](https://github.com/yobel-sungkooklee/extreme-quadruped-parkour) — 该项目利用Isaac Lab平台训练Go2四足机器人完成高难度越障任务，包括跨越80cm间隙和攀爬45cm台阶。通过在7种极端地形（如障碍台阶和间隙横杆）上进行神经网络消融实验，验证控制策略的鲁棒性。项目基于Isaac Lab构建仿真环境并集成其强化学习训练框架，适用于机器人运动控制与仿真的研究人员。 ![GitHub stars](https://img.shields.io/github/stars/yobel-sungkooklee/extreme-quadruped-parkour?style=social)

- [JeffrinSam_G1](https://github.com/JeffrinSam/JeffrinSam_G1) — 该项目利用Isaac Lab中的模仿学习为Unitree G1/H1机器人生成合成关节数据，并在Isaac Sim中进行仿真与可视化。通过Cosmos增强视觉真实感，并融合遥操作数据微调Gr00t N1.5模型，最终在Isaac Sim中完成抓取放置任务的推理验证。主要面向使用Isaac Sim生态开发人形机器人技能的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/JeffrinSam/JeffrinSam_G1?style=social)

- [isaac-lab-devcontainer](https://github.com/miguelasd688/isaac-lab-devcontainer) — 该项目提供了一个独立的开发容器（Devcontainer）配置，用于在隔离环境中快速部署和运行 Isaac Lab。通过预配置的 Dockerfile 和开发环境设置，用户可一键搭建包含 Isaac Sim 依赖的开发环境，避免本地配置冲突。主要面向希望高效开展 Isaac Lab 开发与测试的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/miguelasd688/isaac-lab-devcontainer?style=social)

- [Isaac-Lab-Push](https://github.com/Yannyehao/Isaac-Lab-Push) — 该项目基于 Isaac Lab 平台，利用近端策略优化（PPO）算法解决多物体推挤任务，并引入分层控制框架以提升任务性能与可扩展性。其核心实现紧密依赖 Isaac Lab 的强化学习环境和物理仿真能力，适用于机器人操作策略研究。目标用户为使用 Isaac Sim 生态进行机器人强化学习研究的科研人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/Yannyehao/Isaac-Lab-Push?style=social)

- [AAM-SEALS](https://github.com/konakarthik12/AAM-SEALS) — AAM-SEALS 是一个面向空–水两栖操作臂的高保真仿真平台，支持跨海、空、陆多域机器人研究。该项目基于 Isaac Sim 构建，利用其 GPU 加速的多物理场仿真能力实现逼真的环境交互与传感器模拟，适用于需要跨介质操作的具身智能算法开发与验证。目标用户为多域机器人系统研究人员及开发者。 ![GitHub stars](https://img.shields.io/github/stars/konakarthik12/AAM-SEALS?style=social)

- [text2nav](https://github.com/oadamharoon/text2nav) — 该项目提供了一个轻量级框架，用于实现语言引导的机器人导航，利用冻结的视觉-语言嵌入（如CLIP）进行空间推理，无需微调即可在Isaac Sim仿真环境中达到74%的成功率。其核心通过行为克隆将语言指令与机器人动作映射，并直接集成Isaac Sim作为训练和评估平台。适用于研究语言接地与具身智能的机器人学习研究者。 ![GitHub stars](https://img.shields.io/github/stars/oadamharoon/text2nav?style=social)

- [real2sim](https://github.com/lukehollis/real2sim) — 该项目提供从真实图像输入到生成带语言特征的3D高斯泼溅（3DGS）场景的完整流程，并将对象分割为场景图以支持预测性物理仿真。其明确集成Isaac Sim进行机器人仿真与物理交互，利用Isaac Sim的GPU加速多物理引擎实现真实感动力学行为。目标用户为从事real2sim迁移、具身智能及机器人仿真研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/lukehollis/real2sim?style=social)

- [nvidia-omniverse-cloud-env](https://github.com/everskyrube/nvidia-omniverse-cloud-env) — 该项目提供在 AWS 云平台上部署 NVIDIA Isaac Sim 环境的自动化配置方案，利用 Terraform 和 Docker 实现基础设施即代码（IaC）的部署流程。它专门针对 Isaac Sim 的 GPU 加速仿真需求，预配置了 Omniverse Connect、Isaac Sim 容器及必要的网络与安全设置，显著简化了云端仿真环境的搭建。适用于需要在云中运行 Isaac Sim 进行机器人仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/everskyrube/nvidia-omniverse-cloud-env?style=social)

- [isaac-sim-lab-installer](https://github.com/robosmiths/isaac-sim-lab-installer) — 该项目提供一键式自动化安装脚本，用于在 Ubuntu 22.04/24.04 系统上快速部署 NVIDIA Isaac Sim 5.1.0 及 Isaac Lab，显著节省环境配置时间。通过 Shell 脚本自动处理依赖、容器运行时及权限设置，专为希望高效搭建机器人仿真与强化学习开发环境的研究者和工程师设计。 ![GitHub stars](https://img.shields.io/github/stars/robosmiths/isaac-sim-lab-installer?style=social)

- [Holodeck](https://github.com/Rodgers-254/Holodeck) — Holodeck 是一个文本到仿真的引擎，利用本地大语言模型（LLM）和 OpenUSD 自动生成适用于 NVIDIA Isaac Sim 的物理就绪 3D 环境。该项目直接面向 Isaac Sim 生态，通过自然语言输入快速构建可仿真场景，显著提升机器人训练环境的创建效率。其核心技术结合 LLM 语义理解与 OpenUSD 场景描述，目标用户为使用 Isaac Sim 进行 AI 机器人开发的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/Rodgers-254/Holodeck?style=social)

- [Reinforcement-Learning-Based-Robotic-Object-Picking-with-Koopman-Linear-Dynamics](https://github.com/Ankush0903/Reinforcement-Learning-Based-Robotic-Object-Picking-with-Koopman-Linear-Dynamics) — 该项目在NVIDIA Isaac Sim中实现基于PPO与Koopman线性动力学模型的强化学习机械臂抓取任务，利用课程学习和大规模并行环境（128–8192个）提升训练效率，相比原始状态PPO获得更平滑稳定的动作。项目包含Isaac Sim场景构建、数据生成及RL环境封装，适用于机器人学习研究者与Isaac Sim开发者。 ![GitHub stars](https://img.shields.io/github/stars/Ankush0903/Reinforcement-Learning-Based-Robotic-Object-Picking-with-Koopman-Linear-Dynamics?style=social)

- [IsaacLab-Asset-FrankaUMI](https://github.com/Vector-Wangel/IsaacLab-Asset-FrankaUMI) — 该项目提供了Franka Panda机械臂与UMI（FinRay）夹爪的Isaac Lab资产模型，专为在Isaac Sim中进行高保真机器人仿真而构建。它包含完整的URDF/SDF定义、碰撞与视觉几何体，并适配Isaac Lab的资产加载和物理配置规范，支持快速集成到强化学习或操作任务中。目标用户为使用Isaac Lab开发灵巧操作策略的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Vector-Wangel/IsaacLab-Asset-FrankaUMI?style=social)

- [Isaac-sim-action-graphs](https://github.com/sahilrajpurkar03/Isaac-sim-action-graphs) — 该项目提供了一系列基于 NVIDIA Isaac Sim 的 Action Graphs，利用 Omniverse 的可视化脚本系统实现无代码的机器人控制、传感器仿真与交互行为构建。通过 USD 架构和 Omniverse Kit，用户可直观地搭建复杂仿真逻辑，适用于希望快速原型开发且避免传统编程的机器人研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/sahilrajpurkar03/Isaac-sim-action-graphs?style=social)

- [agilebot_isaac_usd_assets](https://github.com/sh-agilebot/agilebot_isaac_usd_assets) — 该项目提供专为Agilebot机器人设计的OpenUSD资产，明确面向Isaac Sim和Isaac Lab环境使用。这些资产基于OpenUSD格式构建，支持在NVIDIA Isaac平台中进行高保真机器人仿真、传感器配置与物理交互。目标用户为在Isaac Sim或Isaac Lab中开发Agilebot相关应用的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/sh-agilebot/agilebot_isaac_usd_assets?style=social)

- [ros2-isaac-sim-devcontainer](https://github.com/pozasl/ros2-isaac-sim-devcontainer) — 该项目提供了一个预配置的开发容器（devcontainer），集成了 ROS 2 Humble 工作空间和 Isaac Sim 环境，便于开发者在统一环境中进行机器人应用的开发与仿真。通过 Docker 和 VS Code Dev Containers 实现一键搭建 Isaac Sim 与 ROS 2 的集成开发环境，显著降低配置复杂度。主要面向需要在 Isaac Sim 中开发或测试 ROS 2 机器人应用的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/pozasl/ros2-isaac-sim-devcontainer?style=social)

- [Nvidia-Isaac-Sim---Isaac-Lab-Dev](https://github.com/KYH-99/Nvidia-Isaac-Sim---Isaac-Lab-Dev) — 该项目专注于基于NVIDIA Isaac Sim和Isaac Lab的JetBot自动驾驶研究，结合物理AI、高保真物理仿真与强化学习技术，实现从仿真到现实（sim2real）的迁移。项目直接利用Isaac Sim的GPU加速多物理引擎和Isaac Lab的模块化RL框架，为机器人自主驾驶算法开发提供端到端实验平台，适合从事具身智能与自主移动机器人研究的开发者。 ![GitHub stars](https://img.shields.io/github/stars/KYH-99/Nvidia-Isaac-Sim---Isaac-Lab-Dev?style=social)

- [replicator-yolo-writer](https://github.com/Neubotech-AB/replicator-yolo-writer) — 该项目是一个专为 NVIDIA Omniverse Replicator 和 Isaac Sim Replicator 设计的 YOLO 格式数据集写入器，用于将合成生成的标注数据自动转换并保存为 YOLO 所需的文本格式。它通过集成 Isaac Sim 的 Replicator API 实现边界框提取与坐标转换，支持高效构建用于目标检测训练的合成数据集。主要面向使用 Isaac Sim 进行机器人视觉仿真与数据生成的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Neubotech-AB/replicator-yolo-writer?style=social)

- [isaac-sim-ros2-handbook](https://github.com/usamajahangir/isaac-sim-ros2-handbook) — 该项目提供了一本关于使用 NVIDIA Isaac Sim、ROS 2 和 CuRobo 进行工业机器人仿真的实践手册，包含 GP-180 机器人参考实现及 Scan-n-Polish 应用示例。其核心内容聚焦于 Isaac Sim 与 ROS 2 的深度集成，利用 CuRobo 实现运动规划，并通过 Isaac Sim 的 GPU 加速物理引擎进行高保真仿真，适用于希望在 Isaac Sim 生态中开发工业自动化应用的工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/usamajahangir/isaac-sim-ros2-handbook?style=social)

- [isaac-orca-scene-gen](https://github.com/RoseCityRobotics/isaac-orca-scene-gen) — 该项目是一个基于 NVIDIA Isaac Sim 的合成数据集生成管道，专为机械臂训练设计。它可生成带随机物体布局的场景，支持自定义相机视角、图像渲染及元数据收集，并针对 ORCA GPU 集群的无头（headless）执行进行了优化。主要面向需要大规模仿真数据进行机器人视觉或控制模型训练的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/RoseCityRobotics/isaac-orca-scene-gen?style=social)

- [JetBot-PPO-MazeSolver](https://github.com/dericktrinidad/JetBot-PPO-MazeSolver) — 该项目利用近端策略优化（PPO）算法，在NVIDIA Isaac Sim中训练JetBot机器人自主解决复杂迷宫。系统集成了GPS和360°激光雷达，通过仿真学习避障与目标导航能力，直接基于Isaac Sim的物理和传感器模拟环境实现强化学习训练，适用于机器人自主导航研究者和Isaac Sim开发者。 ![GitHub stars](https://img.shields.io/github/stars/dericktrinidad/JetBot-PPO-MazeSolver?style=social)

- [Four_Wheels_Steering_bot](https://github.com/Avg2006/Four_Wheels_Steering_bot) — 该项目提供了一个高保真度的Anveshak火星车1:1 Isaac Sim模型，集成了LiDAR、立体相机、GPS和IMU传感器，用于在Isaac Sim中测试导航、建图与自主算法。模型基于Python构建，专为复现真实火星车系统而设计，适用于机器人研究人员和开发者在Isaac Sim环境下验证感知与控制策略。 ![GitHub stars](https://img.shields.io/github/stars/Avg2006/Four_Wheels_Steering_bot?style=social)

- [full_stack_AV](https://github.com/Ashrith5321/full_stack_AV) — 该项目基于 NVIDIA Isaac Sim 构建了一个端到端的全栈自动驾驶系统，包含逼真的城市仿真环境及完整的感知、建图、规划与控制模块。它通过集成多模态传感器数据，在 Isaac Sim 中实现闭环自动驾驶研究，并利用其 GPU 加速的物理和渲染引擎支持高保真训练与评估，适用于自动驾驶算法研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/Ashrith5321/full_stack_AV?style=social)

- [IsaacLab-Quadruped-Locomotion](https://github.com/huangfq07/IsaacLab-Quadruped-Locomotion) — 该项目基于Isaac Lab平台，使用高级PPO算法实现四足机器人运动控制，专注于在GPU加速的物理仿真环境中训练高动态的四足步态策略。它利用Isaac Lab提供的强化学习框架和机器人仿真接口，集成了自定义奖励函数、观测空间和动作空间设计，适用于希望在Isaac Sim生态中研究四足机器人强化学习的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/huangfq07/IsaacLab-Quadruped-Locomotion?style=social)

- [MiniCheetah_IsaacLabExtension](https://github.com/evelyd/MiniCheetah_IsaacLabExtension) — 该项目为Isaac Lab提供了一个Mini Cheetah四足机器人的强化学习扩展模块，包含完整的URDF模型、传感器配置和任务定义，便于在Isaac Sim环境中进行高性能RL训练。它利用Isaac Lab的模块化架构实现与PhysX物理引擎的深度集成，支持GPU加速仿真。主要面向使用Isaac Sim开展四足机器人控制研究的科研人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/evelyd/MiniCheetah_IsaacLabExtension?style=social)

- [IsaacLabPouringExtension_v2](https://github.com/robegi/IsaacLabPouringExtension_v2) — 该项目是一个面向Isaac Lab的扩展模块，专注于流体操作与倾倒任务，基于Isaac Sim 5.0.0构建，利用其GPU加速的多物理场仿真能力实现高保真液体动力学模拟。通过集成到Isaac Lab框架中，为机器人学习流体操控策略提供专用环境和工具。适用于从事机器人灵巧操作、特别是液体转移任务研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/robegi/IsaacLabPouringExtension_v2?style=social)

- [isaac-lab-classic-rl-algorithms](https://github.com/CMUYUY/isaac-lab-classic-rl-algorithms) — 该项目在 Isaac Lab 的 Cartpole 环境中实现了四种经典深度强化学习算法（PPO、DDPG、TD3、SAC）的训练流程，直接基于 Isaac Sim 的机器人仿真框架 Isaac Lab 构建。代码利用 Isaac Lab 提供的 GPU 加速物理仿真和 RL 接口，展示了如何在其标准环境中部署主流 RL 算法。适用于希望在 Isaac Sim 生态中快速上手强化学习训练的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/CMUYUY/isaac-lab-classic-rl-algorithms?style=social)

- [GenReal_CogRob](https://github.com/saiga006/GenReal_CogRob) — 该项目实现了基于Isaac Lab的厨房抓取放置任务，利用行为克隆和模仿学习训练Franka机械臂完成从冰箱取出番茄罐头并放入微波炉的操作。项目包含完整的数据生成管道、Visuomotor控制模型（结合ResNets与RNN）及在Isaac Sim中的仿真环境集成，适用于认知机器人与具身智能研究者。 ![GitHub stars](https://img.shields.io/github/stars/saiga006/GenReal_CogRob?style=social)

- [IsaacLab](https://github.com/DoD0d0/IsaacLab) — 该项目是一个基于 NVIDIA Isaac Sim 构建的统一机器人学习框架，旨在为强化学习和仿真训练提供模块化、可扩展的基础设施。它深度集成 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能，支持多种机器人模型与任务场景。目标用户为从事机器人 AI 算法研发与仿真实验的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/DoD0d0/IsaacLab?style=social)

- [IsaacLab](https://github.com/kaneki-desu/IsaacLab) — 该项目是一个基于 NVIDIA Isaac Sim 构建的统一机器人学习框架，旨在简化强化学习与仿真训练流程。它深度集成 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能，提供模块化环境配置、任务定义和训练接口。主要面向希望在高保真仿真中快速开发和测试机器人策略的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/kaneki-desu/IsaacLab?style=social)

- [IsaacLab](https://github.com/JonasGrutter/IsaacLab) — 该项目是一个基于 NVIDIA Isaac Sim 构建的统一机器人学习框架，旨在简化强化学习与仿真环境的集成。它利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟能力，提供模块化组件以支持多种机器人任务训练。目标用户为从事机器人学习研究与开发的工程师和科研人员。 ![GitHub stars](https://img.shields.io/github/stars/JonasGrutter/IsaacLab?style=social)

- [IsaacAutomator](https://github.com/k-rks/IsaacAutomator) — 该项目旨在自动化部署 Isaac Sim 和 Isaac Lab 至主流云平台（包括 AWS、Azure、Google Cloud 和阿里云），提供一键式基础设施配置与环境搭建。通过 Terraform 和云原生工具链实现 GPU 实例的自动创建、驱动安装及 Isaac Sim 运行时依赖配置，显著降低在云端使用 NVIDIA 机器人仿真平台的门槛。目标用户为需要在多云环境中快速部署 Isaac Sim/Lab 进行大规模机器人仿真的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/k-rks/IsaacAutomator?style=social)

- [IsaacLab-Scanbot](https://github.com/RobotArm-Scanner/IsaacLab-Scanbot) — 该项目是一个基于 NVIDIA Isaac Sim 构建的统一机器人学习框架，专为 ScanBot 机器人设计，集成了 Isaac Lab 的仿真与强化学习能力。它利用 Isaac Sim 的 GPU 加速多物理仿真环境，支持机器人感知、控制与自主任务训练。目标用户为从事机器人扫描与自动化研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/RobotArm-Scanner/IsaacLab-Scanbot?style=social)

- [Isaac_sim_4.5.0-IsaacLab_install](https://github.com/NanashiMumee/Isaac_sim_4.5.0-IsaacLab_install) — 该项目提供了一份详细的 Isaac Sim 4.5.0 与 Isaac Lab 的安装指南，旨在帮助用户解决在不同系统环境下配置 NVIDIA Isaac Sim 和 Isaac Lab 时可能遇到的依赖和兼容性问题。内容涵盖环境准备、版本匹配建议及常见错误排查，特别针对 Isaac Sim 与 Isaac Lab 的联合使用场景进行优化。目标用户为希望快速搭建 Isaac Sim + Isaac Lab 开发环境的机器人仿真与强化学习研究者。 ![GitHub stars](https://img.shields.io/github/stars/NanashiMumee/Isaac_sim_4.5.0-IsaacLab_install?style=social)

- [wcr-isaac-sim](https://github.com/CRTA-Lab/wcr-isaac-sim) — 该项目为四轮独立转向四轮独立驱动（4WIS4WID）机器人提供 Isaac Sim 与 Isaac Lab 的专用仿真支持，包含针对该底盘构型的运动学模型、控制器及仿真环境配置。项目直接基于 Isaac Sim 和 Isaac Lab 构建，利用其 GPU 加速物理引擎和传感器模拟功能，实现高保真移动机器人仿真。主要面向从事全向移动机器人研发的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/CRTA-Lab/wcr-isaac-sim?style=social)

- [ASE-IsaacSim](https://github.com/Mohamed-Zouhaier-DLH/ASE-IsaacSim) — 该项目将NVIDIA的ASE（对抗性技能嵌入）框架从Isaac Gym迁移到Isaac Sim/Isaac Lab，旨在支持在新一代机器人仿真平台中复用和扩展该强化学习算法。通过适配Isaac Lab的模块化架构和任务定义方式，实现了与Isaac Sim生态的深度集成，便于研究人员在高保真物理仿真环境中开发和测试具身智能策略。目标用户为使用Isaac Sim进行机器人强化学习研究的开发者和学术人员。 ![GitHub stars](https://img.shields.io/github/stars/Mohamed-Zouhaier-DLH/ASE-IsaacSim?style=social)

- [nvidia-robotics-training](https://github.com/mongdmin/nvidia-robotics-training) — 该项目提供面向物理AI与机器人领域的训练资源，明确整合NVIDIA Isaac Sim、Isaac Lab及ROS，用于构建和测试机器人仿真环境。内容涵盖基于GPU加速的多物理仿真工作流，支持在Isaac Sim中部署强化学习与感知算法，并通过ROS实现通信集成。目标用户为希望利用NVIDIA机器人平台进行AI驱动机器人开发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/mongdmin/nvidia-robotics-training?style=social)

- [fhi.isaac.grippers](https://github.com/FraunhoferItalia/fhi.isaac.grippers) — 该项目旨在减少 Nvidia Isaac Sim 中抓取任务的仿真到现实（sim2real）差距，通过高保真夹爪模型和物理参数优化提升仿真真实性。项目提供与 Isaac Sim 深度集成的夹爪资产库及校准工具，利用 GPU 加速多物理仿真精确复现真实世界抓取行为。主要面向机器人抓取研究者和 Isaac Sim 开发者，助力其在仿真中高效验证抓取策略。 ![GitHub stars](https://img.shields.io/github/stars/FraunhoferItalia/fhi.isaac.grippers?style=social)

- [singularity-isaac-sim](https://github.com/j3soon/singularity-isaac-sim) — 该项目提供非官方指南，用于在基于 Singularity/Apptainer 和 SLURM 的集群环境中部署和运行 Isaac Sim 与 Isaac Lab。通过容器化封装 NVIDIA Omniverse 和 Isaac Sim 所需的依赖，解决了在多用户高性能计算集群中部署图形密集型仿真环境的难题。主要面向需要在 HPC 集群上规模化运行 Isaac Sim 仿真的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/j3soon/singularity-isaac-sim?style=social)

- [Isaac-Sim-ML](https://github.com/siddu7g/Isaac-Sim-ML) — 该项目是一个基于强化学习的无人机自主导航框架，专为Isaac Sim设计，从PPO微航点导航起步，逐步引入基于立体视觉的避障能力，并进一步发展为利用BEV感知的多智能体协同定位与导航。其核心在Isaac Sim中实现GPU加速的多智能体仿真训练，结合PyTorch和共享空间上下文机制，面向机器人学习研究人员及自主系统开发者。 ![GitHub stars](https://img.shields.io/github/stars/siddu7g/Isaac-Sim-ML?style=social)

- [ETHRC_Isaac_Sim_Workshop](https://github.com/JulesHere/ETHRC_Isaac_Sim_Workshop) — 该项目是苏黎世联邦理工学院机器人俱乐部举办的强化学习工作坊材料，专门面向 NVIDIA Isaac Sim 平台。内容涵盖在 Isaac Sim 中构建强化学习训练环境、与 RL 框架集成及 GPU 加速仿真的实践教程，使用 Python 和 Isaac Sim 的 Replicator 与 PhysX 功能。目标用户为希望利用 Isaac Sim 开发机器人强化学习应用的研究者与学生。 ![GitHub stars](https://img.shields.io/github/stars/JulesHere/ETHRC_Isaac_Sim_Workshop?style=social)

- [isaac-sim-synth-data](https://github.com/aryaMehta26/isaac-sim-synth-data) — 该项目是一个基于 NVIDIA Omniverse Isaac Sim 构建的高保真合成数据生成管道，利用 USD 格式构建仿真环境，支持域随机化和多传感器（相机/LiDAR/IMU）建模，可批量生成 RGB、深度图、分割掩码及 COCO 格式的标注数据。其核心功能紧密集成 Isaac Sim 的渲染与传感器模拟能力，专为机器人感知任务和 sim-to-real 迁移研究设计，适合需要大规模标注数据的机器人学习开发者使用。 ![GitHub stars](https://img.shields.io/github/stars/aryaMehta26/isaac-sim-synth-data?style=social)

- [Isaac-Sim2Real-Pipeline](https://github.com/UoA-CARES/Isaac-Sim2Real-Pipeline) — 该项目是一个端到端的仿真到现实（sim-to-real）强化学习自动化工具包，专为 Isaac Sim 设计，提供从仿真训练、域随机化到真实机器人部署的完整流程。它深度集成 Isaac Sim 的传感器模拟、物理引擎和 RL 环境接口，利用其 GPU 加速多物理场仿真能力提升策略迁移效率。目标用户为使用 Isaac Sim 进行机器人强化学习研究与部署的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/UoA-CARES/Isaac-Sim2Real-Pipeline?style=social)

- [isaac-simulation-agent](https://github.com/cerulion-inc/isaac-simulation-agent) — 该项目是一个面向 NVIDIA Isaac Sim 的自主仿真代理，通过集成 MCP（Multi-agent Control Protocol）和 Bedrock Agent Core，实现端到端的仿真任务编排。它专为 Isaac Sim 环境设计，可自动化启动、监控和管理仿真流程，利用大模型驱动的智能体提升机器人仿真效率。目标用户为需要自动化、智能化 Isaac Sim 工作流的机器人研发团队。 ![GitHub stars](https://img.shields.io/github/stars/cerulion-inc/isaac-simulation-agent?style=social)

- [Doosan-Robotics-Isaac-Lab-Tutorial](https://github.com/HoonBK/Doosan-Robotics-Isaac-Lab-Tutorial) — 该项目提供了一个详细教程，指导用户如何安装 Isaac Sim 和 Isaac Lab，并基于强化学习训练 Doosan M0609 机械臂。内容涵盖 Isaac Lab 环境配置、机器人 URDF 导入、自定义任务定义及 PPO 算法训练流程，专为希望在 Isaac Sim 平台开展工业机器人强化学习研究的开发者和研究人员设计。 ![GitHub stars](https://img.shields.io/github/stars/HoonBK/Doosan-Robotics-Isaac-Lab-Tutorial?style=social)

- [AGV-Simulation-in-NVIDIA-Isaac-Sim](https://github.com/DonatoCerciello/AGV-Simulation-in-NVIDIA-Isaac-Sim) — 该项目在 NVIDIA Isaac Sim 中构建了一个动态仓库环境下的自动导引车（AGV）仿真系统，实现了自主导航、动态避障、人员跟踪以及 LiDAR 与相机的合成数据生成。项目直接基于 Isaac Sim 的传感器模型和物理引擎开发，利用其 Python API 构建完整机器人工作流，适用于希望在高保真 GPU 加速仿真中测试 AGV 算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/DonatoCerciello/AGV-Simulation-in-NVIDIA-Isaac-Sim?style=social)

- [humanoid_lite](https://github.com/Coincade/humanoid_lite) — 该项目提供了 Humanoid_Lite 人形机器人的强化学习（RL）与模仿学习（IL）训练代码，明确基于 Isaac Sim 和 Isaac Lab 构建，利用其 GPU 加速的物理仿真和机器人学习框架。代码实现了与 Isaac Lab 环境的深度集成，支持在 Isaac Sim 中进行高保真仿真训练。主要面向使用 NVIDIA Isaac 平台开发人形机器人控制策略的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Coincade/humanoid_lite?style=social)

- [isaaclab.actuatornet](https://github.com/ami-iit/isaaclab.actuatornet) — 该项目旨在训练神经网络以建模执行器的硬件与软件机制，从而缩小仿真到现实的差距。它基于 Isaac Lab 构建，利用其强化学习和物理仿真能力来训练执行器模型，适用于需要高保真执行器仿真的机器人研究者。 ![GitHub stars](https://img.shields.io/github/stars/ami-iit/isaaclab.actuatornet?style=social)

- [asset_placer_isaac](https://github.com/K-YUTAA/asset_placer_isaac) — 该项目是一个面向Isaac Sim的AI驱动家具配置扩展工具，能够从输入的平面布局图像自动生成完整的3D室内场景。它利用计算机视觉和深度学习技术解析2D户型图，并在Isaac Sim中自动放置相应的3D资产，实现高效、逼真的仿真环境构建。该工具专为机器人导航、交互或强化学习研究者设计，显著简化了Isaac Sim中复杂室内场景的搭建流程。 ![GitHub stars](https://img.shields.io/github/stars/K-YUTAA/asset_placer_isaac?style=social)

- [isaac-sim-lab-manipulator-basics](https://github.com/OlajuwonDele/isaac-sim-lab-manipulator-basics) — 该项目展示了在 NVIDIA Isaac Sim 和 Isaac Lab 中使用机械臂的基础操作，包含示例脚本、任务定义、控制器实现及机器人资产。它直接面向 Isaac Sim 生态，利用其 Python API 实现机械臂控制与仿真，适用于希望快速上手 Isaac Sim 机械臂仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/OlajuwonDele/isaac-sim-lab-manipulator-basics?style=social)

- [everything-isaacsim](https://github.com/lazy-top/everything-isaacsim) — 该项目汇集了基于 NVIDIA Isaac Sim 构建的实用示例、演示和实验，聚焦于感知、导航、操作等真实机器人仿真场景，并涵盖与 Isaac Sim 的集成工作流。内容以 Python 实现，展示了 Isaac Sim 在多模态机器人任务中的具体应用，适合希望快速上手或拓展 Isaac Sim 应用的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/lazy-top/everything-isaacsim?style=social)

- [isaac_diff_drive_nav](https://github.com/saman-aboutorab/isaac_diff_drive_nav) — 该项目在 NVIDIA Isaac Sim 中实现了一个差速驱动移动机器人，集成了基于 LiDAR 的避障、物理精确的 PID 速度控制和传感器噪声建模。通过 Isaac Sim 的 PhysX 物理引擎和 ROS 2 接口，实现了高保真仿真与控制算法验证，适用于机器人导航算法开发者和 Isaac Sim 用户。 ![GitHub stars](https://img.shields.io/github/stars/saman-aboutorab/isaac_diff_drive_nav?style=social)

- [IsaacLab_manipulation](https://github.com/Toby0614/IsaacLab_manipulation) — 该项目实现了基于模态丢弃（Modality Dropout）的特权姿态机器人操作策略，专为Isaac Lab环境构建，用于研究多模态感知在强化学习中的鲁棒性。代码基于Isaac Lab框架开发，利用其GPU加速的物理仿真和机器人操作任务接口，支持灵活的传感器模态配置与消融实验。主要面向机器人学习研究人员及Isaac Sim开发者。 ![GitHub stars](https://img.shields.io/github/stars/Toby0614/IsaacLab_manipulation?style=social)

- [IsaacLabExtensions](https://github.com/pareshrchaudhary/IsaacLabExtensions) — 该项目提供了一个模板和工具集，用于构建、打包和管理 Isaac Lab 的容器化自定义模块化扩展，允许开发者在不修改原始 IsaacLab 代码库的情况下进行独立开发。它通过容器化技术实现与 Isaac Lab 的解耦集成，便于维护和部署。目标用户为需要扩展 Isaac Lab 功能的机器人仿真开发者。 ![GitHub stars](https://img.shields.io/github/stars/pareshrchaudhary/IsaacLabExtensions?style=social)

- [XRL_IsaacLab](https://github.com/Field-Robotics-Lab/XRL_IsaacLab) — 该项目提供了一个基于可解释强化学习（XRL）的框架，专门用于在 Isaac Lab 中训练地面和水下自主机器人系统。它深度集成 Isaac Lab 的仿真与强化学习环境，利用其 GPU 加速物理引擎和 RL 训练能力，实现高保真、可解释的智能体训练。目标用户为从事野外或水下机器人研究的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Field-Robotics-Lab/XRL_IsaacLab?style=social)

- [IsaacLabEvalTasks](https://github.com/xyao-nv/IsaacLabEvalTasks) — 该项目用于在 Isaac Lab 中对 GR00T N1 策略进行基准测试，提供标准化的评估任务和环境配置。它直接基于 Isaac Lab 构建，利用其机器人仿真框架和 RL 评估接口，实现对具身智能策略的性能量化。目标用户为使用 Isaac Sim/Isaac Lab 开发或评估机器人学习算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/xyao-nv/IsaacLabEvalTasks?style=social)

- [Mistletoe-IsaacLab-Extension](https://github.com/real-robotics/Mistletoe-IsaacLab-Extension) — 该项目是一个 Isaac Lab 扩展，专门用于训练 Mistletoe 四足机器人，提供了完整的仿真环境和训练配置。它基于 Isaac Sim 的强化学习框架构建，利用 GPU 加速的物理仿真来实现高效的机器人策略训练。目标用户为使用 Isaac Lab 进行四足机器人控制算法开发的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/real-robotics/Mistletoe-IsaacLab-Extension?style=social)

- [BALLU_IsaacLab_Extension](https://github.com/ankitdipto/BALLU_IsaacLab_Extension) — 该项目是一个 Isaac Lab 扩展，用于模拟具有浮力辅助的机器人 BALLU，旨在实现高效动态的双足运动。它基于 Isaac Sim 的物理仿真与强化学习框架，集成了自定义浮力模型和运动控制策略。主要面向研究浮力辅助机器人 locomotion 的科研人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/ankitdipto/BALLU_IsaacLab_Extension?style=social)

- [IsaacLab.ext_template](https://github.com/fishjohn/IsaacLab.ext_template) — 该项目提供了一个基于 Isaac Lab 的外部扩展模板，帮助开发者快速创建与 Isaac Lab 兼容的自定义扩展模块。它遵循 Isaac Lab 的扩展架构，包含必要的目录结构、配置文件和示例代码，便于集成新功能或第三方工具。目标用户为希望在 Isaac Sim 生态中开发可复用组件的机器人仿真研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/fishjohn/IsaacLab.ext_template?style=social)

- [agilebot_isaac_lab](https://github.com/sh-agilebot/agilebot_isaac_lab) — 该项目为Agilebot机器人提供基于Isaac Lab的强化学习环境和训练示例，包含任务定义与学习流程，但不包含机器人模型资产。它直接利用Isaac Lab框架构建仿真任务，适用于在Isaac Sim生态中开发和测试四足机器人控制策略的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/sh-agilebot/agilebot_isaac_lab?style=social)

- [isaac-lab-dev-template](https://github.com/trushant05/isaac-lab-dev-template) — 该项目提供了一个容器化的开发模板，用于快速搭建 Isaac Lab 的开发环境。通过 Docker 封装 Isaac Lab 及其依赖，简化了在不同系统上的部署与配置流程，确保环境一致性。主要面向希望高效开展 Isaac Lab 机器人仿真与强化学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/trushant05/isaac-lab-dev-template?style=social)

- [getting-started-with-isaac-lab](https://github.com/neuraljoel/getting-started-with-isaac-lab) — 该项目为 YouTube 教程系列《Getting Started with Isaac Lab》提供配套代码，旨在帮助初学者快速上手 Isaac Lab 框架。内容涵盖 Isaac Lab 的基础环境搭建、机器人仿真配置及强化学习任务实现，使用 Python 编写并与 Isaac Sim 深度集成。目标用户为希望利用 Isaac Lab 进行机器人仿真与 AI 训练的新手开发者。 ![GitHub stars](https://img.shields.io/github/stars/neuraljoel/getting-started-with-isaac-lab?style=social)

- [SimPickGen](https://github.com/bluejade115/SimPickGen) — SimPickGen 是一个在 Isaac Sim 中实现自主抓取与放置任务的项目，利用 cuRobo 进行运动规划，并同步记录关节状态与视觉等多模态数据，用于具身智能研究。该项目直接基于 Isaac Sim 构建，充分利用其 GPU 加速物理仿真和传感器模拟能力，为机器人操作任务提供高质量训练数据。目标用户为从事具身 AI 与机器人仿真的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/bluejade115/SimPickGen?style=social)

- [NaVILA-Bench-for5090](https://github.com/jouta15123/NaVILA-Bench-for5090) — 该项目是一个面向Isaac Lab的视觉-语言导航（Vision-Language Navigation）基准测试平台，专为在Isaac Sim环境中评估具身智能体的跨模态理解与导航能力而设计。它利用Isaac Lab的GPU加速物理仿真和传感器模拟功能，构建了支持自然语言指令与视觉感知交互的室内导航任务。目标用户为从事具身人工智能、机器人导航及多模态学习研究的开发者与科研人员。 ![GitHub stars](https://img.shields.io/github/stars/jouta15123/NaVILA-Bench-for5090?style=social)

- [Go_BDX_Motion_Tracking](https://github.com/ajytak/Go_BDX_Motion_Tracking) — 该项目基于 Isaac Lab 实现了 Go-BDX 机器人的运动跟踪训练，利用 DeepMimic 算法通过模仿学习生成自然的机器人动作。代码直接构建于 Isaac Sim 的强化学习框架之上，使用其物理仿真和 GPU 加速能力进行高效训练。适用于希望在 Isaac Sim 生态中开发仿人机器人运动控制的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/ajytak/Go_BDX_Motion_Tracking?style=social)

- [isaaclab_hsr](https://github.com/mikegroom765/isaaclab_hsr) — 该项目是一个面向 Isaac Lab 的外部模板项目，专门集成了丰田 HSR 机器人，用于在 Isaac Lab 环境中进行强化学习训练。它利用 Isaac Lab 的 GPU 加速物理仿真能力，为 HSR 提供了完整的机器人模型、传感器配置和任务接口，便于研究人员快速构建和测试 RL 算法。目标用户为使用 Isaac Sim 生态进行服务机器人 AI 训练的开发者与科研人员。 ![GitHub stars](https://img.shields.io/github/stars/mikegroom765/isaaclab_hsr?style=social)

- [ar4MP](https://github.com/OlajuwonDele/ar4MP) — 该项目为开源AR4机械臂提供基于强化学习的自适应控制方案，核心功能包括运动学感知奖励设计、动态建模与轨迹优化，并通过Isaac Lab和Isaac Sim实现仿真训练及sim-to-real验证，结合ROS2 Jazzy、Docker和Ray Tune支持端到端开发。其明确将Isaac Sim和Isaac Lab作为主要仿真与训练平台，深度集成NVIDIA Isaac生态，适用于机器人强化学习研究者与工业自动化开发者。 ![GitHub stars](https://img.shields.io/github/stars/OlajuwonDele/ar4MP?style=social)

- [wheel_leg_humanoid_lab](https://github.com/chohh7391/wheel_leg_humanoid_lab) — 该项目提供了一个基于 Isaac Lab 的强化学习环境，用于训练轮腿人形机器人实现行走、驾驶及模式切换。它利用 Isaac Sim 的 GPU 加速物理仿真能力，构建高保真机器人动力学模型，并集成 RL 训练框架。目标用户为从事轮腿混合移动机器人研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/chohh7391/wheel_leg_humanoid_lab?style=social)

- [acel-isaaclab](https://github.com/JHU-ACEL/acel-isaaclab) — 该项目提供用于训练移动机器人的强化学习环境，专为 NVIDIA Isaac Lab 构建。它利用 Isaac Lab 的 GPU 加速物理仿真能力，实现高保真、高效的机器人策略训练。项目包含针对地面移动机器人设计的定制化任务和传感器配置，适用于机器人学习研究人员及开发者。 ![GitHub stars](https://img.shields.io/github/stars/JHU-ACEL/acel-isaaclab?style=social)

- [ARISE](https://github.com/ARC-Mission/ARISE) — 该项目结合Mistral Magistral大语言模型与强化学习策略，用于机器人任务推理，其RL策略在NVIDIA Isaac Lab中训练。项目利用Isaac Lab提供的GPU加速物理仿真环境，实现具身智能体的端到端训练与评估。主要面向研究具身人工智能与机器人自主决策的开发者和科研人员。 ![GitHub stars](https://img.shields.io/github/stars/ARC-Mission/ARISE?style=social)

- [teaching-a-bound-gait-ANYmalC](https://github.com/SalvatorePiccolo/teaching-a-bound-gait-ANYmalC) — 该项目利用强化学习在NVIDIA Isaac Lab中训练ANYmal-C四足机器人的跳跃步态，基于Isaac Lab的GPU加速物理仿真环境实现高效策略训练。项目直接构建于Isaac Lab框架之上，使用其提供的机器人模型、传感器接口和RL工具链，适用于希望在高保真仿真中开发四足机器人运动控制算法的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/SalvatorePiccolo/teaching-a-bound-gait-ANYmalC?style=social)

- [PegasusSimulator](https://github.com/PhoenixAI-LLC/PegasusSimulator) — PegasusSimulator 是一个基于 NVIDIA Isaac Sim 构建的无人机仿真框架，提供对 PX4 飞控系统的原生支持，利用 Isaac Sim 的 GPU 加速多物理场模拟能力实现高保真无人机动力学与传感器仿真。项目深度集成 Isaac Sim 的核心功能，适用于需要在逼真环境中开发和测试自主无人机算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/PhoenixAI-LLC/PegasusSimulator?style=social)

- [URP_Semantic-Arm](https://github.com/airman-and/URP_Semantic-Arm) — 该项目是一个基于ROS2的模块化机械臂控制系统，结合大语言模型（LLM）、视觉Transformer（ViT）和PPO强化学习算法，在NVIDIA Isaac Sim中实现语义驱动的机器人控制。它明确将Isaac Sim作为核心仿真平台，利用其GPU加速物理引擎进行策略训练与多模态感知集成，适用于希望在高保真仿真环境中开发智能机器人控制系统的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/airman-and/URP_Semantic-Arm?style=social)

- [so101_sim2real_nix](https://github.com/jason9075/so101_sim2real_nix) — 该项目为SO-101机械臂构建Sim-to-Real桥梁，核心基于NVIDIA Isaac Sim在NixOS系统上实现。它提供可复现的Docker环境、硬件遥操作和数据采集功能，利用Isaac Sim进行高保真仿真，并通过Omniverse集成支持数字孪生工作流。目标用户为在NixOS环境下开展机器人Sim2Real研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/jason9075/so101_sim2real_nix?style=social)

- [Autonomous-Vehicle-Simulation-Framework](https://github.com/ashishrai12/Autonomous-Vehicle-Simulation-Framework) — 该项目是一个自动驾驶车辆仿真框架，核心采用高性能Rust物理引擎，并通过PyO3与Python AI控制器集成。明确针对NVIDIA Isaac Sim优化，提供完整的Docker支持（含GUI和GPU），便于在Isaac Sim环境中部署和运行自动驾驶算法。适用于希望在Isaac Sim中开发或测试自动驾驶系统的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/ashishrai12/Autonomous-Vehicle-Simulation-Framework?style=social)

- [DexRL](https://github.com/imendezval/DexRL) — 该项目将伯克利自动化实验室的GQ-CNN抓取质量评估模型集成到NVIDIA Isaac Lab中，并通过单步马尔可夫决策过程（MDP）强化学习智能体优化抓取提案。其核心在于利用Isaac Lab的仿真环境实现抓取策略的闭环训练与评估，关键技术包括PyTorch实现的RL代理与Isaac Sim物理引擎的交互。目标用户为从事机器人抓取与强化学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/imendezval/DexRL?style=social)

- [Datum-AI](https://github.com/Daksh-Aneja-Projects/Datum-AI) — 该项目构建了一个用于00级花岗岩制造的自主信息物理系统，结合阻抗控制机器人、掠入射干涉测量和深度强化学习实现纳米级精度抛光。其核心特性是利用NVIDIA Isaac Sim构建数字孪生，实现闭环自适应抛光控制。系统采用GCP原生不可变架构，主要面向高精度制造领域的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Daksh-Aneja-Projects/Datum-AI?style=social)

- [RL-MyRobot](https://github.com/JingyuZhang-01/RL-MyRobot) — 该项目提供了一套完整的强化学习工作流，用于在 NVIDIA Isaac Lab 中训练 MyRobot 的运动策略，并将训练好的策略迁移到 MuJoCo 仿真器中进行 Sim2Sim 验证。项目包含 Isaac Lab 环境配置、训练脚本、机器人资产及 MuJoCo 集成代码，展示了 Isaac Lab 与第三方物理引擎的协同验证流程。主要面向希望在 Isaac Sim 生态中开发并验证机器人策略的研究者和工程师。 ![GitHub stars](https://img.shields.io/github/stars/JingyuZhang-01/RL-MyRobot?style=social)

- [Autonomous_Flying_Beast](https://github.com/Vaibhav-S-98/Autonomous_Flying_Beast) — 该项目提供了一个模块化的自主无人机仿真系统，明确集成了 NVIDIA Isaac Sim 5.x 作为核心仿真平台，并结合 PX4 SITL、Pegasus 后端和 QGroundControl 构建端到端飞行控制管道。通过稳定的 MAVLink 通信实现车辆控制与仿真同步，为开发避障与路径规划等高级自主功能奠定基础。主要面向基于 Isaac Sim 开发无人机自主算法的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Vaibhav-S-98/Autonomous_Flying_Beast?style=social)

- [Isaac-Diffusion-PushT](https://github.com/GDLKWAKEUP/Isaac-Diffusion-PushT) — 该项目基于 NVIDIA Isaac Sim 实现 Diffusion Policy 的 Sim2Real 机器人操作复现，涵盖 Blender 场景建模、Xbox 手柄遥操作数据采集、模型训练及 Isaac Sim 中的闭环推理全流程。其核心是利用 Isaac Sim 提供的高保真物理仿真环境进行策略训练与部署，目标用户为从事机器人学习与 Sim2Real 迁移的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/GDLKWAKEUP/Isaac-Diffusion-PushT?style=social)

- [isaac-objnav-semistatic-eval](https://github.com/utiasDSL/isaac-objnav-semistatic-eval) — 该项目是一个基于 Isaac Sim 构建的对象目标导航（Object-Goal Navigation）评估套件，专门用于在半静态场景中测试和验证机器人导航策略。它利用 Isaac Sim 的 GPU 加速物理仿真能力，构建包含动态与静态障碍物的可控测试环境，并提供标准化的评估指标。该工具面向从事具身智能、语义导航研究的科研人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/utiasDSL/isaac-objnav-semistatic-eval?style=social)

- [isaacsim-python-tutorials](https://github.com/peakzero96/isaacsim-python-tutorials) — 该项目提供了一系列使用 Isaac Sim Python API 的示例代码，涵盖传感器配置、机器人控制和场景搭建等核心功能，帮助用户快速上手 NVIDIA Isaac Sim 的开发。代码基于 Isaac Sim 的官方 API 编写，展示了如何利用其 GPU 加速的物理仿真能力进行机器人应用开发。适合希望学习或扩展 Isaac Sim 自动化仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/peakzero96/isaacsim-python-tutorials?style=social)

- [Easy_DRL_Isaac_Sim](https://github.com/makiJanus/Easy_DRL_Isaac_Sim) — 该项目提供了一套简化深度强化学习（DRL）在 Isaac Sim 中部署的工具和示例，主要面向希望快速上手 Isaac Sim 进行机器人训练的研究者与开发者。它封装了 Isaac Sim 的基础环境配置流程，并集成了常见 DRL 算法接口，降低了使用门槛。项目明确以 Isaac Sim 为核心平台，包含针对性的仿真环境设置与训练脚本。 ![GitHub stars](https://img.shields.io/github/stars/makiJanus/Easy_DRL_Isaac_Sim?style=social)

- [OakInk2-SimEnv-IsaacGym](https://github.com/kelvin34501/OakInk2-SimEnv-IsaacGym) — 该项目基于 Isaac Gym 构建了一个用于 OakInk2 数据集的仿真环境，主要用于手部动作与物体交互的强化学习研究。它利用 Isaac Gym 的 GPU 加速物理模拟能力，复现了 OakInk2 中的手-物交互场景，便于在 Isaac Sim 生态中进行策略训练与迁移。适用于从事灵巧手操作和人机交互仿真的研究人员。 ![GitHub stars](https://img.shields.io/github/stars/kelvin34501/OakInk2-SimEnv-IsaacGym?style=social)

- [simple-raycaster](https://github.com/btx0424/simple-raycaster) — 该项目是一个支持多网格和动态网格的光线投射器，专为与 Isaac Sim 集成而设计，利用 Python 实现高效的射线与网格碰撞检测。其核心功能可直接用于 Isaac Sim 中的传感器模拟或环境交互任务，适合需要在 Isaac Sim 内进行自定义射线检测的机器人仿真开发者。 ![GitHub stars](https://img.shields.io/github/stars/btx0424/simple-raycaster?style=social)

- [isaac-sim-terrain-mapping](https://github.com/yohanlegars/isaac-sim-terrain-mapping) — 该项目用于在可定制的 Isaac Sim 环境中回放 ZED 相机的 SVO 录制文件，并结合深度信息生成地形网格，适用于越野场景下的数字孪生构建。它直接集成 Isaac Sim 作为仿真平台，利用其渲染与物理能力实现高保真地形重建。主要面向需要将真实传感器数据与 Isaac Sim 仿真相融合的机器人感知与导航开发者。 ![GitHub stars](https://img.shields.io/github/stars/yohanlegars/isaac-sim-terrain-mapping?style=social)

- [IsaacLab-SO_100_teleoperation](https://github.com/kabilankb/IsaacLab-SO_100_teleoperation) — 该项目实现了基于 Isaac Lab 的遥操作（teleoperation）功能，用于控制 SO-100 机器人。它利用 Isaac Sim 的仿真环境和传感器接口，通过 Python 脚本实现人机交互控制，适用于需要实时远程操控机器人的研究与开发场景。 ![GitHub stars](https://img.shields.io/github/stars/kabilankb/IsaacLab-SO_100_teleoperation?style=social)

- [AILAB-isaac-sim-pick-place](https://github.com/gist-ailab/AILAB-isaac-sim-pick-place) — 该项目提供了一个在 Isaac Sim 中实现的抓取与放置（pick-and-place）任务示例，使用 Jupyter Notebook 展示如何利用 Isaac Sim 的 Python API 构建机械臂操作仿真环境。项目直接基于 Isaac Sim 的物理引擎和传感器模拟功能，演示了任务流程、物体交互及控制逻辑，适合希望快速上手机器人操作仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/gist-ailab/AILAB-isaac-sim-pick-place?style=social)

- [IsaacLab4.5](https://github.com/jnskkmhr/IsaacLab4.5) — 该项目提供了基于 Isaac Sim 4.5 版本的 IsaacLab 仿真代码，旨在与最新版 IsaacLab 主干代码集成。它利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能，实现高性能机器人仿真环境。主要面向使用 Isaac Lab 进行强化学习或机器人控制研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/jnskkmhr/IsaacLab4.5?style=social)

- [hexapod-locomotion-isaac-sim](https://github.com/lrse/hexapod-locomotion-isaac-sim) — 该项目实现了六足机器人在 Isaac Sim 中的运动控制与仿真，利用 Isaac Sim 的 GPU 加速物理引擎和机器人 API 构建了完整的六足步态控制流程。代码集成了 Isaac Sim 的传感器模拟、关节控制和场景搭建功能，适用于研究多足机器人 locomotion 算法的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/lrse/hexapod-locomotion-isaac-sim?style=social)

- [DreamwaqIssacLab](https://github.com/navinash47/DreamwaqIssacLab) — 该项目旨在为双足机器人DreamWaQ提供在Isaac Lab环境中的仿真与控制实现，利用Isaac Lab的GPU加速物理引擎和强化学习框架进行运动策略训练。代码基于Python构建，集成了Isaac Lab的API以支持高保真动力学模拟和RL训练流程，主要面向研究双足机器人运动控制的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/navinash47/DreamwaqIssacLab?style=social)

- [Isaac-Sim-code](https://github.com/tpy001/Isaac-Sim-code) — 该项目是一个基于 NVIDIA Isaac Sim 构建的模块化 Python 库，旨在简化机器人仿真实验与原型开发。它封装了 Isaac Sim 的常用功能，提供更简洁的 API 接口，便于快速搭建和测试机器人控制策略。目标用户为使用 Isaac Sim 进行机器人算法研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/tpy001/Isaac-Sim-code?style=social)

- [Isaac-Sim-Physical-consistency-plugin](https://github.com/ZC502/Isaac-Sim-Physical-consistency-plugin) — 该项目是一个专为Isaac Sim开发的物理一致性插件，旨在提升仿真环境中物理行为的真实性和稳定性。它通过扩展Isaac Sim的物理引擎接口，实现对刚体动力学、接触力和约束条件的精细化控制，确保仿真结果符合真实世界物理规律。主要面向使用Isaac Sim进行机器人仿真与强化学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/ZC502/Isaac-Sim-Physical-consistency-plugin?style=social)

- [CoRE-jp-Isaac-Sim-ROS2-packages](https://github.com/TKG-Tou-Kai-Group/CoRE-jp-Isaac-Sim-ROS2-packages) — 该项目提供面向CoRE-jp项目的Isaac Sim专用ROS 2软件包，实现Isaac Sim与ROS 2 Humble的深度集成，支持机器人仿真数据在GPU加速环境与ROS 2节点间的高效通信。代码基于Python开发，包含传感器消息桥接、控制接口封装等关键功能，适用于需要在Isaac Sim中部署ROS 2工作流的日本CoRE社区开发者及研究人员。 ![GitHub stars](https://img.shields.io/github/stars/TKG-Tou-Kai-Group/CoRE-jp-Isaac-Sim-ROS2-packages?style=social)

- [Franka-Isaac-Sim-Start](https://github.com/Utter-pulsar/Franka-Isaac-Sim-Start) — 该项目提供了一个在Isaac Sim中控制Franka机械臂夹爪移动到指定位置的示例，展示了如何利用Isaac Sim的Python API实现机械臂的运动控制。代码基于Isaac Sim的仿真环境，通过调用其内置的物理引擎和机器人控制接口，实现对Franka Emika Panda机械臂的精准操作。适合希望快速上手Isaac Sim进行机械臂仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Utter-pulsar/Franka-Isaac-Sim-Start?style=social)

- [delivery_packing_python](https://github.com/loanBRNT/delivery_packing_python) — 该项目是一个基于 Isaac Sim 5.0.0 的机器人协作原型，用于模拟自然语言驱动的配送打包任务：一个机器人将物品放置到托盘，另一个运输货箱。系统使用 Python 实现，集成 Isaac Sim 的物理仿真与机器人控制接口，支持多智能体协同操作。主要面向参与 Lychee x Revel 黑客松的开发者及 Isaac Sim 机器人应用研究者。 ![GitHub stars](https://img.shields.io/github/stars/loanBRNT/delivery_packing_python?style=social)

- [summit_arm_sim](https://github.com/lonelyfluency/summit_arm_sim) — 该项目基于 Isaac Sim 和 ROS 2，为 Summit 移动平台及机械臂提供仿真与控制功能。它利用 Isaac Sim 的 GPU 加速物理引擎实现高保真机器人仿真，并通过 ROS 2 接口实现传感器数据发布与控制指令接收。主要面向使用 Summit 机器人平台进行移动操作研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/lonelyfluency/summit_arm_sim?style=social)

- [Isaaclab-TableTennisRobot](https://github.com/leonardung/Isaaclab-TableTennisRobot) — 该项目基于 Isaac Lab 构建了一个乒乓球机器人仿真环境，利用 Isaac Sim 的 GPU 加速物理引擎和强化学习框架训练机器人击球策略。通过集成 Isaac Lab 的任务定义、传感器模拟和 RL 训练流程，实现了对高速动态交互场景的建模。主要面向研究人机协作或敏捷机器人控制的科研人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/leonardung/Isaaclab-TableTennisRobot?style=social)

- [balancio-sim](https://github.com/alvgaona/balancio-sim) — 该项目是一个面向Isaac Sim的自平衡机器人仿真示例，使用Python实现控制算法并在Isaac Sim环境中运行。它直接利用Isaac Sim的物理引擎和传感器模拟功能，展示了如何在该平台上构建和测试机器人控制策略。适合希望在Isaac Sim中开发或学习自平衡机器人控制的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/alvgaona/balancio-sim?style=social)

- [isaac_sim_moveit](https://github.com/IRVLUTD/isaac_sim_moveit) — 该项目为Isaac Sim提供了与MoveIt（ROS运动规划框架）的接口，使用户能在Isaac Sim中集成和使用MoveIt进行机器人运动规划。通过Python实现，该工具桥接了Isaac Sim的仿真环境与ROS生态，支持在高保真GPU加速仿真中测试和验证MoveIt规划算法。适用于需要在Isaac Sim中结合ROS工具链进行机器人控制与规划的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/IRVLUTD/isaac_sim_moveit?style=social)

- [IsaacLab-Go2](https://github.com/Gepetto/IsaacLab-Go2) — 该项目为Unitree Go2四足机器人在Isaac Lab环境中的仿真与控制提供专用支持，基于Isaac Sim构建，包含机器人模型、传感器配置及运动控制示例。它利用Isaac Lab的强化学习和物理仿真框架，实现高保真GPU加速的四足机器人训练与测试，适用于机器人学习研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/Gepetto/IsaacLab-Go2?style=social)

- [inspire-hand-contact-visual-sensing-IsaacLab](https://github.com/24029100313/inspire-hand-contact-visual-sensing-IsaacLab) — 该项目旨在基于 Isaac Lab 实现灵巧手的接触与视觉感知仿真，利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能，构建高保真机器人手部交互环境。项目通过集成 Isaac Lab 的强化学习框架与 ROS 2 接口，支持触觉反馈与视觉数据融合，适用于机器人操作研究与具身智能算法开发。 ![GitHub stars](https://img.shields.io/github/stars/24029100313/inspire-hand-contact-visual-sensing-IsaacLab?style=social)

- [DexGrasp](https://github.com/bendibendi/DexGrasp) — 该项目基于 Isaac Lab 实现灵巧手对不规则物体的抓取，利用 Isaac Sim 的 GPU 加速物理仿真能力构建抓取策略训练环境。通过集成 Isaac Lab 的机器人控制与感知模块，支持高保真多指手模型的强化学习训练。主要面向从事灵巧操作与机器人抓取研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/bendibendi/DexGrasp?style=social)

- [g1_23dof_locomotion_isaac](https://github.com/jloganolson/g1_23dof_locomotion_isaac) — 该项目实现了基于Isaac Sim的G1人形机器人23自由度运动控制，利用Isaac Gym进行强化学习训练，通过GPU加速的物理仿真优化步态策略。代码集成了NVIDIA Isaac Sim的API以构建高保真机器人环境，适用于研究人形机器人运动控制与强化学习算法的开发者。 ![GitHub stars](https://img.shields.io/github/stars/jloganolson/g1_23dof_locomotion_isaac?style=social)

- [docker-isaac-sim](https://github.com/j3soon/docker-isaac-sim) — 该项目提供了一个非官方的轻量级 Dockerfile，用于简化 Isaac Sim 的容器化部署。它集成了 ROS 2 Humble 支持，并兼容 Omniverse 平台，便于在隔离环境中运行基于 Isaac Sim 的机器人仿真任务。目标用户为希望快速搭建 Isaac Sim 开发或测试环境的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/j3soon/docker-isaac-sim?style=social)

- [isaaclab-sim](https://github.com/wuji-technology/isaaclab-sim) — 该项目提供了一个在Isaac Sim中加载和控制Wuji灵巧手的最小化仿真演示，专为Isaac Lab环境构建。通过Python脚本实现机械手的加载、关节控制与基础交互，展示了如何将定制机器人模型集成到Isaac Sim的GPU加速物理仿真框架中。适用于希望在Isaac Sim中快速验证灵巧手控制策略的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/wuji-technology/isaaclab-sim?style=social)

- [isaacsim-ackermann](https://github.com/lollolha97/isaacsim-ackermann) — 该项目为 Isaac Sim 提供基于 Ackermann 转向模型的车辆控制、SLAM 与导航功能，通过 ROS 2（Humble）实现与 Isaac Sim 的深度集成。利用 Python 编写，封装了传感器驱动、运动控制和导航栈，支持在 Isaac Sim 的高保真仿真环境中测试自动驾驶算法。主要面向使用 Isaac Sim 进行地面机器人或自动驾驶车辆研发的开发者。 ![GitHub stars](https://img.shields.io/github/stars/lollolha97/isaacsim-ackermann?style=social)

- [Nvidia-Isaac-Sim-Procedual-Forest-Generator](https://github.com/joevento/Nvidia-Isaac-Sim-Procedual-Forest-Generator) — 该项目是一个用于NVIDIA Isaac Sim的扩展插件，能够程序化生成森林场景，适用于机器人导航、感知训练等仿真需求。它通过Python脚本在Isaac Sim环境中动态创建带有树木、地形和植被的3D森林环境，利用Isaac Sim的USD和PhysX集成能力实现高效渲染与物理交互。主要面向需要复杂自然环境仿真的机器人开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/joevento/Nvidia-Isaac-Sim-Procedual-Forest-Generator?style=social)

- [agriculture_bot](https://github.com/dueiras/agriculture_bot) — 该项目在Isaac Sim中构建了一个农业环境下的Segway Nova Carter机器人仿真系统，利用Isaac Sim的GPU加速物理引擎和传感器模拟能力，实现对农业场景中移动机器人的行为建模与测试。项目通过Python脚本集成Isaac Sim的API，配置机器人动力学、环境交互及感知模块，适用于农业机器人算法开发者和自主系统研究人员。 ![GitHub stars](https://img.shields.io/github/stars/dueiras/agriculture_bot?style=social)

- [bdx_nao_rl_isaaclab](https://github.com/louislelay/bdx_nao_rl_isaaclab) — 该项目旨在基于 Isaac Lab 框架对 NAO 人形机器人进行强化学习训练，利用 Isaac Sim 提供的 GPU 加速物理仿真环境。它集成了 Isaac Lab 的 RL 工具链，并针对 NAO 机器人的动力学模型和传感器配置进行了适配，便于研究人员快速开展双足行走等复杂行为的学习实验。目标用户为从事人形机器人强化学习研究的开发者与学术人员。 ![GitHub stars](https://img.shields.io/github/stars/louislelay/bdx_nao_rl_isaaclab?style=social)

- [Isaacsim_tutorial](https://github.com/cold-young/Isaacsim_tutorial) — 该项目提供面向初学者的 NVIDIA Isaac Sim 教程材料，涵盖基础操作与仿真场景构建，使用 Python 编写，内容源自 KAIST 研讨会。教程明确围绕 Isaac Sim 平台展开，包含环境设置、API 使用及简单机器人仿真实例，旨在帮助用户快速上手该 GPU 加速的机器人模拟平台。目标用户为希望学习 Isaac Sim 的学生和开发者。 ![GitHub stars](https://img.shields.io/github/stars/cold-young/Isaacsim_tutorial?style=social)

- [stretch_isaacsim](https://github.com/hello-robot/stretch_isaacsim) — 该项目为 Hello Robot 的 Stretch 机器人提供 Isaac Sim 专用的仿真集成，包含 URDF 模型导入、传感器配置及与 Isaac Sim 环境的交互脚本。它利用 Isaac Sim 的 PhysX 物理引擎和 ROS 2 接口，实现高保真机器人仿真，便于在虚拟环境中开发和测试导航与操作算法。主要面向使用 Stretch 机器人的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/hello-robot/stretch_isaacsim?style=social)

- [robots_usd](https://github.com/konu-droid/robots_usd) — 该项目提供了一系列适用于 Isaac Sim 和 Isaac Lab 的自定义 USD 机器人模型文件，涵盖移动机器人和机械臂，并集成了 ROS2 节点支持。这些资产可直接用于 NVIDIA Isaac 平台的仿真与强化学习任务，便于开发者快速构建机器人应用场景。目标用户为使用 Isaac Sim 进行机器人开发与仿真的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/konu-droid/robots_usd?style=social)

- [Hunav_isaac_wrapper](https://github.com/robotics-upo/Hunav_isaac_wrapper) — 该项目是一个基于 NVIDIA Isaac Sim 构建的独立仿真封装器，用于集成 HuNavSim（人类导航模拟器），实现人群与机器人在 Isaac Sim 环境中的协同仿真。它通过 Python 接口将 HuNavSim 的行人行为模型嵌入 Isaac Sim 的 GPU 加速物理引擎中，支持复杂人机交互场景的快速部署。主要面向需要在高保真仿真中测试服务机器人导航策略的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/robotics-upo/Hunav_isaac_wrapper?style=social)

- [openarm_isaaclab_experiment](https://github.com/enactic/openarm_isaaclab_experiment) — 该项目旨在为 OpenArm 机器人在 Isaac Lab 环境中提供强化学习实验支持，利用 Isaac Sim 的 GPU 加速物理仿真能力进行机器人控制策略训练。项目基于 Isaac Lab 框架构建任务与环境，集成其传感器模拟和 RL 训练流程，适用于希望在高保真仿真中开发机械臂智能控制算法的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/enactic/openarm_isaaclab_experiment?style=social)

- [isaacsim_g1_locomotion](https://github.com/kdh4970/isaacsim_g1_locomotion) — 该项目提供了一个独立的 Python 脚本，用于在 Isaac Sim 中实现 Unitree G1 人形机器人的运动控制。它直接利用 Isaac Sim 的仿真环境和物理引擎，构建了 G1 机器人的运动策略与控制逻辑，适用于希望在 Isaac Sim 平台快速部署和测试人形机器人步态的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/kdh4970/isaacsim_g1_locomotion?style=social)

- [UavSwarm](https://github.com/juliorosa22/UavSwarm) — 该项目旨在利用Isaac Lab平台开发基于多智能体强化学习（MARL）的无人机集群导航任务。它直接构建于Isaac Lab之上，利用其GPU加速的物理仿真和机器人控制接口实现多UAV协同策略训练。项目面向希望在Isaac Sim生态中研究多智能体系统与自主导航的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/juliorosa22/UavSwarm?style=social)

- [GroundControl](https://github.com/UWRobotLearning/GroundControl) — 该项目是为地面自主系统开发的Isaac Sim扩展，提供在Isaac Sim中构建和测试地面机器人自主导航与控制算法的工具集。它深度集成Isaac Sim的仿真环境，利用其GPU加速物理引擎和传感器模拟功能，支持快速原型设计与算法验证。主要面向从事地面移动机器人研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/UWRobotLearning/GroundControl?style=social)

- [unittree-go2-usd](https://github.com/lancerzhang/unittree-go2-usd) — 该项目为Unitree Go2四足机器人提供专用于NVIDIA Isaac Sim的USD场景文件，包含完整的机器人模型与环境配置，便于在Isaac Sim中进行仿真、控制算法测试与强化学习训练。通过USD格式实现与Isaac Sim的原生集成，支持物理精确模拟和传感器仿真。主要面向使用Isaac Sim开发四足机器人应用的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/lancerzhang/unittree-go2-usd?style=social)

- [isaac-hrc](https://github.com/fdcl-gwu/isaac-hrc) — 该项目基于 Isaac Sim 构建人机协作（HRC）仿真环境，利用其 GPU 加速的物理引擎和传感器模拟能力，实现人类与机器人在共享工作空间中的安全交互。项目集成了 Isaac Sim 的 USD 场景构建、ROS 2 通信接口及行为策略模块，支持实时碰撞检测与动态路径规划。主要面向研究人机协作算法的机器人开发者与学术研究人员。 ![GitHub stars](https://img.shields.io/github/stars/fdcl-gwu/isaac-hrc?style=social)

- [pow](https://github.com/isaac-powerpack/pow) — 该项目是一个简化 Isaac Sim 与 Isaac ROS 开发的工具包，提供脚手架、配置管理和开发辅助功能，帮助开发者快速搭建和调试基于 Isaac Sim 的机器人仿真项目。其核心通过 TypeScript 实现，集成常用工作流模板和自动化脚本，降低 Isaac Sim 生态的入门门槛。主要面向使用 Isaac Sim 进行机器人仿真与 AI 训练的开发者。 ![GitHub stars](https://img.shields.io/github/stars/isaac-powerpack/pow?style=social)

- [IsaacSIM-Robot-Simulation](https://github.com/kdh4970/IsaacSIM-Robot-Simulation) — 该项目提供了一个多传感器移动机器人在Isaac Sim中的仿真配置方案，利用Python脚本集成激光雷达、相机等传感器，并基于Isaac Sim的PhysX和ROS 2接口实现环境感知与导航仿真。项目直接面向Isaac Sim平台构建，展示了典型机器人系统的端到端部署流程，适合希望快速搭建自主移动机器人仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/kdh4970/IsaacSIM-Robot-Simulation?style=social)

- [IsaacSim_DataCollector](https://github.com/qorgh346/IsaacSim_DataCollector) — 该项目利用NVIDIA Isaac Sim进行机器人控制与数据采集，提供Python脚本以自动化记录传感器数据、状态信息和动作指令。其核心功能围绕Isaac Sim的仿真环境构建，通过调用Isaac Sim API实现实时交互与高保真数据输出，适用于需要大规模训练数据的机器人学习研究者。 ![GitHub stars](https://img.shields.io/github/stars/qorgh346/IsaacSim_DataCollector?style=social)

- [Quadruped-Isaac-Sim](https://github.com/SKYBIRDSGP/Quadruped-Isaac-Sim) — 该项目旨在使用 Isaac Sim 模拟并控制四足机器人，实现其运动控制算法与步态生成。通过 Isaac Sim 的物理仿真环境，项目构建了四足机器人的动力学模型，并利用 Python 编写控制器以驱动机器人完成基本步态运动。主要面向希望在 Isaac Sim 中开发或测试四足机器人控制策略的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/SKYBIRDSGP/Quadruped-Isaac-Sim?style=social)

- [A1_Simulation_Isaac_Sim_Usage_Tutorial](https://github.com/userguide-galaxea/A1_Simulation_Isaac_Sim_Usage_Tutorial) — 该项目是一个面向 Isaac Sim 的使用教程，旨在帮助用户快速上手 NVIDIA Isaac Sim 仿真平台。内容涵盖 Isaac Sim 的基础操作、场景搭建及与机器人仿真的集成方法，基于 Python 编写示例脚本。目标用户为希望利用 Isaac Sim 进行机器人仿真与 AI 训练的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/userguide-galaxea/A1_Simulation_Isaac_Sim_Usage_Tutorial?style=social)

- [Isaac_vla](https://github.com/LouetteArthur/Isaac_vla) — 该项目为Isaac Lab环境提供视觉语言动作（VLA）模型的集成支持，主要用途是构建和测试结合视觉与语言指令的机器人控制策略。它利用Isaac Lab的GPU加速仿真能力，通过Jupyter Notebook实现交互式开发，包含针对VLA任务定制的环境配置和接口。目标用户为研究具身智能、多模态机器人学习的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/LouetteArthur/Isaac_vla?style=social)

- [legged_lab](https://github.com/xliu0105/legged_lab) — 该项目基于 Isaac Lab 框架训练足式机器人，实现了 Unitree A1 的跌倒恢复、盲走与连续后空翻，以及 Unitree H1 的舞蹈动作模仿。它直接利用 Isaac Lab 的强化学习和仿真环境，采用 Python 编写任务配置与训练逻辑，面向希望在 Isaac Sim 生态中开发高动态腿式机器人控制策略的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/xliu0105/legged_lab?style=social)

- [isaaclab_amp_rsl_rl](https://github.com/yoosunkyum/isaaclab_amp_rsl_rl) — 该项目基于 Isaac Lab 框架，结合 AMP（Adversarial Motion Priors）与 rsl_rl 强化学习库，用于训练人形或双足机器人在仿真环境中实现高动态运动控制。它利用 Isaac Sim 的 GPU 加速物理仿真能力，通过对抗性运动先验提升策略的自然性和稳定性，适用于希望在 Isaac Lab 生态中开发高级运动技能的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/yoosunkyum/isaaclab_amp_rsl_rl?style=social)

- [isaaclab_fetch_project](https://github.com/jih189/isaaclab_fetch_project) — 该项目基于 Isaac Lab 框架，实现了对 Fetch 机器人在 Isaac Sim 中的仿真控制与任务部署。通过集成 Isaac Lab 的强化学习和机器人学工具链，提供了针对 Fetch 机械臂的操作示例，利用 GPU 加速物理仿真进行策略训练或测试。主要面向希望在 Isaac Sim 生态中快速开发 Fetch 机器人应用的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/jih189/isaaclab_fetch_project?style=social)

- [leatherback.example.ackermann](https://github.com/boredengineering/leatherback.example.ackermann) — 该项目是一个面向 Isaac Sim 的阿克曼转向机器人示例，基于 Omniverse Kit 扩展开发，展示了如何在 Isaac Sim 中构建和控制差速或阿克曼底盘的车辆模型。它利用 Isaac Sim 的物理引擎和传感器模拟能力，为自动驾驶和移动机器人研究提供可复用的模板。目标用户为使用 Isaac Sim 进行机器人仿真与算法验证的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/boredengineering/leatherback.example.ackermann?style=social)

- [isaaclab-tutorial](https://github.com/danifuertes/isaaclab-tutorial) — 该项目是一个面向 Isaac Lab 的教程仓库，旨在帮助用户快速上手 NVIDIA Isaac Sim 中的 Isaac Lab 框架。通过 Python 示例代码，展示如何在 GPU 加速的物理仿真环境中构建和训练机器人策略。内容涵盖环境配置、任务定义与强化学习集成，适合希望利用 Isaac Lab 进行机器人仿真与 AI 训练的开发者。 ![GitHub stars](https://img.shields.io/github/stars/danifuertes/isaaclab-tutorial?style=social)

- [foot_reach](https://github.com/Hymwgk/foot_reach) — 该项目基于 Isaac Lab 实现了 Unitree Go2 机器人的足端目标到达任务，提供了一个轻量级强化学习训练环境。它利用 Isaac Sim 的 GPU 加速物理仿真能力，通过 Isaac Lab 框架构建自定义任务逻辑和奖励函数，支持高效策略训练。适用于希望在 Isaac Sim 生态中快速开发四足机器人控制算法的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/Hymwgk/foot_reach?style=social)

- [DeformableObjectGrasping](https://github.com/islexu/DeformableObjectGrasping) — 该项目是一个面向Isaac Sim的Omniverse扩展，专注于可变形物体的抓取仿真。它利用Isaac Sim的物理引擎和GPU加速能力，实现对柔性物体（如布料、软体）的建模与交互控制，包含抓取策略和传感器反馈集成。主要面向机器人学习与软体操作研究者，提供在Isaac Sim中快速部署和测试可变形物体操作任务的工具。 ![GitHub stars](https://img.shields.io/github/stars/islexu/DeformableObjectGrasping?style=social)

- [wheeled_bipedal_lab](https://github.com/L-SY/wheeled_bipedal_lab) — 该项目利用 Isaac Lab 和 Isaac Sim 对轮式双足机器人进行强化学习训练，展示了如何在 Isaac Sim 的 GPU 加速物理仿真环境中构建和部署机器人控制策略。项目基于 Python 实现，集成了 Isaac Lab 的任务框架与 Isaac Sim 的渲染及物理引擎，适用于希望在高保真仿真中开发混合移动机器人控制算法的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/L-SY/wheeled_bipedal_lab?style=social)

- [QuadrupedRobotSimulator](https://github.com/AuTURBO/QuadrupedRobotSimulator) — 该项目是一个基于 Isaac Sim 构建的四足机器人仿真器，利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能，实现高保真四足机器人的运动控制与环境交互仿真。项目通过 Python 脚本集成 Isaac Sim 的 API，支持自定义机器人模型与地形场景，适用于机器人算法开发与测试的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/AuTURBO/QuadrupedRobotSimulator?style=social)

- [IsaacSim_Routing](https://github.com/BruceLin90620/IsaacSim_Routing) — 该项目提供 Spot 机器人在 NVIDIA Isaac Sim 中进行导航仿真的完整设置与运行指南，基于 ROS 2 Humble 实现。它利用 Isaac Sim 的高保真物理和传感器模拟能力，结合 ROS 2 导航栈，实现路径规划与自主移动。项目包含环境配置、机器人模型加载及导航算法集成，适用于希望在 Isaac Sim 中开发或测试四足机器人导航系统的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/BruceLin90620/IsaacSim_Routing?style=social)

- [IsaacLabUR10eSim2Real](https://github.com/booooza/IsaacLabUR10eSim2Real) — 该项目基于 Isaac Lab 实现 UR10e 机械臂的视觉引导抓取任务，专注于从仿真到现实（Sim-to-Real）的迁移。它利用强化学习在 Isaac Sim 中训练策略，并通过域随机化和真实世界微调提升泛化能力，最终部署到物理机器人。主要面向使用 Isaac Lab 进行机器人 Sim-to-Real 研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/booooza/IsaacLabUR10eSim2Real?style=social)

- [CameraModel](https://github.com/orbbec/CameraModel) — 该项目提供奥比中光RGB-D相机的USD模型文件，专为Isaac Sim设计，用于在NVIDIA Isaac Sim中快速集成和仿真该深度相机。通过标准USD格式封装相机参数与外观，支持即插即用的传感器模拟，便于机器人开发者在高保真仿真环境中进行感知算法开发与测试。 ![GitHub stars](https://img.shields.io/github/stars/orbbec/CameraModel?style=social)

- [simple-joints-identification-isaaclab](https://github.com/iit-DLSLab/simple-joints-identification-isaaclab) — 该项目提供了一个简单的关节标定流程，旨在促进从 Isaac Lab 仿真环境到真实机器人的 sim-to-real 迁移。它通过在 Isaac Sim（Isaac Lab）中运行校准例程，识别并调整机器人关节的动力学参数，以缩小仿真与现实之间的差距。项目基于 Python 实现，适用于使用 Isaac Sim 进行强化学习和机器人仿真的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/iit-DLSLab/simple-joints-identification-isaaclab?style=social)

- [EasyUUV-Isaac-Simulation](https://github.com/360ZMEM/EasyUUV-Isaac-Simulation) — 该项目实现了论文《EasyUUV》中基于Isaac Sim的无人水下航行器（UUV）姿态控制仿真部分，利用NVIDIA Isaac Sim构建高保真水下物理环境，并集成强化学习与大语言模型（LLM）辅助策略优化。代码通过Isaac Sim的PhysX和流体动力学插件模拟水下扰动与推进效应，为UUV控制算法提供sim-to-real训练平台，主要面向水下机器人研究者与Isaac Sim开发者。 ![GitHub stars](https://img.shields.io/github/stars/360ZMEM/EasyUUV-Isaac-Simulation?style=social)

- [agent-world](https://github.com/sherndon79/agent-world) — 该项目提供了一套专为 Isaac Sim 设计的 Omniverse 扩展和 MCP 服务，用于构建、查看、勘测和记录仿真世界。它包含统一配置系统、航点数据库支持及数据采集工具，基于 Python 实现，旨在提升机器人仿真的效率与可管理性，适合使用 Isaac Sim 进行 AI 机器人开发的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/sherndon79/agent-world?style=social)

- [IsaacLab-Viser](https://github.com/uynitsuj/IsaacLab-Viser) — 该项目利用 Viser 实现 Isaac Lab 机器人仿真的无头开发与可视化，支持在无图形界面环境下远程查看和交互式调试仿真场景。通过集成 Viser 的 3D 渲染能力，为 Isaac Lab 提供轻量级、可扩展的可视化方案，适用于需要远程开发或服务器部署的机器人研究人员。 ![GitHub stars](https://img.shields.io/github/stars/uynitsuj/IsaacLab-Viser?style=social)

- [doosan-robot-isaac-driver](https://github.com/DoosanRobotics/doosan-robot-isaac-driver) — 该项目是斗山机器人官方提供的 Isaac Sim 驱动程序，用于在 NVIDIA Isaac Sim 中控制和仿真斗山机械臂。它通过 ROS 2 接口实现与 Isaac Sim 的深度集成，支持实时关节控制、状态反馈和传感器数据同步，基于 C++ 开发以确保低延迟性能。主要面向使用斗山机器人并希望在 Isaac Sim 中进行高保真仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/DoosanRobotics/doosan-robot-isaac-driver?style=social)

- [telesim_isaac](https://github.com/Ubb90/telesim_isaac) — 该项目是TelesimPnP遥操作系统的一部分，专为Isaac Sim设计，提供数字孪生环境下的简易遥操作功能。它通过Python实现与Isaac Sim的深度集成，支持实时控制机器人并同步物理仿真状态，适用于需要低延迟人机交互的机器人开发场景。目标用户为基于Isaac Sim进行遥操作或远程机器人实验的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Ubb90/telesim_isaac?style=social)

- [LeggedLab_wsy](https://github.com/wangsy1999/LeggedLab_wsy) — 该项目提供面向足式机器人的 Isaac Lab 直接工作流，基于 NVIDIA Isaac Sim 构建，专注于四足机器人仿真与控制策略开发。它利用 Isaac Lab 的模块化框架实现环境搭建、传感器模拟和强化学习训练，支持 GPU 加速的物理仿真。目标用户为从事足式机器人研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/wangsy1999/LeggedLab_wsy?style=social)

- [legged_rl_lab](https://github.com/ZihanWang0422/legged_rl_lab) — 该项目是一个基于Isaac Lab的扩展仓库，专注于腿式机器人（包括人形和四足）的强化学习研究，支持sim2sim2real工作流。它利用Isaac Sim的GPU加速物理仿真能力，提供针对运动控制与迁移学习的模块化训练框架。主要面向从事具身智能与机器人仿真的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/ZihanWang0422/legged_rl_lab?style=social)

- [leatherback.example.interactive](https://github.com/boredengineering/leatherback.example.interactive) — 该项目是一个 Omniverse Kit 扩展，允许用户通过第三人称视角与真实机器人进行交互式游戏控制。它明确面向 Isaac Sim 平台，利用其仿真环境实现虚实结合的机器人操控，基于 Python 开发并集成 NVIDIA Omniverse 生态。适用于希望在 Isaac Sim 中开发沉浸式人机交互应用的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/boredengineering/leatherback.example.interactive?style=social)

- [isaaclab-skrl](https://github.com/wmy-1/isaaclab-skrl) — 该项目将 Isaac Lab 与 skrl 强化学习库集成，提供在 Isaac Sim 环境中训练和部署机器人策略的示例与工具。它利用 Isaac Lab 的 GPU 加速物理仿真能力，并通过 skrl 实现模块化强化学习算法，支持 PPO、SAC 等主流方法。目标用户为希望在 Isaac Sim 生态中快速开展机器人强化学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/wmy-1/isaaclab-skrl?style=social)

- [at_factory](https://github.com/momoiorg-repository/at_factory) — 该项目提供了一个基于 Isaac Sim 5.0.0 的工厂仿真环境，利用其 GPU 加速的多物理引擎构建工业自动化场景。项目通过 Isaac Sim 实现产线布局、机器人协作与物流流程的高保真模拟，支持传感器仿真和数字孪生应用。主要面向智能制造研发人员和工业机器人系统集成商。 ![GitHub stars](https://img.shields.io/github/stars/momoiorg-repository/at_factory?style=social)

- [isaac_sim_voxposer](https://github.com/abigfreshman/isaac_sim_voxposer) — 该项目在Isaac Sim中重新实现了Voxposer，一个基于视觉语言模型的机器人任务规划框架。通过集成Isaac Sim的GPU加速物理仿真能力，该实现支持将高层自然语言指令转化为可执行的机器人动作序列，并利用场景体素化表示进行空间推理。目标用户为希望在高保真仿真环境中开发或测试具身智能任务规划算法的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/abigfreshman/isaac_sim_voxposer?style=social)

- [PX_IsaacSim_URDF_Importer](https://github.com/ProximityRobotics/PX_IsaacSim_URDF_Importer) — 该项目扩展了Isaac Sim内置的URDF导入器功能，提供示例脚本用于通过URDF文件快速构建机器人场景，并演示如何在Isaac Sim中集成ROS 2节点以控制导入的机器人。其核心基于Isaac Sim的Python API和USD工作流，适用于需要将真实机器人模型高效导入仿真环境并实现ROS 2通信的开发者。 ![GitHub stars](https://img.shields.io/github/stars/ProximityRobotics/PX_IsaacSim_URDF_Importer?style=social)

- [Drone-Stable-Hover-RL](https://github.com/NUSNiuMu/Drone-Stable-Hover-RL) — 该项目利用强化学习实现无人机在风扰环境下的稳定悬停，基于 Isaac Sim 构建高保真仿真环境并集成其物理引擎与传感器模型。通过 Isaac Sim 的 GPU 加速多物理场模拟能力，训练策略可有效应对动态干扰。主要面向机器人强化学习研究者及 Isaac Sim 开发者。 ![GitHub stars](https://img.shields.io/github/stars/NUSNiuMu/Drone-Stable-Hover-RL?style=social)

- [Nvidia-Isaac-Sim-Tree-Generator](https://github.com/joevento/Nvidia-Isaac-Sim-Tree-Generator) — 该项目是一个用于NVIDIA Isaac Sim的扩展工具，允许用户通过读取.txt文件批量生成大量树木模型，实现高效的大规模植被布置。它直接集成到Isaac Sim环境中，利用其场景构建能力，适用于需要复杂自然环境仿真的机器人或自动驾驶训练场景。目标用户为使用Isaac Sim进行高保真仿真开发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/joevento/Nvidia-Isaac-Sim-Tree-Generator?style=social)

- [Mapping--Navigation--and-Simulation-with-NVIDIA-Isaac-Sim---RTAB-Map---Nav2---RViz2](https://github.com/SaurabhKhimesra/Mapping--Navigation--and-Simulation-with-NVIDIA-Isaac-Sim---RTAB-Map---Nav2---RViz2) — 该项目提供了一个端到端的自主导航演示系统，核心使用 NVIDIA Isaac Sim 作为仿真环境，集成 RTAB-Map 实现 SLAM 建图、Nav2 进行路径规划与控制，并通过 RViz2 可视化。项目通过 ROS 2 桥接 Isaac Sim 与 Nav2/RTAB-Map，展示了 Isaac Sim 在机器人导航仿真中的关键作用，适用于希望在 Isaac Sim 中部署标准 ROS 2 导航栈的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/SaurabhKhimesra/Mapping--Navigation--and-Simulation-with-NVIDIA-Isaac-Sim---RTAB-Map---Nav2---RViz2?style=social)

- [FoodAssets](https://github.com/worv-ai/FoodAssets) — 该项目提供了一系列与食物相关的USD资产、材质及轻量级Python辅助工具，专为在Isaac Sim中快速生成和配置食物物品而设计。通过Omniverse Kit扩展形式集成，支持开发者高效构建餐饮、抓取或分拣等机器人仿真场景。目标用户为使用Isaac Sim进行食品相关机器人训练或仿真的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/worv-ai/FoodAssets?style=social)

- [oc-cobot](https://github.com/bemunin/oc-cobot) — 该项目展示了如何从零构建 NVIDIA Isaac Sim 场景，控制机械臂并集成 ROS2 生态系统，同时实验计算机视觉算法。它直接使用 Isaac Sim 作为核心仿真平台，通过 C++ 实现机器人控制与感知模块，适用于希望在 Isaac Sim 中开发 ROS2 兼容机器人应用的研究者和工程师。 ![GitHub stars](https://img.shields.io/github/stars/bemunin/oc-cobot?style=social)

- [HR_IsaacLab](https://github.com/junghs1040/HR_IsaacLab) — 该项目为基于Isaac Lab构建的人形机器人仿真环境，主要用于开发和测试人形机器人的运动控制与强化学习策略。它利用Isaac Sim的PhysX物理引擎和GPU加速能力，提供了定制化的任务场景与机器人模型，适配Isaac Lab的模块化框架。目标用户为从事人形机器人研究与仿真的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/junghs1040/HR_IsaacLab?style=social)

- [IsaacLab_avoid_obstacle](https://github.com/JEONGSE0/IsaacLab_avoid_obstacle) — 该项目基于强化学习实现机器人避障功能，专为 NVIDIA Isaac Lab 环境构建，利用其提供的仿真框架和 RL 训练基础设施。代码集成了 Isaac Lab 的任务定义、传感器模拟（如 LiDAR）和物理引擎，通过 PPO 算法训练智能体在复杂环境中导航。适用于希望在 Isaac Sim 生态中快速开发和测试自主导航策略的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/JEONGSE0/IsaacLab_avoid_obstacle?style=social)

- [remote_isaac_lab_docker](https://github.com/XinyuKhan/remote_isaac_lab_docker) — 该项目提供了一个 Docker 配置，用于在远程服务器上部署和运行 Isaac Lab（基于 Isaac Sim 的强化学习框架）。通过容器化方式简化了 Isaac Lab 的环境搭建，并支持远程访问，便于研究人员在无本地 GPU 的情况下使用 Isaac Sim 的 GPU 加速仿真能力。目标用户为需要远程开发或训练机器人策略的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/XinyuKhan/remote_isaac_lab_docker?style=social)

- [Isaac_Lab_UR5e_Lift_Cube](https://github.com/JonasFano/Isaac_Lab_UR5e_Lift_Cube) — 该项目利用强化学习在 Isaac Lab 中控制 UR5e 或 Franka 机械臂，通过微分逆运动学（differential IK）将立方体提升至目标位姿。代码基于 Isaac Lab 构建，展示了如何在其框架下实现机器人操作任务的训练与仿真，适用于希望在 Isaac Sim 生态中开发 RL 控制策略的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/JonasFano/Isaac_Lab_UR5e_Lift_Cube?style=social)

- [PickAndPlace](https://github.com/SamithVa/PickAndPlace) — 该项目使用 Isaac Lab 训练 Franka 机械臂执行抓取与放置任务，基于 Python 实现强化学习训练流程。它直接利用 Isaac Sim 的物理仿真与传感器模拟能力，结合 Isaac Lab 的机器人学习框架构建任务环境。适用于希望在 Isaac Sim 生态中开发机器人操作技能的研究者和工程师。 ![GitHub stars](https://img.shields.io/github/stars/SamithVa/PickAndPlace?style=social)

- [WobbleGo](https://github.com/noxrick91/WobbleGo) — WobbleGo 是一个面向初学者的 Isaac Lab 学习项目，实现了飞轮倒立摆（FIP）的仿真控制。该项目基于 Isaac Lab 构建，利用其强化学习和物理仿真能力，提供了一个结构清晰、易于理解的入门示例。适合希望快速上手 Isaac Lab 机器人仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/noxrick91/WobbleGo?style=social)

- [Isacclab-Docker](https://github.com/MouDARLEK/Isacclab-Docker) — 该项目提供了一个用于构建 Isaac Lab 开发环境的 Docker 配置，简化了 Isaac Sim 生态中 Isaac Lab 的本地部署流程。通过预配置的容器镜像，集成了必要的依赖和 CUDA 支持，便于用户快速启动基于 Isaac Sim 的机器人学习实验。主要面向希望高效搭建 Isaac Lab 仿真训练环境的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/MouDARLEK/Isacclab-Docker?style=social)

- [sim_footrl](https://github.com/kongbai666ciallo/sim_footrl) — 该项目在 Isaac Sim/Lab 环境中实现足式机器人强化学习（footrl），利用 Isaac Lab 提供的 GPU 加速物理仿真和 RL 训练框架，构建适用于四足或双足机器人的运动控制策略。项目基于 Isaac Lab 的任务定义、传感器模拟和训练流程，目标用户为研究足式机器人运动控制与强化学习的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/kongbai666ciallo/sim_footrl?style=social)

- [franka-ik](https://github.com/srianumakonda/franka-ik) — 该项目提供了一个用于 Franka 机械臂的数值逆运动学（IK）求解器，专为 Isaac Gym 环境设计。它利用 Jupyter Notebook 实现，通过迭代优化方法计算关节角度以达到目标末端位姿，可直接集成到基于 Isaac Gym 的强化学习或机器人控制流程中。适用于在 Isaac Sim 生态中开发 Franka 操作任务的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/srianumakonda/franka-ik?style=social)

- [ma_quadruped_lab](https://github.com/yan9900/ma_quadruped_lab) — 该项目是一个基于 Isaac Lab 构建的多智能体四足机器人仿真环境，利用 Isaac Sim 的 GPU 加速物理引擎和强化学习框架，实现了多个四足机器人的协同控制与训练。代码结构遵循 Isaac Lab 的任务与场景定义规范，支持自定义奖励函数和观测空间，适用于研究多智能体强化学习在复杂地形中的运动策略。目标用户为从事机器人多智能体系统研究的科研人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/yan9900/ma_quadruped_lab?style=social)

- [yhbot_navigation](https://github.com/ya7ya-hussein/yhbot_navigation) — 该项目基于PPO算法实现移动机器人导航，专为Isaac Lab环境构建，利用其GPU加速的物理仿真和强化学习接口进行训练。代码集成了Isaac Lab的机器人控制与传感器模拟功能，采用PyTorch实现策略网络，适用于希望在Isaac Sim生态中开发自主导航智能体的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/ya7ya-hussein/yhbot_navigation?style=social)

- [olympus_lab](https://github.com/ntnu-arl/olympus_lab) — 该项目为OLYMPUS项目提供基于Isaac Lab的强化学习环境，利用Isaac Sim的GPU加速物理仿真能力构建机器人训练场景。它直接集成Isaac Lab框架，实现高性能、可扩展的RL训练流程，适用于需要在逼真模拟环境中开发和测试机器人策略的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/ntnu-arl/olympus_lab?style=social)

- [reach_standalone](https://github.com/kabirraymalik/reach_standalone) — 该项目提供了一个基于 Isaac Lab 的强化学习环境，用于训练机械臂的定位与抓取策略。它利用 Isaac Sim 的 GPU 加速物理仿真能力，结合 RL 算法实现高效策略学习，适用于机器人操作任务研究。目标用户为使用 Isaac Sim/Isaac Lab 进行机器人感知与控制开发的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/kabirraymalik/reach_standalone?style=social)

- [isaac_tutorial](https://github.com/rise-lab-skku/isaac_tutorial) — 该项目提供面向 Isaac Gym 和 Isaac Sim 的入门教程，涵盖基础环境搭建、机器人仿真及强化学习示例。内容专为初学者设计，通过 Python 脚本演示如何在 Isaac Sim 平台中加载资产、配置传感器和运行物理仿真。目标用户为希望快速上手 NVIDIA Isaac 机器人仿真生态的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/rise-lab-skku/isaac_tutorial?style=social)

- [ACT4IsaacSim](https://github.com/ssapsu/ACT4IsaacSim) — 该项目用于在 Isaac Sim 中部署和运行 ACT（Action Chunking with Transformers）策略，支持基于模仿学习的机器人控制。它集成了 ROS 2 Humble 接口，并利用 Isaac Sim 的 GPU 加速仿真环境进行策略测试与数据生成。主要面向从事机器人模仿学习与仿真训练的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/ssapsu/ACT4IsaacSim?style=social)

- [IsaacSIM_Jackal_Navigation](https://github.com/qorgh346/IsaacSIM_Jackal_Navigation) — 该项目基于 Isaac Sim 和 ROS 实现了 Jackal 机器人导航功能，利用 Isaac Sim 的 GPU 加速仿真环境进行机器人定位与路径规划。通过 ROS 与 Isaac Sim 的集成，构建了完整的导航栈，适用于在高保真仿真中开发和测试自主移动机器人算法。目标用户为使用 Isaac Sim 进行机器人导航研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/qorgh346/IsaacSIM_Jackal_Navigation?style=social)

- [SoftRobot_IsaacSim](https://github.com/SIRGLab/SoftRobot_IsaacSim) — 该项目在 Isaac Sim 中实现了连续体软体机器人的仿真，利用其 GPU 加速的物理引擎对柔性结构进行建模与控制。通过自定义关节和材料属性，支持高保真软体机器人动力学模拟，适用于需要在 Isaac Sim 环境中开发或测试软体机器人算法的研究人员。 ![GitHub stars](https://img.shields.io/github/stars/SIRGLab/SoftRobot_IsaacSim?style=social)

- [isaac-sim-ros-agent](https://github.com/Isaacsimkr-2nd/isaac-sim-ros-agent) — 该项目旨在通过集成NASA的ROSA（Robot Operating System Agent）与NVIDIA Isaac Sim，增强基于ROS2的自主机器人仿真能力。它利用Isaac Sim的GPU加速多物理场仿真环境，为ROSA提供高保真传感器模拟和实时交互接口，支持复杂决策与控制算法的开发与测试。主要面向使用ROS2和Isaac Sim进行智能机器人研发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Isaacsimkr-2nd/isaac-sim-ros-agent?style=social)

- [twip-isaac-sim](https://github.com/TheNewtonCapstone/twip-isaac-sim) — 该项目基于 Isaac Sim 构建，用于在仿真环境中训练和测试两轮倒立摆（TWIP）机器人的强化学习策略。它利用 Isaac Gym 的 GPU 加速物理仿真能力，实现高效的 RL 训练流程，并支持将训练好的策略迁移到真实机器人。项目包含完整的任务定义、奖励函数和域随机化配置，适用于希望在 Isaac Sim 中开展机器人控制研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/TheNewtonCapstone/twip-isaac-sim?style=social)

- [IsaacSim_ObjectDetection_learning](https://github.com/Johnny-Hu-406/IsaacSim_ObjectDetection_learning) — 该项目旨在开发草莓采摘机器人，利用 Isaac Sim 构建虚拟仿真环境，集成 YOLO 目标检测模型进行成熟草莓识别与导航决策训练，并将训练好的策略部署至真实机器人。项目直接基于 Isaac Sim 平台实现感知-决策-控制闭环，展示了其在农业机器人仿真与迁移学习中的应用。适合关注 Isaac Sim 在具体机器人任务中端到端训练与部署的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/Johnny-Hu-406/IsaacSim_ObjectDetection_learning?style=social)

- [isaac_sim_grasp_splats](https://github.com/trushant05/isaac_sim_grasp_splats) — 该项目用于在 NVIDIA Isaac Sim 中训练、仿真和评估基于高斯泼溅（Gaussian Splatting）的抓取模型 Grasp Splats，通过合成数据生成与机器人操作任务紧密结合。项目直接利用 Isaac Sim 的 GPU 加速物理仿真能力，为机械臂抓取任务提供逼真的视觉与交互环境。主要面向从事机器人抓取感知与仿真研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/trushant05/isaac_sim_grasp_splats?style=social)

- [Deploy-Tutorial-A1-Simulation](https://github.com/Nagato-Yukii/Deploy-Tutorial-A1-Simulation) — 该项目是一个面向A1机器人的Isaac Sim使用与部署教程，详细介绍了如何在Isaac Sim中配置和运行A1四足机器人的仿真环境。教程涵盖USD场景搭建、机器人URDF导入、传感器配置及与Isaac Sim内置工具链（如Replicator和Omniverse）的集成方法，适合希望快速上手Isaac Sim进行四足机器人仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Nagato-Yukii/Deploy-Tutorial-A1-Simulation?style=social)

- [isaac-sim-2023.1.1-humble-Dockerfile](https://github.com/eunseon02/isaac-sim-2023.1.1-humble-Dockerfile) — 该项目提供了一个 Dockerfile，用于构建包含 Isaac Sim 2023.1.1 和 ROS 2 Humble 的容器环境，便于在隔离环境中运行 Isaac Sim 并与 ROS 2 集成。通过预配置的依赖和环境变量，简化了 Isaac Sim 与 ROS 2 节点通信的设置流程。适用于需要在 Docker 中开发或部署 Isaac Sim 与 ROS 2 联合仿真应用的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/eunseon02/isaac-sim-2023.1.1-humble-Dockerfile?style=social)

- [CartpoleSKRL](https://github.com/felipemohr/CartpoleSKRL) — 该项目提供使用SKRL强化学习库在Isaac Sim中训练Cartpole环境的脚本，展示了如何将SKRL与Isaac Sim集成以实现GPU加速的物理仿真和策略训练。代码基于Python实现，利用了Isaac Sim的高性能模拟能力，适用于希望快速上手Isaac Sim与SKRL结合进行机器人控制实验的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/felipemohr/CartpoleSKRL?style=social)

- [Multi-agent-LLM-Humanoid-Robot-Control-With-Isaac-Gr00t-Integration-in-Isaac-Simulator](https://github.com/jwcha1030/Multi-agent-LLM-Humanoid-Robot-Control-With-Isaac-Gr00t-Integration-in-Isaac-Simulator) — 该项目旨在通过多智能体大语言模型（LLM）实现人形机器人的高层决策与控制，并深度集成NVIDIA Isaac Gr00t框架，在Isaac Sim中进行仿真验证。它利用Isaac Sim的GPU加速物理引擎和Gr00t提供的具身智能接口，实现自然语言指令到机器人动作的端到端映射，适用于研究LLM驱动的具身智能与多机器人协作的科研人员。 ![GitHub stars](https://img.shields.io/github/stars/jwcha1030/Multi-agent-LLM-Humanoid-Robot-Control-With-Isaac-Gr00t-Integration-in-Isaac-Simulator?style=social)

- [Multi-object-grasping-with-dexterous-robot-hand-in-simulation](https://github.com/Henry-Kim-00/Multi-object-grasping-with-dexterous-robot-hand-in-simulation) — 该项目在 NVIDIA Isaac Sim 中实现灵巧手对多物体的抓取仿真，利用 Isaac Sim 的 GPU 加速物理引擎和机器人 SDK 构建抓取策略与环境交互。项目包含 URDF 模型集成、传感器配置及基于强化学习或规划的抓取控制逻辑，适用于研究多物体操作与灵巧手控制的机器人学者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/Henry-Kim-00/Multi-object-grasping-with-dexterous-robot-hand-in-simulation?style=social)

- [isaacsim5.0_ros2_go2](https://github.com/tosemfdk/isaacsim5.0_ros2_go2) — 该项目旨在通过 ROS 2 框架实现对 Unitree Go2 四足机器人的完整控制，并将其集成到 Isaac Sim 5.0 仿真环境中。项目利用 Isaac Sim 的 GPU 加速物理仿真能力，结合 ROS 2 的通信机制，构建机器人控制与感知的闭环系统。主要面向希望在 Isaac Sim 中开发和测试四足机器人算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/tosemfdk/isaacsim5.0_ros2_go2?style=social)

- [ros2-agv-navigation-stack-Isaac-Sim](https://github.com/AndresIslas99/ros2-agv-navigation-stack-Isaac-Sim) — 该项目提供了一个面向生产的 ROS2 导航栈，集成了 RTAB-Map 3D SLAM，专为在 Isaac Sim 中运行的 AGV/AMR 平台设计。它通过 ROS2 与 Isaac Sim 的仿真环境深度集成，支持高保真传感器模拟和实时导航算法验证。目标用户为需要在 Isaac Sim 中开发和测试自主移动机器人导航系统的工程师与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/AndresIslas99/ros2-agv-navigation-stack-Isaac-Sim?style=social)

- [Isaacsim_ros2_multi_robots](https://github.com/killianpinier/Isaacsim_ros2_multi_robots) — 该项目提供了一个ROS 2工作空间，用于在NVIDIA Isaac Sim中同时运行两个Franka Emika Panda机器人，并通过命名空间（panda1和panda2）隔离话题与参数以避免冲突。项目直接集成Isaac Sim的ROS 2桥接功能，利用其GPU加速的多物理仿真能力实现多机器人协同控制，适用于需要在Isaac Sim中开发和测试多臂机器人系统的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/killianpinier/Isaacsim_ros2_multi_robots?style=social)

- [RosIsaacSimWarehouseCarterx10](https://github.com/MUFacultyOfEngineering/RosIsaacSimWarehouseCarterx10) — 该项目基于 Isaac Sim 的 ROS 工作区进行定制，用于在“简易仓库”场景中同时控制 10 台 Carter 机器人。通过 ROS 与 Isaac Sim 深度集成，实现多机器人协同仿真，利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能。适用于需要大规模移动机器人集群仿真的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/MUFacultyOfEngineering/RosIsaacSimWarehouseCarterx10?style=social)

- [Pick-Place_Imitation-Learning-Isaac-sim-ROS2](https://github.com/uiseoklee/Pick-Place_Imitation-Learning-Isaac-sim-ROS2) — 该项目基于模仿学习实现机器人抓取与放置任务，核心仿真平台为NVIDIA Isaac Sim，并通过ROS2进行通信集成。项目利用Isaac Sim的高保真物理仿真能力构建训练环境，结合Python脚本实现行为克隆算法，适用于希望在Isaac Sim中开发ROS2兼容的机器人操作任务的研究者和工程师。 ![GitHub stars](https://img.shields.io/github/stars/uiseoklee/Pick-Place_Imitation-Learning-Isaac-sim-ROS2?style=social)

- [simlab](https://github.com/RoryMB/simlab) — 该项目是一个面向自主实验室环境的仿真平台，主要整合了Isaac Sim与MADSci框架，用于科学实验协议的自动化研究。它利用Isaac Sim的GPU加速多物理仿真能力，构建可编程、可感知的虚拟实验室场景，支持机器人执行复杂实验流程。目标用户为从事自动化科研、AI驱动实验平台开发的研究人员。 ![GitHub stars](https://img.shields.io/github/stars/RoryMB/simlab?style=social)

- [ocean_frontier_exploration](https://github.com/umfieldrobotics/ocean_frontier_exploration) — 该项目是一个基于 ROS 2 的水下机器人前沿探索框架，专为在 Isaac Sim 的 OceanSim 环境中运行而设计。它通过 ROS 2 话题与 Isaac Sim 深度集成，提供建图、前沿检测和控制流水线，利用声学与视觉传感实现自主探索。主要面向水下机器人研究人员和开发者，适用于在 Isaac Sim 中开发和测试自主探索算法。 ![GitHub stars](https://img.shields.io/github/stars/umfieldrobotics/ocean_frontier_exploration?style=social)

- [manipulation-lab](https://github.com/j9smith/manipulation-lab) — 该项目是一个基于 NVIDIA Isaac Sim 构建的框架，专注于实现机器人操作任务中模仿学习算法的评估与基准测试。它利用 Isaac Sim 的 GPU 加速物理仿真能力，提供标准化环境以复现和比较不同模仿学习方法的性能。目标用户为从事机器人学习与仿真的研究人员及开发者。 ![GitHub stars](https://img.shields.io/github/stars/j9smith/manipulation-lab?style=social)

- [dual_robot_arm](https://github.com/emusman-lab/dual_robot_arm) — 该项目展示了在 NVIDIA Isaac Sim 4.2.0 中使用 MoveIt 2 和 MoveIt Task Constructor 对双 Dobot Nova5 机械臂进行仿真与操作。项目通过 ROS 2 与 Isaac Sim 深度集成，利用其 GPU 加速的物理引擎实现高保真多机器人协同任务仿真，适用于需要复杂运动规划和任务编排的机器人研究场景。 ![GitHub stars](https://img.shields.io/github/stars/emusman-lab/dual_robot_arm?style=social)

- [IsaacLabBittle](https://github.com/dkechrisBU/IsaacLabBittle) — 该项目为Bittle四足机器人在Isaac Lab环境中实现强化学习训练提供专用配置和任务文件。它基于Isaac Sim的Isaac Lab框架，利用其GPU加速的物理仿真和RL工具链，定义了适用于Bittle的运动控制任务和奖励函数。目标用户是希望在Isaac Lab中快速部署和训练Bittle机器人的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/dkechrisBU/IsaacLabBittle?style=social)

- [IsaacLab_delto_envs](https://github.com/VAlikV/IsaacLab_delto_envs) — 该项目基于Isaac Lab构建了用于强化学习和控制实验的仿真环境，集成了Tesollo Delto机械臂模型。通过利用Isaac Sim的GPU加速物理引擎和传感器模拟功能，实现了高保真、高性能的机器人控制训练场景。主要面向使用Isaac Lab进行机器人学习算法开发的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/VAlikV/IsaacLab_delto_envs?style=social)

- [IsaacLabPouringExtension](https://github.com/robegi/IsaacLabPouringExtension) — 该项目是一个 Isaac Lab 扩展，用于训练智能体执行液体倾倒任务。它基于 Isaac Sim 的物理仿真能力，利用 GPU 加速的流体动力学模拟实现高保真 pouring 场景，并集成了强化学习训练流程。主要面向机器人操作与流体交互研究领域的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/robegi/IsaacLabPouringExtension?style=social)

- [Isaac_Lab_Husky](https://github.com/Kerkane/Isaac_Lab_Husky) — 该项目为Clearpath Husky机器人在Isaac Lab环境中的集成提供支持，主要用途是实现该移动机器人平台在NVIDIA Isaac Sim中的仿真与控制。项目基于Isaac Lab框架构建，利用其模块化机器人建模和强化学习训练能力，适配Husky的URDF模型及传感器配置。目标用户为希望在Isaac Sim中快速部署和测试Husky机器人算法的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/Kerkane/Isaac_Lab_Husky?style=social)

- [go2_isaac_lab](https://github.com/YumaMatsumura/go2_isaac_lab) — 该项目为Unitree Go2四足机器人在Isaac Lab环境中的仿真与控制提供支持，包含针对Go2的资产配置、运动控制器和任务定义，利用Isaac Lab的GPU加速物理引擎实现高保真机器人仿真。项目直接基于Isaac Lab框架构建，适用于希望在NVIDIA Isaac Sim生态中开发或测试四足机器人算法的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/YumaMatsumura/go2_isaac_lab?style=social)

- [isaac-importer](https://github.com/pearl-robot-lab/isaac-importer) — 该项目是一个用于将 Blender 创建的环境导入到 Isaac Sim 中的工具，通过解析 Blender 导出的 USD 或 glTF 格式并转换为 Isaac Sim 兼容的场景结构，简化了自定义仿真环境的构建流程。其核心功能聚焦于 Isaac Sim 与 Blender 生态的衔接，适用于需要在 Isaac Sim 中复用复杂 3D 场景的机器人研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/pearl-robot-lab/isaac-importer?style=social)

- [isaaclab_so100](https://github.com/narcispr/isaaclab_so100) — 该项目为SO100机械臂在Isaac Lab环境中提供了多个强化学习任务的实现，基于Python开发，利用Isaac Sim的GPU加速物理仿真能力进行机器人控制策略训练。它直接构建于Isaac Lab框架之上，包含针对该机械臂的专用配置、资产和训练脚本，适用于希望在Isaac Sim生态中开展具身智能与机器人强化学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/narcispr/isaaclab_so100?style=social)

- [F1Tenth-RL](https://github.com/Squidtoon99/F1Tenth-RL) — 该项目是一个基于 Isaac Lab 的强化学习训练平台，专注于自动驾驶赛车（F1Tenth）的智能体开发。它利用 Isaac Lab 提供的 GPU 加速物理仿真环境，构建高保真赛道场景并集成 RL 算法进行车辆控制策略训练。目标用户为研究自动驾驶与强化学习在 Isaac Sim 生态中应用的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Squidtoon99/F1Tenth-RL?style=social)

- [affordance-learning-sandbox](https://github.com/Pipe-Runner-Lab/affordance-learning-sandbox) — 该项目是一个基于GPU物理仿真的可供性学习沙盒，利用强化学习探索物体交互设计。它明确构建于NVIDIA Omniverse平台，并直接集成Isaac Sim作为核心仿真环境，通过其GPU加速的多物理引擎实现高保真交互模拟。主要面向机器人感知与交互研究者，尤其适用于开发和测试在Isaac Sim中运行的可供性学习算法。 ![GitHub stars](https://img.shields.io/github/stars/Pipe-Runner-Lab/affordance-learning-sandbox?style=social)

- [ti5_isaaclab](https://github.com/Kong-Huiyang/ti5_isaaclab) — 该项目基于 Isaac Lab 框架实现人形机器人的强化学习训练，利用 Isaac Sim 提供的 GPU 加速物理仿真环境，构建适用于双足行走控制的任务场景。项目集成了 Isaac Lab 的 RL 训练流程与机器人建模工具，目标用户为从事人形机器人运动控制研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Kong-Huiyang/ti5_isaaclab?style=social)

- [GR00T-N1.5-PiPER](https://github.com/jundaree/GR00T-N1.5-PiPER) — 该项目基于 NVIDIA 的 Isaac-GR00T 仓库，专为 Agilex Robotics 的 PiPER 机械臂提供支持，利用 Isaac Sim 进行机器人策略训练与仿真。通过集成 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能，实现对 PiPER 机器人的运动控制与任务学习。主要面向希望在 Isaac Sim 生态中开发或适配新型机械臂的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/jundaree/GR00T-N1.5-PiPER?style=social)

- [isaacgym-anymal-training](https://github.com/sathwik58/isaacgym-anymal-training) — 该项目使用近端策略优化（PPO）在NVIDIA Isaac Gym中训练ANYmal-C四足机器人实现稳健的地形自适应行走，基于PyTorch构建了actor-critic神经网络控制策略。代码专为Isaac Gym环境设计，直接利用其GPU加速的物理仿真能力进行高效强化学习训练，适用于希望在Isaac Sim生态中开发四足机器人运动控制的研究者和工程师。 ![GitHub stars](https://img.shields.io/github/stars/sathwik58/isaacgym-anymal-training?style=social)

- [RoboticArm-RL](https://github.com/grgcncr/RoboticArm-RL) — 该项目使用强化学习训练智能体控制Franka Emika Panda机械臂抓取立方体，基于Isaac Sim构建仿真环境并利用其GPU加速的物理引擎实现高效训练。项目集成了Isaac Sim的机器人控制接口与传感器模拟功能，适用于希望在高保真仿真中开发机械臂操作策略的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/grgcncr/RoboticArm-RL?style=social)

- [Galaxea_Lab](https://github.com/Robotic-Developer-Road/Galaxea_Lab) — 该项目主要用于将 Galaxea_Lab 从 Isaac Sim 2023 版本迁移到 Isaac Sim 4.5.0，确保其在新版平台上的兼容性与功能适配。项目通过更新 Python 脚本和配置文件，解决 API 变更、场景加载及传感器接口等关键迁移问题，直接面向 Isaac Sim 生态用户提供版本升级支持。 ![GitHub stars](https://img.shields.io/github/stars/Robotic-Developer-Road/Galaxea_Lab?style=social)

- [ur5_isaaclab](https://github.com/ManggoF/ur5_isaaclab) — 该项目在 Isaac Lab 中实现了 UR5 机器人强化学习任务，提供操作机器人及仿真环境中资产的示例。它直接基于 Isaac Lab 构建，利用其 RL 框架和 GPU 加速物理仿真能力，适用于希望在 Isaac Sim 生态中开发机械臂控制策略的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/ManggoF/ur5_isaaclab?style=social)

- [dropbear_isaac](https://github.com/Hyperspawn/dropbear_isaac) — 该项目为 Dropbear 机器人提供在 Isaac Sim 和 Isaac Lab 环境中的训练与仿真支持，明确面向 NVIDIA 的 Isaac 平台构建。它利用 Isaac Sim 的 GPU 加速物理仿真和 Isaac Lab 的强化学习框架，实现机器人控制策略的开发与测试。目标用户为使用 Isaac 生态进行机器人仿真的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/Hyperspawn/dropbear_isaac?style=social)

- [IsaacSimExamples](https://github.com/kickthemoon0817/IsaacSimExamples) — 该项目提供了一系列 Isaac Sim 的使用示例，涵盖机器人仿真、传感器模拟和场景搭建等常见任务。代码基于 Python 编写，利用 Isaac Sim 的 API 展示了如何构建和控制仿真环境，适合初学者和开发者快速上手 Isaac Sim 平台。 ![GitHub stars](https://img.shields.io/github/stars/kickthemoon0817/IsaacSimExamples?style=social)

- [wcr_diplomski](https://github.com/marijamacek/wcr_diplomski) — 该项目为4WIS4WID全向移动机器人在Isaac Sim/Isaac Lab环境中提供仿真与控制实现，利用Isaac Lab的强化学习框架和GPU加速物理引擎构建机器人模型与任务环境。项目包含自定义机器人URDF、传感器配置及运动控制策略，适用于研究多轮独立驱动/转向系统的导航与控制算法。目标用户为基于Isaac Sim开展移动机器人仿真的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/marijamacek/wcr_diplomski?style=social)

- [physical-ai-lab](https://github.com/myidentity/physical-ai-lab) — 该项目提供面向 Isaac Sim 与 Isaac Lab 的教程资源，帮助用户快速上手 NVIDIA 的物理 AI 开发平台。内容涵盖环境搭建、基础仿真任务及与 Isaac Lab 的集成示例，采用 HTML 格式组织教学材料。目标用户为希望利用 Isaac Sim 进行机器人仿真与强化学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/myidentity/physical-ai-lab?style=social)

- [Isaac-Sim-with-Gr00t-Tutorial](https://github.com/donghoYee/Isaac-Sim-with-Gr00t-Tutorial) — 该项目提供了一个结合 Isaac Sim 与 Gr00t 框架的教程，演示如何在 Isaac Sim 中集成 Gr00t 实现机器人任务规划与执行。通过 Python 脚本调用 Isaac Sim 的仿真环境，并利用 Gr00t 的行为树和任务编排能力控制虚拟机器人。适合希望在 Isaac Sim 中探索高级任务自动化和人机协作仿真的开发者。 ![GitHub stars](https://img.shields.io/github/stars/donghoYee/Isaac-Sim-with-Gr00t-Tutorial?style=social)

- [Isaac-Sim-5.1-IsaacLab-Full-Install-Train-Play-Headless-WebRTC-](https://github.com/maduwanthasl/Isaac-Sim-5.1-IsaacLab-Full-Install-Train-Play-Headless-WebRTC-) — 该项目提供在无Docker环境下于服务器上完整安装Isaac Sim 5.1与Isaac Lab的详细流程，并支持无头（headless）模式运行、WebRTC远程可视化以及训练与推理全流程。其核心价值在于为无法使用容器化部署的用户提供了原生安装方案，涵盖依赖配置、GPU驱动适配及WebRTC流媒体集成，适用于希望在远程服务器上高效开发和测试机器人仿真的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/maduwanthasl/Isaac-Sim-5.1-IsaacLab-Full-Install-Train-Play-Headless-WebRTC-?style=social)

- [isaac-hpc](https://github.com/npho/isaac-hpc) — 该项目旨在构建一个原生支持 Apptainer 的 Isaac Sim 环境，便于在高性能计算（HPC）集群中部署和运行 Isaac Sim。通过容器化封装 Isaac Sim 及其依赖，解决了在多用户 HPC 系统中环境隔离与 GPU 资源调度的难题，利用 Apptainer 实现安全、可复现的仿真工作流。主要面向需要在 HPC 平台上规模化运行 Isaac Sim 仿真的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/npho/isaac-hpc?style=social)

- [RLHumanoid_Ver2](https://github.com/DanielTruong99/RLHumanoid_Ver2) — 该项目基于 Isaac Lab 扩展模板，针对新版 Isaac Sim 和 Isaac Lab 进行了适配修改，主要用于人形机器人强化学习任务。它利用 Isaac Sim 的 GPU 加速物理仿真能力，结合 Isaac Lab 的 RL 框架，实现高效训练流程。目标用户为在 Isaac Sim 生态中开发人形机器人控制策略的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/DanielTruong99/RLHumanoid_Ver2?style=social)

- [omniverse-synthetic-data-generation](https://github.com/franklinselva/omniverse-synthetic-data-generation) — 该项目基于 Isaac Sim 构建，专注于利用 Omniverse 平台生成合成数据，适用于机器人感知和 AI 训练任务。通过 Jupyter Notebook 提供可交互的脚本，调用 Isaac Sim 的渲染与传感器模拟能力（如 RGB、深度、语义分割等），自动化生成带标注的多模态数据集。目标用户为需要高效构建高质量合成训练数据的机器人与计算机视觉开发者。 ![GitHub stars](https://img.shields.io/github/stars/franklinselva/omniverse-synthetic-data-generation?style=social)

- [Isaac-Sim-PX4](https://github.com/uditray02/Isaac-Sim-PX4) — 该项目提供在 Isaac Sim 中进行无人机编程的完整框架，通过集成 PX4 飞控与 ROS 2 实现高保真仿真。它利用 Isaac Sim 的多旋翼动力学模型和传感器模拟能力，结合 MAVSDK 控制接口，支持目标检测（YOLO）与集群飞行（Swarming）等高级功能。主要面向基于 Isaac Sim 开发自主无人机系统的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/uditray02/Isaac-Sim-PX4?style=social)

- [warehouse_simulation](https://github.com/YonduAI/warehouse_simulation) — 该项目利用 Isaac Sim 在仓库环境中模拟可变形物体（如软体物品）的物理行为，专注于物流场景下的抓取与操作任务。通过 Isaac Sim 的 GPU 加速多物理引擎实现高保真软体动力学仿真，并集成 ROS 2 接口以支持机器人控制算法开发。主要面向仓储自动化领域的研究人员和机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/YonduAI/warehouse_simulation?style=social)

- [isaac-sim-franka](https://github.com/franklinselva/isaac-sim-franka) — 该项目提供在 Isaac Sim 4.0.0 中控制 Franka Emika Panda 机械臂的 Python 示例，通过 Isaac Sim 的 USD 和 PhysX 引擎实现机器人关节控制与交互。代码展示了如何加载 Panda 机器人模型、配置关节驱动器并实现基本运动控制，适用于希望在 Isaac Sim 中快速上手真实机器人仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/franklinselva/isaac-sim-franka?style=social)

- [uav-nav-isaac-sim](https://github.com/vhdang-upb-acgroup/uav-nav-isaac-sim) — 该项目在Isaac Sim中构建了无人机（UAV）导航仿真场景，利用其GPU加速的物理引擎和传感器模拟功能，实现基于Python的自主飞行控制与环境交互。项目直接面向Isaac Sim平台开发，包含无人机动力学建模、路径规划及感知模块集成，适用于机器人研究人员和自动驾驶开发者。 ![GitHub stars](https://img.shields.io/github/stars/vhdang-upb-acgroup/uav-nav-isaac-sim?style=social)

- [IsaacSim-Pegasus-Environment](https://github.com/BjarkeHJ/IsaacSim-Pegasus-Environment) — 该项目提供了一个基于 Isaac Sim 的空中飞行器仿真环境，利用 PegasusSim 框架实现无人机动力学与控制的高保真模拟。它通过 Isaac Sim 的 GPU 加速物理引擎和传感器模型，支持复杂空域场景下的自主飞行算法开发与测试。主要面向从事无人机或空中机器人研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/BjarkeHJ/IsaacSim-Pegasus-Environment?style=social)

- [sim-env](https://github.com/ToothlessOS/sim-env) — 该项目提供了一个专为 Isaac Sim 与 Isaac Lab 设计的配套仿真环境，通过 Python 实现与 NVIDIA Isaac 平台的集成，支持机器人算法的快速部署与测试。其核心功能包括场景配置管理、传感器模拟及与 Isaac Sim 的通信接口封装，便于开发者构建定制化训练或验证流程。目标用户为使用 Isaac Sim/Lab 进行机器人仿真与强化学习研究的工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/ToothlessOS/sim-env?style=social)

- [dp_franka_with_heatmap](https://github.com/li-rh/dp_franka_with_heatmap) — 该项目在Isaac Sim环境中实现基于热力图（affordance）的扩散策略（Diffusion Policy），用于Franka机械臂的视觉引导操作。通过将热力图作为动作条件输入扩散模型，提升机器人对可交互区域的感知能力，并利用Isaac Sim提供的GPU加速物理仿真进行高效训练与验证。适用于研究具身智能与视觉-动作联合理论的机器人学习开发者。 ![GitHub stars](https://img.shields.io/github/stars/li-rh/dp_franka_with_heatmap?style=social)

- [magnav_isaac_sim](https://github.com/aprilab-uf/magnav_isaac_sim) — 该项目提供了一个基于Isaac Sim的仿真环境，用于集成和测试基于神经网络的磁力计系统。它利用Isaac Sim的高保真传感器模拟能力，实现对磁力计数据的生成与处理，并支持与神经网络模型的联合训练或验证。目标用户为从事导航、SLAM或磁传感研究的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/aprilab-uf/magnav_isaac_sim?style=social)

- [Z1_ISAACSIM](https://github.com/NicoleKJ9721/Z1_ISAACSIM) — 该项目为Unitree Z1机器人提供Isaac Sim扩展，支持URDF模型导入与RMPflow运动控制。通过集成Isaac Sim的仿真环境，实现对Z1机械臂的高保真动力学模拟与实时控制策略部署。主要面向使用Isaac Sim进行机器人算法开发与仿真的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/NicoleKJ9721/Z1_ISAACSIM?style=social)

- [isaac-autogen-sim](https://github.com/Whynotus777/isaac-autogen-sim) — 该项目是一个基于 NVIDIA Isaac Lab 的自主仿真平台，利用 PyTorch 和 AutoGen 多智能体框架实现 AI 驱动的物理仿真。它将 Isaac Lab 作为核心仿真环境，集成多智能体协作与强化学习能力，支持复杂机器人任务的自动化训练与测试。主要面向希望在 Isaac Sim 生态中开发多智能体 AI 仿真的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/Whynotus777/isaac-autogen-sim?style=social)

- [agilebot_isaac_sim](https://github.com/sh-agilebot/agilebot_isaac_sim) — 该项目为Agilebot机器人提供Isaac Sim集成与仿真配置，包含启动脚本和演示示例，利用Python实现与Isaac Sim的环境对接，便于在GPU加速的多物理场仿真中测试控制算法。虽未包含机器人资产，但为使用Agilebot的研究者和开发者提供了快速接入Isaac Sim生态的工具链。 ![GitHub stars](https://img.shields.io/github/stars/sh-agilebot/agilebot_isaac_sim?style=social)

- [isaac_sim_assembly](https://github.com/mkuznets23/isaac_sim_assembly) — 该项目构建了一个四机械臂装配工作站，用于在 NVIDIA Isaac Sim 中组装小型轮式机器人。它利用 Isaac Sim 的物理仿真与机器人控制功能，通过 Python 脚本实现多臂协同操作和任务编排，展示了复杂装配任务的仿真流程。适合希望在 Isaac Sim 中开发多机器人协作或自动化装配应用的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/mkuznets23/isaac_sim_assembly?style=social)

- [IsaacSim-RC-Car-Dynamics](https://github.com/AmitPratap175/IsaacSim-RC-Car-Dynamics) — 该项目在NVIDIA Isaac Sim中实现了一个遥控（RC）小车的物理仿真，通过配置车辆关节的articulation结构并控制轮子关节实现运动，利用Isaac Sim的3D可视化环境展示动态行为。项目使用Python脚本与Isaac Sim API交互，适用于希望学习或开发基于Isaac Sim的地面机器人动力学仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/AmitPratap175/IsaacSim-RC-Car-Dynamics?style=social)

- [LimoIsaacSIM](https://github.com/WeGo-Robotics/LimoIsaacSIM) — 该项目为Limo机器人提供Isaac Sim专用的仿真包，包含URDF模型、传感器配置及控制接口，支持在Isaac Sim中进行高保真物理仿真与算法验证。通过集成Isaac Sim的PhysX引擎和ROS 2通信框架，实现对Limo差速驱动底盘的精确模拟。主要面向使用Limo平台进行移动机器人开发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/WeGo-Robotics/LimoIsaacSIM?style=social)

- [IsaacLab-Simple-Tutorial-Walkthrough](https://github.com/marcelpatrick/IsaacLab-Simple-Tutorial-Walkthrough) — 该项目提供了一个面向初学者的 Isaac Lab 简明教程，通过逐步示例演示如何在 Isaac Sim 平台上构建和运行基础机器人仿真任务。内容涵盖环境设置、基本场景搭建及与 Isaac Lab 框架的交互方式，帮助用户快速上手 NVIDIA 的 GPU 加速机器人仿真工具。目标用户为希望入门 Isaac Sim 和 Isaac Lab 的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/marcelpatrick/IsaacLab-Simple-Tutorial-Walkthrough?style=social)

- [LineFollow-Robocon-IsaacSim](https://github.com/rahulpanchall7/LineFollow-Robocon-IsaacSim) — 该项目基于 Isaac Sim 和 ROS2 构建了一个虚拟机器人竞速仿真环境，使用两个 Robotnik Summit 机器人进行循线比赛，支持 PID 与强化学习（RL）控制策略的实现与对比。项目深度集成 Isaac Sim 的物理引擎和传感器模拟功能，并通过 ROS2 实现控制逻辑通信，适合希望在 Isaac Sim 中开发和测试自主机器人控制算法的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/rahulpanchall7/LineFollow-Robocon-IsaacSim?style=social)

- [tactile_self_modeling](https://github.com/cKohl10/tactile_self_modeling) — 该项目利用Isaac Sim结合触觉传感数据来建模机器人形态，通过仿真环境中的触觉反馈实现对机器人自身结构的自适应建模。项目直接基于Isaac Sim构建仿真场景，并集成触觉传感器模拟，用于研究具身智能与形态感知。主要面向机器人自建模与触觉感知研究者。 ![GitHub stars](https://img.shields.io/github/stars/cKohl10/tactile_self_modeling?style=social)

- [isaacsim-ros2-docker](https://github.com/Hoang-Trung-Le/isaacsim-ros2-docker) — 该项目提供了一个预配置的 Docker 镜像，集成了 NVIDIA Isaac Sim 与 ROS 2 环境，便于用户快速搭建支持机器人开发的仿真平台。通过 Docker 封装 Isaac Sim 和 ROS 2 的复杂依赖，简化了安装和部署流程，特别适用于需要在隔离环境中进行机器人算法开发与测试的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/Hoang-Trung-Le/isaacsim-ros2-docker?style=social)

- [h12-sim](https://github.com/Matero952/h12-sim) — 该项目为Unitree H1-2人形机器人提供Isaac Lab扩展实现，主要用途是在Isaac Sim环境中构建和控制H1-2的仿真模型。它基于NVIDIA Isaac Lab框架，集成了机器人URDF、控制器及任务配置，利用GPU加速物理仿真进行强化学习训练。目标用户为使用Isaac Sim开发人形机器人算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Matero952/h12-sim?style=social)

- [SpotWithArmExtension](https://github.com/ashwinsnambiar/SpotWithArmExtension) — 该项目为 Boston Dynamics 的 Spot 机器人添加了机械臂扩展，专为 Isaac Sim 平台构建，使其支持带操作臂的 Spot 仿真。通过 USD 场景描述和 Python 脚本集成到 Isaac Sim 环境中，实现了对复合机器人系统的物理模拟与控制。适用于希望在 Isaac Sim 中开发或测试带臂 Spot 机器人的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/ashwinsnambiar/SpotWithArmExtension?style=social)

- [silver2_isaacsim](https://github.com/Joagai23/silver2_isaacsim) — 该项目用于在 Isaac Sim 中控制和仿真水下腿式机器人 SILVER2，基于 ROS 2 Jazzy 构建，实现了机器人与 Isaac Sim 的深度集成。通过利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟能力，支持高保真水下环境下的运动控制与感知测试。主要面向水下机器人研究与开发人员。 ![GitHub stars](https://img.shields.io/github/stars/Joagai23/silver2_isaacsim?style=social)

- [isaac_system_interface](https://github.com/YeatsWang/isaac_system_interface) — 该项目是一个ROS 2硬件接口插件，用于将ROS 2 Control与NVIDIA Isaac Sim的关节状态和命令话题进行桥接。通过订阅和发布Isaac Sim中定义的关节数据，实现真实或仿真机器人控制系统的无缝集成。主要面向使用ROS 2生态并希望在Isaac Sim中部署控制器的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/YeatsWang/isaac_system_interface?style=social)

- [nvidia-isaac-sim-macos](https://github.com/Tanmay0929/nvidia-isaac-sim-macos) — 该项目是一个面向 macOS 平台的自主仓储机器人仿真示例，利用 NVIDIA Isaac Sim 与 ROS2 实现 SLAM、导航和机械臂操作功能。项目通过 Docker 容器化部署，在 Isaac Sim 中构建仓库场景并集成 ROS2 节点进行感知与控制，展示了 Isaac Sim 与 ROS2 的协同工作流。适用于希望在 macOS 上学习 Isaac Sim 机器人仿真的开发者和教育用户。 ![GitHub stars](https://img.shields.io/github/stars/Tanmay0929/nvidia-isaac-sim-macos?style=social)

- [Isaac_Sim_5.0_Floating_in_water](https://github.com/WandersondaSC/Isaac_Sim_5.0_Floating_in_water) — 该项目演示了在 Isaac Sim 5.0 中实现一个立方体在水面漂浮的物理仿真，利用 Isaac Sim 的流体模拟与刚体动力学功能，通过 Python 脚本配置浮力与碰撞参数。项目直接面向 Isaac Sim 用户，提供了一个基础但实用的水下/水面交互示例，适用于学习或扩展机器人在涉水环境中的仿真场景。 ![GitHub stars](https://img.shields.io/github/stars/WandersondaSC/Isaac_Sim_5.0_Floating_in_water?style=social)

- [isaac-simulator-usage](https://github.com/park-sangbeom/isaac-simulator-usage) — 该项目是一个面向 Isaac Sim 的入门教程，通过 Jupyter Notebook 形式演示如何在 Omniverse 平台中使用 Isaac Sim 进行机器人仿真。内容涵盖环境搭建、基本 API 调用及简单仿真实例，帮助用户快速上手 NVIDIA 的 GPU 加速物理仿真工具。适合希望学习 Isaac Sim 基础操作的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/park-sangbeom/isaac-simulator-usage?style=social)

- [isaac-teleop-device-plugins](https://github.com/isaac-sim/isaac-teleop-device-plugins) — 该项目为 Isaac Sim 提供遥操作设备插件支持，用于将物理输入设备（如手柄、操纵杆等）与仿真环境集成，实现对虚拟机器人的实时控制。作为官方 isaac-sim 组织下的仓库，其命名和上下文明确表明专为 Isaac Sim 设计，采用 CMake 构建，便于嵌入 Isaac Sim 的插件体系。主要面向需要在 Isaac Sim 中进行人机交互或远程操作机器人仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/isaac-sim/isaac-teleop-device-plugins?style=social)

- [Isaac-lab-ARH2-grasp-teleop](https://github.com/abdulhafiz7794/Isaac-lab-ARH2-grasp-teleop) — 该项目实现了在NVIDIA Isaac Sim/Lab中通过遥操作（基于ZMQ和LabVIEW）控制拟人化机器人手ARH2抓取刚性和可变形物体。它直接利用Isaac Lab的仿真环境与物理引擎，结合外部控制接口，展示了高保真手部灵巧操作能力。适用于研究灵巧手遥操作与抓取策略的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/abdulhafiz7794/Isaac-lab-ARH2-grasp-teleop?style=social)

- [xarm_isaac](https://github.com/gadorneles/xarm_isaac) — 该项目实现了UFactory XArm机械臂系列与NVIDIA Isaac Sim的集成，提供ROS2控制节点及简单任务示例，并完全兼容xarm_ros2包中的MoveIt2节点。通过Isaac Sim的物理仿真环境，用户可在GPU加速的多物理场中测试和开发XArm的控制策略。主要面向使用Isaac Sim进行机器人仿真的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/gadorneles/xarm_isaac?style=social)

- [3d-Printed-5DOF-robotic-arm-Isaac-Simulator-integration-inverse-kinematics](https://github.com/DmitriyB51/3d-Printed-5DOF-robotic-arm-Isaac-Simulator-integration-inverse-kinematics) — 该项目实现了一个3D打印的5自由度机械臂，并集成了NVIDIA Isaac Sim进行数字孪生仿真，重点应用了逆运动学算法控制机械臂运动。项目从机械设计到仿真全流程覆盖，利用Isaac Sim的物理引擎和渲染能力构建高保真虚拟环境，便于验证控制策略。适合机器人爱好者和研究人员快速搭建与仿真低成本机械臂系统。 ![GitHub stars](https://img.shields.io/github/stars/DmitriyB51/3d-Printed-5DOF-robotic-arm-Isaac-Simulator-integration-inverse-kinematics?style=social)

- [h12_exts](https://github.com/Matero952/h12_exts) — 该项目为 Unitree H1-2 人形机器人在 Isaac Sim 中提供完整的 ROS2 仿真扩展，专为 Correll 实验室开发。它通过自定义扩展集成 ROS2 通信与 Isaac Sim 的物理仿真环境，支持传感器数据发布、关节控制等关键功能。目标用户是使用 Isaac Sim 进行人形机器人算法开发与测试的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/Matero952/h12_exts?style=social)

- [umi_sim_interface](https://github.com/dwijenchawra/umi_sim_interface) — 该项目修改了斯坦福UMI推理管道，使其能与Isaac Sim中的仿真机械臂通过ROS进行交互。它实现了UMI模型在Isaac Sim环境下的部署，利用ROS桥接实现动作指令传递与状态反馈，支持在高保真GPU加速仿真中测试和验证机器人策略。主要面向希望在Isaac Sim中集成UMI操作模型的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/dwijenchawra/umi_sim_interface?style=social)

- [sdg_training_custom](https://github.com/pastoriomarco/sdg_training_custom) — 该项目利用 Isaac Sim 生成针对自定义物体的合成数据（SDG），并基于这些数据训练 YOLOv8 目标检测模型。其核心在于通过 Isaac Sim 的高保真渲染和物理模拟能力创建多样化、带标注的训练图像，从而减少对真实数据的依赖。适用于希望在机器人视觉任务中快速构建定制化检测模型的研究者或工程师。 ![GitHub stars](https://img.shields.io/github/stars/pastoriomarco/sdg_training_custom?style=social)

- [RC-Sim2Real](https://github.com/maxboels/RC-Sim2Real) — 该项目是一个基于 NVIDIA Isaac Lab 构建的机器人仿真与训练框架，专注于开发和训练具备仿真到现实（sim-to-real）迁移能力的自定义机器人控制器。它利用 Isaac Lab 的 GPU 加速物理仿真和强化学习基础设施，支持快速迭代控制策略。主要面向需要高效 sim-to-real 工作流的机器人研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/maxboels/RC-Sim2Real?style=social)

- [Paint-Spraying-Simulation](https://github.com/shonbabu/Paint-Spraying-Simulation) — 该项目利用 Isaac Warp 和 OpenUSD 构建了一个逼真的喷漆仿真系统，实现了基于粒子物理的喷漆过程模拟、油漆累积追踪及可视化功能。其核心依赖 NVIDIA 的 Isaac Sim 生态中的 Warp 物理计算框架，并通过 OpenUSD 实现场景描述与渲染，适用于需要高保真喷涂效果验证的机器人或自动化喷涂应用开发者。 ![GitHub stars](https://img.shields.io/github/stars/shonbabu/Paint-Spraying-Simulation?style=social)

- [LLM-Guided-Robot-Agent](https://github.com/VedSoni-dev/LLM-Guided-Robot-Agent) — 该项目构建了一个基于大语言模型（LLM）控制的GPU加速机器人智能体，专为Isaac Sim平台开发。它利用视觉感知、记忆机制与推理能力，在Isaac Sim提供的逼真环境中实现导航与交互，核心依赖Isaac Sim的渲染与物理仿真能力。适用于希望探索LLM与具身智能在高保真仿真中结合的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/VedSoni-dev/LLM-Guided-Robot-Agent?style=social)

- [PeopleAPI](https://github.com/worv-ai/PeopleAPI) — PeopleAPI 为 Isaac Sim / Omniverse 中的动画人物扩展（omni.anim.people）提供公开 Python API，支持外部程序控制角色行为，如移动、坐下、交谈等。该项目直接基于 Isaac Sim 的人物动画系统构建，通过封装底层命令实现对虚拟角色的程序化操控，适用于需要在 Isaac Sim 场景中集成人群仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/worv-ai/PeopleAPI?style=social)

- [JetBot-Navigation](https://github.com/ChenBoAn/JetBot-Navigation) — 该项目是一个面向JetBot机器人的智能导航系统，结合A*路径规划与Pure Pursuit跟踪控制算法，在NVIDIA Isaac Sim环境中实现自主导航。它利用Isaac Sim的仿真能力对复杂道路网络进行路径优化与平滑运动控制，适用于希望在Isaac Sim中开发或测试移动机器人导航算法的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/ChenBoAn/JetBot-Navigation?style=social)

- [IsaacLabDocker](https://github.com/easylab2008/IsaacLabDocker) — 该项目提供 Isaac Lab 的 Docker 容器化部署方案，简化了 Isaac Sim 机器人仿真环境的搭建流程。通过预配置的镜像集成 Isaac Lab 所需的 CUDA、ROS 和 Isaac Sim 依赖，支持快速启动训练与测试。适用于希望高效部署 NVIDIA Isaac Lab 开发环境的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/easylab2008/IsaacLabDocker?style=social)

- [IsaacLabFarming](https://github.com/greatroboticslab/IsaacLabFarming) — 该项目是 Isaac Lab 的一个定制化分支，专门用于人形农业机器人的开发与仿真。它基于 NVIDIA Isaac Sim 平台，针对农业场景优化了机器人控制、感知和任务逻辑，并集成了相应的作物与环境模型。目标用户为从事农业机器人研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/greatroboticslab/IsaacLabFarming?style=social)

- [pixi-IsaacLab-Unitree](https://github.com/Jaebeom-git/pixi-IsaacLab-Unitree) — 该项目提供基于 Pixi 的环境配置方案，用于快速搭建 Isaac Sim、Isaac Lab 以及 Unitree 强化学习实验室的开发环境。通过声明式依赖管理，简化了 NVIDIA Isaac 平台与 Unitree 机器人 RL 训练框架的集成流程，利用 Pixi 实现跨平台一致性部署。主要面向希望在 Isaac Sim 生态中开展四足机器人强化学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Jaebeom-git/pixi-IsaacLab-Unitree?style=social)

- [IsaacLab_G1](https://github.com/smg0411/IsaacLab_G1) — 该项目为基于 Isaac Lab 的机器人仿真环境配置，主要用途是提供针对特定机器人（如 G1 人形机器人）的强化学习训练框架。它利用 Isaac Lab 的 GPU 加速物理仿真能力，集成了传感器模型、运动控制策略和任务场景，便于在 Isaac Sim 中进行高保真机器人行为训练。目标用户为从事人形机器人强化学习研究的开发者与科研人员。 ![GitHub stars](https://img.shields.io/github/stars/smg0411/IsaacLab_G1?style=social)

- [IsaacLab_Reach_cubepick](https://github.com/junshi356rl/IsaacLab_Reach_cubepick) — 该项目使用PPO算法在Isaac Lab环境中训练机械臂完成抓取立方体的任务，展示了如何基于Isaac Sim的强化学习框架构建和训练机器人操作策略。代码利用Isaac Lab提供的物理仿真与RL接口，实现了从环境配置、策略训练到评估的完整流程，适合希望在Isaac Sim生态中开展机器人操作研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/junshi356rl/IsaacLab_Reach_cubepick?style=social)

- [IsaacLabExtensionTemplate](https://github.com/crowznl/IsaacLabExtensionTemplate) — 该项目是一个用于在 Isaac Lab 中快速创建自定义扩展的模板，主要帮助开发者标准化扩展开发流程。它提供了与 Isaac Lab 紧密集成的目录结构、示例代码和配置文件，基于 Python 实现，并遵循 NVIDIA Omniverse 扩展规范。目标用户是希望为 Isaac Lab 开发机器人仿真或训练模块的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/crowznl/IsaacLabExtensionTemplate?style=social)

- [SpotMicro-IsaacLab](https://github.com/tonhathuy/SpotMicro-IsaacLab) — 该项目旨在基于 Isaac Lab 框架实现 SpotMicro 四足机器人的强化学习控制，利用 Isaac Sim 的 GPU 加速物理仿真能力进行训练。项目通过集成 Isaac Lab 的 RL 工具链和机器人建模接口，构建适用于四足步态学习的仿真环境。主要面向希望在 Isaac Sim 生态中开发或研究四足机器人控制策略的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/tonhathuy/SpotMicro-IsaacLab?style=social)

- [IsaacLab_f1tenth](https://github.com/kyeonghyeon0314/IsaacLab_f1tenth) — 该项目基于 Isaac Lab 构建 F1TENTH 自动驾驶小车系统，用于参加相关竞赛。它利用 Isaac Lab 的 GPU 加速物理仿真能力，实现车辆动力学建模、传感器模拟和强化学习训练环境搭建。项目包含赛道配置、控制策略和训练脚本，面向希望在 Isaac Sim 生态中开发自动驾驶算法的研究者与参赛团队。 ![GitHub stars](https://img.shields.io/github/stars/kyeonghyeon0314/IsaacLab_f1tenth?style=social)

- [IsaacLabExtensionGo2](https://github.com/al-oman/IsaacLabExtensionGo2) — 该项目是一个面向Isaac Lab的扩展，旨在通过自定义强化学习算法控制Unitree Go2四足机器人。它直接基于Isaac Lab框架构建，利用其GPU加速的物理仿真和RL训练基础设施，实现对Go2机器人的策略部署与测试。主要面向希望在Isaac Sim生态中开发或实验四足机器人控制算法的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/al-oman/IsaacLabExtensionGo2?style=social)

- [IsaacLab_RL_Robotic_Arm_IK_Reach](https://github.com/PhiLia093/IsaacLab_RL_Robotic_Arm_IK_Reach) — 该项目基于Isaac Lab平台，使用PPO强化学习算法训练UR机械臂完成逆运动学（IK）可达性任务。它利用Isaac Sim的GPU加速物理仿真和机器人建模能力，构建了面向机械臂控制的RL训练环境。项目为希望在Isaac Lab中快速上手强化学习与机器人控制集成的开发者提供了一个简洁示例。 ![GitHub stars](https://img.shields.io/github/stars/PhiLia093/IsaacLab_RL_Robotic_Arm_IK_Reach?style=social)

- [openarm_isaac_lab](https://github.com/DavidLXu/openarm_isaac_lab) — 该项目旨在为OpenArm机器人提供在Isaac Lab环境中的仿真支持，主要功能包括机器人模型集成、任务配置及强化学习训练流程。它直接基于Isaac Lab框架构建，利用其GPU加速的物理仿真和RL训练基础设施，适配URDF模型并定义自定义场景与奖励函数。目标用户为希望在Isaac Sim生态中快速部署和测试机械臂控制策略的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/DavidLXu/openarm_isaac_lab?style=social)

- [DoublePendulumIsaacLab](https://github.com/NRdrgz/DoublePendulumIsaacLab) — 该项目在 Isaac Lab 中实现了倒立双摆的强化学习训练，利用 Isaac Sim 的 GPU 加速物理仿真能力构建控制策略。通过 Isaac Lab 的 RL 框架和传感器接口，实现对复杂动力学系统的稳定控制。适用于希望在 Isaac Sim 生态中研究经典控制问题或验证强化学习算法的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/NRdrgz/DoublePendulumIsaacLab?style=social)

- [discrete-lfd-isaac-lab](https://github.com/AlbinEV/discrete-lfd-isaac-lab) — 该项目实现了面向机器人抛光任务的离散动作空间示教学习（LfD）方法，专为 Isaac Lab 2.0.1 构建。它利用 Isaac Lab 的强化学习框架和物理仿真能力，将专家演示转化为离散控制策略，适用于高精度表面处理场景。目标用户为在 Isaac Sim 生态中研究模仿学习与机器人操作的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/AlbinEV/discrete-lfd-isaac-lab?style=social)

- [ubuntu24-isaac-lab-setup](https://github.com/xiransong/ubuntu24-isaac-lab-setup) — 该项目提供了一个 Shell 脚本，用于在 Ubuntu 24.04 系统上自动化配置 Isaac Lab 的运行环境。它处理依赖安装、CUDA 配置及 Isaac Sim 相关组件的设置，简化了开发环境搭建流程。主要面向希望快速部署 Isaac Lab 进行机器人仿真与强化学习研究的开发者。 ![GitHub stars](https://img.shields.io/github/stars/xiransong/ubuntu24-isaac-lab-setup?style=social)

- [Isaac_Lab_UR5e_Reach](https://github.com/JonasFano/Isaac_Lab_UR5e_Reach) — 该项目利用强化学习在 Isaac Lab 中控制 UR5e 机械臂，通过微分逆运动学（differential IK）实现末端执行器对目标位姿的精准到达。项目基于 Isaac Lab 的机器人仿真框架，集成了其物理引擎与 RL 训练流程，适用于希望在 Isaac Sim 生态中开发机械臂控制策略的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/JonasFano/Isaac_Lab_UR5e_Reach?style=social)

- [RL-Control-of-Bipedal-Robots-with-Isaac-Lab](https://github.com/hsksfje/RL-Control-of-Bipedal-Robots-with-Isaac-Lab) — 该项目基于 Isaac Lab 实现双足机器人的强化学习控制，利用其 GPU 加速的物理仿真和 RL 训练框架开发行走策略。代码集成了 Isaac Lab 的机器人建模、传感器模拟与训练流程，适用于希望在高保真仿真环境中研究双足运动控制的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/hsksfje/RL-Control-of-Bipedal-Robots-with-Isaac-Lab?style=social)

- [Arm-X4](https://github.com/xiaohu-art/Arm-X4) — 该项目实现了基于强化学习的 Arm-X4 机械臂控制，明确使用 Isaac Sim 作为仿真平台进行训练和测试。代码集成了 Isaac Sim 的 Python API，利用其 GPU 加速的物理引擎和传感器模拟功能构建训练环境。项目包含完整的训练脚本与配置文件，适合希望在 Isaac Sim 中开发机械臂强化学习应用的研究者和工程师。 ![GitHub stars](https://img.shields.io/github/stars/xiaohu-art/Arm-X4?style=social)

- [dual_kinova](https://github.com/kedarrajpathak/dual_kinova) — 该项目专注于双臂机械臂的模仿学习，基于 Isaac Lab 构建仿真环境与训练流程。它利用 Isaac Sim 的 GPU 加速物理引擎和机器人模拟能力，实现高保真双臂操作任务的策略学习。项目包含自定义任务配置、动作空间设计及数据采集模块，适用于研究多臂协同控制与模仿学习的科研人员。 ![GitHub stars](https://img.shields.io/github/stars/kedarrajpathak/dual_kinova?style=social)

- [wheel_leg_rl](https://github.com/null-qwerty/wheel_leg_rl) — 该项目是一个基于 Isaac Lab 构建的强化学习训练框架，专注于五连杆轮腿底盘机器人的运动控制策略开发。它利用 Isaac Lab 提供的 GPU 加速仿真环境和机器人建模工具，实现高效的策略训练与部署。目标用户为从事轮腿机器人研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/null-qwerty/wheel_leg_rl?style=social)

- [dexHand](https://github.com/Shuteng-0608/dexHand) — 该项目基于 Isaac Sim 5.1.0 和 Isaac Lab，利用 skrl 框架实现 PPO 算法对灵巧手（dexHand）进行强化学习训练。它直接集成 Isaac Sim 的仿真环境与 Isaac Lab 的任务配置，采用 GPU 加速的物理模拟支持高保真机器人控制策略开发。适用于希望在 Isaac Sim 生态中研究灵巧操作与强化学习的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Shuteng-0608/dexHand?style=social)

- [Grade](https://github.com/aquacommander/Grade) — GRADE 是一个用于生成逼真动态机器人仿真环境的框架，支持在 Isaac Sim 中创建包含人类、动物等动态元素的场景。该项目利用 Omniverse 和 Isaac Sim 的 API 实现环境自动生成，适用于需要复杂交互场景的机器人研究。目标用户为使用 Isaac Sim 进行 AI 与机器人仿真的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/aquacommander/Grade?style=social)

- [AISL-RL](https://github.com/DiligentYoon/AISL-RL) — 该项目是一个基于 Isaac Lab 的强化学习框架，专为在 NVIDIA Isaac Sim 环境中开发和训练机器人策略而设计。它利用 Isaac Lab 提供的 GPU 加速物理仿真与 RL 接口，实现高效智能体训练。主要面向自主与智能系统实验室的研究人员及 Isaac Sim 开发者。 ![GitHub stars](https://img.shields.io/github/stars/DiligentYoon/AISL-RL?style=social)

- [CAI_walkerE](https://github.com/cailab-hy/CAI_walkerE) — 该项目基于TienKung-Lab定制，集成了AMP自定义数据集、30自由度动作重定向，并明确采用IsaacLab训练流程，用于高自由度人形机器人的强化学习训练。其核心功能依赖IsaacLab提供的GPU加速仿真与RL训练框架，适用于需要在Isaac Sim环境中开发复杂双足行走策略的研究人员。 ![GitHub stars](https://img.shields.io/github/stars/cailab-hy/CAI_walkerE?style=social)

- [isaaclab-RL-tutorials](https://github.com/marcelpatrick/isaaclab-RL-tutorials) — 该项目提供面向 Isaac Lab 的强化学习教程，旨在帮助用户利用 Isaac Sim 的 GPU 加速物理仿真能力进行机器人策略训练。仓库内容聚焦于 Isaac Lab 框架下的 RL 算法实现与环境配置，包含基于 PyTorch 和 RLlib 的示例代码。目标用户为希望在 Isaac Sim 生态中快速上手强化学习的机器人研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/marcelpatrick/isaaclab-RL-tutorials?style=social)

- [object-gym](https://github.com/robowork/object-gym) — 该项目利用深度强化学习（DRL）在NVIDIA Isaac Gym中训练机械臂操作大型不可抓握物体，专注于解决传统抓取方法难以处理的物体操纵任务。通过Isaac Gym提供的GPU加速物理仿真环境，实现了高效的并行化训练流程。主要面向机器人学习研究者及Isaac Sim开发者，探索复杂物体交互策略。 ![GitHub stars](https://img.shields.io/github/stars/robowork/object-gym?style=social)

- [Research-on-End-to-End-Diffusion-Driving-Strategy-Based-on-SAC-Reinforcement-Learning](https://github.com/WUJIAHAO-HKU/Research-on-End-to-End-Diffusion-Driving-Strategy-Based-on-SAC-Reinforcement-Learning) — 该项目研究基于去噪扩散概率模型（DDPM）与软演员-评论家（SAC）强化学习算法的端到端自动驾驶策略，明确在NVIDIA Isaac Lab高保真仿真环境中进行训练与验证。其核心利用Isaac Lab提供的物理精确模拟和GPU加速能力，实现自动驾驶策略的高效迭代。目标用户为从事自主驾驶与机器人学习的研究人员。 ![GitHub stars](https://img.shields.io/github/stars/WUJIAHAO-HKU/Research-on-End-to-End-Diffusion-Driving-Strategy-Based-on-SAC-Reinforcement-Learning?style=social)

- [env-isaaclab](https://github.com/simonguest/env-isaaclab) — 该项目提供了一个基于 uv 的 Python 环境管理方案，专门用于简化在 Windows 系统上运行 NVIDIA Isaac Lab 实验的配置流程。通过预定义依赖和环境设置，解决了 Isaac Lab 在 Windows 平台部署时常见的兼容性与依赖冲突问题。目标用户为希望在 Windows 上快速启动 Isaac Lab 仿真实验的机器人研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/simonguest/env-isaaclab?style=social)

- [wandelbots-openusd-schema-extension](https://github.com/wandelbotsgmbh/wandelbots-openusd-schema-extension) — 该项目为 Isaac Sim 提供 OpenUSD 架构扩展，集成了 Wandelbots NOVA API 及其机器人原语，使用户能在 Omniverse 环境中直接使用 NOVA 的高层机器人控制接口。通过自定义 USD Schema，该扩展增强了 Isaac Sim 对工业机器人工作流的支持，适用于希望在 NVIDIA Omniverse 中结合 Wandelbots NOVA 平台进行机器人仿真的开发者。 ![GitHub stars](https://img.shields.io/github/stars/wandelbotsgmbh/wandelbots-openusd-schema-extension?style=social)

- [stretch_isaac](https://github.com/Harro4135/stretch_isaac) — 该项目提供了Hello Robot SE3 Stretch机器人在Isaac Sim中的仿真模型，包含URDF文件和必要的配置，用于在NVIDIA Isaac Sim环境中进行机器人控制、感知与任务仿真。项目直接面向Isaac Sim平台构建，支持GPU加速的物理模拟和传感器仿真，适用于希望在Isaac Sim中开发或测试Stretch机器人应用的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/Harro4135/stretch_isaac?style=social)

- [trossen_ai_isaac](https://github.com/TrossenRobotics/trossen_ai_isaac) — 该项目提供Trossen Robotics机器人与Isaac Sim及Isaac Lab的集成方案，主要用途是将真实机器人硬件（如Interbotix机械臂）接入NVIDIA Isaac仿真平台。通过Python实现URDF导入、控制器配置和任务自动化，支持在Isaac Lab中进行强化学习训练和仿真部署。目标用户为使用Trossen机器人并希望利用Isaac Sim进行AI驱动机器人开发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/TrossenRobotics/trossen_ai_isaac?style=social)

- [back_flip_go2](https://github.com/SheYuqi/back_flip_go2) — 该项目基于 Isaac Lab 实现四足机器人 Go2 的后空翻动作控制，利用 Isaac Sim 的强化学习与物理仿真环境训练策略。通过集成 Isaac Lab 的任务框架和 GPU 加速的 PhysX 物理引擎，实现了高动态运动技能的学习与部署。主要面向使用 Isaac Sim 进行四足机器人高级行为研究的科研人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/SheYuqi/back_flip_go2?style=social)

- [isaac_installation_script](https://github.com/QiYuanyang/isaac_installation_script) — 该项目提供了一个 Shell 脚本，用于自动化安装 NVIDIA Isaac Sim 和 Isaac Lab，简化了在 Linux 系统上配置这两个机器人仿真平台的复杂依赖和环境设置过程。脚本封装了官方安装流程，适用于希望快速部署 Isaac Sim 生态工具的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/QiYuanyang/isaac_installation_script?style=social)

- [nrmk_isaaclab_public](https://github.com/neuromeka-robotics/nrmk_isaaclab_public) — 该项目为Neuromeka机器人在Isaac Lab环境中的集成提供支持，包含用于配置、控制和仿真的Python模块。它直接面向Isaac Lab框架，实现了机器人模型加载、传感器接口和任务定义等关键功能，便于在GPU加速的物理仿真中进行强化学习或运动控制研究。目标用户为使用Isaac Lab开发Neuromeka机器人应用的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/neuromeka-robotics/nrmk_isaaclab_public?style=social)

- [limxtron1-isaaclab](https://github.com/wizard-lhx/limxtron1-isaaclab) — 该项目基于 Isaac Lab 框架，用于训练逐际动力（LimX Dynamics）的双足机器人模型，利用 Isaac Sim 提供的 GPU 加速物理仿真环境实现强化学习策略训练。项目集成了机器人 URDF 模型、运动控制任务定义及训练脚本，适配 Isaac Lab 的模块化架构。主要面向使用 Isaac Sim 进行人形或双足机器人仿真的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/wizard-lhx/limxtron1-isaaclab?style=social)

- [RL_Arm](https://github.com/pietrodardano/RL_Arm) — 该项目专注于基于强化学习的机器人臂操作任务，明确支持 Isaac Lab 和 Isaac Gym 作为仿真平台，并同时兼容 MuJoCo。它提供了针对 FR3 和 UR5e 机械臂的训练环境与算法实现，利用 Isaac Sim 的 GPU 加速物理模拟能力进行高效策略训练。目标用户为从事机器人操作学习研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/pietrodardano/RL_Arm?style=social)

- [rev2fwd-il](https://github.com/qiaoqy/rev2fwd-il) — 该项目实现了反向到前向的模仿学习方法（Reverse-to-Forward Imitation Learning），专为 Isaac Lab 环境设计，用于从反向轨迹中提取策略并迁移到前向任务。它利用 Isaac Lab 提供的 GPU 加速物理仿真和强化学习接口，构建高效的行为克隆与策略迁移流程。主要面向在 Isaac Sim 生态中研究机器人技能学习与迁移的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/qiaoqy/rev2fwd-il?style=social)

- [RL_bipedal_locomotion_Isaaclab](https://github.com/81578823/RL_bipedal_locomotion_Isaaclab) — 该项目是一个面向初学者的双足机器人强化学习步态训练示例，专门基于 Isaac Lab 框架实现，用于教学和实践。它利用 Isaac Sim 的 GPU 加速物理仿真能力，在 Isaac Lab 环境中构建了完整的 RL 训练流程，包括自定义任务、奖励函数和策略训练。项目适合作为学习 Isaac Lab 强化学习工作流的入门资源。 ![GitHub stars](https://img.shields.io/github/stars/81578823/RL_bipedal_locomotion_Isaaclab?style=social)

- [husky_virtual_commissioning](https://github.com/GrigoryArtazyan/husky_virtual_commissioning) — 该项目旨在简化Husky机器人系统的虚拟调试流程，基于Isaac Sim和Omniverse构建仿真环境，并通过ROS 2 Humble实现与真实机器人的接口对接。项目利用Python开发，提供传感器配置、运动控制和任务验证等功能，支持在部署前于Isaac Sim中完成完整的行为测试。主要面向使用Husky平台并希望借助Isaac Sim加速开发与调试的机器人工程师。 ![GitHub stars](https://img.shields.io/github/stars/GrigoryArtazyan/husky_virtual_commissioning?style=social)

- [isaac_usd](https://github.com/lo-imperatore/isaac_usd) — 该项目提供用于在 Isaac Sim 中进行仿真的 USD 模型资源，直接支持 Isaac Sim 的核心仿真格式需求。USD（Universal Scene Description）是 Isaac Sim 的原生场景与资产描述标准，这些模型可直接加载用于机器人仿真、传感器测试等任务。项目面向 Isaac Sim 用户，特别是需要现成 3D 资产快速构建仿真环境的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/lo-imperatore/isaac_usd?style=social)

- [alphaDrone-Isaac](https://github.com/nodale/alphaDrone-Isaac) — 该项目旨在为 Isaac Sim 和 Isaac Lab 提供无人机仿真支持，主要功能包括构建适用于强化学习训练的四旋翼飞行器环境。项目基于 Python 实现，利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟能力，并与 Isaac Lab 的任务框架集成，便于开发和测试自主飞行控制策略。目标用户为使用 NVIDIA Isaac 平台进行空中机器人研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/nodale/alphaDrone-Isaac?style=social)

- [isaacsim](https://github.com/amk-robotlabor/isaacsim) — 该项目汇集了基于 NVIDIA Isaac Sim 和 Isaac Lab 的机器人仿真项目，主要提供面向 Isaac Sim 平台的示例场景与训练环境。仓库内容聚焦于利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能，实现机器人行为开发与强化学习训练。适合希望快速上手 Isaac Sim 生态并开展机器人仿真实验的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/amk-robotlabor/isaacsim?style=social)

- [go2_isaac_driver](https://github.com/siddarth09/go2_isaac_driver) — 该项目是一个专为Unitree Go2四足机器人开发的Isaac Sim驱动程序，使用C++实现，旨在将Go2机器人与NVIDIA Isaac Sim仿真环境深度集成。它提供了机器人状态通信、控制指令接口及传感器数据同步功能，便于在Isaac Sim中进行高保真仿真与强化学习训练。目标用户为希望在Isaac Sim中快速部署和测试Go2机器人的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/siddarth09/go2_isaac_driver?style=social)

- [IsaacFlow](https://github.com/trushant05/IsaacFlow) — IsaacFlow 提供了一种声明式方法来配置和管理 Isaac Sim 仿真环境，通过 YAML 或 JSON 文件定义场景、传感器和物理参数，简化了复杂仿真的搭建流程。该项目直接面向 Isaac Sim 用户，利用其 Python API 实现高层抽象，使研究人员和开发者能更高效地构建可复现的机器人仿真任务。 ![GitHub stars](https://img.shields.io/github/stars/trushant05/IsaacFlow?style=social)

- [IsaacLab_RL](https://github.com/aneangel/IsaacLab_RL) — 该项目基于 Isaac Lab 在 Isaac Sim 中实现强化学习训练，提供面向机器人控制任务的 RL 环境和训练脚本。它直接利用 Isaac Lab 的 GPU 加速物理仿真与传感器模拟能力，采用 Python 构建，适用于希望在高保真 Isaac Sim 平台中快速开发和测试强化学习算法的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/aneangel/IsaacLab_RL?style=social)

- [Robots_IsaacLab](https://github.com/Cyber-physical-Systems-Lab/Robots_IsaacLab) — 该项目为 Isaac Sim 提供机器人仿真实现，聚焦于运动控制与操作任务，包含 URDF 模型并适配 Isaac Lab 环境。其内容直接面向 Isaac Sim 生态，利用其 GPU 加速物理引擎进行机器人行为模拟，适用于需要在 Isaac Sim 中快速部署和测试机器人策略的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/Cyber-physical-Systems-Lab/Robots_IsaacLab?style=social)

- [isaac_sim_tutorials](https://github.com/todelice/isaac_sim_tutorials) — 该项目是一个专为 Isaac Sim 设计的教程仓库，提供使用 Python 编写的示例和教学内容，帮助用户快速上手 NVIDIA Isaac Sim 平台。教程涵盖基础操作、传感器配置、机器人仿真等核心功能，直接面向 Isaac Sim 的开发与应用。目标用户为希望学习或深入使用 Isaac Sim 进行机器人仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/todelice/isaac_sim_tutorials?style=social)

- [spot_isaac_driver](https://github.com/siddarth09/spot_isaac_driver) — 该项目为波士顿动力Spot机器人提供了一个基于Isaac Sim的强化学习与ROS 2集成驱动框架，利用Isaac Sim的GPU加速物理仿真能力，实现高保真机器人控制策略训练。项目通过ROS 2接口连接真实或模拟的Spot机器人，并在Isaac Sim环境中部署RL算法，适用于希望在逼真仿真中开发和测试四足机器人智能控制的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/siddarth09/spot_isaac_driver?style=social)

- [IsaacNav-scenes](https://github.com/ZJYIII/IsaacNav-scenes) — 该项目为 Isaac Sim 提供了专用于社交导航（social navigation）的仿真场景资源，包含针对行人交互、动态障碍物避让等任务优化的环境布局。这些场景可直接加载到 Isaac Sim 中，用于开发和测试机器人在复杂人群环境中的导航策略，适用于基于 GPU 加速仿真的自主移动机器人研究。 ![GitHub stars](https://img.shields.io/github/stars/ZJYIII/IsaacNav-scenes?style=social)

- [isaac-tb3](https://github.com/sachinkum0009/isaac-tb3) — 该项目为TurtleBot3机器人提供了在Isaac Sim中的仿真环境，包含URDF模型导入、传感器配置及基本控制示例。通过Isaac Sim的PhysX物理引擎和ROS 2接口，实现高保真移动机器人仿真，适用于希望在Isaac Sim中快速部署和测试TurtleBot3算法的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/sachinkum0009/isaac-tb3?style=social)

- [dx_isaac_assets](https://github.com/shadow-robot/dx_isaac_assets) — 该项目提供与Dexee机器人相关的Isaac Sim资源，包括模型、配置文件或场景资产，用于在NVIDIA Isaac Sim中进行仿真和开发。其内容专为Isaac Sim环境定制，支持快速集成Dexee硬件到GPU加速的多物理仿真流程中。目标用户为使用Isaac Sim开发灵巧手或人形机器人应用的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/shadow-robot/dx_isaac_assets?style=social)

- [isaac_go2_nav_rl](https://github.com/dream-rec/isaac_go2_nav_rl) — 该项目基于 Isaac Sim 构建四足机器人 Go2 的导航强化学习仿真环境，利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能，实现高保真移动机器人训练场景。项目集成了 RLlib 或类似框架进行策略训练，并通过 Isaac Sim 的 Python API 控制机器人运动与感知。主要面向使用 Isaac Sim 进行四足机器人自主导航研究的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/dream-rec/isaac_go2_nav_rl?style=social)

- [robot-nav](https://github.com/avantikashah/robot-nav) — 该项目专注于在 Isaac Sim 中实现机器人导航功能，利用其 GPU 加速的物理仿真环境构建导航任务。项目通过 Python 脚本与 Isaac Sim 的 API 集成，实现传感器模拟、路径规划和运动控制等核心导航模块。主要面向希望在高保真仿真环境中开发和测试自主导航算法的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/avantikashah/robot-nav?style=social)

- [Custom_IsaacSim](https://github.com/rjros/Custom_IsaacSim) — 该项目提供了一个针对可变形体仿真的Isaac Sim定制版本，专门优化了软体物理交互的模拟能力。通过修改Isaac Sim底层配置和参数，增强了对高保真可变形材料的支持，适用于需要精细软体动力学的研究场景。目标用户为从事柔性机器人、生物力学或高级物理仿真开发的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/rjros/Custom_IsaacSim?style=social)

- [IsaacLab](https://github.com/katari16/IsaacLab) — 该项目是一个基于 NVIDIA Isaac Sim 构建的统一机器人学习框架，旨在为强化学习和仿真训练提供模块化、可扩展的基础设施。它深度集成 Isaac Sim 的 GPU 加速物理引擎与传感器模拟功能，支持多机器人场景快速部署。目标用户为从事机器人 AI 算法研发与仿真实验的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/katari16/IsaacLab?style=social)

- [IsaacSim](https://github.com/sisterly-neck577/IsaacSim) — 该项目提供基于 NVIDIA Isaac Sim 的 AI 机器人仿真开发环境，利用 Docker 容器化部署，支持 ROS 2（Humble）、Isaac Gym 和 Isaac Lab，并涵盖四足机器人与无人机仿真场景。通过集成 Flax 和 PyTorch 框架，项目强调 sim2real 迁移能力，适用于需要在 Omniverse 平台中快速构建、测试和部署 GPU 加速机器人仿真的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/sisterly-neck577/IsaacSim?style=social)

- [IsaacLab](https://github.com/suyourice/IsaacLab) — 该项目是一个基于 NVIDIA Isaac Sim 构建的统一机器人学习框架，旨在简化强化学习与仿真环境的集成。它利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟能力，提供模块化组件以支持多种机器人任务训练。主要面向希望在高保真仿真中快速开发和测试机器人学习算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/suyourice/IsaacLab?style=social)

- [IsaacASE](https://github.com/sim-intel/IsaacASE) — 该项目复现了对抗性技能嵌入（Adversarial Skill Embedding）方法，明确基于 Isaac Lab 和 Isaac Sim 构建，利用其 GPU 加速的物理仿真与强化学习框架实现智能体技能学习。项目直接依赖 Isaac Sim 的仿真环境和 Isaac Lab 的 RL 工具链，适用于研究机器人策略泛化与技能表征的科研人员。 ![GitHub stars](https://img.shields.io/github/stars/sim-intel/IsaacASE?style=social)

- [CERLAB_Warehouse_Environment_IsaacSim](https://github.com/ryanwu0521/CERLAB_Warehouse_Environment_IsaacSim) — 该项目为卡内基梅隆大学CERLAB实验室构建了一个基于NVIDIA Isaac Sim的仓库仿真环境，主要用于机器人任务（如搬运、导航）的开发与测试。它利用Isaac Sim的USD场景搭建能力和PhysX物理引擎，创建了包含货架、托盘和障碍物的逼真仓库布局，并支持与ROS 2集成以实现感知与控制算法验证。目标用户为使用Isaac Sim进行物流或仓储机器人研究的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/ryanwu0521/CERLAB_Warehouse_Environment_IsaacSim?style=social)

- [isaac-sim-pick-and-place-simulation](https://github.com/raymondngiam/isaac-sim-pick-and-place-simulation) — 该项目提供了一个基于 Isaac Sim 的抓取与放置（Pick-and-Place）任务仿真环境，利用 Python 脚本在 Isaac Sim 中构建机械臂操作场景，包含 URDF 模型加载、物体交互和任务逻辑控制。它直接使用 Isaac Sim 的核心 API 实现物理仿真与传感器模拟，适用于希望快速开发和测试机器人操作策略的研究人员或工程师。 ![GitHub stars](https://img.shields.io/github/stars/raymondngiam/isaac-sim-pick-and-place-simulation?style=social)

- [Imitation_Learning](https://github.com/17enunez/Imitation_Learning) — 该项目专注于在NVIDIA Isaac Sim中实现机器人操作的模仿学习，利用Isaac Sim提供的高保真物理仿真环境训练机械臂执行复杂任务。项目通过记录专家演示数据并训练策略网络，实现对机器人动作的复现，适用于希望在Isaac Sim中快速验证模仿学习算法的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/17enunez/Imitation_Learning?style=social)

- [IsaacLab2](https://github.com/luoye2333/IsaacLab2) — 该项目是一个基于 NVIDIA Isaac Sim 构建的统一机器人学习框架，旨在简化强化学习与仿真环境的集成。它利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟能力，提供模块化组件用于快速搭建机器人训练流程。主要面向希望在高保真仿真中开发和测试机器人控制策略的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/luoye2333/IsaacLab2?style=social)

- [IsaacLab2](https://github.com/thallys-smo/IsaacLab2) — 该项目是一个基于 NVIDIA Isaac Sim 构建的统一机器人学习框架，旨在简化强化学习与仿真环境的集成。它直接利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能，提供模块化组件以支持多种机器人任务训练。目标用户为从事机器人学习研究与开发的工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/thallys-smo/IsaacLab2?style=social)

- [Stewart_IsaacSIm](https://github.com/Lancee0812/Stewart_IsaacSIm) — 该项目提供了一种在 Isaac Sim 中开发 Stewart 平台移动机器人的方法，利用 Isaac Sim 的 GPU 加速物理仿真能力构建并控制六自由度并联机器人。项目通过 Python 脚本实现机器人建模、驱动与运动控制逻辑，直接基于 Isaac Sim 的 API 进行场景搭建和动力学仿真。适用于希望在 Isaac Sim 中研究或部署 Stewart 平台的机器人开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Lancee0812/Stewart_IsaacSIm?style=social)

- [arctos_isaac_exts](https://github.com/lukasdante/arctos_isaac_exts) — 该项目为Arctos机械臂提供Isaac Sim扩展插件，主要用途是在Isaac Sim中集成和控制Arctos机器人手臂。通过自定义Python扩展实现与Isaac Sim的深度集成，支持在GPU加速的多物理仿真环境中进行机器人控制、测试与训练。目标用户为使用Arctos机械臂并希望在Isaac Sim中进行仿真的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/lukasdante/arctos_isaac_exts?style=social)

- [isaaclab](https://github.com/walt-neb/isaaclab) — 该项目提供了一个面向 Isaac Sim 的开发环境与机器人实验框架，主要用于搭建和测试基于 Isaac Lab 的强化学习与机器人控制任务。它集成了 Isaac Sim 的核心功能，支持 GPU 加速的物理仿真，并包含典型机器人场景的示例配置。目标用户为使用 NVIDIA Isaac Sim 进行机器人算法研发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/walt-neb/isaaclab?style=social)

- [IsaacLab-v221](https://github.com/JongYun-Kim/IsaacLab-v221) — 该项目是一个基于 NVIDIA Isaac Sim 构建的统一机器人学习框架，旨在简化强化学习与仿真环境的集成。它利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟能力，提供模块化组件以支持多种机器人任务训练。主要面向希望在高保真仿真中快速开发和测试机器人策略的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/JongYun-Kim/IsaacLab-v221?style=social)

- [IsaacLab-for-wm](https://github.com/Steven0928/IsaacLab-for-wm) — 该项目是一个基于 NVIDIA Isaac Sim 构建的机器人学习统一框架，旨在为 Isaac Lab 提供扩展支持。它利用 Isaac Sim 的 GPU 加速物理仿真能力，集成强化学习与运动控制模块，便于研究人员快速开发和测试机器人策略。目标用户为使用 Isaac Sim 进行机器人 AI 训练与仿真的开发者和科研人员。 ![GitHub stars](https://img.shields.io/github/stars/Steven0928/IsaacLab-for-wm?style=social)

- [IsaacSim_SDG](https://github.com/ArqumUddin/IsaacSim_SDG) — 该项目提供在Isaac Sim中生成合成数据（Synthetic Data Generation, SDG）的代码实现，主要利用Isaac Sim的渲染与传感器模拟能力创建带标注的多模态训练数据。通过Python脚本控制场景、物体和相机参数，自动化生成用于计算机视觉或机器人感知任务的数据集。目标用户为需要高效构建仿真训练数据的AI与机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/ArqumUddin/IsaacSim_SDG?style=social)

- [IsaacLab_sim2sim](https://github.com/Holiclife-KTH/IsaacLab_sim2sim) — 该项目旨在实现 Isaac Lab 中的仿真到仿真（sim2sim）迁移，主要用于在不同物理参数或环境配置下验证强化学习策略的鲁棒性。其核心基于 Isaac Lab 构建，利用其模块化任务框架和 GPU 加速物理引擎，支持快速部署与测试机器人控制策略。目标用户为使用 Isaac Sim/Isaac Lab 进行机器人仿真研究的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Holiclife-KTH/IsaacLab_sim2sim?style=social)

- [IsaacSim2IsaacLab](https://github.com/dattran-itrvn/IsaacSim2IsaacLab) — 该项目旨在帮助用户学习和迁移 NVIDIA Omniverse 中的机器人仿真工具 Isaac Sim 与 Isaac Lab，提供两者之间的对比、转换示例或集成方法。通过 Python 脚本展示如何在 Isaac Sim 和 Isaac Lab 之间复用资产、传感器配置或任务逻辑，利用 Omniverse 的 USD 架构和 PhysX 物理引擎实现一致性仿真。适合希望掌握 NVIDIA 最新机器人开发栈的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/dattran-itrvn/IsaacSim2IsaacLab?style=social)

- [Biped-Simulation-Isaac-Sim-stage](https://github.com/roger20415/Biped-Simulation-Isaac-Sim-stage) — 该项目提供了一个用于双足机器人仿真的 Isaac Sim USD 场景文件（.usda），可直接在 Isaac Sim 中加载以构建双足运动仿真环境。其核心是基于 NVIDIA Omniverse 的 USD 格式资产，便于与 Isaac Sim 的物理引擎和传感器系统集成。适用于希望快速搭建双足机器人仿真场景的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/roger20415/Biped-Simulation-Isaac-Sim-stage?style=social)

- [isaac-sim-examples](https://github.com/arthur-coast/isaac-sim-examples) — 该项目复现了 NVIDIA Isaac Sim 官方文档中的教程示例，主要用途是帮助用户快速上手 Isaac Sim 的核心功能。它通过 Python 脚本展示了如何在 Isaac Sim 中构建场景、加载资产、配置传感器及运行仿真，紧密贴合官方最新教程内容。目标用户为希望学习 Isaac Sim 基础操作和工作流的开发者与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/arthur-coast/isaac-sim-examples?style=social)

- [UR3_moveit_isaacsim](https://github.com/nktchen/UR3_moveit_isaacsim) — 该项目展示了如何在 Isaac Sim 中集成 MoveIt 进行 UR3 机械臂的运动规划，通过 Python 脚本实现 ROS 与 Isaac Sim 的通信，利用 Isaac Sim 的 GPU 加速物理仿真能力验证 MoveIt 生成的轨迹。项目直接面向 Isaac Sim 用户，提供具体机器人平台（UR3）的运动规划示例，适合希望在 Isaac Sim 中使用 MoveIt 的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/nktchen/UR3_moveit_isaacsim?style=social)

- [UR3eDT](https://github.com/BogdanCBC1/UR3eDT) — 该项目为UR3e机械臂构建了一个基于Isaac Sim的数字孪生系统，利用Isaac Sim的GPU加速物理仿真能力实现高保真虚拟复现。通过Python脚本集成UR3e的运动学与动力学模型，并支持与真实硬件的潜在数据交互。主要面向机器人研究人员和工程师，用于在Isaac Sim环境中开发和测试UR3e控制策略。 ![GitHub stars](https://img.shields.io/github/stars/BogdanCBC1/UR3eDT?style=social)

- [isaacsim-webrtc](https://github.com/robotecht/isaacsim-webrtc) — 该项目演示了如何通过 WebRTC 技术将 Isaac Sim 以网页客户端形式进行远程托管和访问，利用 Docker 容器化部署实现流式传输 Isaac Sim 的仿真画面。其核心是为 Isaac Sim 提供基于浏览器的轻量化交互入口，便于远程操作与展示。目标用户为需要在无本地安装环境下访问 Isaac Sim 仿真的开发者或测试人员。 ![GitHub stars](https://img.shields.io/github/stars/robotecht/isaacsim-webrtc?style=social)

- [IsaacSimTests](https://github.com/Autrio/IsaacSimTests) — 该项目主要用于测试 Isaac Sim 中的控制器性能与物理模拟能力，通过 Python 脚本验证其多物理引擎（如 PhysX）在机器人控制任务中的表现。项目直接基于 Isaac Sim 构建，包含针对其仿真环境的定制化测试用例，适用于希望评估或调试 Isaac Sim 物理仿真精度与控制器集成效果的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Autrio/IsaacSimTests?style=social)

- [Bittle-IsaacSim](https://github.com/Dafodilrat/Bittle-IsaacSim) — 该项目旨在使用Isaac Sim训练四足机器人Bittle，提供了一个GUI扩展界面，允许用户选择强化学习算法、配置地面类型并调整RL参数。项目直接基于Isaac Sim构建，利用其GPU加速的物理仿真能力进行机器人训练，适用于希望在Isaac Sim中快速实验四足机器人控制策略的研究者和开发者。 ![GitHub stars](https://img.shields.io/github/stars/Dafodilrat/Bittle-IsaacSim?style=social)

- [IsaacSim_Teleoperation](https://github.com/0right0705/IsaacSim_Teleoperation) — 该项目实现了一个基于RMPflow和XR手部追踪的双手遥操作系统，专为Isaac Sim构建，利用其物理仿真与机器人控制能力，通过手部追踪设备实时驱动双臂机器人。系统集成NVIDIA Isaac Sim的仿真环境与RMPflow运动规划框架，适用于需要高保真人机交互的机器人遥操作研究与开发人员。 ![GitHub stars](https://img.shields.io/github/stars/0right0705/IsaacSim_Teleoperation?style=social)

- [isaac_multi_robot](https://github.com/mylad13/isaac_multi_robot) — 该项目旨在在 Isaac Sim 中实现多机器人导航功能，提供基于 Python 的示例代码和配置，利用 Isaac Sim 的多智能体仿真能力与 GPU 加速物理引擎，支持多个机器人在共享环境中协同导航与避障。项目直接面向 Isaac Sim 用户，适用于需要开发或测试多机器人系统的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/mylad13/isaac_multi_robot?style=social)

- [unitree_isaaclab](https://github.com/leeyngdo/unitree_isaaclab) — 该项目是 IsaacLab 的修改克隆版本，专门针对 Unitree 四足机器人进行适配和定制。它继承了 Isaac Sim 的 GPU 加速物理仿真能力，并集成了 Unitree 机器人的 URDF 模型、控制器和任务配置，便于在 Isaac Lab 框架下快速开发和测试四足运动策略。目标用户为使用 Unitree 机器人并希望基于 Isaac Sim 生态进行强化学习或控制算法研究的开发者。 ![GitHub stars](https://img.shields.io/github/stars/leeyngdo/unitree_isaaclab?style=social)

- [AMR_IsaacSim_VSLAM](https://github.com/PiatekBartosz/AMR_IsaacSim_VSLAM) — 该项目在NVIDIA Isaac Sim中构建了一个AMR（自主移动机器人）的视觉SLAM（V-SLAM）仿真系统，利用Isaac Sim的高保真传感器模拟和物理引擎实现摄像头数据生成与机器人运动控制。项目直接基于Isaac Sim环境开发，展示了如何集成V-SLAM算法进行定位与建图，适用于机器人感知与导航研究者及开发者。 ![GitHub stars](https://img.shields.io/github/stars/PiatekBartosz/AMR_IsaacSim_VSLAM?style=social)

- [Sim-to-Real-Isaac-Sim](https://github.com/IGL5/Sim-to-Real-Isaac-Sim) — 该项目利用 Isaac Sim Replicator 和域随机化技术生成合成图像，旨在缩小仿真与现实之间的差距。它直接基于 Isaac Sim 的合成数据生成能力，通过 Python 脚本控制场景、材质、光照等参数的随机化，为机器人感知模型提供多样化训练数据。主要面向从事 Sim-to-Real 迁移研究的机器人开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/IGL5/Sim-to-Real-Isaac-Sim?style=social)

- [ros2-camera-publisher](https://github.com/surong15/ros2-camera-publisher) — 该项目是一个Isaac Sim扩展插件，通过ROS2 Bridge将Isaac Sim中生成的相机图像发布到ROS2话题，实现仿真传感器数据与ROS2生态的无缝对接。其核心功能依赖于Isaac Sim的扩展机制和NVIDIA提供的ROS2桥接工具，适用于需要在Isaac Sim中进行机器人视觉算法开发并集成到ROS2系统的开发者。 ![GitHub stars](https://img.shields.io/github/stars/surong15/ros2-camera-publisher?style=social)

- [isaac-sim-use-cases](https://github.com/wty-yy/isaac-sim-use-cases) — 该项目整理了学习 Isaac Sim 过程中的多个使用案例，主要通过 Python 脚本展示如何在 Isaac Sim 中构建和操作仿真场景。内容涵盖传感器配置、机器人控制和环境交互等典型任务，直接基于 Isaac Sim 的 API 实现，适合初学者和开发者快速上手 Isaac Sim 的核心功能。 ![GitHub stars](https://img.shields.io/github/stars/wty-yy/isaac-sim-use-cases?style=social)

- [IsaacSimJackalMazeEscape](https://github.com/ArathBC/IsaacSimJackalMazeEscape) — 该项目是一个基于 Isaac Sim 的迷宫逃脱程序，利用 Jackal 机器人内置的 LiDAR 进行环境感知，并通过 A* 算法规划路径以实现自主导航。项目直接使用 Isaac Sim 提供的 Jackal 机器人模型和仿真环境，展示了在 Isaac Sim 中集成感知与路径规划算法的完整流程。适用于希望在 Isaac Sim 中开发移动机器人导航功能的研究者或开发者。 ![GitHub stars](https://img.shields.io/github/stars/ArathBC/IsaacSimJackalMazeEscape?style=social)

- [isaac-sim-launcher](https://github.com/eesoymilk/isaac-sim-launcher) — 该项目提供了一个 Shell 脚本，用于在 Docker 容器中启动 NVIDIA Isaac Sim，并通过 WebRTC 实现远程流式传输。它简化了 Isaac Sim 的部署流程，特别适用于无图形界面的服务器环境，利用 Docker 封装依赖并集成 WebRTC 以支持浏览器端可视化交互。目标用户为需要远程访问或云端部署 Isaac Sim 的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/eesoymilk/isaac-sim-launcher?style=social)

- [isaac-sim-docker](https://github.com/efwoods/isaac-sim-docker) — 该项目提供了一个在 Docker 容器中运行 Isaac Sim 的解决方案，通过 Shell 脚本简化了环境配置与部署流程。它封装了 Isaac Sim 所需的依赖和 GPU 驱动设置，便于用户快速启动仿真环境。主要面向希望在隔离、可复现环境中使用 Isaac Sim 进行机器人仿真与 AI 训练的开发者。 ![GitHub stars](https://img.shields.io/github/stars/efwoods/isaac-sim-docker?style=social)

- [NonPlanarIsaacSim](https://github.com/mlab-upenn/NonPlanarIsaacSim) — 该项目为非完整约束轮式机器人提供 Isaac Sim 仿真环境配置，专门针对非平面地形下的运动控制与导航任务。通过集成 Isaac Sim 的物理引擎和传感器模拟功能，支持自定义机器人模型与复杂地形交互的高保真仿真。主要面向从事移动机器人研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/mlab-upenn/NonPlanarIsaacSim?style=social)

- [Nvidia-Isaac-Learning-Note](https://github.com/BroPants/Nvidia-Isaac-Learning-Note) — 该项目是一份关于 NVIDIA Isaac Sim 和 Isaac Lab 的学习笔记，旨在帮助用户理解和使用这两个机器人仿真平台。内容涵盖基础概念、环境搭建、API 使用及示例代码解析，侧重于 Isaac Sim 的功能特性和 Isaac Lab 的强化学习集成。适合刚接触 NVIDIA 机器人仿真生态的开发者和研究人员参考。 ![GitHub stars](https://img.shields.io/github/stars/BroPants/Nvidia-Isaac-Learning-Note?style=social)

- [isaac-downloader](https://github.com/dyz9219/isaac-downloader) — 该项目是一个跨平台桌面应用，用于批量下载 Isaac Sim 平台文件，专为需要高效获取 Isaac Sim 相关资源（如资产、示例或版本包）的开发者和研究人员设计。基于 Svelte 构建，提供图形化界面简化下载流程，直接服务于 Isaac Sim 用户在离线或低带宽环境下的部署需求。 ![GitHub stars](https://img.shields.io/github/stars/dyz9219/isaac-downloader?style=social)

- [isaac-sim-tutorial-4-5-0](https://github.com/Isaacsimkr-2nd/isaac-sim-tutorial-4-5-0) — 该项目是面向 Isaac Sim 4.5.0 版本的韩语教程仓库，旨在帮助用户学习和掌握 Isaac Sim 的基本操作与开发流程。内容涵盖环境搭建、仿真场景构建及机器人控制等核心功能，直接基于 Isaac Sim 官方平台进行教学演示。目标用户为希望使用 Isaac Sim 进行机器人仿真的韩语开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Isaacsimkr-2nd/isaac-sim-tutorial-4-5-0?style=social)

- [Simulation](https://github.com/AGIBotTF/Simulation) — 该项目结合物理仿真与强化学习，专为 NVIDIA Isaac Sim 构建，利用其 GPU 加速的多物理引擎进行机器人训练。通过 Isaac Sim 的 Python API 实现环境搭建与智能体交互，支持自定义 RL 任务。主要面向希望在高保真仿真中开发和测试机器人控制策略的研究者与工程师。 ![GitHub stars](https://img.shields.io/github/stars/AGIBotTF/Simulation?style=social)

- [fanuc_isaac_wrapper](https://github.com/AtlasAtCal87/fanuc_isaac_wrapper) — 该项目为FANUC M-900iB/700机器人臂提供了一个Isaac Sim专用的Python封装，使其能在NVIDIA Isaac Sim环境中进行高保真仿真与控制。通过集成URDF模型和关节配置，支持在Isaac Sim的PhysX引擎中实现精确的动力学模拟，便于开发和测试机器人控制算法。目标用户为使用FANUC工业机械臂并希望在Isaac Sim中进行仿真的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/AtlasAtCal87/fanuc_isaac_wrapper?style=social)

- [spot_isaac_adapter](https://github.com/strapsai/spot_isaac_adapter) — 该项目允许用户直接在 Isaac Sim 中调用 Boston Dynamics Spot 机器狗的 API，实现真实机器人与仿真环境的无缝对接。通过 Python 接口封装，它将 Spot 的控制、传感和状态数据集成到 Isaac Sim 的仿真流程中，便于开发和测试机器人算法。主要面向使用 Spot 并希望在 Isaac Sim 中进行高保真仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/strapsai/spot_isaac_adapter?style=social)

- [isaac_sim_lerobot](https://github.com/shetshield/isaac_sim_lerobot) — 该项目旨在利用 Isaac Sim 进行机器人学习数据采集，并将数据保存为 LeRobot v3 格式。它通过 Isaac Sim 的传感器模拟和物理引擎生成高质量的机器人交互数据，适用于模仿学习和行为克隆任务。项目直接集成 Isaac Sim 作为仿真后端，目标用户为使用 LeRobot 框架进行机器人学习研究的开发者。 ![GitHub stars](https://img.shields.io/github/stars/shetshield/isaac_sim_lerobot?style=social)

- [firefighter_isaacsim_ros2](https://github.com/seunghyeonsim/firefighter_isaacsim_ros2) — 该项目实现了一个面向消防机器人的 Isaac Sim ROS2 节点，通过自定义 ROS2 接口与 Isaac Sim 仿真环境集成，支持传感器数据发布与控制指令接收。项目利用 Isaac Sim 的 Python API 构建仿真场景，并通过 ROS2 Humble 实现机器人与仿真器的双向通信，适用于需要在 Isaac Sim 中开发和测试 ROS2 驱动型消防或应急响应机器人的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/seunghyeonsim/firefighter_isaacsim_ros2?style=social)

- [IsaacLab_sim2real](https://github.com/syed-dce/IsaacLab_sim2real) — 该项目专注于在 Isaac Lab 中训练 PKL Gen3 机器人，并实现从仿真到现实（sim2real）的迁移及 ROS 部署。它直接基于 Isaac Lab 构建，利用其强化学习和物理仿真能力进行策略训练，并通过 ROS 接口将训练好的策略部署到真实机器人上。适用于希望利用 Isaac Sim 生态进行机器人 sim2real 研究与应用的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/syed-dce/IsaacLab_sim2real?style=social)

- [isaac_sim_mqtt](https://github.com/angkira/isaac_sim_mqtt) — 该项目为 NVIDIA Isaac Sim 4.5.0 提供了一个自定义的 MQTT 桥接器，用于在仿真环境与外部系统之间通过 MQTT 协议实现实时数据通信。它直接面向 Isaac Sim 构建，利用其扩展机制实现传感器数据发布或控制指令订阅，适用于需要将 Isaac Sim 接入物联网或远程控制系统的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/angkira/isaac_sim_mqtt?style=social)

- [IsaacSim_InstallScript](https://github.com/cmjang/IsaacSim_InstallScript) — 该项目提供 Shell 脚本，用于在 CentOS 7 和 Ubuntu 20.04 等旧版 Linux 发行版上安装 NVIDIA Isaac Sim，解决因 glibc 版本过低导致的兼容性问题。通过自动化依赖处理和环境配置，简化了在非官方支持系统上的部署流程。主要面向需要在遗留系统中使用 Isaac Sim 进行机器人仿真的开发者。 ![GitHub stars](https://img.shields.io/github/stars/cmjang/IsaacSim_InstallScript?style=social)

- [IsaacSim-Hil-Serl](https://github.com/Incalos/IsaacSim-Hil-Serl) — 该项目基于 Isaac Sim 构建的虚拟环境，实现真实世界强化学习算法 Hil-Serl 的训练与部署。它明确使用 Isaac Lab（Isaac Sim 的机器人学习框架）作为核心仿真平台，并通过 Python 实现与物理机器人的闭环交互。目标用户为从事具身智能与真实机器人强化学习研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Incalos/IsaacSim-Hil-Serl?style=social)

- [Isaac_spot_tutorials](https://github.com/carolzyy/Isaac_spot_tutorials) — 该项目提供在 Isaac Sim 中配置和控制 Spot 机器人任务的教程，主要使用 Python 编写，涵盖机器人环境搭建、传感器配置及基本控制逻辑。项目直接基于 Isaac Sim 平台开发，利用其 PhysX 物理引擎和 ROS 2 集成功能，帮助用户快速上手四足机器人仿真。适用于希望在 Isaac Sim 中开展 Spot 机器人仿真实验的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/carolzyy/Isaac_spot_tutorials?style=social)

- [hp-sim3](https://github.com/tobbelobb/hp-sim3) — 该项目利用 Isaac Lab 对 Hangprinter（一种绳驱3D打印机）进行仿真，通过 Isaac Sim 的物理引擎和机器人模拟能力构建高保真动力学模型。它集成了 Isaac Lab 的任务框架与传感器模拟功能，支持对绳索张力、运动控制及打印轨迹的实时仿真与分析。主要面向机器人研究人员和增材制造开发者，用于测试新型控制算法或机械设计在复杂绳驱系统中的表现。 ![GitHub stars](https://img.shields.io/github/stars/tobbelobb/hp-sim3?style=social)

- [IsaacSimBestPractice](https://github.com/yizhouzhao-nvidia/IsaacSimBestPractice) — 该项目旨在提供 Isaac Sim 的最佳实践指南，涵盖高效使用该平台进行机器人仿真与AI训练的推荐方法。内容聚焦于 Isaac Sim 特有的工作流优化、性能调优及常见问题解决方案，采用 Python 编写示例脚本以演示核心功能。目标用户为希望提升 Isaac Sim 开发效率和仿真质量的工程师与研究人员。 ![GitHub stars](https://img.shields.io/github/stars/yizhouzhao-nvidia/IsaacSimBestPractice?style=social)

- [Quadruped-Robot-IsaacSim](https://github.com/aquacommander/Quadruped-Robot-IsaacSim) — 该项目旨在使用强化学习（RL）在NVIDIA Omniverse中训练四足机器人行走，明确基于Isaac Sim平台构建仿真环境。它利用Isaac Sim的GPU加速物理引擎和RL训练能力，实现四足机器人的运动控制策略开发。目标用户为从事机器人强化学习研究与仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/aquacommander/Quadruped-Robot-IsaacSim?style=social)

- [isaac-sim-docker-playground](https://github.com/B-ramB/isaac-sim-docker-playground) — 该项目提供了一个基于 Docker 的运行环境，用于快速启动和测试 NVIDIA Isaac Sim，简化了依赖配置和部署流程。通过容器化封装 Isaac Sim 所需的 GPU 驱动、CUDA 和 Omniverse 组件，支持在兼容系统上一键运行仿真。主要面向希望便捷使用 Isaac Sim 进行机器人仿真与 AI 训练的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/B-ramB/isaac-sim-docker-playground?style=social)

- [isaac-anymal-runner](https://github.com/willh003/isaac-anymal-runner) — 该项目用于在NVIDIA Isaac Sim中加载并控制Anymal四足机器人，提供Python脚本实现机器人模型导入、关节控制及基础运动逻辑。代码直接调用Isaac Sim的仿真接口，适配其物理引擎与传感器模拟功能，便于开发者快速测试四足机器人控制算法。主要面向使用Isaac Sim进行足式机器人研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/willh003/isaac-anymal-runner?style=social)

- [Isaac-fishing-rod](https://github.com/sidthebuilder/Isaac-fishing-rod) — 该项目基于 NVIDIA Isaac Sim 4.5 实现了一个钓鱼竿的物理仿真，核心特性是使用可断裂的 D6 关节模拟鱼线或竿节的动态断裂行为。通过 Isaac Sim 的 GPU 加速多体动力学系统，展示了复杂约束与破坏效果的建模方法，适用于对柔性结构或断裂机制感兴趣的机器人仿真开发者。 ![GitHub stars](https://img.shields.io/github/stars/sidthebuilder/Isaac-fishing-rod?style=social)

- [isaac-sim-ufactory-example](https://github.com/heig-vd-iAi-LaRA/isaac-sim-ufactory-example) — 该项目提供将uFactory xArm6机器人导入NVIDIA Isaac Sim所需的文件，包括URDF模型和配置脚本，便于在Isaac Sim中进行仿真与控制。通过适配Isaac Sim的资产加载和关节控制接口，用户可快速集成该机械臂用于机器人算法开发或教学演示。主要面向使用Isaac Sim进行协作机器人仿真的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/heig-vd-iAi-LaRA/isaac-sim-ufactory-example?style=social)

- [tm-digital-robot-is45-publish](https://github.com/TM-Vision/tm-digital-robot-is45-publish) — 该项目为 TM Digital Robot 提供了针对 Omniverse Isaac Sim 4.5 的专用集成，使用户能在 Isaac Sim 环境中加载和控制该数字机器人模型。项目通过 Python 脚本实现机器人 URDF/SDF 模型导入、关节控制及与 Isaac Sim 物理引擎的对接，支持在 GPU 加速仿真中进行机器人算法开发与测试。主要面向使用 TM 机器人并希望在 Isaac Sim 中进行仿真的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/TM-Vision/tm-digital-robot-is45-publish?style=social)

- [Isaac-Sim-Document](https://github.com/OMS524/Isaac-Sim-Document) — 该项目提供 Isaac Sim 的安装指南与基础教程，帮助用户快速上手该仿真平台。内容聚焦于环境配置和基本操作流程，适用于初学者或需要本地部署支持的开发者。作为专门面向 Isaac Sim 的文档资源，它直接服务于 NVIDIA Isaac Sim 用户群体。 ![GitHub stars](https://img.shields.io/github/stars/OMS524/Isaac-Sim-Document?style=social)

- [Isaac-Sim-Biped-Manager](https://github.com/roger20415/Isaac-Sim-Biped-Manager) — 该项目是一个专为 Isaac Sim 开发的扩展包，用于管理和控制双足机器人。它通过 Python 实现与 Isaac Sim 的深度集成，提供机器人状态监控、运动控制和仿真管理功能。主要面向在 Isaac Sim 中进行双足机器人仿真的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/roger20415/Isaac-Sim-Biped-Manager?style=social)

- [Isaac-Sim-Mobile-Robot-Simulation](https://github.com/Prajyot9501/Isaac-Sim-Mobile-Robot-Simulation) — 该项目主要用于在 Isaac Sim 中演示移动机器人仿真，提供完整的场景搭建与控制逻辑示例。它直接基于 Isaac Sim 构建，利用其 PhysX 物理引擎和 ROS 2 集成能力实现移动机器人的运动控制与环境交互。适合希望快速上手 Isaac Sim 进行移动机器人开发的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/Prajyot9501/Isaac-Sim-Mobile-Robot-Simulation?style=social)

- [isaac-sim-livekit](https://github.com/ian8053/isaac-sim-livekit) — 该项目实现在 Isaac Sim 中通过 LiveKit WebRTC 将实时视频流传输至网页浏览器，利用 Isaac Sim 的传感器渲染能力与 LiveKit 的低延迟通信技术，为远程监控或人机交互场景提供可视化支持。主要面向需要在 Web 端实时查看 Isaac Sim 仿真画面的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/ian8053/isaac-sim-livekit?style=social)

- [fork-isaac_rover_2.0](https://github.com/superdiode/fork-isaac_rover_2.0) — 该项目实现了基于 Isaac Gym/Sim 的火星车 2.0 仿真系统，利用 NVIDIA Isaac Sim 的 GPU 加速物理引擎对火星车进行动力学建模与控制算法测试。项目通过 URDF 导入和自定义传感器配置，构建了适用于行星探测任务的高保真仿真环境，目标用户为从事空间机器人或自主漫游车研发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/superdiode/fork-isaac_rover_2.0?style=social)

- [isaacsim-pick-and-place-hackathon](https://github.com/thiagolages/isaacsim-pick-and-place-hackathon) — 该项目是为 LycheeAI 与 REVEL Studios 联合举办的 Isaac Sim 抓取放置（Pick & Place）黑客松活动提供的示例或参赛模板，专注于在 Isaac Sim 中实现机器人操作任务。项目直接基于 Isaac Sim 构建，利用其 GPU 加速的物理仿真和机器人 SDK 实现抓取、物体识别与放置等核心功能，适合参与该黑客松的开发者或希望学习 Isaac Sim 机器人操作应用的用户。 ![GitHub stars](https://img.shields.io/github/stars/thiagolages/isaacsim-pick-and-place-hackathon?style=social)

- [IsaacSim-IsaacLab-installation-for-Windows-Easy-Tutorial](https://github.com/marcelpatrick/IsaacSim-IsaacLab-installation-for-Windows-Easy-Tutorial) — 该项目提供了一个面向 Windows 用户的简易教程，指导如何安装 NVIDIA Isaac Sim 及其配套框架 Isaac Lab。内容聚焦于解决 Windows 平台下常见的依赖、环境配置和兼容性问题，帮助用户快速搭建 Isaac Sim 开发环境。目标用户为希望在 Windows 系统上开展机器人仿真与强化学习研究的开发者或研究人员。 ![GitHub stars](https://img.shields.io/github/stars/marcelpatrick/IsaacSim-IsaacLab-installation-for-Windows-Easy-Tutorial?style=social)

- [HuNavIsaacPlugin](https://github.com/vballeo/HuNavIsaacPlugin) — HuNav-Isaac Plugin 是一个专为 NVIDIA Isaac Sim 开发的扩展插件，用于集成 HuNavSim 人类导航模拟器，实现逼真的人类智能体行为仿真。该插件通过 Python 接口将 HuNavSim 的人群动力学模型嵌入 Isaac Sim 场景，支持在机器人与人类共存环境中进行交互测试。主要面向需要在 Isaac Sim 中引入高保真人类行为模拟的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/vballeo/HuNavIsaacPlugin?style=social)

- [aloha_isaac_sim](https://github.com/LiTaobate/aloha_isaac_sim) — 该项目旨在将 ALOHA 双臂遥操作机器人系统移植到 Isaac Sim 平台，利用其 GPU 加速的物理仿真能力进行高保真机器人控制与学习研究。仓库包含针对 Isaac Sim 的环境配置、URDF 模型集成及任务脚本，支持在 Isaac Sim 中复现 ALOHA 的模仿学习流程。主要面向希望在 Isaac Sim 中开展双臂操作研究的机器人学习开发者。 ![GitHub stars](https://img.shields.io/github/stars/LiTaobate/aloha_isaac_sim?style=social)

- [isaac_sim_lukebot](https://github.com/whittlel/isaac_sim_lukebot) — 该项目实现了一个名为Lukebot的自定义全向麦轮机器人模型，专为NVIDIA Isaac Sim设计，集成了HolonomicController控制器并支持键盘遥操作。通过Isaac Sim的Python API构建，展示了如何在仿真环境中部署和控制全向移动机器人。适用于希望在Isaac Sim中开发或测试全向底盘控制算法的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/whittlel/isaac_sim_lukebot?style=social)

- [Isaac-sim_learning](https://github.com/jayounghoyos/Isaac-sim_learning) — 该项目是面向 NVIDIA Isaac Sim 的学习课程资源，以 Jupyter Notebook 形式提供交互式教程，帮助用户掌握 Isaac Sim 的基础操作与仿真开发流程。内容涵盖环境搭建、场景构建及机器人仿真等核心功能，直接围绕 Isaac Sim 平台展开教学。目标用户为希望快速上手 Isaac Sim 进行机器人仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/jayounghoyos/Isaac-sim_learning?style=social)

- [IsaacSim-Autonomous-Forklift-System](https://github.com/hasantahabagci/IsaacSim-Autonomous-Forklift-System) — 该项目实现了一个基于颜色识别的自主叉车系统，用于在 Isaac Sim 仿真环境中完成仓库货物分拣任务。它利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟（如 RGB 相机）实现感知与导航，并通过 Python 脚本控制叉车运动逻辑。项目直接构建于 Isaac Sim 平台之上，适用于机器人算法开发者和物流自动化研究人员。 ![GitHub stars](https://img.shields.io/github/stars/hasantahabagci/IsaacSim-Autonomous-Forklift-System?style=social)

- [stunt_sim_rl](https://github.com/stianFinjord/stunt_sim_rl) — 该项目利用Isaac Gym实现特技动作的强化学习仿真，专注于训练智能体完成高难度物理动作。通过Isaac Gym提供的GPU加速物理引擎和RL环境接口，构建了高效的训练流程。适用于研究基于Isaac Sim平台的机器人运动控制与强化学习算法的开发者。 ![GitHub stars](https://img.shields.io/github/stars/stianFinjord/stunt_sim_rl?style=social)

- [icar_2025_tutorial](https://github.com/Ekumen-OS/icar_2025_tutorial) — 该项目是为 ICAR 2025 研讨会准备的教程，专注于使用 Isaac Sim 生成合成数据。它提供了基于 Python 的示例代码和工作流程，展示如何利用 Isaac Sim 的 GPU 加速渲染与传感器模拟功能创建用于机器人感知任务的高质量合成数据集。目标用户为参与该研讨会的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/Ekumen-OS/icar_2025_tutorial?style=social)

- [isaacsim-blickfeld-sim](https://github.com/TL-4319/isaacsim-blickfeld-sim) — 该项目用于生成RTX LiDAR配置文件，以在NVIDIA Omniverse中模拟Blickfeld Cube1激光雷达传感器。它直接面向Isaac Sim环境，通过定制化配置实现高保真LiDAR仿真，依赖Omniverse的RTX渲染和传感器模拟能力。主要服务于需要在Isaac Sim中集成真实LiDAR模型的机器人感知与自动驾驶研发人员。 ![GitHub stars](https://img.shields.io/github/stars/TL-4319/isaacsim-blickfeld-sim?style=social)

- [quadruped-rl](https://github.com/rcrym/quadruped-rl) — 该项目在Isaac Sim中实现了一个12自由度四足机器人的强化学习训练框架，利用Isaac Sim的GPU加速物理仿真能力进行高效策略学习。项目直接基于Isaac Sim构建环境，采用Python编写，集成了机器人建模、传感器模拟与RL训练流程。适用于希望在高保真仿真中开发四足机器人控制算法的研究者和工程师。 ![GitHub stars](https://img.shields.io/github/stars/rcrym/quadruped-rl?style=social)

- [similitude](https://github.com/Kukanani/similitude) — 该项目旨在为 Isaac Sim 和 Isaac Lab 验证并创建资产与场景，提供工具链支持以确保内容兼容性和正确性。其核心功能包括场景结构校验、USD 资产合规性检查及与 Isaac Sim/Lab 环境的集成验证，基于 Python 和 Omniverse USD 工具构建。主要面向使用 Isaac Sim 进行机器人仿真开发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/Kukanani/similitude?style=social)

- [walkie-xr-teleop](https://github.com/EIC-Robocup-2026/walkie-xr-teleop) — 该项目提供基于XR（扩展现实）的遥操作功能，支持通过WalkieSDK在Isaac Sim仿真环境和真实机器人之间进行控制。其核心是实现Isaac Sim与XR设备的集成，利用Python开发交互接口，使用户能以沉浸式方式操控人形机器人。主要面向参与RoboCup 2026竞赛的EIC团队及使用Isaac Sim进行人形机器人仿真的开发者。 ![GitHub stars](https://img.shields.io/github/stars/EIC-Robocup-2026/walkie-xr-teleop?style=social)

- [isaac_sim_robot_base_eval](https://github.com/li-rh/isaac_sim_robot_base_eval) — 该项目提供了一个 Isaac Sim 测试环境，用于验证 Isaac Sim 安装和基础功能是否正常运行，并作为构建新机器人仿真环境的基底。它通过 Python 脚本加载简单机器人模型并执行基本仿真循环，帮助用户快速确认 Isaac Sim 的 GPU 加速物理引擎和渲染管线是否就绪。适用于刚部署 Isaac Sim 并希望快速验证或以此为基础开发自定义场景的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/li-rh/isaac_sim_robot_base_eval?style=social)

- [DexLab](https://github.com/raymondyu5/DexLab) — DexLab 是一个基于 NVIDIA Isaac Sim 构建的统一机器人学习框架，旨在简化强化学习与仿真环境的集成。项目直接利用 Isaac Sim 的 GPU 加速物理仿真能力，提供模块化组件用于灵巧手操作等任务的训练与测试。其核心采用 Python 实现，面向希望在高保真 Isaac Sim 环境中快速开发和部署机器人学习算法的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/raymondyu5/DexLab?style=social)

- [Pushing-Assisted-Placing-on-a-Tabletop](https://github.com/ChenXYxm/Pushing-Assisted-Placing-on-a-Tabletop) — 该项目是一个基于 NVIDIA Isaac Sim 构建的机器人学习统一框架，专注于桌面场景下的推动物体辅助放置任务。它利用 Isaac Sim 的 GPU 加速物理仿真能力，实现高保真环境交互与策略训练，适用于研究接触丰富的操作任务的科研人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/ChenXYxm/Pushing-Assisted-Placing-on-a-Tabletop?style=social)

- [isaac-sim-synthetic-data](https://github.com/13anurag/isaac-sim-synthetic-data) — 该项目提供用于 Isaac Sim 的 Python 脚本，支持相机与光照随机化、LiDAR 点云生成及 3D 网格创建，旨在提升合成数据多样性。其直接利用 Isaac Sim 的传感器模拟和渲染能力，通过 Omniverse Kit 和 USD 场景操作实现自动化数据生成流程。适用于需要在 Isaac Sim 中高效生成高质量训练数据的机器人感知研究人员。 ![GitHub stars](https://img.shields.io/github/stars/13anurag/isaac-sim-synthetic-data?style=social)

- [ShiBot-Inu](https://github.com/caelyasutake/ShiBot-Inu) — 该项目是一个基于强化学习训练的四足机器人ShiBot-Inu，专门在NVIDIA Isaac Sim和Isaac Lab中进行仿真与训练。它利用Isaac Lab提供的RL框架和Isaac Sim的高保真物理模拟环境，实现四足机器人的运动控制策略开发。目标用户为使用Isaac平台研究腿式机器人强化学习的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/caelyasutake/ShiBot-Inu?style=social)

- [isaac-sim-ros2](https://github.com/ian8053/isaac-sim-ros2) — 该项目提供了一个 Docker 启动器，用于运行 NVIDIA Isaac Sim 4.2.0 并集成 ROS 2 桥接功能，支持图形界面显示。通过 Shell 脚本封装了 Isaac Sim 与 ROS 2 的环境配置和容器启动流程，简化了在 Linux 系统上部署 Isaac Sim + ROS 2 联合仿真环境的复杂度。目标用户为需要在隔离容器中快速搭建 Isaac Sim 与 ROS 2 集成开发环境的机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/ian8053/isaac-sim-ros2?style=social)

- [isaac_jazzy_amr_ws](https://github.com/goooodday/isaac_jazzy_amr_ws) — 该项目是一个面向自主移动机器人（AMR）开发的ROS 2工作空间，专为在Isaac Sim中使用Jazzy Jalopy机器人模型而构建。它集成了Isaac Sim的仿真环境，提供传感器配置、导航栈和控制节点等关键组件，便于在GPU加速的多物理场仿真中进行算法开发与测试。目标用户为基于Isaac Sim开展AMR研发的机器人工程师和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/goooodday/isaac_jazzy_amr_ws?style=social)

- [DeformableIsaac](https://github.com/fmdazhar/DeformableIsaac) — 该项目提供了基于Isaac Sim的可变形四足机器人强化学习环境，支持PPO算法训练，并集成rsl_rl库实现高效策略学习。其核心是利用Isaac Sim的GPU加速物理仿真能力，构建包含软体或可变形部件的四足运动场景，适用于机器人控制与仿真的研究人员及开发者。 ![GitHub stars](https://img.shields.io/github/stars/fmdazhar/DeformableIsaac?style=social)

- [isaac-sim-simple-robot](https://github.com/Adhree1/isaac-sim-simple-robot) — 该项目提供了一个基于物理的差速驱动机器人仿真，专为 NVIDIA Isaac Sim 构建，并集成 ROS 2 实现 LiDAR 数据发布与 RViz 可视化。它利用 Isaac Sim 的 GPU 加速多物理引擎模拟真实传感器行为和机器人动力学，适用于希望在 Isaac Sim 中快速搭建 ROS 2 机器人仿真环境的研究者与开发者。 ![GitHub stars](https://img.shields.io/github/stars/Adhree1/isaac-sim-simple-robot?style=social)

- [Isaac-Sim-Particle-Simulation](https://github.com/Pharah4829/Isaac-Sim-Particle-Simulation) — 该项目为月球车（Luna Rover）在Isaac Sim中实现粒子仿真，利用Isaac Sim的GPU加速物理引擎模拟月壤等颗粒环境，支持机器人与松散地形的交互测试。项目直接基于Isaac Sim构建，包含场景设置、粒子系统配置及与机器人的动力学耦合，适用于行星探测机器人开发者和空间机器人研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Pharah4829/Isaac-Sim-Particle-Simulation?style=social)

- [Synthetic-data-generation](https://github.com/YASHWANT-HK/Synthetic-data-generation) — 该项目利用 NVIDIA Isaac Sim 生成苹果果实的合成图像数据，通过 Isaac Sim 的高保真渲染和物理模拟能力创建逼真的农业场景数据集。项目使用 Python 脚本控制 Isaac Sim 中的物体摆放、光照和相机参数，以生成多样化的训练样本。主要面向农业机器人视觉系统开发者，用于提升果实检测与识别模型的泛化能力。 ![GitHub stars](https://img.shields.io/github/stars/YASHWANT-HK/Synthetic-data-generation?style=social)

- [ArtificialDatasets](https://github.com/yprabhu23/ArtificialDatasets) — 该项目利用 NVIDIA Omniverse Replicator 在 Isaac Sim 中生成人工合成数据集，通过 Python 脚本控制场景、物体和传感器配置，实现高保真、带标注的多模态数据（如 RGB、深度、语义分割）自动化采集。其核心功能直接依赖 Isaac Sim 的渲染与仿真能力，专为需要大规模训练数据的机器人感知任务设计，适用于 AI 与机器人开发者。 ![GitHub stars](https://img.shields.io/github/stars/yprabhu23/ArtificialDatasets?style=social)

- [fluxa](https://github.com/vickiekknight/fluxa) — Fluxa 是一个 AI 代理，专门用于在 Isaac Sim 中自动生成合成场景，支持机器人仿真环境的快速构建。该项目直接集成 Isaac Sim 的场景生成 API，利用其 GPU 加速的多物理仿真能力，动态创建包含物体、光照和布局的多样化训练场景。目标用户为需要大规模合成数据进行机器人感知或行为训练的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/vickiekknight/fluxa?style=social)

- [O-Ring-Manipulation](https://github.com/cold-young/O-Ring-Manipulation) — 该项目是一个面向可变形O型环操作的仿真框架，基于NVIDIA Isaac Sim构建，利用其GPU加速的多物理场仿真能力实现高保真柔性体交互。项目集成了Isaac Sim的PhysX和Flex后端，支持机械臂对弹性环状物体的抓取、拉伸与装配任务模拟，适用于机器人操作算法研究与训练。目标用户为从事软体物体操作或工业装配自动化的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/cold-young/O-Ring-Manipulation?style=social)

- [sim2real_project](https://github.com/minseo104/sim2real_project) — 该项目基于 Isaac Lab 框架，使用 UR5e 机械臂与 Hand-E 夹爪实现 sim2real（仿真到现实）的机器人控制任务。项目利用 Isaac Sim 的 GPU 加速物理仿真能力，构建高保真机器人操作环境，并探索从仿真策略迁移到真实硬件的方法。主要面向从事机器人强化学习与 sim2real 迁移研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/minseo104/sim2real_project?style=social)

- [orbit](https://github.com/hojae-io/orbit) — 该项目是一个基于 NVIDIA Isaac Sim 构建的统一机器人学习框架，旨在为强化学习和仿真训练提供模块化工具链。它深度集成 Isaac Sim 的 GPU 加速物理引擎与传感器模拟功能，支持快速构建机器人任务环境。主要面向使用 Isaac Sim 进行机器人 AI 算法研发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/hojae-io/orbit?style=social)

- [SDG_Pipeline_Isaac_Sim](https://github.com/ElieGF/SDG_Pipeline_Isaac_Sim) — 该项目是一个基于Isaac Sim构建的模块化合成数据生成管道，专门用于生成带颜色和标注信息的3D点云数据。它利用Isaac Sim的传感器模拟能力（如深度相机）和场景渲染功能，结合Python脚本实现自动化数据采集与标注。目标用户为需要高质量3D训练数据的机器人感知或计算机视觉研究人员。 ![GitHub stars](https://img.shields.io/github/stars/ElieGF/SDG_Pipeline_Isaac_Sim?style=social)

- [fetch_nav_isaac](https://github.com/IRVLUTD/fetch_nav_isaac) — 该项目提供了一个Python接口，用于在NVIDIA Isaac Sim中控制Fetch机器人执行导航任务。它直接利用Isaac Sim的仿真环境和API，实现机器人运动控制与导航算法的集成，适用于需要在高保真物理仿真中开发和测试移动机器人导航策略的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/IRVLUTD/fetch_nav_isaac?style=social)

- [bravo_7_setup_for_isaac_sim](https://github.com/ashaig/bravo_7_setup_for_isaac_sim) — 该项目提供在 Isaac Sim 中模拟 Reach Bravo 7 机械臂所需的配置文件和操作指南，包含 URDF 模型导入、关节控制设置及与 Isaac Sim 物理引擎的集成方法。通过 Python 脚本实现机器人初始化与基本交互，便于用户快速部署该机械臂的仿真环境。主要面向使用 Isaac Sim 进行机器人算法开发与测试的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/ashaig/bravo_7_setup_for_isaac_sim?style=social)

- [FlockingEaglesIsaacSim](https://github.com/KevinFham/FlockingEaglesIsaacSim) — 该项目是 NASA Minds 2024 的参赛作品，利用 Isaac Sim 构建基于 GPU 加速物理仿真的鹰群编队飞行模拟系统。它通过 Isaac Sim 的多智能体仿真能力实现生物启发的群体行为算法，并集成 ROS 与传感器模型以支持自主导航研究。主要面向机器人集群控制与仿生飞行器开发的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/KevinFham/FlockingEaglesIsaacSim?style=social)

- [aau-rover-isaac-sim](https://github.com/AAU-Space-Robotics/aau-rover-isaac-sim) — 该项目为AAU空间机器人团队开发的火星车仿真模型，专为NVIDIA Isaac Sim平台构建，提供完整的机器人URDF模型、传感器配置及任务场景，支持在Isaac Sim中进行高保真物理仿真与自主导航算法测试。项目利用Isaac Sim的GPU加速多物理引擎和ROS 2接口，便于部署感知、规划与控制模块。主要面向从事行星探测机器人研究与开发的科研人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/AAU-Space-Robotics/aau-rover-isaac-sim?style=social)

- [isaac-sim-duckiebot-ros2](https://github.com/Yugeonu/isaac-sim-duckiebot-ros2) — 该项目在 NVIDIA Isaac Sim 中实现基于 Duckiebot 的自动驾驶仿真，通过 ROS2 OmniGraph 桥接实现通信，并采用 HSV 颜色空间进行红立方体目标跟踪。其核心功能依赖 Isaac Sim 的传感器模拟与物理引擎，专为希望在 Isaac Sim 中集成 ROS2 机器人应用的开发者设计。 ![GitHub stars](https://img.shields.io/github/stars/Yugeonu/isaac-sim-duckiebot-ros2?style=social)

- [ClaudeCode_PlanMode_PickAndPlace](https://github.com/scholarchoi-yjchoi/ClaudeCode_PlanMode_PickAndPlace) — 该项目提供了一个基于Isaac Sim 4.5的Pick and Place任务演示，使用Franka Panda机械臂实现抓取与放置操作。通过Python脚本调用Isaac Sim的仿真环境和机器人控制接口，展示了任务规划与执行流程。适用于希望在Isaac Sim中快速上手操作任务仿真的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/scholarchoi-yjchoi/ClaudeCode_PlanMode_PickAndPlace?style=social)

- [LabSim](https://github.com/DungCal/LabSim) — LabSim 是一个基于 NVIDIA Isaac Sim 构建的机器人仿真环境，沿用了 Isaac Lab 的项目结构，旨在提供模块化的机器人训练与测试框架。该项目直接依赖 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能，并利用其 Python API 实现任务配置与环境交互。主要面向希望在 Isaac Sim 生态中快速搭建自定义机器人仿真场景的研究人员与开发者。 ![GitHub stars](https://img.shields.io/github/stars/DungCal/LabSim?style=social)

- [isaaclab-a1-sim2real](https://github.com/TaroHime/isaaclab-a1-sim2real) — 该项目旨在基于 Isaac Lab 实现 A1 四足机器人的仿真到现实（sim2real）迁移，利用 Isaac Sim 的 GPU 加速物理仿真能力构建高保真训练环境。项目可能包含针对 Unitree A1 机器人的专用配置、强化学习策略及域随机化技术，以提升控制器在真实世界中的泛化性能。目标用户为从事四足机器人 sim2real 研究的科研人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/TaroHime/isaaclab-a1-sim2real?style=social)

- [VlaSim](https://github.com/DaiDai-106/VlaSim) — 该项目利用Isaac Sim仿真平台对开源视觉-语言-动作（VLA）模型进行推理与训练，直接基于Isaac Sim构建仿真环境以支持具身智能体的端到端学习。通过集成Isaac Sim的GPU加速物理引擎和传感器模拟功能，实现高保真交互训练。主要面向机器人AI研究人员及VLA模型开发者。 ![GitHub stars](https://img.shields.io/github/stars/DaiDai-106/VlaSim?style=social)

- [isaacsim-lio-sam](https://github.com/lollolha97/isaacsim-lio-sam) — 该项目是LIO-SAM激光惯性里程计的修改版本，专为集成NVIDIA Isaac Sim而设计，新增了适用于Isaac Sim环境的启动文件。通过适配传感器数据接口和时间同步机制，使LIO-SAM能在Isaac Sim的高保真仿真环境中运行，用于评估SLAM算法性能。主要面向在Isaac Sim中开发或测试机器人定位与建图系统的研究人员和工程师。 ![GitHub stars](https://img.shields.io/github/stars/lollolha97/isaacsim-lio-sam?style=social)

- [Isaac-Sim-Kuka-iiwa-14](https://github.com/ishangala16/Isaac-Sim-Kuka-iiwa-14) — 该项目在 Isaac Sim 中实现了 Kuka iiwa 14 机械臂与 Robotiq 2f 85 夹爪协同完成抓取和提升方块的任务。通过 USD 场景构建和 Python 脚本控制，展示了 Isaac Sim 的机器人操作仿真能力，适用于希望快速上手 Isaac Sim 进行机械臂任务开发的用户。 ![GitHub stars](https://img.shields.io/github/stars/ishangala16/Isaac-Sim-Kuka-iiwa-14?style=social)

- [Kuka_iiwa_14_Isaac_Sim](https://github.com/ishangala16/Kuka_iiwa_14_Isaac_Sim) — 该项目在 NVIDIA Isaac Sim 中实现了 KUKA iiwa 14 机械臂的仿真，采用微分逆运动学（Differential IK）控制使其精准到达随机目标位置。项目集成了夹爪控制、工作台和 NIST 标准测试板，构建了一个动态机器人操作环境，适用于 Isaac Sim 用户进行机器人控制算法开发与测试。 ![GitHub stars](https://img.shields.io/github/stars/ishangala16/Kuka_iiwa_14_Isaac_Sim?style=social)

- [isaac-sim-omnigraph-exts-template](https://github.com/Z3ZEL/isaac-sim-omnigraph-exts-template) — 该项目提供了一个用于创建 Isaac Sim Omnigraph Python 扩展的模板，包含一个示例节点，帮助开发者快速构建自定义计算图节点。它直接面向 Isaac Sim 的 Omnigraph 系统，利用其 Python API 实现节点逻辑，适用于需要扩展 Isaac Sim 可视化编程能力的机器人仿真开发者。 ![GitHub stars](https://img.shields.io/github/stars/Z3ZEL/isaac-sim-omnigraph-exts-template?style=social)

- [sdl_curobo](https://github.com/chohh7391/sdl_curobo) — 该项目利用 cuTAMP 在 Isaac Sim 中实现自驱动实验室（SDL），通过集成 NVIDIA 的 GPU 加速物理仿真环境，支持自动化实验流程的规划与执行。项目结合了任务与运动规划技术，面向需要在高保真仿真中进行自主科学实验的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/chohh7391/sdl_curobo?style=social)

- [Isaac_Launcher](https://github.com/brunorios1080/Isaac_Launcher) — Isaac_Launcher 提供一体化图形界面，简化 Isaac Sim 的安装、更新与启动流程，避免用户手动操作 Nucleus、GitHub 或扩展管理器。该项目专为 Isaac Sim 设计师打造，通过封装底层复杂性提升易用性，核心技术基于 Isaac Sim 官方工具链集成。目标用户是希望快速上手 Isaac Sim 而无需处理环境配置的机器人仿真开发者。 ![GitHub stars](https://img.shields.io/github/stars/brunorios1080/Isaac_Launcher?style=social)

- [IsaacGym_IsaacLab_Wiki](https://github.com/open-rdc/IsaacGym_IsaacLab_Wiki) — 该项目是一个汇总了Isaac Gym及其周边软件使用方法与故障排除指南的Wiki目录，明确面向Isaac Sim生态中的Isaac Gym和Isaac Lab组件。内容涵盖环境配置、常见问题解决及基础操作教程，采用文档形式组织，便于开发者快速上手。主要服务于使用NVIDIA Isaac平台进行机器人仿真与强化学习研究的用户。 ![GitHub stars](https://img.shields.io/github/stars/open-rdc/IsaacGym_IsaacLab_Wiki?style=social)

- [IsaacLab](https://github.com/kunkunwei/IsaacLab) — 该项目基于 Isaac Lab 框架，专注于轮腿平衡步兵机器人的强化学习训练，利用 Isaac Sim 提供的 GPU 加速物理仿真环境进行策略开发与验证。项目集成了 Isaac Gym 的高效并行仿真能力，并采用 PPO 等强化学习算法实现动态平衡控制。主要面向机器人强化学习研究者及 Isaac Sim 生态开发者。 ![GitHub stars](https://img.shields.io/github/stars/kunkunwei/IsaacLab?style=social)

- [IsaacLab](https://github.com/alvarobelmontebaeza/IsaacLab) — 该项目是 Isaac Lab 的一个分支，旨在添加局部操作（locomanipulation）环境，扩展了 Isaac Sim 平台在机器人灵巧操作任务中的模拟能力。它基于 Isaac Lab 框架构建，利用其 GPU 加速的物理仿真和强化学习基础设施，为研究人形机器人或移动操作平台提供定制化训练场景。主要面向需要在 Isaac Sim 生态中开发高级操作策略的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/alvarobelmontebaeza/IsaacLab?style=social)

- [IsaacLabTemplate](https://github.com/dlrdaile/IsaacLabTemplate) — 该项目是一个面向 Isaac Lab 的模板仓库，旨在为基于 Isaac Sim 的强化学习和机器人仿真项目提供标准化的代码结构和启动配置。它集成了 Isaac Lab 的核心功能，利用其 GPU 加速的物理仿真与 RL 训练框架，帮助用户快速搭建可复现的实验环境。目标用户为使用 Isaac Sim 进行机器人 AI 算法开发的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/dlrdaile/IsaacLabTemplate?style=social)

- [IsaacLab_tasks](https://github.com/ALRhub/IsaacLab_tasks) — 该项目提供面向 Isaac Lab 的自定义强化学习任务实现，主要用于机器人控制与仿真训练。通过继承 Isaac Lab 的任务框架，用户可快速构建和测试新型 RL 环境，并利用其 GPU 加速的物理仿真能力。项目适用于希望在 Isaac Sim 生态中开发或扩展机器人学习任务的研究人员与工程师。 ![GitHub stars](https://img.shields.io/github/stars/ALRhub/IsaacLab_tasks?style=social)

- [IsaacLab-Tutorial](https://github.com/Lab-of-AI-and-Robotics/IsaacLab-Tutorial) — 该项目是一个面向 Isaac Lab 的教程仓库，旨在帮助用户学习和使用 NVIDIA Isaac Lab 进行机器人仿真与强化学习开发。从其命名和所属组织可明确其专注于 Isaac Lab 生态，提供示例代码或教学材料以降低入门门槛。目标用户为希望利用 Isaac Sim 平台进行 AI 驱动机器人研究的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Lab-of-AI-and-Robotics/IsaacLab-Tutorial?style=social)

- [IsaacLab_Dodo](https://github.com/DoD0d0/IsaacLab_Dodo) — 该项目是一个轻量级的 Isaac Lab 工作区，专为 Dodo 机器人训练定制，提供针对该机器人的配置、任务定义和训练脚本。它基于 NVIDIA Isaac Lab 构建，利用其 GPU 加速的物理仿真和强化学习框架，简化了特定机器人模型的开发流程。主要面向使用 Dodo 机器人进行 AI 训练的研究人员和开发者。 ![GitHub stars](https://img.shields.io/github/stars/DoD0d0/IsaacLab_Dodo?style=social)

- [IsaacLab_snake](https://github.com/niels-holzmann/IsaacLab_snake) — 该项目基于 Isaac Lab 框架实现了一个蛇形机器人的仿真环境，利用 Isaac Sim 的 GPU 加速物理引擎对多关节柔性机器人进行建模与控制。代码展示了如何在 Isaac Lab 中构建自定义机器人资产、配置传感器及实现强化学习训练流程，适用于研究仿生机器人运动控制的开发者和研究人员。 ![GitHub stars](https://img.shields.io/github/stars/niels-holzmann/IsaacLab_snake?style=social)

- [IsaacLabDPPO](https://github.com/Aitthikit/IsaacLabDPPO) — 该项目提供了一个开箱即用的 Isaac Lab 配置与示例代码，专注于实现 DPPO（Decoupled PPO）算法及感知蒸馏编码器，便于在 Isaac Sim 的 GPU 加速仿真环境中快速开展强化学习训练。其核心内容包括针对 Isaac Lab 框架定制的训练配置、策略网络结构和感知模块集成，适用于希望在 NVIDIA Isaac Sim 平台上研究高效策略学习与感知-控制联合优化的机器人研究人员。 ![GitHub stars](https://img.shields.io/github/stars/Aitthikit/IsaacLabDPPO?style=social)

- [Wheelchair_IsaacLab](https://github.com/devpatel2003/Wheelchair_IsaacLab) — 该项目旨在基于 Isaac Lab 构建轮椅机器人的仿真环境，利用 Isaac Sim 的 GPU 加速物理引擎和传感器模拟功能，实现对轮椅运动控制与导航算法的开发与测试。项目直接基于 Isaac Lab 框架构建，包含自定义机器人模型、任务配置及强化学习训练流程，适用于康复机器人研究与辅助移动设备开发人员。 ![GitHub stars](https://img.shields.io/github/stars/devpatel2003/Wheelchair_IsaacLab?style=social)

- [IsaacLab-Work](https://github.com/scsean19/IsaacLab-Work) — 该项目主要用于探索在 NVIDIA Isaac Lab 中实现强化学习模型的方法，通过 Jupyter Notebook 提供了具体的实验代码和训练流程。项目直接基于 Isaac Lab 构建，展示了如何利用其 API 进行机器人策略训练与仿真，涉及 RL 环境配置、智能体训练及结果可视化等关键技术。适合希望快速上手 Isaac Lab 强化学习开发的研究者和工程师。 ![GitHub stars](https://img.shields.io/github/stars/scsean19/IsaacLab-Work?style=social)


---

<a id="related"></a>
## ⭐ 相关 Awesome 列表

- [awesome-isaac-gym](https://github.com/wangcongrobot/awesome-isaac-gym)
- [awesome-robotics](https://github.com/ahundt/awesome-robotics)

---

<div align="center">

## 🤖 自动生成

此列表由 [GPT-Awesome-List-Generator](https://github.com/shaoxiang/GPT-Awesome-List-Generator) 自动维护。

使用 AI 发现、筛选并组织 Isaac Sim 相关的高质量资源。

更新时间: 2026-02-03

</div>