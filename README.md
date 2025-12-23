# Android Dictionary Pens Tools 🛠️

> [!NOTE]
> This README document is only available in Chinese (Simplified).
> 
> 此README文件僅提供中文（簡體）版本。

为Android词典笔爱好者打造的系统增强与应用集合，解锁设备的完整潜力！  
当然，也可以不止词典笔。

[![Platform](https://img.shields.io/badge/Android-1.6%2B-green.svg)]()
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/ZhouboLee/Dictionary_Pens_Tools/pulls)

## 📋 项目简介

本仓库收集了一系列经过测试的Android应用与工具，专门针对词典笔这类特殊设备进行优化。无论是想提升系统流畅度、增强功能，还是增加娱乐性，这里都能找到合适的解决方案。

> [!WARNING]
> 使用前请确保了解刷机/安装第三方应用的风险，并自行备份重要数据。作者不对任何设备损坏负责。

## 🚀 快速开始

### 前置要求
- 已开启USB调试的Android词典笔
- 电脑上安装[ADB工具](https://developer.android.google.cn/tools/releases/platform-tools?hl=zh-cn)
- 基础命令行操作知识

### 安装步骤
1. 在词典笔的设置中开启「开发者选项」和「USB调试」
2. 通过USB连接电脑
3. 下载所需APK文件到电脑
4. 执行安装命令：
```bash
adb install -r app_name.apk
```

## 📦 应用分类

### 🏠 系统与启动器
| 应用 | 最低Android版本 | 主要功能 | 适用设备 |
|------|----------------|----------|----------|
| **悬浮辅助** | 5.0+ | 补充手势导航、悬浮球功能 | 全系 |
| **Lawnchair** | 8.0+ | 轻量级现代启动器 | 高性能设备 |
| **Emerald Launcher** | 1.6+ | 极简启动器 | 低性能/旧系统 |
| **MI Control Center** | 7.0+ | 替换控制中心与通知栏 | 全系 |
| **Shizuku** | 6.0+ | 获取系统API权限 | 需要Root/ADB |

### 🎵 影音娱乐
| 应用 | 架构 | 特点 | 推荐场景 |
|------|------|------|----------|
| **Bilibili车机版** | 通用 | 界面简洁，资源占用低 | 视频学习/娱乐 |
| **网易云音乐手表版** | 通用 | 极致轻量，基础功能 | 低性能设备听歌 |
| **网易云音乐极速版** | 通用 | 平衡功能与性能 | 中等性能设备 |
| **Open Camera** | 通用 | 开源相机应用 | 带摄像头的设备 |
| **Google Gallery** | 通用 | 简洁快速的图片浏览 | 图片管理 |

### 🛠️ 工具与实用
| 应用 | 类别 | 亮点 | 备注 |
|------|------|------|------|
| **Files By Google** | 文件管理 | 简洁智能，自动清理 | 替代系统文件管理器 |
| **MT管理器** | 高级工具 | 双窗口、Root探索、APK编辑 | 极客必备 |
| **Via浏览器** | 浏览器 | 仅1MB，插件支持 | 日常浏览 |
| **Chrome** | 浏览器 | 完整功能，同步支持 | 需要现代Web体验 |
| **Termux** | 终端 | Linux环境，包管理器 | 开发/学习Linux |

### 🌐 网络与服务
| 应用 | 用途 | 依赖 | 注意 |
|------|------|------|------|
| **Clash Meta For Android** | 网络代理 | 配置文件 | 需合法使用 |
| **microG** | Google服务替代 | 无 | 不完全兼容所有应用 |
| **Aurora Store** | 应用商店 | 网络 | 匿名下载Google Play应用 |

### ⌨️ 输入与个性化
| 应用 | 功能 | 替代方案 |
|------|------|----------|
| **讯飞输入法** | 中文输入 | 系统输入法 |
| **Lawnicons** | 图标包 | 配合Lawnchair使用 |
| **几何天气** | 天气信息 | 开源美观 |

## 🔧 进阶配置

### Lawnchair + Lawnicons 美化组合
1. 先安装Lawnchair并设置为默认启动器
2. 安装Lawnicons图标包
3. 在Lawnchair设置中应用图标包
4. 调整桌面网格、图标大小等参数

### Shizuku 授权使用
```bash
# 通过ADB激活Shizuku
adb shell sh /sdcard/Android/data/moe.shizuku.privileged.api/files/start.sh
```

### Termux 基础设置
```bash
# 更新包管理器
pkg update && pkg upgrade
# 安装常用工具
pkg install python nodejs git vim
```

> [!WARNING]
> ## 兼容性说明
>
> | 应用 | 已知问题 | 解决方案 |
> |------|----------|----------|
> | MI Control Center | 有无法触发的情况 | 使用桌面快捷方式或悬浮辅助固定快捷方式 |
> | microG | 部分应用仍需要GSF | 配合FakeGApps使用或使用不需要Google专有库或支持microG这类FOSS的软件 |
> | Lawnchair | 快捷栏文件夹会导致崩溃，且在Lawnchair 15 Beta 2仍未修复 | 不使用快捷栏文件夹 |
> | 悬浮辅助 | 在某些裁切屏设备无法正常显示 | 在悬浮辅助设置关闭自动贴边并手动调整悬浮球XY位置 |

## 🤔 常见问题

**Q: 安装后应用无法打开或闪退？**  
A: 检查Android版本（[Android SDK API级别](https://developer.android.google.cn/tools/releases/platforms?hl=zh-cn)）和CPU架构（ABI）是否匹配，尝试安装旧版本。

**Q: 如何恢复原厂系统？**  
A: 大部分应用可正常卸载或通过恢复出厂设置，如果是系统级修改，那只能靠您自己了。

**Q: 词典笔没有USB调试选项？**  
A: 连续点击「关于设备」中的版本号7次开启开发者选项，如果开发者选项被禁用，，您可以到工厂测试软件寻找adb开关，如果没有则说明厂商没有开放adb权限。

**Q: 这些应用耗电吗？**  
A: 后台服务类应用（如悬浮辅助、microG）可能增加耗电，不需要时可关闭。

## 📁 文件结构
```
.
├── README.md
├── launchers/          # 启动器相关
│   ├── lawnchair/
│   ├── emerald/
│   └── lawnicons/
├── media/              # 影音应用
│   ├── bilibili/
│   ├── netease-music/
│   └── camera-gallery/
├── tools/              # 实用工具
│   ├── file-managers/
│   ├── browsers/
│   └── termux/
├── system/             # 系统增强
│   ├── microg/
│   ├── shizuku/
│   └── control-center/
└── input-personalization/ # 输入与个性化
    ├── input-method/
    ├── weather/
    └── icons/
```

## 🤝 贡献指南

欢迎提交Issue和Pull Request！

1. Fork本仓库
2. 创建功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启Pull Request

### 贡献者
<a href="https://github.com/Zhoubolee/dictionary_pens_tools/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ZhouboLee/Dictionary_Pens_Tools" />
</a>

## 📄 许可证

本项目采用MIT许可证 - 详见 [LICENSE](LICENSE) 文件。

## 🔗 相关资源

- [ADB官方文档](https://developer.android.com/studio/command-line/adb)
- [XDA Developers论坛](https://forum.xda-developers.com/)
- [F-Droid开源应用商店](https://f-droid.org/)
- [Android版本分布](https://developer.android.com/about/dashboards)

## 💬 反馈

如有问题或建议，可通过以下方式联系：
- GitHub Issues: [提交问题](https://github.com/ZhouboLee/Dictionary_Pens_Tools/issues)
- Email: zhoubolee@163.com

---

**如果你觉得这个项目有帮助，请给个⭐️ Star支持！**

*最后更新：2025年12月*

> 提示：定期检查应用更新，获取更好的兼容性和安全性。
