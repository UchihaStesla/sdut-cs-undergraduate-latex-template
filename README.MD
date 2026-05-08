# SDUT CS Undergraduate Design LaTeX Template

> 山东理工大学计算机科学与技术专业本科毕业论文 LaTeX 模板

## 关于

本仓库提供山东理工大学计算机科学与技术专业本科毕业论文的 LaTeX 模板。
模板入口为 `main.tex`，正文、摘要、封面等内容放在 `data/` 目录中。

该模板以 XeLaTeX 编译为目标，适合需要中文字体和中文断行的论文场景。

## 快速开始

1. 安装 TeX Live、MiKTeX 或其他包含 XeLaTeX 的发行版。
2. 修改 `main.tex` 中的题目、学院、专业、姓名、学号、指导教师和日期。
3. 修改 `data/` 目录下的摘要、章节、参考文献和致谢内容。
4. 在仓库根目录运行：

```powershell
xelatex main.tex
xelatex main.tex
```

如果使用参考文献工具，可以根据自己的 `.bib` 工作流改造 `data/bibliography.tex`。

## 目录结构

```text
.
├── main.tex              # 论文入口文件
├── csbachelor.cls        # 模板样式定义
├── csbachelor.cfg        # 论文信息命令定义
├── data/
│   ├── cover-zh.tex      # 中文封面
│   ├── cover-en.tex      # 英文封面
│   ├── agreement.tex     # 原创性声明
│   ├── abstract-zh.tex   # 中文摘要
│   ├── abstract-en.tex   # 英文摘要
│   ├── chapter-*.tex     # 正文章节
│   ├── bibliography.tex  # 参考文献
│   └── acknowledgment.tex # 致谢
└── README.MD
```

## 使用建议

- 正式提交前，请根据学院最新论文格式要求核对封面、页眉、字号、行距和参考文献格式。
- `main.pdf` 可以作为示例预览文件；实际写作时建议只提交源文件并自行编译最终 PDF。
- 如果编译时报字体错误，请先确认系统中存在 `Times New Roman`、`Arial`、`Courier New` 以及常见中文字体。

## 感谢

感谢 [浙江大学的 LaTeX 模板](https://github.com/zhanghai/zju-csse-undergraduate-design-latex-template) 提供参考。

