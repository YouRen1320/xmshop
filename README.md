# XMShop - 基于小米商城的Flutter项目

[![Flutter](https://img.shields.io/badge/Flutter-blue.svg)](https://flutter.dev/)
[![GitHub](https://img.shields.io/badge/GitHub-YouRen1320%2Fxmshop-181717.svg)](https://github.com/YouRen1320/xmshop)

一个基于小米商城UI设计的Flutter学习项目，参考了小米商城的界面风格，实现了商品浏览、购物车、用户登录等基础电商功能，适合Flutter初学者学习和参考。

## 🎯 项目特色

- 🎨 **UI还原**：参考小米商城的界面设计风格
- 📱 **跨平台**：基于Flutter框架支持多端运行
- 🏗️ **规范架构**：采用GetX状态管理，模块化开发
- 💻 **学习项目**：适合Flutter初学者学习电商App开发
- 🛠️ **基础功能**：实现了部分电商应用的基础功能

## ✨ 已实现功能

### 🏠 首页展示
- 商品轮播图展示
- 热门商品推荐
- 分类快捷入口

### 🔍 商品浏览
- 商品分类页面
- 商品列表展示
- 商品详情查看
- 商品搜索功能
- 价格排序筛选

### 🔐 用户认证
- 手机号登录
- 短信验证码登录
- 用户注册功能

### 👤 个人中心
- 用户信息展示
- 基础设置页面

> **注意**: 这是一个学习项目，部分功能为演示版本，不包含完整的后端服务和支付功能。

## 🛠️ 技术栈

- **前端框架**: Flutter（需自带满足下述约束的 Dart SDK）
- **编程语言**: Dart >= 3.3.0 且 < 4.0.0，与 `pubspec.yaml` 一致
- **状态管理**: GetX
- **网络请求**: Dio

## 📱 支持平台

- ✅ Android

## 🚀 快速开始

### 环境要求

- Flutter SDK（Dart >= 3.3.0 且 < 4.0.0）
- Android Studio
- Android SDK (Android开发)

### 安装步骤

1. **克隆项目**
   ```bash
   git clone https://github.com/YouRen1320/xmshop.git
   cd xmshop
   ```

2. **安装依赖**
   ```bash
   flutter pub get
   ```

3. **运行项目**
   ```bash
   # Android
   flutter run

   # 指定设备
   adb pair 192.168.0.x # 匹配设备
   adb connect 192.168.0.x # 链接设备
   adb devices # 查看当前链接设备
   flutter run # 启动项目
   ```

### 构建发布版本

```bash
# Android APK
flutter build apk --release
```

## 📁 项目结构

```
lib/
├── app/
│   ├── models/           # 数据模型
│   │   ├── address_model.dart
│   │   ├── category_model.dart
│   │   ├── focus_model.dart
│   │   └── ...
│   ├── modules/          # 功能模块
│   │   ├── address/      # 地址管理
│   │   ├── cart/         # 购物车
│   │   ├── category/     # 商品分类
│   │   ├── checkout/     # 结算
│   │   ├── home/         # 首页
│   │   ├── order/        # 订单
│   │   ├── pass/         # 登录注册
│   │   ├── pay/          # 支付
│   │   ├── productContent/ # 商品详情
│   │   ├── productList/  # 商品列表
│   │   ├── search/       # 搜索
│   │   ├── tabs/         # 底部导航
│   │   └── user/         # 用户中心
│   ├── routes/           # 路由配置
│   │   ├── app_pages.dart
│   │   └── app_routes.dart
│   ├── services/         # 服务层
│   │   ├── cartServices.dart
│   │   ├── httpsClient.dart
│   │   └── ...
│   └── widget/           # 公共组件
│       ├── logo.dart
│       ├── passButton.dart
│       └── ...
├── main.dart             # 应用入口
└── ...
assets/
├── fonts/               # 字体文件
├── images/              # 图片资源
└── ...
```

## 🎨 界面预览

### 📱 主要功能界面

<div align="center">

| 首页 | 分类 |
|:---:|:---:|
| ![首页](assets/readme/首页.jpg) | ![分类](assets/readme/分类.jpg) |

| 搜索 | 用户中心 |
|:---:|:---:|
| ![搜索](assets/readme/搜索.jpg) | ![用户](assets/readme/用户.jpg) |

</div>

### 📝 界面说明
- **首页**: 展示商品轮播图、推荐商品、分类入口
- **分类**: 商品分类浏览、基础筛选功能
- **搜索**: 商品搜索界面、搜索结果展示
- **用户中心**: 个人信息展示、基础功能页面

## 🔧 开发指南

### 代码规范

- 遵循Dart官方代码规范
- 使用GetX进行状态管理和路由管理
- 采用MVC架构模式
- 组件化开发，提高代码复用性

### 添加新功能

1. 在`lib/app/modules/`下创建新的功能模块
2. 按照GetX规范创建Controller、View和Binding
3. 在`app_pages.dart`中添加路由配置
4. 在`app_routes.dart`中定义路由常量

### API集成

API服务配置在`lib/app/services/httpsClient.dart`中，支持：
- 请求拦截器
- 响应拦截器
- 错误处理
- 统一的请求格式

## 📈 性能优化

- 使用GetX进行高效的状态管理
- 图片懒加载和缓存
- 列表虚拟化渲染
- 代码分割和懒加载

## 🤝 贡献指南

欢迎贡献代码！请遵循以下步骤：

1. Fork 项目
2. 创建功能分支 (`git checkout -b feature/AmazingFeature`)
3. 使用中文描述提交更改 (`git commit -m '完善商品展示说明'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 📄 许可证

原 README 声明采用 MIT 许可证，但仓库当前缺少独立 `LICENSE` 文件，许可文本与权利归属仍待补齐。小米品牌、界面参考素材与第三方资源不因本项目声明而自动获得授权。

## 📞 联系方式

- 作者账号：YouRen1320
- 项目地址：[YouRen1320/xmshop](https://github.com/YouRen1320/xmshop)
- 原项目参考：小米商城官方设计

## 🙏 致谢

- 感谢小米官方提供的优秀UI设计参考
- 感谢Flutter团队提供的跨平台框架
- 感谢GetX库作者提供的状态管理方案

---

⭐ 如果这个项目对你有帮助，请给它一个星标！
