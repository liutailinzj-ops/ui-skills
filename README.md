# IWISH AI UI Skills

IWISH 内部网站 UI 生产 Skills。UI 只需调用 `$iwish-ui-workflow`，其余 Skills 负责行业调研、Figma 基础、组件解析、页面生成和 QA。

## 适用范围

- Shopify / WordPress
- 模板建站 / 模板二次开发 / 纯定制
- DTC / B2B
- 从空白 Figma 文件开始，或继续已有项目文件
- 客户素材完整、部分缺失或全部使用占位内容

## 前提

- Codex 已安装并连接 Figma 能力。
- 使用者对目标 Figma 文件具有编辑权限，或允许创建新文件。
- 行业调研需要联网能力。
- 私有仓库安装需要 GitHub 访问权限。

## 安装

在已获得私有仓库权限的 Codex 中使用：

```text
请从 https://github.com/liutailinzj-ops/ui-skills.git 安装以下 Skills：
```

并提供以下路径：

```text
skills/iwish-ui-workflow
skills/iwish-page-strategy
skills/iwish-figma-foundation
skills/iwish-component-resolver
skills/iwish-figma-page-builder
skills/iwish-figma-qa
```

也可以使用 Codex 自带的 `skill-installer` 从 GitHub 仓库一次安装多个路径。安装完成后，在下一轮任务中使用。

## UI 启动示例

```text
使用 $iwish-ui-workflow 生成本项目的可编辑 Figma 网站设计。

客户资料：<文件或链接>
客户素材：<目录或链接>
内部项目范围：<文件或说明>
主题或现有网站：<链接或“无”>
目标 Figma：<设计文件链接或“新建”>
本次页面：首页
素材模式：允许缺失内容使用占位
```

## 设计原则

- 客户只提供事实和现有素材；AI 负责调研和页面策略。
- UI 负责创意方向、品牌判断和最终微调。
- 技术部负责平台、主题和实现边界。
- Figma Starter File 可选；Figma 文件结构和生成契约必须遵守。
- 最终产物必须是原生、可编辑的 Figma 节点和组件结构，不是整页截图。
