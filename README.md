# proj317--efficient-user-level-threads-scheduling-and-mapping
# 高效用户态线程调度

### 项目描述

用户态线程是实现parallel loop和SIMD的一个典型途径，例如openmp，已成为系统的基础组件。他自动将数据分成多块，并分发给多个线程并行处理。

但现有openmp的实现，由于负载均衡、调度分发等问题，不能高效地支持嵌套并行、应用混布等场景。

通过该项目，可以帮助学生深入理解系统线程管理、任务调度、数据并行等核心知识，并掌握系统软件设计方法，了解前沿科研技术。

该项目通过阅读前沿论文，优化openmp中的调度策略、负载均衡、弹性扩展等设计实现，提升系统性能。

### 项目价值

- 项目解决现有技术痛点，可以输出A类顶会（ATC、ASPLOS、OSDI等）论文。即使完成部分功能也可以作为毕业设计。
- 项目面向系统核心功能，有机会合入开源社区，为成千上万的实际产品所应用。
- 导师可以长期辅导

### 相关资源

1. 论文：Maximizing systemutilizationviaparallelismmanagementforco-locatedparallelapplications（PACT'18)
2. 论文：Callisto: co-scheduling parallel runtime systems（EuroSys'14)
3. 论文：Parcae: a system forflexibleparallelexecution（PLDI'12)
4. 论文：FJOS: Practical, Predictable, and Efficient System Support for Fork/Join Parallelism (RTAS'14)

### 所属赛道

2024全国大学生操作系统比赛的“OS功能”挑战赛道

### 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校
- 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
- 请遵循“2024全国大学生操作系统比赛”的章程和技术方案要求

### 赛题分类
系统调试/支撑库的设计

### 项目导师

任玉鑫

- email renyuxin1@huawei.com

吴一凡

- email shinbokuow@163.com

### 难度

中等

### 特征

- 搭建开发环境，熟悉使用openmp。
- 梳理洞察前沿论文，理解现有方案的缺陷，识别优化点。
- 针对不同场景目标，实现高效调度策略。

### License

# 预期目标

### 注意：选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标

通过调研，优化openmp中的调度策略、负载均衡、弹性扩展等设计实现，提升系统性能。

### 第一题：基本的环境搭建和熟悉

- 熟悉现有工具的使用
- 理解parallel loop、simd等数据并行，以及调度相关的背景知识

### 第二题：高效调度策略

- 洞察前沿论文，分析其冷热识别的核心算法
- 支持混合应用，支持多种策略，实现不同场景的需求

### 第三题：内核与用户态协同调度

- 分析由于不感知用户态的调度策略，内核的调度如何影响应用性能
- 改进内核里的调度策略，与用户态的调度协同感知，提升性能
