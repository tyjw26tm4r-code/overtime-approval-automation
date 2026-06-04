# 加班申请审批自动化系统

## 📋 项目概述

这是一个基于 **Microsoft 365** 的完整加班申请审批自动化解决方案，适合部门级使用（10人以下团队）。

**核心功能：**
- ✅ 员工在线填写加班申请表
- ✅ 三层自动审批流程（直属主管 → 部门经理 → HR）
- ✅ 邮件自动通知
- ✅ 审批历史记录和追踪
- ✅ 无需编程，完全通过配置实现

---

## 🏗️ 系统架构

```
┌─────────────────────────────────────────────────────────────┐
│                     Microsoft 365 云端环境                   │
├─────────────────────────────────────────────────────────────┤
│                                                               │
│  ┌──────────────┐      ┌──────────────┐    ┌─────────────┐  │
│  │  Power Apps  │      │ SharePoint   │    │   Excel     │  │
│  │  Canvas App  │◄────►│   Online     │◄──►│   Online    │  │
│  │ (申请表单)   │      │ (审批流程)   │    │(员工信息)   │  │
│  └──────────────┘      └──────────────┘    └─────────────┘  │
│         │                     ▲                                │
│         │                     │                                │
│         └─────────────────────┼────────────────────┐          │
│                               │                    │          │
│                         ┌─────┴─────┐      ┌──────▼───────┐  │
│                         │   Power    │      │  Exchange    │  │
│                         │ Automate   │◄────►│  Online      │  │
│                         │ (审批流)   │      │ (邮件通知)   │  │
│                         └────────────┘      └──────────────┘  │
│                                                               │
└─────────────────────────────────────────────────────────────┘
```

**完全云端部署，无需本地服务器！**

---

## 📚 文档目录

### 快速开始
- [快速开始指南](docs/00_快速开始.md) - 5分钟理解系统

### 详细部署步骤
1. [环境准备](docs/01_环境准备.md) - 检查前置条件
2. [SharePoint 设置](docs/02_SharePoint设置.md) - 创建审批流程数据库
3. [Excel 准备](docs/03_Excel准备.md) - 准备员工信息
4. [Power Apps 创建](docs/04_PowerApps创建) - 逐步构建应用
5. [Power Automate 配置](docs/05_PowerAutomate流程.md) - 配置审批流程
6. [邮件通知设置](docs/06_邮件模板.md) - 邮件模板配置
7. [部署清单](docs/07_部署清单.md) - 上线前检查
8. [常见问题](docs/08_常见问题.md) - FAQ 和故障排查
9. [用户手册](docs/09_用户手册.md) - 最终用户操作指南

### 配置文件
- [templates/](templates/) - 可复用的模板文件
  - `employee-info-template.xlsx` - 员工信息 Excel 模板
  - `sharepoint-list-setup.md` - SharePoint List 创建步骤
  - `power-automate-flow.json` - 审批流程配置
  - `power-apps-export.json` - Power Apps 导出文件

---

## ⏱️ 部署时间估算

| 阶段 | 内容 | 时间 |
|------|------|------|
| 第一阶段 | 环境准备 | 30分钟 |
| 第二阶段 | 数据源创建 | 1小时 |
| 第三阶段 | Power Apps 构建 | 1.5小时 |
| 第四阶段 | 审批流程配置 | 1.5小时 |
| 第五阶段 | 测试和优化 | 1小时 |
| 第六阶段 | 发布上线 | 30分钟 |
| **总计** | | **约6小时** |

---

## 🚀 快速开始（3步）

### 步骤 1：检查环境
```
□ Microsoft 365 账户
□ Power Apps 访问权限
□ SharePoint Online 站点
□ 管理员权限
```
详见：[环境准备](docs/01_环境准备.md)

### 步骤 2：准备数据
```
□ 创建 SharePoint List（审批流程）
□ 准备 Excel Online（员工信息）
□ 配置权限
```
详见：[SharePoint 设置](docs/02_SharePoint设置.md) 和 [Excel 准备](docs/03_Excel准备.md)

### 步骤 3：构建应用和流程
```
□ 创建 Power Apps 应用
□ 配置 Power Automate 审批流程
□ 测试和发布
```
详见：[Power Apps 创建](docs/04_PowerApps创建.md) 和 [Power Automate 配置](docs/05_PowerAutomate流程.md)

---

## 📖 推荐学习路径

**针对初级用户（很少接触 Power Apps/Power Automate）：**

