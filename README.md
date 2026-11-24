# Ask the Library · 问知阁

遇到不懂的，就来这里查一查。

这里收录协议规范、技术手册和书籍的阅读 skill。每个阅读器都携带原始材料、章节知识库和检索工具，帮助从具体版本的原文中寻找依据。

协议类资料统一存放在 [protocols/](protocols/)，已收录资料见[书单](BOOKS.md)。

## 构建阅读 skill

支持带文字层的 PDF、DOCX、Markdown 和 TXT。以协议资料为例，可以直接让 AI 助手使用本仓库的构建器：

```text
使用 readskill-builder，把 /path/to/protocol.pdf 构建成阅读 skill，输出到当前仓库的 protocols/ 目录。
```

也可以使用 Python 3，在仓库根目录手动执行：

```bash
python3 readskill-builder/scripts/build_protocol_skill.py --input "/path/to/protocol.pdf" --output-parent protocols
```

名称和标题默认从文件名生成，可用 `--output-parent` 指定分类目录。构建 PDF 前需安装依赖：`python3 -m pip install pymupdf`。更多用法见 [readskill-builder](readskill-builder/SKILL.md)。
