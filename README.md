<p align="center">
  <img src="assets/banner.svg" alt="HoarfrostKimi · 黎枝" width="100%" />
</p>

<p align="center">
  <a href="https://github.com/HoarfrostKimi?tab=repositories"><img alt="repositories" src="https://img.shields.io/badge/REPOSITORIES-0A0D14?style=flat-square&logo=github&logoColor=white"></a>
  <a href="https://github.com/HoarfrostKimi/Video-Merger/releases"><img alt="video-merger" src="https://img.shields.io/github/v/release/HoarfrostKimi/Video-Merger?style=flat-square&label=VIDEO-MERGER&color=0A0D14&logo=electron&logoColor=9FEAF9"></a>
  <a href="https://github.com/HoarfrostKimi/PredictCoin/releases"><img alt="predictcoin" src="https://img.shields.io/github/v/release/HoarfrostKimi/PredictCoin?style=flat-square&label=PREDICT-COIN&color=0A0D14&logo=android&logoColor=3DDC84"></a>
</p>

---

### 关于

写代码的动机通常很朴素：**有些事太重复了，重复到值得写个工具。**

录播下播后是一堆 FLV 分段，要按场次拼起来、还要投到 B 站 —— 于是有了 [Video-Merger](https://github.com/HoarfrostKimi/Video-Merger)。
B 站赛事预测每场都要算仓位，靠感觉容易上头 —— 于是有了 [PredictCoin](https://github.com/HoarfrostKimi/PredictCoin)，顺手把凯利公式在双边奖池下重新推了一遍。

主战场是 **Kotlin / Android**：MVVM、Room、自绘组件、不依赖 Android 的纯函数计算引擎。
桌面上的活交给 **TypeScript + Electron**，音视频交给 **FFmpeg**。

---

### 作品

| 项目 | 解决什么问题 | 技术栈 |
| :-- | :-- | :-- |
| **[Video-Merger](https://github.com/HoarfrostKimi/Video-Merger)** | 录播 FLV 分段自动识别场次、无损合并成 MP4；带定时合并、B 站自动投稿、局域网手机控制面板 | `Electron` `React` `TypeScript` `FFmpeg` |
| **[PredictCoin](https://github.com/HoarfrostKimi/PredictCoin)** | 预测币仓位计算器。双边奖池下赔率就是池比例，期望对数增长率求导得 `f* = (q − p) / (1 − p)`；六层收缩后给建议区间，没优势就直接不下注 | `Kotlin` `Android` `Canvas 自绘` |
| **[TODO](https://github.com/HoarfrostKimi/TODO)** | 待办 + 番茄钟。Room 多用户隔离、拖动排序、侧滑删除、自定义时长 | `Kotlin` `MVVM` `Room` `RxJava` |
| **[RedRockHomeWork](https://github.com/HoarfrostKimi/RedRockHomeWork)** | 安卓登录系统（早期练习） | `Java` `Android` |
| **[GreetingCard](https://github.com/HoarfrostKimi/GreetingCard)** · **[Zhihu](https://github.com/HoarfrostKimi/Zhihu)** | 贺卡、知乎客户端 —— 练手用 | `Kotlin` |

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
![Material Design](https://img.shields.io/badge/Material%20Design-0A0D14?style=flat-square&logo=materialdesign&logoColor=757575)
![RxJava](https://img.shields.io/badge/RxJava-0A0D14?style=flat-square&logo=reactivex&logoColor=B7178C)
![Room](https://img.shields.io/badge/Room-0A0D14?style=flat-square&logo=sqlite&logoColor=003B57)

**桌面与工具**

![Electron](https://img.shields.io/badge/Electron-0A0D14?style=flat-square&logo=electron&logoColor=9FEAF9)
![React](https://img.shields.io/badge/React-0A0D14?style=flat-square&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-0A0D14?style=flat-square&logo=vite&logoColor=646CFF)
![Node.js](https://img.shields.io/badge/Node.js-0A0D14?style=flat-square&logo=nodedotjs&logoColor=5FA04E)
![FFmpeg](https://img.shields.io/badge/FFmpeg-0A0D14?style=flat-square&logo=ffmpeg&logoColor=007808)
![Git](https://img.shields.io/badge/Git-0A0D14?style=flat-square&logo=git&logoColor=F05032)

---

### 工程习惯

- **提交前跑测试和类型检查**，卡住就修，不用 `--no-verify` 绕过去
- **一次提交只装一件事**，无关改动单独留着，方便回退
- **依赖能不加就不加**，能用标准库就不引框架
- **能本地算的不要联网**，能不申请权限就不申请
- **界面能自己画就自己画** —— 预测币的卡片、滑块、收益曲线都是 View + Canvas 手写的

---

### 在做

- 给 PredictCoin 补引擎单测：边界盘口、连败降档、约束取最小
- Video-Merger 的投稿链路跟着 B 站改版走：双比例封面、创作声明必填、后台标签页节流
- 系统补 Android 基础：View 的测量与绘制、启动性能、Jetpack 组件到底在做什么

<sub>主页自己维护 · 最近更新 2026.11</sub>