1. **第一天**
   - 阅读：[快速开始指南](docs/00_快速开始.md)
   - 视频：Microsoft 365 基础介绍（见下方视频链接）
   - 任务：完成环境检查

2. **第二天**
   - 阅读：[环境准备](docs/01_环境准备.md)
   - 视频：SharePoint Online 入门
   - 任务：创建 SharePoint List 和 Excel

3. **第三天**
   - 视频：Power Apps 基础入门
   - 任务：按指南创建 Power Apps 应用

4. **第四天**
   - 视频：Power Automate 基础入门
   - 任务：配置审批流程

5. **第五天**
   - 任务：完整测试和优化
   - 发布上线

---

## 🎓 推荐视频教程

### Microsoft 官方教程（中文）
- [Microsoft 365 基础](https://learn.microsoft.com/zh-cn/training/paths/m365-fundamentals/)
- [Power Apps 画布应用入门](https://learn.microsoft.com/zh-cn/training/paths/create-powerapps/)
- [Power Automate 云流入门](https://learn.microsoft.com/zh-cn/training/paths/automate-process-using-flow/)
- [SharePoint Online 入门](https://learn.microsoft.com/zh-cn/training/paths/m365-teams-sharepoint-get-started/)

### YouTube 中文频道
- [微软 Azure 官方频道](https://www.youtube.com/c/MicrosoftAzure)
- [Power Platform 官方演示](https://www.youtube.com/c/MicrosoftPowerPlatform)

---

## 📞 需要帮助？

- 📖 查看 [常见问题](docs/08_常见问题.md) 
- 🔍 搜索故障排查指南
- 📧 联系项目维护者

---

## ✅ 系统需求

| 项目 | 要求 |
|------|------|
| **Microsoft 365** | 包含 Power Apps 和 Power Automate 的许可证 |
| **SharePoint Online** | 已启用 |
| **Exchange Online** | 用于邮件通知 |
| **网络** | 互联网连接 |
| **浏览器** | Edge、Chrome、Safari（最新版本） |

---

## 📝 项目结构

```
overtime-approval-automation/
├── README.md                          # 本文件
├── docs/
│   ├── 00_快速开始.md
│   ├── 01_环境准备.md
│   ├── 02_SharePoint设置.md
│   ├── 03_Excel准备.md
│   ├── 04_PowerApps创建.md
│   ├── 05_PowerAutomate流程.md
│   ├── 06_邮件模板.md
│   ├── 07_部署清单.md
│   ├── 08_常见问题.md
│   └── 09_用户手册.md
├── templates/
│   ├── employee-info-template.xlsx
│   ├── sharepoint-list-setup.md
│   ├── power-automate-flow.json
│   └── power-apps-export.json
└── images/
    ├── architecture.png
    ├── flow-diagram.png
    └── ui-screenshot.png
```

---

## 🎯 核心功能详解

### 1. 加班申请表单
- 员工自助填写加班信息
- 自动获取员工基本信息
- 表单验证和提交

### 2. 三层审批流程
- **第一层**：直属主管审批（1个工作日）
- **第二层**：部门经理审批（1个工作日）
- **第三层**：HR 最终审批（1个工作日）

### 3. 自动通知系统
- 申请提交时通知主管
- 审批完成时通知员工
- 每个阶段状态变化时通知相关人员

### 4. 数据追踪
- 完整的审批历史记录
- 每个审批人的意见
- 审批时间和状态

---

## 📊 预期效果

✅ **效率提升**
- 从手动审批→自动流程，节省 80% 审批时间
- 审批流程透明，员工可随时查看进度

✅ **数据准确**
- 减少手动输入错误
- 所有数据自动保存和备份

✅ **成本降低**
- 无需购买额外软件
- 利用现有 Microsoft 365 许可证

✅ **易于维护**
- 无需编程或 IT 支持
- 完全通过 UI 配置

---

## 🔒 安全性和合规

- ✅ Microsoft 365 企业级安全
- ✅ 数据加密传输和存储
- ✅ 完整的访问控制和权限管理
- ✅ 审批日志和审计记录
- ✅ GDPR 和合规性支持

---

## 📄 许可证

本项目为开源项目，欢迎在组织内部使用、修改和改进。

---

## 🙋 反馈和建议

如有问题或建议，欢迎提交 Issues 或 Pull Requests。

---

**准备好开始了吗？👉 [快速开始指南](docs/00_快速开始.md)**

