# 敏捷产品经理工作流 (Agile PM Workflow)

这是一个专为产品经理（尤其是新手或希望系统化产出的人）打造的 **AI 辅助需求产出工作流**。

我们打破了传统的“先想清楚再写长篇文档”模式，采用 **“启发式对话引导 -> 详细的初版 PRD -> 原型视觉化验证 -> 逻辑与细节补全”** 的敏捷迭代方式。借助 AI 强大的理解和生成能力，它能帮助你快速理清思路，并最终产出极具专业度的高保真原型和结构化 PRD。

---

## ✨ 核心亮点

- 💬 **告别填表，对话式采集**：采用灵活的对话式需求采集，AI 主动评估维度并温和追问，极大地降低了认知门槛。
- 🎨 **原型先行验证**：在编写复杂的业务逻辑前，先让 AI 产出高保真 HTML 原型。通过“看图说话”，直观发现逻辑漏洞。
- 🔗 **PRD 与原型双向联动**：文档与原型不再割裂。在工作流中，PRD 逻辑和原型视觉同步进行迭代优化，保证所想即所见。
- 🧩 **沙盒切片，所见即所得的 PRD**：最终产出的 PRD 中，直接以 `iframe` 沙盒切片的形式嵌入可交互的原型。左边是规则描述，右边/旁边是真实界面。
- 📂 **自动化项目初始化**：内置“步骤零”，一键生成标准的产品项目文件夹结构（PRD、原型、流程图、附件等），告别文件存放混乱。
- 📈 **结构化版本迭代管理**：规范化历史版本控制。通过物理隔离（如从 `v1.0` 复制出 `v1.1` 进行迭代）与 PRD 右上角的“版本切换器”，轻松管理项目的生命周期。

---

## 📁 仓库目录结构

本仓库包含两个核心部分：

- `pm_workflow_template/`：包含工作流的核心指令定义（`pm_workflow_definition.md`）、标准 PRD 模板（`prd_template.md`）和详细的使用指南。
- `agile-pm-workflow_skill/`：已经封装好的 Trae/Cursor 专属 AI 技能（Skill），支持一键安装调用。

---

## 🚀 工作流如何使用？

如果你**不使用**带 Skill 系统的 IDE，也可以直接在任何 AI 助手（如 ChatGPT, Claude 等）中手动使用这套工作流：

1. 打开 `pm_workflow_template/pm_workflow_definition.md`，将里面的全部内容发送给你的 AI 助手。
2. 附上你最原始、甚至有些模糊的想法（例如：“我想做一个给装修工人用的打卡小程序，能拍照就行”）。
3. 跟随 AI 的引导，像聊天一样依次完成：**需求采集与确认 -> 建立目录架构 -> 产出详细的第一版 PRD -> HTML 原型生成 -> 流程图绘制 -> 最终版内嵌原型 PRD**。

*(详细的模板说明与使用指南，请查看 `pm_workflow_template/README.md`)*

---

## 🛠️ AI IDE Skill 插件如何安装与使用？

如果你使用的是支持 Skill 扩展的现代 AI IDE（例如 **Trae, Cursor, Claude Code, Codex CLI 等**），我们已经为你封装好了专属的 Skill 插件。安装后只需输入 `/agile-pm-workflow` 即可一键开启！

### 安装步骤：

1. 下载或 `git clone` 本仓库到你的本地电脑。
2. 找到本仓库中的 `agile-pm-workflow_skill` 文件夹。
3. 将该文件夹复制并重命名，放到你所使用的 AI 助手的全局技能目录中：
   - **Trae / Cursor / 绝大多数 AI IDE**: 
     - Windows: `C:\Users\你的用户名\.trae\skills\agile-pm-workflow` (或 `.cursor\skills\`)
     - Mac/Linux: `~/.trae/skills/agile-pm-workflow` (或 `~/.cursor/skills/`)
   - **Claude Code**: 放在 `~/.claude/skills/`
   - **Gemini CLI**: 放在 `~/.gemini/skills/`
   *(注意：如果没有 `skills` 文件夹，请手动新建一个)*
4. 重新启动你的 AI IDE。

### 使用方法：

在 AI 的对话框中直接输入 `/agile-pm-workflow` 并发送，然后告诉它你的新项目想法。AI 就会自动帮你建好标准的文件夹结构，并开始一步步引导你产出专业的需求文档了！

---

> 💡 **进阶推荐**：为了让生成的 HTML 原型达到专业级的设计效果，强烈建议搭配 [Impeccable Skills](https://impeccable.style/)（前端设计专家指令集）一起使用！