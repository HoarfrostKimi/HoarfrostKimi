<p align="center">
  <img src="assets/banner.svg" alt="HoarfrostKimi · 黎枝" width="100%" />
</p>

<p align="center">
  <a href="https://github.com/generalio/OpenEyes"><img alt="openeyes" src="https://img.shields.io/badge/OPEN--EYES-0A0D14?style=flat-square&logo=android&logoColor=3DDC84"></a>
  <a href="https://github.com/HoarfrostKimi?tab=repositories"><img alt="repositories" src="https://img.shields.io/badge/REPOSITORIES-0A0D14?style=flat-square&logo=github&logoColor=white"></a>
  <a href="https://github.com/HoarfrostKimi/Video-Merger/releases"><img alt="video-merger" src="https://img.shields.io/github/v/release/HoarfrostKimi/Video-Merger?style=flat-square&label=VIDEO-MERGER&color=0A0D14&logo=electron&logoColor=9FEAF9"></a>
  <a href="https://github.com/HoarfrostKimi/PredictCoin/releases"><img alt="predictcoin" src="https://img.shields.io/github/v/release/HoarfrostKimi/PredictCoin?style=flat-square&label=PREDICT-COIN&color=0A0D14&logo=android&logoColor=3DDC84"></a>
</p>

---

### 简介

Android 开发，技术栈以 **Kotlin / Jetpack** 为主，负责过多模块应用的发现与排行模块，覆盖列表分页、页面转场与媒体播放。
桌面端使用 **TypeScript + Electron**，媒体处理基于 **FFmpeg**。

项目多源于具体需求：录播文件整理、投稿流程自动化、虚拟币仓位计算。

---

### 主要项目 · 开眼 OpenEyes

> 两人团队协作完成的短视频 Android 客户端，2025 年 7 月。
> 采用多模块架构：`app` / `lib_base` / `lib_net` / `module_home` / `module_discover` / `module_rankings`，接口层与 UI 层分离，各模块可独立编译。
> 负责 **发现** 与 **排行** 两个模块，包含 UI 设计、分页加载与播放器实现。

<p align="center">
  <img src="assets/shots/theme.gif" width="29%" alt="发现 · 推荐主题" />
  &nbsp;&nbsp;&nbsp;
  <img src="assets/shots/rankings.gif" width="29%" alt="排行 · 自动播放" />
</p>

<p align="center"><sub>发现 · 主题列表共享元素转场　　·　　排行 · 首项切换为视频卡并自动播放</sub></p>

- **发现** ｜ 分类网格与主题推荐。分类页以 RecyclerView 嵌套 RecyclerView 替代 ScrollView，保证列表滚动与底部导航联动；分类详情采用 CoordinatorLayout，折叠后分类名收进 Toolbar；主题列表使用共享元素转场，并预留 50ms 延迟，避免首帧未加载造成的动画畸变
- **排行** ｜ ViewPager2 双页切换，重写 ConstraintLayout 处理与外层滚动的滑动冲突；进入排行页时首个列表项切换为视频卡并由 ExoPlayer 播放，滑出屏幕后降级并释放播放器
- **数据层** ｜ Paging 3 + Flow 实现无限加载，`LoadStateAdapter` 统一加载、重试与到底状态；网络层以 Retrofit + Flow + StateFlow 为主，部分历史页面沿用 RxJava + LiveData
- **问题定位** ｜ 处理过列表复用导致的播放器错位、共享元素转场首帧畸变、ViewPager2 与内层 RecyclerView 滑动争抢

`Kotlin` `Jetpack` `MVVM` `Paging 3` `Coroutines` `Flow` `Retrofit` `RxJava` `ExoPlayer` `ViewPager2`

