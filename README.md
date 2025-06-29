# 西电计科院计网项目作业

## 作业要求

编程实现停止等待ARQ(10分)、返回N帧ARQ (40分)和选择性重复ARQ算法(50分)，要求在手工删除数据帧或确认帧(即模拟丢帧)时算法能正确处理丢帧的情况。

## ARQ协议可视化仿真系统使用说明

#### 1. 系统概述

ARQ 协议可视化仿真系统用于交互式演示停止等待 ARQ、返回 N 帧 ARQ 和选择重传 ARQ 三种协议的运行机制，支持丢帧模拟和参数调整。通过该系统，用户可以直观地观察不同 ARQ 协议在不同条件下的工作过程。

#### 2. 界面布局与功能模块

系统界面主要分为以下几个部分：

- **控制面板**：用于选择协议、设置窗口大小和传输参数、进行帧操作和仿真控制。
- **协议可视化区域**：展示协议的运行过程，包括帧的传输和确认，以及滑动窗口状态和传输进度。
- **统计信息面板**：显示发送帧数、接收帧数、重传帧数和吞吐量等统计信息。
- **操作说明**：提供系统的基本操作和测试场景说明。

#### 3. 具体操作步骤

##### 3.1 选择协议

在控制面板的 “选择协议” 部分，有三个按钮分别对应三种 ARQ 协议：

- **停止等待 ARQ**：点击 “停止等待 ARQ” 按钮，系统将切换到停止等待 ARQ 协议模式，并更新协议说明。
- **返回 N 帧 ARQ**：点击 “返回 N 帧 ARQ” 按钮，系统将切换到返回 N 帧 ARQ 协议模式，并更新协议说明。
- **选择重传 ARQ**：点击 “选择重传 ARQ” 按钮，系统将切换到选择重传 ARQ 协议模式，并更新协议说明。

##### 3.2 设置参数

- **窗口设置**：通过拖动 “发送窗口大小” 滑块，可以调整发送窗口的大小，范围为 1 到 8。滑块旁边会实时显示当前的窗口大小值。
- **传输参数：**
  - **帧传输延迟**：通过拖动 “帧传输延迟 (ms)” 滑块，可以设置帧从发送方到接收方的传输延迟，范围为 500 到 3000ms，步长为 100ms。滑块旁边会实时显示当前的延迟值。
  - **超时时间**：通过拖动 “超时时间 (ms)” 滑块，可以设置帧超时未确认的时间，范围为 1000 到 5000ms，步长为 100ms。滑块旁边会实时显示当前的超时时间值。

##### 3.3 帧操作

- **丢弃数据帧**：在仿真运行过程中，点击 “丢弃数据帧” 按钮，系统将随机选择一个未丢失的数据帧进行丢弃，并更新当前状态和窗口状态。
- **丢弃确认帧**：在仿真运行过程中，点击 “丢弃确认帧” 按钮，系统将随机选择一个未丢失的确认帧进行丢弃，并更新当前状态和窗口状态。

##### 3.4 仿真控制

- **开始**：点击 “开始” 按钮，系统将启动仿真，开始发送帧并显示仿真运行状态。
- **暂停**：点击 “暂停” 按钮，系统将暂停仿真，显示仿真已暂停状态。
- **单步**：在仿真暂停状态下，点击 “单步” 按钮，系统将执行一步仿真操作，发送下一帧。
- **重置**：点击 “重置” 按钮，系统将重置仿真状态，清除所有帧和确认帧，恢复到初始状态。

##### 3.5 快速演示

点击 “快速演示 (返回 N 帧 ARQ + 丢帧)” 按钮，系统将自动选择返回 N 帧 ARQ 协议，设置窗口大小为 4，重置仿真并开始运行。在运行过程中，会模拟在第 3 帧丢失的情况。

#### 4. 观察结果

- **协议可视化区域**：可以观察到帧从发送方到接收方的传输过程，以及确认帧从接收方返回发送方的过程。同时，还可以看到滑动窗口状态和传输进度的变化。
- **统计信息面板**：实时显示发送帧数、接收帧数、重传帧数和吞吐量等统计信息，帮助用户了解协议的性能。

