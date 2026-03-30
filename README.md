# 企业微信 CLI 开源项目发布

> 支持通过 CLI 使用企业微信核心接口能力，兼容主流 AI Agent 调用。

---

## 1. 企业微信支持 CLI 开源

企业微信 CLI 开源项目上架 GitHub 社区，开放企业微信**消息、日程、文档、智能表格、会议、待办、通讯录**等核心产品能力，支持主流 AI Agent 调用。

📦 **下载地址：** [GitHub - WeComTeam/wecom-cli](https://github.com/WeComTeam/wecom-cli)

---

## 2. CLI 可使用的能力

| 应用 | 可执行的命令 |
|------|-------------|
| 💬 消息 | 获取单聊、群聊消息，并可向指定用户和群聊发送消息 |
| 📄 文档 | 新建、写入、读取文档 |
| 📊 智能表格 | 新建、写入、读取智能表格 |
| 📅 日程 | 新建、查询、更新日程，查看其他人的闲忙状态，添加日程的参与人员 |
| 💻 会议 | 预定、查询、取消会议，添加参会人 |
| ✅ 待办 | 创建待办任务，查询你指定时间内的待办列表、添加待办参与人、更改待办状态 |
| 👥 通讯录 | 获取用户通讯录内的成员 userid、姓名、备注信息 |

---

## 3. 如何安装使用 CLI

### 3.1 环境要求

- **Node.js**（npm / npx）
- **企业微信机器人的 Bot ID 和 Secret**，获取步骤如下：

  1. 登录企微，进入工作台，找到「智能机器人」，并点击「手动创建」；
  2. 选择 **API 模式**创建；
  3. 连接方式选择「**使用长连接**」，即可获取并保存 Bot ID 及 Secret；
  4. 配置可见成员，并完成权限授权，保存即可完成机器人创建。

### 3.2 安装

```bash
# 安装 CLI
npm install -g @wecom/cli

# 安装 CLI SKILL（必需）
npx skills add WeComTeam/wecom-cli -y -g
```

### 3.3 快速开始

```bash
# 1. 配置机器人凭证（仅需一次）
wecom-cli init --botId "YOUR_BOT_ID" --secret "YOUR_BOT_SECRET"

# 2. 查看支持的品类和能力
wecom-cli --help

# 3. 列出某个品类下的所有工具
wecom-cli list contact

# 4. 调用工具
wecom-cli call contact get_userlist '{}'
```

### 3.4 包含的 Skills

| Skill | 所属应用 | 说明 |
|-------|----------|------|
| `wecom-preflight` | — | 前置条件检查，确保工具权限配置正确（所有其他 skill 自动依赖） |
| `wecom-contact-lookup` | 通讯录 | 通讯录成员查询，按姓名/别名搜索 |
| `wecom-get-todo-list` | 待办 | 待办列表查询，按时间过滤和分页 |
| `wecom-get-todo-detail` | 待办 | 待办详情批量查询 |
| `wecom-edit-todo` | 待办 | 待办创建、更新、删除、状态变更 |
| `wecom-meeting-create` | 会议 | 创建预约会议 |
| `wecom-meeting-manage` | 会议 | 取消会议、更新受邀成员 |
| `wecom-meeting-query` | 会议 | 查询会议列表和详情 |
| `wecom-msg` | 消息 | 会话列表、消息记录、媒体下载、文本发送 |
| `wecom-schedule` | 日程 | 日程 CRUD、参与人管理、闲忙查询 |
| `wecom-doc-manager` | 文档 | 文档创建 / 读取 / 编辑 |
| `wecom-smartsheet-schema` | 文档 | 智能表格子表与字段管理 |
| `wecom-smartsheet-data` | 文档 | 智能表格记录增删改查 |
| `wecom-send-media` | — | 通过 MEDIA 指令向用户发送本地文件（仅限 wecom 通道） |
| `wecom-send-template-card` | — | 发送结构化模板卡片消息（仅限 wecom 通道） |

> 更多请参考 [GitHub 使用文档](https://github.com/WeComTeam/wecom-cli)

---

## 4. 声明

- **使用要求：** CLI 的使用需要用户绑定长连接方式机器人的 BOT ID 和 Secret 授权。授权后机器人将以用户身份使用对应能力。同时为避免越权，授权了 CLI 能力的机器人将限制仅创建者可对话，其他成员不可使用。**企业微信 CLI 目前优先对 ≤10 人企业开放使用。**

- **⚠️ 风险提示：** 由 AI Agent 调用 CLI 操作企业微信内部应用，可能受模型幻觉等影响，存在数据泄露、越权等风险。建议在测试企业中先行验证后请谨慎使用，安装使用 CLI 后默认用户接受潜在风险。

---

## 5. 相关链接

- 📖 [详细使用文档](https://doc.weixin.qq.com/doc/w3_AFYA1wY6ACoCNRxfnyGRJQaSa6jjJ?scode=AJEAIQdfAAoLJ5pm3iAFYA1wY6ACo)
- 🛠️ [企业微信帮助中心](https://open.work.weixin.qq.com/help2/pc/21676)
- 💻 [GitHub 仓库](https://github.com/WeComTeam/wecom-cli)

---

*本文档整理自企业微信官方发布公告。*
