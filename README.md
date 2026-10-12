# 李宏钢 · Honggang Li

**LLM Agents · AI for Science · Scientific Machine Learning**

华南师范大学硕士研究生，研究方向为人工智能驱动的科学研究与光学逆向设计。

我关注如何让智能体理解研究问题、获取专业材料、调用科学计算工具，并依据真实反馈持续推进任务。我的工作横跨 **Agent 系统、科学计算工具与机器学习模型**：既研究生成式模型和强化学习如何解决物理设计问题，也将检索、规划、仿真、写作和业务决策连接成可运行的研究链路。

[邮箱：2024022406@m.scnu.edu.cn](mailto:2024022406@m.scnu.edu.cn) · [GitHub](https://github.com/Lihonggang-scnu) · [已发表论文](https://www.oejournal.org/ioe/article/doi/10.67704/ioe.2026.260016)

## 研究兴趣与工作方向

| 研究方向 | 代表工作 |
| --- | --- |
| **科研 Agent 与任务编排** | 从自然语言研究问题出发，连接需求拆解、专业检索、材料读取、规划、工具执行和结果交付；处理长上下文、阶段恢复与模型调用成本 |
| **面向 Agent 的科学工具** | 将光学仿真、梯度优化、物理检查和容差分析封装为结构化工具，让模型能够根据计算反馈继续研究 |
| **物理机器学习与算法研究** | Encoder–Decoder 逆向设计、可微物理精修、机制可解释性、延迟奖励强化学习与仿真样本效率 |
| **跨领域应用集成** | 将科研链路经验迁移到纺织功能化学，连接资料判断、主动实验、配方优化、库存预测与约束排程 |

## 项目导航

| 项目 | 方向 | 核心工作 |
| --- | --- | --- |
| [OptoMind-Review](https://github.com/Lihonggang-scnu/OptoMInd-Review/tree/lihonggang-dev) | 科研 Agent / 文献综述 | 研究问题到材料理解、正文规划、写作指南与出版交付 |
| [OptoMind-Article](https://github.com/Lihonggang-scnu/OptoMind-Article) | 自主研究 / 闭环优化 | 文献启发、工具仿真、结果分析与反馈驱动的研究迭代 |
| [ChemIntent](https://github.com/Lihonggang-scnu/ChemIntent) | 化学 Agent / 研发决策 | 条件辨识、实验选择与生产资源协同 |
| [VeriTMM](https://github.com/Lihonggang-scnu/VeriTMM) | 科学计算 / Agent 工具 | 多层膜计算、可微逆向设计与独立物理核验 |
| [optomind-fulltext-acquisition](https://github.com/Lihonggang-scnu/optomind-fulltext-acquisition) | Agent 工具 / 材料获取 | 从文献身份到开放或机构授权全文的获取与交付 |
| [SpecFormer](https://github.com/Lihonggang-scnu/SpecFormer) | 生成式 AI / 光学逆向设计 | 全光谱条件编码、结构序列生成与可微物理精修 |
| [DG-DRL](https://github.com/Lihonggang-scnu/DG-DRL) | 强化学习 / AI4S | 逐变量决策与延迟评价，减少昂贵仿真调用 |

## 科研 Agent 与应用系统

### OptoMind-Review：从研究问题到完整综述的科研链路

**项目负责人 / 核心开发者** · `Agent Harness` `Literature Research` `Long Context` `Scientific Writing`

围绕“智能体如何充分理解材料，并将知识组织成有解释力的综述”设计端到端系统。

- **研究入口与材料理解**：将用户问题拆为研究子问题，组织检索表达与候选语料；接入论文身份解析、全文获取、本地材料搜索和按问题补读，为后续规划提供具体研究发现与适用条件。
- **深度规划与协作**：组织全局构思、章节分工、来源路由、章节负责人细化、案例选择及全文协调，保留机制解释、研究比较、条件与阴性结果在论证中的具体职责。
- **上下文与质量改进**：实现局部细纲加强、自主按需供材与可恢复执行；将细纲转化为写作指南，处理主讲位置、后章增量和连续写作安排。
- **写作与交付**：连接编排、正文写作、后置首尾生成、图表与引用统一及 Markdown / TeX / PDF 输出，管理材料、任务和来源在各环节间的交接。
- **代表运行**：历史光学场景的三次完整运行生成英文综述，平均每篇约 39 页、118 条参考文献；保留对应稿件与运行结果，后续版本持续开展真实材料上的局部和全链测试。

[新版开发入口](https://github.com/Lihonggang-scnu/OptoMInd-Review/tree/lihonggang-dev) · [链路说明](https://github.com/Lihonggang-scnu/OptoMInd-Review/blob/lihonggang-dev/docs/current/PIPELINE.md)

### OptoMind-Article：文献与仿真反馈驱动的自主科研

**项目负责人 / 核心开发者** · `Research Agent` `Tool Use` `Closed-loop Optimization` `Physics Simulation`

将科研任务组织为“问题分析 → 文献研究 → 路线设计 → 物理计算 → 结果分析 → 路线更新”的交互闭环。

- **任务与评价组织**：从自然语言目标建立研究任务，区分目标、约束与评价标准，使不同轮次的候选可以在一致标准下比较。
- **文献到设计的连接**：让专业材料参与路线构思，组织文献启发方案与独立对照方案，检查材料中的设计思想能否在计算中转化为收益。
- **工具驱动迭代**：将 VeriTMM 接入研究执行，获取光谱、约束及容差反馈，支持根据失败原因与性能变化继续调整结构和研究路线。
- **研究结果交付**：保存候选结构、评价结果、计算记录与研究过程，支持进一步复算和比较。
- **公开案例**：提供 12 组薄膜设计研究案例，覆盖量子通信、环境监测与热管理等应用方向。

[项目与研究案例](https://github.com/Lihonggang-scnu/OptoMind-Article)

### ChemIntent：面向功能化学的研究与业务决策 Agent

**项目构思 / 系统设计与开发** · `Domain Agent` `Bayesian Decision` `Multi-objective Optimization` `Operations Research`

将科研智能体能力迁移到纺织功能化学，围绕性能、工艺、成本和生产资源共同约束的客户需求构建应用原型。

- **需求与知识判断**：拆解性能目标、硬约束和未知条件，结合本地材料与认证学术检索，组织供应商资料和论文的条件感知比较。
- **主动研究决策**：实现适用性、竞争假设、贝叶斯预测、实验价值与行动选择的协同机制，支持澄清条件、建议实验、等待结果及依据观测更新判断。
- **数值与业务工具集成**：接入 BayBE / BoTorch 配方探索、StatsForecast 需求预测、Stockpyl 补货策略与 OR-Tools CP-SAT 排程，将研究候选与库存、设备、清洗和交期约束连接起来。
- **动态更新**：按依赖关系重算受影响判断；资源变化时保留已有实验认识，避免每轮重新组织全部研究状态。
- **验证结果**：已开展 Qwen 真实联网客户交互，并保存软件回归及合成研究闭环示例。归档回归快照为 870 项通过；合成排程覆盖 24 张订单、3 台设备，独立检查约束违规为 0。实体化学小试尚未开展。

[项目源码](https://github.com/Lihonggang-scnu/ChemIntent) · [运行与测试结果](https://github.com/Lihonggang-scnu/ChemIntent/tree/main/test-results/20261012)

## 科学计算与研究基础设施

### VeriTMM：面向智能体的多层膜物理计算工作台

**核心开发者** · `Differentiable Physics` `Optical Simulation` `Inverse Design` `Agent Tools`

将多层光学薄膜计算封装为智能体可以调用、检查和继续优化的科学工具。

- **计算与设计**：提供 S-matrix、特征矩阵与独立参考计算路径，覆盖平面各向同性一维多层膜；结合 PyTorch 可微厚度优化、灵敏度与容差分析，连接连续设计变量和光学目标。
- **物理适用性判断**：将适用范围、能量守恒和数值收敛等检查转化为可执行反馈，帮助调用方识别结果是否值得继续使用。
- **独立复算**：对候选结构进行独立计算与核对，使模型生成的结构能够进入实际物理评价。
- **Agent 集成**：提供 CLI、Python 接口与可选 MCP 工具面，包含能力发现、任务预检、结构化结果和失败诊断，支持从任务目标到仿真及后续改进的调用链。
- **验证规模**：2.0.0 发布记录包含 788 项回归通过、3 项跳过，以及 85 / 85 项离线 AgentBench 用例通过；基准中不支持物理任务的误接受为 0。

[项目源码与示例](https://github.com/Lihonggang-scnu/VeriTMM) · [AgentBench](https://github.com/Lihonggang-scnu/VeriTMM/blob/main/docs/AGENTBENCH.md)

### optomind-fulltext-acquisition：面向 Agent 的文献全文获取工具

**核心开发者** · `Information Retrieval` `Document Acquisition` `Browser Automation` `Research Infrastructure`

解决研究智能体从“找到论文”到“实际读到材料”的工程接缝。

- **来源解析**：围绕 DOI、论文元数据和来源身份组织获取流程，将检索记录连接到实际可读取的材料。
- **多路径获取**：结合 OpenAlex / Unpaywall 的开放获取线索，组织 JATS、TEI、HTML 与 PDF 候选；在机构授权场景下，通过可见的 Edge-CDP 浏览器复用现有登录态。
- **内容判断与交付**：区分论文正文、摘要页和订阅提示页，向上层交付实际取得的内容与材料位置，减少把“找到链接”误当作“已经读到全文”的接线问题。
- **可复用接口**：提供 CLI 与本地 JSON API，包含健康检查、登录入口与材料获取接口，作为独立模块服务于综述和研究 Agent。

[项目源码](https://github.com/Lihonggang-scnu/optomind-fulltext-acquisition)

## 模型方法与论文

### SpecFormer：全光谱 Encoder–Decoder 光学逆向设计

**第一作者** · **已发表：Intelligent Opto-Electronics，2026，2(3)，260016** · `PyTorch` `Transformer` `Generative Design` `Interpretability`

**SpecFormer: full-spectrum encoder–decoder inverse design of multilayer optical thin films**

- **方法设计**：将目标光谱编码为 token memory、summary memory 与全局表示，通过交叉注意力解码可变长度的材料—厚度序列，再以可微传输矩阵精修连续厚度。
- **物理可解释性**：结合线性探测、概念方向编辑、注意力分析和激活补丁，研究网络内部物理条件表示的可读性、可编辑性及其对生成结果的作用。
- **代表结果**：在 3,000 个固定测试目标上，平均 Plain MAE 为 **0.0041**，同协议 OptoGPT 为 **0.0234**，误差相对降低约 **82.5%**；平均 SSIM 为 **0.9993**。
- **泛化与制造约束**：研究部分光谱输入、最小厚度、厚度扰动、界面粗糙度与光学常数不确定性；用于透光率可调辐射制冷窗、光合作用选择性降温膜及光伏带边热管理涂层的计算设计。

2026 年 9 月 30 日正式发表。[论文 / DOI](https://www.oejournal.org/ioe/article/doi/10.67704/ioe.2026.260016) · [代码](https://github.com/Lihonggang-scnu/SpecFormer)

### DG-DRL：有限仿真预算下的深度强化学习逆向设计

**第一作者** · **在审** · `Deep Reinforcement Learning` `Sample Efficiency` `Action Masking` `Photonic Design`

**Delayed-Gratification Deep Reinforcement Learning for Sample-Efficient Photonic Inverse Design**

- **决策机制**：按顺序确定设计变量，以动态动作掩码排除非法选择，仅在完整结构形成后调用物理仿真并返回奖励，减少中间状态的昂贵评价。
- **方法分析**：通过消融区分逐变量决策与延迟奖励的作用，研究二者结合为何能够改善仿真样本效率。
- **论文实验**：面向结构色薄膜、近场光束整形与自由形光栅，分别使用 FDTD、FDFD 和 RCWA 评价。
- **代表结果**：在对应任务与文献基线比较中，结构色使用 2,500 次仿真达到文献报告 30,000 次下的结果；光束整形为 5,000 次与 100,000 次；光栅在 40,000 次仿真下达到 84.5% 效率，对比文献为 200,000 次下的 84.1%。各比较按对应任务与实验设置理解。

公开仓库提供通用参考环境与轻量示例，包含终局评价、动作掩码和中间奖励行为的测试。[代码与方法说明](https://github.com/Lihonggang-scnu/DG-DRL)

## 教育背景

| 时间 | 学校 | 专业与学位 |
| --- | --- | --- |
| 2024.09—至今 | 华南师范大学 | 新一代电子信息技术，硕士研究生 |
| 2020.09—2024.06 | 华南农业大学 | 光电信息科学与工程，学士 |

硕士阶段主要研究深度学习与强化学习驱动的光学逆向设计，并开展自主科研 Agent 与科学工具的开发。

## 技术栈

- **Agent 与应用工程**：Python、结构化工具调用、检索与材料读取、任务编排、长上下文供材、阶段缓存与恢复、模型费用控制；DeepAgents、LangGraph、Chainlit。
- **模型与优化**：PyTorch、Transformer、Encoder–Decoder、深度强化学习、贝叶斯优化、多目标优化与可微计算。
- **科学计算**：MATLAB、TMM、多层膜光学、FDTD / FDFD / RCWA 相关逆向设计与物理分析。
- **验证与交付**：pytest、Git / GitHub、数值复算、消融实验、局部与全链运行检查、Markdown / HTML / LaTeX / PDF 结果组织。

---

我持续探索科学问题理解、模型方法与 Agent 系统之间的联系，希望构建能够推进真实研究任务的科学智能工具。欢迎就 Agent、AI4S、光学逆向设计与开源项目交流。
