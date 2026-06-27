# 快速启动指南

快速了解和使用 Ethan-skills 项目。

## ⚡ 5分钟快速开始

### 1. 安装依赖

```bash
# 克隆项目
git clone https://github.com/yourusername/Ethan-skills.git
cd Ethan-skills

# 安装依赖
pip install -r requirements.txt
```

### 2. 生成你的第一份报告

创建一个 `example.md` 文件：

```markdown
# GitHub 的发展历程

> 研究时间：2026年6月 | 所属领域：开发工具 | 研究对象类型：产品

## 一句话定义

GitHub 是一个基于 Git 的分布式版本控制和协作平台，改变了全球开发者的工作方式。

## 纵向分析：从诞生到当下

### 起源与诞生

GitHub 成立于 2008 年，由 Tom Preston-Werner、Chris Wanstrath 和 P.J. Hyett 三人创办...

（更多内容...）

## 横向分析：竞争图谱

### 主要竞品

1. **GitLab**：功能更全面的企业级解决方案
2. **Gitea**：轻量级的自部署方案
3. **Bitbucket**：Atlassian 生态的版本控制工具

（更多内容...）

## 横纵交汇洞察

GitHub 的成功不仅在于采用了 Git...

（结论...）
```

### 3. 转换为 PDF

```bash
python hv-skills/scripts/md_to_pdf.py example.md example.pdf \
  --title "GitHub 的发展历程" \
  --author "研究员"
```

### 4. 查看生成的 PDF

```bash
open example.pdf  # macOS
# 或
start example.pdf  # Windows
# 或
xdg-open example.pdf  # Linux
```

完成！你的第一份精美的研究报告已生成。

---

## 📚 详细文档

| 文件 | 内容 |
|------|------|
| [README.md](README.md) | 项目概览和功能说明 |
| [hv-skills/SKILL.md](hv-skills/SKILL.md) | 纵横双轴分析的完整指南 |
| [CONTRIBUTING.md](CONTRIBUTING.md) | 如何贡献代码 |
| [CHANGELOG.md](CHANGELOG.md) | 版本变更历史 |

---

## 🛠️ 常见任务

### 修改报告样式

编辑 `hv-skills/scripts/md_to_pdf.py` 中的 `CSS_TEMPLATE` 部分：

```python
CSS_TEMPLATE = """
@page {
    size: A4;
    margin: 25mm 20mm 20mm 20mm;
    /* 自定义页面设置 */
}

h1 {
    color: #1a5276;  /* 改变标题颜色 */
    /* 更多样式... */
}
"""
```

### 更改默认字体

在 CSS 中修改 font-family：

```css
body {
    font-family: "Droid Sans Fallback", "Helvetica Neue", Helvetica, Arial, sans-serif;
}
```

### 禁用作者显示

运行脚本时不提供 `--author` 参数：

```bash
python hv-skills/scripts/md_to_pdf.py example.md example.pdf --title "报告标题"
```

---

## ❓ 常见问题

### Q: 生成的 PDF 中文显示为方块？

A: 确保系统已安装中文字体。在 CSS 中字体已配置为 fallback 链，应该能自动选择。如果不行，尝试安装：

```bash
# macOS
brew install font-droid-sans-mono

# Ubuntu
sudo apt-get install fonts-droid-fallback

# Windows
下载并安装 Droid Sans 字体
```

### Q: 如何自定义 PDF 的页边距？

A: 编辑 `md_to_pdf.py` 中的 CSS：

```python
@page {
    margin: 30mm 25mm 25mm 25mm;  /* 上右下左 */
}
```

### Q: 支持在 PDF 中添加页码吗？

A: 已经支持了！在脚本中的 CSS 配置了 `@bottom-center` 显示页码。

### Q: 可以输出为其他格式吗？

A: 目前仅支持 PDF。Word/HTML 导出在规划中。

---

## 🚀 下一步

- 📖 阅读 [hv-skills/SKILL.md](hv-skills/SKILL.md) 了解深度研究方法
- 🔧 根据需要自定义 PDF 样式
- 📝 参考 [CONTRIBUTING.md](CONTRIBUTING.md) 贡献新功能
- 💬 在 GitHub Issues 中分享你的使用经验

---

## 📞 获取帮助

- 📖 查看详细文档
- 🐛 报告 Bug（创建 GitHub Issue）
- 💡 建议新功能
- 🤝 贡献代码

---

**Happy researching!** 🎉

*最后更新: 2026-06-27*
