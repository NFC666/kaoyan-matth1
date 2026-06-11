# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Purpose

This is a high-density, exam-oriented digital notebook for 考研数学一 (高等数学). The goal is to maximize score efficiency through a concept-plus-example (概念与例题并重) approach. Every abstract definition must be paired with a concrete minimal example.

## Project Structure

```
kaoyan-math-notes/
├── README.md                  # Navigation index & chapter progress tracker
├── Methodologies/             # Cross-chapter universal methods (构造法, 放缩法, etc.)
├── Ch01_函数与极限/            # Chapter folder
│   ├── Ch01_Function_Limit_Continuity.md  # Main note (framework + index)
│   ├── 题型1_0除0型极限.md
│   └── ...（7 题型文件）
├── Ch02_导数与微分/
│   ├── Ch02_Derivative_Differential.md
│   ├── 题型1_导数定义与可导性判定.md
│   ├── ...（8 题型 + 1 方法文件）
│   └── 方法_求导路径选择策略.md
└── Methodologies/             # Cross-chapter universal methods
```

## Chapter File Template (Framework Matrix)

Every chapter file MUST follow this exact structure:

### ① 本章核心知识框架 (Core Concept Map)
- Hierarchical Markdown bullets for definitions, theorems, formulas, and conditions.
- **Rule**: For EVERY abstract definition/theorem, include a **1-sentence minimal example (极简例子)** inline.

### ② 必考题型分类索引 (Core Exam Question Types Index)
- Compact table with type name, key signal, and **Obsidian wiki-link** `[[题型文件]]` to the independent file.
- Each 题型 is a standalone `.md` file in the same chapter folder.

## 题型 File Template (Independent Question-Type File)

Every 题型 file MUST follow this structure:

```markdown
# 题型名

## 识别特征
(2-3 triggering signals)

## 解题流程
(mermaid flowchart — Obsidian natively renders this)

## 通法步骤
(Step-by-step, corresponds to flowchart nodes)

## 常见陷阱
(2-4 items)

## 经典母题
(1-2 problems + full solution)
```

- **Mermaid flowcharts**: Use `flowchart TD` (top-down) or `flowchart LR` (left-right) for decision trees and state transitions.
- **Obsidian links**: Use `[[filename]]` for internal links between notes in the same vault.

### ③ 高频考点与多维变换 (High-Frequency Focus)
- Top 3-5 most heavily tested concepts
- **【示例：一题多角度】** — ONE concept shown through 2 different test styles (conceptual MC trap vs. calculation-heavy problem)

### ④ 方法论与解题通法 (Methodology)
- General thinking frameworks (构造辅助函数, 变量代换, 放缩, 数形结合)
- **Rule**: Prioritize "判断依据 (When to use / Crucial signals)" over "操作步骤 (How to do)"
- Include shortcuts/formulas (口诀)

### ⑤ 易错点红黑榜 (The Pitfall List)
- ❌ **错误表现** + **正确理解** per entry
- **【对比示例】** — side-by-side wrong vs right minimal example

### ⑥ 考研导向复习策略 (Exam Strategy)
- Priority (High/Medium/Low) & suggested problem count
- Cross-chapter connections (prerequisites / post-requisites / composite problems)
- **【终极母题推荐】** — 1 ultimate problem the user must master to consider this chapter "done"

## Content Rules

- **Language**: Highly concise, professional Chinese math terms, zero filler
- **Formulas**: Standard LaTeX — `$...$` for inline, `$$...$$` for display. Format brackets, limits, integrals flawlessly
- **Anti-patterns to avoid**: Pure textbook theory dumps, brute-force calculation grinding, verbose explanations that don't directly improve exam scores
- **In-text links**: Use relative links between chapter files and methodology files (e.g., `[构造法](../Methodologies/Construction_Method.md)`)

## Workflow When Editing a Chapter

1. **Analyze** the topic/outline the user provides
2. **Web Search** for latest 考研 trends, high-frequency trap points, and standard solutions for that chapter (use `WebSearch` tool)
3. **Generate** content following the Framework Matrix
4. **Stop and ask** for user feedback before continuing — the user will request modifications

## README.md Convention

The README serves as the navigation hub. Each chapter line should follow this format:
- Checkbox `[ ]` for progress tracking
- Link to chapter file
- Brief scope description (what's covered)
- Priority tag: `[高]` / `[中]` / `[低]`

## When Cross-Referencing

- Methods used across chapters go in `Methodologies/` as standalone files
- Chapter files link to methodology files, never duplicate methodology content
- Cross-chapter connections go in ⑥ section of each chapter
