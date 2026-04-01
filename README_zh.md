# Skills: Research Paper Writing

> 重要归属说明
> 本仓库中的大部分写作经验与方法论来自彭思达老师公开的学习笔记：
> https://pengsida.notion.site/c1a22465a0fa4b15a12985223916048e
> 彭老师原始仓库：
> https://github.com/pengsida/learning_research
> 衷心感谢彭思达老师把这些宝贵经验公开分享出来。
> 我主要做了资料整理、结构化适配，以及 Skills 封装。

## 仓库介绍

当前仓库提供 1 个技能包：

- `research-paper-writing/`
  - `SKILL.md`：核心流程与使用规则
  - `references/`：按章节拆分的写作指南与模板
  - `agents/openai.yaml`：Agent 元信息

常见使用场景：

- 撰写或重写 Abstract / Introduction / Method / Experiments / Conclusion
- 改善段落衔接与章节逻辑
- 做 claim-evidence 对齐检查
- 提交前从 reviewer 视角进行自审

## 安装方式

以下命令默认在仓库根目录执行。下面用**软链接**挂入技能目录：在本仓库 `git pull` 后内容会同步更新；若移动或删除本仓库，需重新执行安装。若某客户端不认软链，可改用 `cp -R research-paper-writing <目标目录>/`。

### 1) Codex

将技能软链接到 `$CODEX_HOME/skills/`：

```bash
mkdir -p "$CODEX_HOME/skills"
ln -sfn "$(pwd)/research-paper-writing" "$CODEX_HOME/skills/research-paper-writing"
```

使用示例：

```text
Use $research-paper-writing to improve my paper's Introduction.
```

### 2) CC（Claude Code）

可选择全局安装或项目级安装。

全局安装：

```bash
mkdir -p "$HOME/.claude/skills"
ln -sfn "$(pwd)/research-paper-writing" "$HOME/.claude/skills/research-paper-writing"
```

项目级安装：

```bash
mkdir -p .claude/skills
ln -sfn "$(pwd)/research-paper-writing" .claude/skills/research-paper-writing
```

使用时建议在提示词中显式指定，例如：`Please use the research-paper-writing skill`。

### 3) Gemini

可将该技能软链接到 Gemini 的技能目录：

```bash
mkdir -p "$HOME/.gemini/skills"
ln -sfn "$(pwd)/research-paper-writing" "$HOME/.gemini/skills/research-paper-writing"
```

随后在 Gemini 中直接给出具体任务（例如：重写 Abstract 并做 claim-evidence 检查）。

### 4) Cursor

可将技能安装到用户级或项目级目录（Cursor 使用 `.cursor/skills/`；请勿放入 `~/.cursor/skills-cursor/`，该目录由 Cursor 保留给内置技能）。

用户级（全局）：

```bash
mkdir -p "$HOME/.cursor/skills"
ln -sfn "$(pwd)/research-paper-writing" "$HOME/.cursor/skills/research-paper-writing"
```

项目级（随仓库共享）：
cp -R research-paper-writing "$HOME/.gemini/skills/"
```bash
mkdir -p .cursor/skills
ln -sfn "$(pwd)/research-paper-writing" .cursor/skills/research-paper-writing
```

使用时在对话中显式说明即可，例如：`请使用 research-paper-writing 技能帮我改写 Introduction`。

## 致谢

再次说明：仓库核心知识来源于彭思达老师公开笔记；我主要负责整理与 Skills 化适配。
彭老师原始仓库：https://github.com/pengsida/learning_research