仓库：[generalio/OpenEyes](https://github.com/generalio/OpenEyes)

---

### 其他项目

| 项目 | 功能 | 技术栈 |
| :-- | :-- | :-- |
| **[Video-Merger](https://github.com/HoarfrostKimi/Video-Merger)** | 录播 FLV 分段按场次自动分组，以 FFmpeg stream copy 无损合并为 MP4；支持定时合并、B 站投稿流程自动化与局域网控制面板 | `Electron` `React` `TypeScript` `FFmpeg` |
| **[PredictCoin](https://github.com/HoarfrostKimi/PredictCoin)** | 虚拟币仓位计算工具。双边奖池场景下赔率等于池占比，对期望对数增长率求导得 `f* = (q − p) / (1 − p)`；经六层收缩后输出建议区间，无正期望时返回不下注 | `Kotlin` `Android` `Canvas` |
| **[TODO](https://github.com/HoarfrostKimi/TODO)** | 待办与番茄钟。Room 实现多用户数据隔离，支持拖动排序、侧滑删除与自定义时长 | `Kotlin` `MVVM` `Room` `RxJava` |
| **[RedRockHomeWork](https://github.com/HoarfrostKimi/RedRockHomeWork)** | 安卓登录系统（课程作业） | `Java` `Android` |
| **[GreetingCard](https://github.com/HoarfrostKimi/GreetingCard)** · **[Zhihu](https://github.com/HoarfrostKimi/Zhihu)** | 贺卡与知乎客户端练习项目 | `Kotlin` |

### 发布

| 应用 | 平台 | 安装包 |
| :-- | :-- | :-- |
| **Video-Merger** `v1.0.0` | Windows 10 / 11 | [video-merger-1.0.0-setup.exe](https://github.com/HoarfrostKimi/Video-Merger/releases/download/v1.0.0/video-merger-1.0.0-setup.exe) · 199 MB，内置 Chromium + FFmpeg |
| **PredictCoin** `v1.0` | Android 7.0+ | [PredictCoin-1.0.apk](https://github.com/HoarfrostKimi/PredictCoin/releases/download/v1.0/PredictCoin-1.0.apk) · 7.8 MB |

---

### 技术栈

**语言**

![Kotlin](https://img.shields.io/badge/Kotlin-0A0D14?style=flat-square&logo=kotlin&logoColor=7F52FF)
![Java](https://img.shields.io/badge/Java-0A0D14?style=flat-square&logo=openjdk&logoColor=ED8B00)
![TypeScript](https://img.shields.io/badge/TypeScript-0A0D14?style=flat-square&logo=typescript&logoColor=3178C6)
![Python](https://img.shields.io/badge/Python-0A0D14?style=flat-square&logo=python&logoColor=3776AB)

**客户端**

![Android](https://img.shields.io/badge/Android-0A0D14?style=flat-square&logo=android&logoColor=3DDC84)
![Jetpack](https://img.shields.io/badge/Jetpack-0A0D14?style=flat-square&logo=android&logoColor=3DDC84)
![Paging 3](https://img.shields.io/badge/Paging%203-0A0D14?style=flat-square&logo=android&logoColor=3DDC84)
![Coroutines](https://img.shields.io/badge/Coroutines%20%2F%20Flow-0A0D14?style=flat-square&logo=kotlin&logoColor=7F52FF)
![Room](https://img.shields.io/badge/Room-0A0D14?style=flat-square&logo=sqlite&logoColor=003B57)
![ExoPlayer](https://img.shields.io/badge/ExoPlayer-0A0D14?style=flat-square&logo=android&logoColor=3DDC84)
![RxJava](https://img.shields.io/badge/RxJava-0A0D14?style=flat-square&logo=reactivex&logoColor=B7178C)

**桌面与工具**

![Electron](https://img.shields.io/badge/Electron-0A0D14?style=flat-square&logo=electron&logoColor=9FEAF9)
![React](https://img.shields.io/badge/React-0A0D14?style=flat-square&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-0A0D14?style=flat-square&logo=vite&logoColor=646CFF)
![Node.js](https://img.shields.io/badge/Node.js-0A0D14?style=flat-square&logo=nodedotjs&logoColor=5FA04E)
![FFmpeg](https://img.shields.io/badge/FFmpeg-0A0D14?style=flat-square&logo=ffmpeg&logoColor=007808)
![Git](https://img.shields.io/badge/Git-0A0D14?style=flat-square&logo=git&logoColor=F05032)

---

### 开发规范

- 提交前执行单元测试与类型检查，不以 `--no-verify` 跳过钩子
- 单次提交只包含相关改动，无关变更单独提交，便于回退
- 优先使用标准库与平台能力，新增依赖需有明确必要性
- 数据优先在本地计算与存储，非必要不联网、不申请权限
- 界面自绘：预测币的卡片、滑块与收益曲线均由 View + Canvas 实现，不套用 Material 默认样式

---

### 近期

- 补充 PredictCoin 引擎单元测试：边界盘口、连败降档、约束取最小
- 同步 Video-Merger 投稿流程至 B 站新版要求：双比例封面、创作声明必填、后台标签页节流
- 补强 Android 基础：View 测量与绘制、启动性能、Jetpack 组件实现原理

<sub>本页面由本人维护 · 更新于 2026.11</sub>
