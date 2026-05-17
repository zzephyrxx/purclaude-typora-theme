# Purclaude

> [English](README.md)

一款精致的深紫色暗色 [Typora](https://typora.io/) 主题，将深紫色调的优雅与极致的读写体验融为一体。灵感来源于 [Claude](https://claude.ai) 的视觉美学。

![Purclaude 主题预览](screenshots/main.png)

## 特性

- **深紫色调色板** — 护眼的紫色色调（`#1a1625` 为基色）
- **优雅排版** — 正文使用 Anthropic Serif 衬线体，UI 使用无衬线体，代码使用等宽字体
- **语法高亮** — 精心调校的代码块配色方案
- **流畅交互** — 精致的悬停状态、选中态和过渡动画
- **CJK 支持** — 使用 Noto Serif SC 提供完整的中文排版支持
- **聚焦模式** — 非活跃段落柔和淡出，打造无干扰写作体验

## 安装

1. 下载或克隆本仓库。
2. 将 `purclaude.css` 和 `purclaude/` 文件夹复制到 Typora 主题目录：
   - **Windows**: `%APPDATA%\Typora\themes\`
   - **macOS**: `~/Library/Application Support/Typora/themes/`
   - **Linux**: `~/.config/Typora/themes/`
3. 重启 Typora，在 **偏好设置 → 外观 → 主题** 中选择 **Purclaude**。

## 文件结构

```
typora-theme-purclaude/
├── purclaude.css              # 主题样式表
├── purclaude/                 # 主题资源（字体）
│   ├── AnthropicSansWebText.ttf
│   ├── AnthropicSerifWebText.ttf
│   ├── AnthropicMonoVariable.ttf
│   └── NotoSerifSC-VariableFont_wght.ttf
├── demo.md                    # 主题演示文档（English）
├── demo_zh.md                 # 主题演示文档（中文）
├── screenshots/               # 主题截图
│   └── main.png
├── LICENSE
├── README.md                  # English
└── README_zh.md               # 中文
```

## 自定义

主题使用 CSS 自定义属性，便于个性化修改。编辑 `purclaude.css` 中的变量：

```css
:root {
    --bg-color: #1a1625;           /* 主背景色 */
    --accent-primary: #a78bfa;     /* 主强调色 */
    --accent-secondary: #8b5cf6;   /* 次强调色 */
    --accent-warm: #c084fc;        /* 暖强调色 */
    --font-color: #e8e4f0;         /* 正文颜色 */
}
```

## 演示

在 Typora 中打开 [`demo_zh.md`](demo_zh.md) 预览完整的主题展示效果，包括标题、表格、数学公式、代码块、引用提示、任务列表等。

## 许可证

[MIT License](LICENSE)

## 致谢

- **基于**: [Tsumugii24/claude-typora-theme](https://github.com/Tsumugii24/claude-typora-theme)（该项目基于 [blaxisomu/CLAUDE-Typora](https://github.com/blaxisomu/CLAUDE-Typora)）
- **设计**: 灵感来源于 [Claude](https://claude.ai) 视觉美学
- **字体**: Anthropic Web Fonts + [Noto Serif SC](https://fonts.google.com/noto/specimen/Noto+Serif+SC)
