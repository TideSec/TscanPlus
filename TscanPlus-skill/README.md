# TscanPlus Agent Skill（skillpack）

本目录为 **唯一权威** Skill 来源，与 IDE/产品无关，供 MCP Agent、GUI 导出 zip、Cursor 等使用。

| 文件 | 说明 |
|------|------|
| `SKILL.md` | Agent 行为说明（授权、八大模块、工具参数、MCP 接入、汇报格式） |
| `examples.md` | 各模块 MCP 对话与参数示例 |
| `mcp-config-example.json` | MCP `mcpServers` 配置示例 |


MCP 服务配置（`mcp stdio` / `mcp serve`）见 `SKILL.md` 正文。

---

## 获取 Skill 包

请用下列方式之一取得与 `TscanPlus-skill` 相同的文件（`SKILL.md`、`examples.md`、`README.md`、`mcp-config-example.json`）：

| 方式 | 说明 |
|------|------|
| **GUI 导出（推荐）** | TscanPlus → **AI 辅助** → **MCP 服务配置** → **导出 Skill 模板**，得到 `TscanPlus-skill.zip`，解压到任意目录 |
| **仓库源码** | 使用 `TscanPlus-skill/` 下文件，或克隆项目后从该目录复制 |

解压 zip 后目录示例：

```text
tscanplus-mcp-skill/
  SKILL.md
  examples.md
  README.md
  mcp-config-example.json
```

再按下方「各宿主如何引用」**导入或手工配置**；仅配置 MCP、不导入 Skill 时见文末「无 Skill、仅 MCP」。

---

## 各宿主如何引用


### Claude Desktop

**Skill：** 从 zip 解压得到 `SKILL.md`，将「授权」至「排错」章节复制到 **Settings → Profile → Custom Instructions**（无内置 Skill 目录，只能手工粘贴）。

**MCP：** 在 `claude_desktop_config.json` 的 `mcpServers` 中加入 `stdio` 或 `url`（可参考 `mcp-config-example.json`），修改后重启应用。

### VS Code / JetBrains 等（支持 MCP 的扩展）

**Skill：** 将解压后的 `SKILL.md` 要点写入 `.github/copilot-instructions.md` 或扩展指定的 `AGENTS.md` / rules 目录。

**MCP：** 在扩展 MCP 设置中添加 `tscanplus`，JSON 结构见 `mcp-config-example.json`。

### Cline、Roo Code、Continue 等 IDE 插件

**Skill：** 将解压后的 `SKILL.md` 全文或核心章节粘贴到插件的 **Custom Rules / .clinerules / 系统提示**；`examples.md` 可作参考，不必全部导入。

**MCP：** 插件中添加 MCP Server（stdio 或 sse），参数见 `SKILL.md` 或 `mcp-config-example.json`。


### Cursor（Cursor IDE / Cursor CLI）

**Skill（下载后导入或手工配置）**

1. **获取文件**：GUI 导出 `TscanPlus-skill.zip` 并解压（见上文「获取 Skill 包」）。
2. **创建目录**（二选一）：
   - **当前项目**：`<你的项目根>/.cursor/skills/tscanplus/`
   - **全局（所有项目）**：`~/.cursor/skills/tscanplus/`（Windows 为 `%USERPROFILE%\.cursor\skills\tscanplus\`）
3. **复制文件**：将解压得到的 `SKILL.md` 放入该目录；建议同时放入 `examples.md`（Agent 可读同目录示例）。
4. **重载**：保存后重启 Cursor，或在设置中重载窗口，使 Skill 生效。
5. **使用**：对话输入 `@tscanplus` 引用技能，或依赖 `SKILL.md` 头部 `description` 自动匹配。

目录结构示例：

```text
.cursor/skills/tscanplus/
  SKILL.md
  examples.md    # 可选，建议保留
```

**MCP**

- 全局：`~/.cursor/mcp.json`
- 项目：`<仓库>/.cursor/mcp.json`

```json
{
  "mcpServers": {
    "tscanplus": {
      "command": "/绝对路径/TscanPlus",
      "args": ["mcp", "stdio"]
    }
  }
}
```

### 自托管 Agent / 其他 MCP 客户端

1. **MCP：** 按 `mcp-config-example.json` 配置 `mcpServers`，推荐 `stdio`。
2. **行为：** 将解压后的 `SKILL.md` 作为系统提示附件，或写入自有 Agent 策略 YAML。
3. **HTTP：** 默认 Streamable HTTP：`TscanPlus mcp serve -listen 127.0.0.1:8088`，客户端填 `http://127.0.0.1:8088/mcp`；旧客户端可用 `-transport sse`，填 `http://127.0.0.1:8088/sse`。

### 无 Skill、仅 MCP

仅配置 MCP 时 Agent 仍可调用工具，但可能缺少授权策略、默认 `MCP` 项目语义与汇报格式。建议至少合并 `SKILL.md` 的「授权」「项目名 MCP」「调用后如何汇报」三节。

---

## 文件对照

| 用途 | 开发者（仓库内） | 普通用户（导出 zip 后） |
|------|------------------|-------------------------|
| Skill 源文件 | `TscanPlus-skill/SKILL.md` | 解压目录中的 `SKILL.md` |
| 示例 | `TscanPlus-skill/examples.md` | 解压目录中的 `examples.md` |
| Cursor 生效位置 | `.cursor/skills/tscanplus/SKILL.md` | 自行复制到 `~/.cursor/skills/tscanplus/` 或项目 `.cursor/skills/tscanplus/` |
