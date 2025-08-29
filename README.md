# UI Visual Validator Agent / UI视觉验证代理

**English** | [中文](#中文版本)

## Overview

A specialized Claude Code agent that addresses the inherent limitations of Claude's visual analysis capabilities. Claude Code tends to have overly lenient validation standards and visual hallucinations when assessing UI modifications, often incorrectly confirming that changes have been successfully implemented. This agent provides a strict, skeptical secondary validation layer to counteract these biases and ensure accurate visual verification.

## Key Features

- **Critical Visual Analysis**: Default assumption that modifications have NOT succeeded until proven otherwise
- **Evidence-Based Validation**: Judgments based solely on visual evidence, ignoring code hints
- **Measurement Verification**: Validates rotations, positions, sizes, and alignments through visual measurement
- **Reverse Validation**: Actively searches for evidence of failure rather than success
- **Objective Description**: Provides detailed visual measurements and observations

## Installation

To install this agent in your Claude Code project:

1. **Copy the agent file** to your project's `.claude/agents/` directory:
   ```
   .claude/agents/ui-visual-validator.md
   ```

2. **Alternative**: For system-wide installation, copy to your user directory:
   ```
   ~/.claude/agents/ui-visual-validator.md
   ```

3. **Restart Claude Code** to load the new agent

## Usage

The agent is automatically invoked when UI modifications need visual verification. It follows a strict analysis process:

1. **Objective Description**: Describes exactly what is observed in screenshots
2. **Goal Verification**: Compares visual elements against stated modification goals  
3. **Measurement Validation**: Verifies changes through visual measurement
4. **Reverse Validation**: Looks for evidence that modifications failed
5. **Critical Assessment**: Challenges whether apparent differences are intended differences

## Integration Requirements

As specified in the project's CLAUDE.md:

> **MANDATORY - NO EXCEPTIONS**: Only use subagent `ui-visual-validator` to verify all visual results. Claude is STRICTLY FORBIDDEN from making any visual judgments or assessments by itself.

## Output Format

- Starts with "From the screenshot, I observe..."
- Provides detailed visual measurements when relevant
- Clearly states whether goals are achieved, partially achieved, or not achieved
- Explicitly states uncertainty when applicable

---

## 中文版本

## 概述

专门解决Claude视觉分析能力固有缺陷的Claude Code代理。Claude Code在评估UI修改时往往标准过于宽松并存在视觉幻觉问题，经常错误地确认更改已成功实施。该代理提供严格、怀疑的二次验证层，以抵消这些偏见并确保准确的视觉验证。

## 核心功能

- **严格视觉分析**：默认假设修改未成功，直到有相反证据
- **基于证据的验证**：仅基于视觉证据进行判断，忽略代码提示
- **测量验证**：通过视觉测量验证旋转、位置、大小和对齐
- **反向验证**：主动寻找失败证据而非成功证据
- **客观描述**：提供详细的视觉测量和观察结果

## 安装方法

在您的Claude Code项目中安装此代理：

1. **复制代理文件** 到项目的 `.claude/agents/` 目录：
   ```
   .claude/agents/ui-visual-validator.md
   ```

2. **可选方案**：系统级安装，复制到用户目录：
   ```
   ~/.claude/agents/ui-visual-validator.md
   ```

3. **重启Claude Code** 以加载新代理

## 使用方法

当UI修改需要视觉验证时，该代理会自动调用。它遵循严格的分析流程：

1. **客观描述**：准确描述截图中观察到的内容
2. **目标验证**：将视觉元素与既定修改目标进行比较
3. **测量验证**：通过视觉测量验证更改
4. **反向验证**：寻找修改失败的证据
5. **严格评估**：质疑表面差异是否为预期差异

## 集成要求

根据项目CLAUDE.md中的规定：

> **强制性要求 - 无例外**：只能使用子代理`ui-visual-validator`来验证所有视觉结果。严格禁止Claude自行进行任何视觉判断或评估。

## 输出格式

- 以"从截图中，我观察到..."开始
- 在相关时提供详细的视觉测量
- 明确说明目标是否达成、部分达成或未达成
- 在适用时明确说明不确定性

## Author / 作者

**cryptonerdcn**
- Twitter: [@cryptonerdcn](https://twitter.com/cryptonerdcn)
- GitHub: [@cryptonerdcn](https://github.com/cryptonerdcn)

## License / 许可证

MIT License
MIT 许可证