# Purclaude Theme Demo

> [中文版](demo_zh.md)

> This example document showcases the typography and styling of the **Purclaude** theme. It covers headings, prose, math, tables, highlights, callouts, quotes, code blocks, lists, tasks, footnotes, and more.
>
> Purclaude is built upon [Tsumugii24/claude-typora-theme](https://github.com/Tsumugii24/claude-typora-theme), redesigned with a deep purple palette, refined interactions, and polished typographic details for an immersive dark writing experience.

---

## 1. Reading Flow

Purclaude is designed for long-form Markdown writing. Paragraph spacing is comfortable, line height is generous, and the Anthropic Serif typeface paired with Noto Serif SC delivers a refined reading experience for both Latin and CJK text.

You can use **bold text**, *italic text*, `inline code`, ==highlighted text==, <u>underlined text</u>, and links such as [Typora](https://typora.io) in the same paragraph. Chinese and English mix naturally: 这是一个中文段落，用来检查中英混排、**加粗**、行距和标点显示效果。

> Good typography should make structure visible without making the interface feel noisy.
>
> This quote block is useful for checking indentation, contrast, and line height.

>> Nested quotes are also carefully styled to maintain clear visual hierarchy.

## 2. Heading Levels

Below are heading styles from H1 through H6. Purclaude assigns a different shade of purple to each level — H1 uses the warm bright purple (`--accent-warm`), H2 the primary accent (`--accent-primary`), H3 the secondary accent (`--accent-secondary`), tapering off gradually.

### Third Level — Secondary Accent

#### Fourth Level — Body Color

##### Fifth Level — Soft Muted Purple

###### Sixth Level — Lowest Tier

## 3. Mathematics

Inline math should sit comfortably within text, for example $E = mc^2$, $a^2 + b^2 = c^2$, and $\alpha + \beta = \gamma$.

Block math should remain centered and readable:

$$
\nabla_\theta J(\theta)
= \mathbb{E}_{x \sim p(x)}
\left[
  \nabla_\theta \log p_\theta(x) \cdot R(x)
\right]
$$

A matrix example:

$$
A =
\begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{bmatrix}
$$

Euler's formula, one of the most elegant equations in mathematics:

$$
e^{i\pi} + 1 = 0
$$

## 4. Tables

The tables below are useful for checking header styles, row separators, alignment, and mixed-language content.

| Feature | Purclaude | Claude Dark | Notes |
| :-- | :--: | :--: | :-- |
| Palette | Deep purple | Dark warm gray | Purclaude uses `#1a1625` as base |
| Body Font | Anthropic Serif | Anthropic Sans | Serif body for richer reading |
| Syntax Colors | Purple family | Warm gray family | Keywords, strings, numbers each have distinct colors |
| CJK Support | Noto Serif SC | Noto Serif SC | Full Chinese serif font support |
| Focus Mode | Custom fade-out | Default | Inactive paragraphs softly fade to deep purple |

| Model | AIME 2025 | MMLU | HumanEval | Notes |
| :-- | --: | --: | --: | :-- |
| Claude 4 Opus | 96.7% | 92.3% | 95.1% | State of the art |
| GPT-5 | 94.2% | 91.8% | 93.7% | Strong contender |
| Qwen3-32B | 76.7% | 85.4% | 88.2% | Open-source leader |

## 5. Lists and Tasks

### Ordered List

1. Copy `purclaude.css` and the `purclaude/` folder to Typora's themes directory.
2. Restart Typora.
3. Select **Purclaude** from **Preferences → Appearance → Themes**.
4. Open this example file and check that every element renders correctly.

### Unordered List

- Prose should remain highly readable.
- Nested information should maintain visual hierarchy.
  - Second-level item
  - Another second-level item
    - Third-level item
- Code, math, tables, and quotes should feel integrated with the page.

### Task List

- [x] Design the deep purple palette
- [x] Integrate the Anthropic font family
- [x] Custom checkbox styling
- [x] Optimize Focus Mode (F8) fade-out effect
- [ ] Add theme screenshots
- [ ] Submit to Typora Theme Gallery

## 6. Code

Inline code such as `font-family`, `@font-face`, and `border-bottom` should align well with surrounding text.

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

## 7. Callouts

> [!NOTE]
> This is a note callout. Useful for neutral supporting information. Purclaude styles blockquotes with a semi-transparent purple background.

> [!TIP]
> Use callouts to highlight workflow hints, writing advice, or small reminders.

> [!IMPORTANT]
> Important callouts should stand out clearly without overwhelming nearby content.

> [!WARNING]
> Warning callouts help draw attention to risky assumptions or breaking changes.

> [!CAUTION]
> Caution callouts are useful for destructive operations or irreversible decisions.

## 8. Images

Insert an image here to test image styling. Purclaude adds rounded borders and shadow to images; on hover, the border transitions to the primary purple accent.

## 9. Horizontal Rule

Below is Purclaude's gradient horizontal rule — fading from transparent to purple and back:

---

## 10. Footnotes

Footnotes should be visible without distracting from the main reading flow.[^1][^2]

---

## About Purclaude

**Purclaude** (Purple + Claude) is a deep purple dark theme for Typora, inspired by the visual aesthetics of [Claude](https://claude.ai).

This theme is built upon [Tsumugii24/claude-typora-theme](https://github.com/Tsumugii24/claude-typora-theme). Key improvements include:

- A completely new deep purple palette, replacing the original warm-gray dark scheme
- Anthropic Serif as the body typeface for a richer long-form reading experience
- Redesigned selection states, hover states, and transition animations
- Custom checkboxes, gradient horizontal rules, and syntax highlight colors
- Enhanced Focus Mode (F8) visual effects

[^1]: Purclaude is released under the MIT License. Free to use and modify.

[^2]: Built upon [Tsumugii24/claude-typora-theme](https://github.com/Tsumugii24/claude-typora-theme), which itself builds on [blaxisomu/CLAUDE-Typora](https://github.com/blaxisomu/CLAUDE-Typora).
