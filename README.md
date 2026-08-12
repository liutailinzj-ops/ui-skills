# IWISH AI UI Skills

IWISH 内部网站 UI 生产 Skills。UI 只需调用 `$iwish-ui-workflow`，其余 Skills 负责行业调研、Figma 基础、组件解析、页面生成和 QA。

## 适用范围

- Shopify / WordPress
- 模板部分二次开发 / 纯定制
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
skills/iwish-visual-direction
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
项目场景：<自主策划 + 模板部分二开 / 指定竞品部分结构 + 模板部分二开 / 纯定制>
指定参考模块：<URL + 模块名称/截图说明；无则写“无”>
内部项目范围：<平台、页面、功能及开发边界>
主题或现有网站：<链接或“无”>
目标 Figma：<设计文件链接或“新建”>
本次页面：首页
素材模式：允许缺失内容使用占位
```

日常项目只使用上面的短启动包。测试提示词和回归夹具不属于 UI 的日常输入。

## 回归与稳定性

仓库使用 `evals/regression-matrix.yaml` 管理跨模式回归：

- 核心案例 B：只有 Logo/品牌色、无指定结构、模板部分二开，验证自主研究、主题选择和逐模块实现决策。
- 核心案例 C：只有 Logo/品牌色、指定竞品部分结构、模板部分二开，验证局部结构转换和二开边界。
- 核心案例 E：纯定制，验证原创页面策略、项目级视觉系统和无主题模块约束的组件生产。
- Logo-only 与 B2B 变体在获得可验证夹具后补充。

一次修改只有在全部就绪案例重新运行后，才能说明回归套件通过；单个案例通过不能证明生产稳定。客户项目、竞品、主题、行业、区块数量、视觉风格和具体布局不得写进通用 Skill。

## 设计原则

- 客户只提供事实和现有素材；AI 负责调研和页面策略。
- UI 负责创意方向、品牌判断和最终微调。
- 技术部负责平台、主题和实现边界。
- 模板部分二开项目必须先生成 Theme Capability Map，并将每个页面模块映射到准确的主题 Section/Block/Setting 或明确的自定义实现。
- 日常指定竞品部分结构的项目采用“局部结构转换”：只锁定明确选中的模块，保留其内容责任、布局关系和阅读链路，其余页面由产品、竞品和转化链路研究生成。
- AI 提出的主题近似方案叫“建议适配”，不等于客户或 UI 已批准。
- 不使用固定 20% 比例判断模板二开。每个模块分别标记为主题原生、主题配置、样式扩展、Custom CSS、Custom Liquid、新建 Section、App/第三方功能或待技术确认，并服从项目实际开发范围。
- 客户预览不显示 `THEME NATIVE`、`SECTION CUSTOM`、素材替换说明等内部标注；这些信息保留在 Manifest 或交付说明中。
- Figma Starter File 可选；Figma 文件结构和生成契约必须遵守。
- 最终产物必须是原生、可编辑的 Figma 节点和组件结构，不是整页截图。
