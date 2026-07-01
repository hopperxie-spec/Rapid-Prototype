# ToB 服务管理信息化系统快速原型

本目录用于存放和预览 ToB 服务管理信息化系统相关的 HTML 快速原型、PRD 页面和交互 Demo。当前已包含《ToB 全链路效能中心》产品需求文档页面，并提供统一入口页用于后续扩展更多原型。

## 项目内容

| 文件 | 说明 |
| --- | --- |
| `index.html` | 快速原型预览入口页，支持原型卡片展示和关键词搜索。 |
| `ToB_全链路效能中心_PRD.html` | 《ToB 全链路效能中心》PRD 页面，包含目录导航、需求概述、功能需求、数据规则、权限设计、接口集成、验收标准和上线计划等内容。 |

## 当前原型

### ToB 全链路效能中心 PRD

围绕客户、拜访、线索、商机、合同、项目、交付、验收、收入、售后等核心对象，建设统一的业务链路还原、效能分析、流程偏差检测、风险预警和治理闭环能力。

主要内容包括：

- 需求背景、建设目标与范围边界
- 用户角色、使用场景与业务流程
- 全链路效能总览、链路分析、实例追踪、流程偏差检测、预警中心、规则配置和 AI 诊断报告
- 核心数据模型、字段规则、指标口径和状态流转
- 权限矩阵、接口集成、消息通知、操作日志与审计
- 验收标准、风险依赖、上线计划和回退方案

## 本地预览

本项目为纯静态 HTML，无需安装依赖。

方式一：直接打开入口页

```bash
open index.html
```

方式二：使用本地静态服务预览

```bash
python3 -m http.server 8000
```

启动后访问：

```text
http://localhost:8000/
```

## 发布到 GitHub Pages

1. 将本目录文件提交到 GitHub 仓库。
2. 在仓库设置中打开 `Pages`。
3. 选择对应分支和目录作为发布来源。
4. 发布完成后访问 GitHub Pages 地址，即可进入 `index.html` 原型目录页。

## 新增原型页面

新增 HTML 原型时，建议按以下方式维护：

1. 将新的 `.html` 文件放在当前目录。
2. 打开 `index.html`。
3. 复制 `prototypeGrid` 中的卡片示例。
4. 修改卡片的 `href`、标题、说明、标签和 `data-keywords`。
5. 保存后刷新入口页确认能正常打开。

示例：

```html
<a class="card" href="./your-prototype.html" data-keywords="关键词 Web 原型">
  <div class="card-top">
    <div class="icon">WEB</div>
    <span class="tag">Web 原型</span>
  </div>
  <h2>原型名称</h2>
  <p>原型说明。</p>
  <div class="card-footer">
    <span>打开预览 →</span>
    <span class="path">./your-prototype.html</span>
  </div>
</a>
```

## 维护说明

- 页面使用内联 CSS 和少量原生 JavaScript，便于单文件分发、评审和归档。
- PRD 页面支持浏览器打印，可通过“打印 / 导出 PDF”导出评审材料。
- `index.html` 中的 `customer-research.html` 仅作为注释示例，当前目录未包含该文件。
- 若文件名包含中文，部署到部分静态服务器时需确认 URL 编码和链接跳转是否正常。

