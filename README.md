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

日常项目只使用上面的短启动包。测试提示词和回归夹具不属于 UI 的日常输入。

## 回归与稳定性

仓库使用 `evals/regression-matrix.yaml` 管理跨模式回归：

- 案例 A：指定结构 + 模板建站，验证严格参考转换。
- 案例 B：无指定结构 + 模板建站，验证自主研究和主题选择。
- 案例 C：指定结构 + 模板二开，验证无法原生实现时能否诚实阻断。
- 案例 D–F：资料不足 DTC、纯定制 DTC 和 B2B，待补充真实项目夹具。

Fiido/Concept 只作为案例 A，不得将其行业、区块数量、视觉风格或具体布局写进通用 Skill。一次修改只有在全部就绪案例重新运行后，才能说明回归套件通过；单个案例通过不能证明生产稳定。

## 设计原则

- 客户只提供事实和现有素材；AI 负责调研和页面策略。
- UI 负责创意方向、品牌判断和最终微调。
- 技术部负责平台、主题和实现边界。
- 模板项目必须先生成 Theme Capability Map，并将每个页面模块映射到主题中的准确 Section/Block。
- 纯模板项目默认不允许自定义 Section；模板二开项目的自定义模块默认不得超过模块数和预计页面高度的 20%。
- 客户预览不显示 `THEME NATIVE`、`SECTION CUSTOM`、素材替换说明等内部标注；这些信息保留在 Manifest 或交付说明中。
- Figma Starter File 可选；Figma 文件结构和生成契约必须遵守。
- 最终产物必须是原生、可编辑的 Figma 节点和组件结构，不是整页截图。
