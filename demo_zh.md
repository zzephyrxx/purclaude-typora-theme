# Purclaude 主题演示

> [English Version](demo.md)

> 这份示例文档用于展示 **Purclaude** 主题的排版效果。包含标题、正文、数学公式、表格、高亮、引用、代码块、列表、任务列表、脚注等常见 Markdown 元素。
>
> Purclaude 基于 [Tsumugii24/claude-typora-theme](https://github.com/Tsumugii24/claude-typora-theme) 构建，在其基础上重新设计了深紫色调色板、交互动效与排版细节，打造更具沉浸感的暗色写作体验。

---

## 1. 正文排版

Purclaude 主题专为长文写作设计。段落间距舒适，行高适中，配合 Anthropic Serif 衬线字体与 Noto Serif SC 中文字体，兼顾中英文混排的阅读体验。

你可以在同一段落中使用 **粗体文本**、*斜体文本*、`行内代码`、==高亮文本==、<u>下划线文本</u>，以及 [Typora 链接](https://typora.io) 等多种行内样式。中英文自然混排：这是一个中文段落，用来检查中英混排、**加粗**、行距和标点显示效果。

> 好的排版应当让结构清晰可见，而不会让界面显得嘈杂。
>
> 这段引用用于检查缩进、对比度和行高表现。

>> 嵌套引用同样经过精心调色，确保层次分明。

## 2. 标题层级

以下展示从 H1 到 H6 的标题样式。Purclaude 为不同层级分配了不同的紫色调——H1 使用温暖的亮紫 (`--accent-warm`)，H2 使用主色调 (`--accent-primary`)，H3 使用次色调 (`--accent-secondary`)，逐级递减。

### 三级标题 — Secondary Accent

#### 四级标题 — 正文色

##### 五级标题 — 柔和灰紫

###### 六级标题 — 最低层级

## 3. 数学公式

行内数学公式应自然融入文本，例如 $E = mc^2$、$a^2 + b^2 = c^2$，以及 $\alpha + \beta = \gamma$。

块级数学公式保持居中与可读性：

$$
\nabla_\theta J(\theta)
= \mathbb{E}_{x \sim p(x)}
\left[
  \nabla_\theta \log p_\theta(x) \cdot R(x)
\right]
$$

矩阵示例：

$$
A =
\begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{bmatrix}
$$

欧拉公式，数学中最优雅的等式之一：

$$
e^{i\pi} + 1 = 0
$$

## 4. 表格

下方表格用于检查表头样式、行分隔线、对齐方式和中英文混合内容的显示效果。

| 特性 | Purclaude | Claude Dark | 说明 |
| :-- | :--: | :--: | :-- |
| 色调 | 深紫色 | 深灰棕色 | Purclaude 采用 `#1a1625` 为基色 |
| 字体 | Anthropic Serif | Anthropic Sans | 正文使用衬线体，更具阅读质感 |
| 代码高亮 | 紫色系 | 灰棕系 | 关键词、字符串、数字各有专属配色 |
| CJK 支持 | Noto Serif SC | Noto Serif SC | 完整中文衬线字体支持 |
| 聚焦模式 | 自定义淡出 | 默认 | 非活跃段落柔和淡出至深紫 |

| Model | AIME 2025 | MMLU | HumanEval | Notes |
| :-: | --: | --: | --: | :-- |
| Claude 4 Opus | 96.7% | 92.3% | 95.1% | State of the art |
| GPT-5 | 94.2% | 91.8% | 93.7% | Strong contender |
| Qwen3-32B | 76.7% | 85.4% | 88.2% | Open-source leader |

## 5. 列表与任务

### 有序列表

1. 将 `purclaude.css` 和 `purclaude/` 文件夹复制到 Typora 主题目录
2. 重启 Typora
3. 在 **偏好设置 → 外观 → 主题** 中选择 **Purclaude**
4. 打开此示例文件，检查所有元素渲染效果

### 无序列表

- 正文排版应保持高可读性
- 嵌套信息应保持视觉层次
  - 二级嵌套项
  - 另一个二级项
    - 三级嵌套项
- 代码、公式、表格和引用应与页面融为一体

### 任务列表

- [x] 完成深紫色调色板设计
- [x] 集成 Anthropic 字体家族
- [x] 自定义复选框样式
- [x] 优化聚焦模式 (F8) 淡出效果
- [ ] 添加主题截图
- [ ] 提交到 Typora Theme Gallery

## 6. 代码

行内代码如 `font-family`、`@font-face`、`border-bottom` 应与周围文本对齐良好。

### CSS

```css
:root {
    --bg-color: #1a1625;
    --accent-primary: #a78bfa;
    --accent-secondary: #8b5cf6;
    --accent-warm: #c084fc;
    --font-color: #e8e4f0;
    --font-serif: "Anthropic Serif Web Text", Georgia, "Noto Serif SC";
    --font-mono: "Anthropic Mono Variable", ui-monospace, monospace;
}

#write blockquote {
    background-color: var(--warning-bg);
    border-left: 3px solid var(--warning-border);
    border-radius: 0 8px 8px 0;
}

```

### Python

```python
def theme_palette(name: str) -> dict:
    """Generate the Purclaude color palette."""
    palette = {
        "bg":      "#1a1625",
        "primary": "#a78bfa",
        "secondary": "#8b5cf6",
        "warm":    "#c084fc",
        "text":    "#e8e4f0",
        "muted":   "#9d94b8",
    }
    return {f"{name}_{k}": v for k, v in palette.items()}

colors = theme_palette("purclaude")
for key, value in colors.items():
    print(f"{key}: {value}")
```

### JavaScript

```javascript
const purclaude = {
  name: 'Purclaude',
  type: 'dark',
  colors: {
    bg: '#1a1625',
    accent: '#a78bfa',
    warm: '#c084fc',
    text: '#e8e4f0',
  },
  fonts: {
    serif: 'Anthropic Serif Web Text',
    sans: 'Anthropic Sans Web Text',
    mono: 'Anthropic Mono Variable',
  },
};

console.log(`Theme: ${purclaude.name} (${purclaude.type})`);
```

## 7. 引用提示 (Callouts)

> [!NOTE]
> 这是一条说明提示。适用于中性的补充信息。Purclaude 主题为引用块设计了半透明紫色背景。

> [!TIP]
> 使用提示框来突出工作流建议、写作技巧或小提醒。

> [!IMPORTANT]
> 重要提示应清晰突出，但不会压倒周围的内容。

> [!WARNING]
> 警告提示用于引起对风险假设或破坏性变更的注意。

> [!CAUTION]
> 注意提示适用于不可逆操作或需要谨慎决策的场景。

## 8. 图像

如果你需要测试图像样式，可以在此处插入图片。Purclaude 为图片添加了圆角边框和阴影效果，悬停时边框会变为主色调紫色。

## 9. 分隔线

下方是 Purclaude 主题的渐变分隔线，从透明渐变到紫色再回到透明：

---

## 10. 脚注

脚注应当可见，但不会干扰正文的阅读流程。[^1][^2]

---

## 关于 Purclaude

**Purclaude** (Purple + Claude) 是一款深紫色暗色 Typora 主题，灵感来源于 [Claude](https://claude.ai) 的视觉美学。

本主题基于 [Tsumugii24/claude-typora-theme](https://github.com/Tsumugii24/claude-typora-theme) 进行二次开发，主要改进包括：

- 全新的深紫色调色板，替换原有的灰棕暗色方案
- 正文采用 Anthropic Serif 衬线字体，提升长文阅读体验
- 重新设计的选中态、悬停态和过渡动画
- 自定义复选框、分隔线渐变和代码高亮配色
- 增强的聚焦模式 (F8) 视觉效果

[^1]: Purclaude 主题以 MIT 协议发布，可自由使用和修改。

[^2]: 基于 [Tsumugii24/claude-typora-theme](https://github.com/Tsumugii24/claude-typora-theme)，该项目又基于 [blaxisomu/CLAUDE-Typora](https://github.com/blaxisomu/CLAUDE-Typora) 开发。
