# 贡献指南

感谢你对 Ethan-skills 项目的兴趣！这份指南将帮助你有效地参与项目的开发。

## 🤝 贡献方式

### 报告缺陷（Issues）

如果你发现了 bug，请创建一个 Issue 并包含：

1. **问题描述**：清楚地说明问题是什么
2. **复现步骤**：详细的步骤来重现问题
3. **期望行为**：说明你期望的结果
4. **实际行为**：说明现在发生的情况
5. **环境信息**：
   - Python 版本
   - 操作系统
   - 相关的依赖包版本

示例：
```markdown
**问题描述**
生成 PDF 时中文字体显示不正常

**复现步骤**
1. 创建包含中文的 Markdown 文件
2. 运行 `python md_to_pdf.py test.md output.pdf`
3. 打开生成的 PDF

**期望行为**
中文文本显示正常，字体清晰可读

**实际行为**
中文显示为方块或乱码

**环境信息**
- Python 3.9
- macOS 12.0
- weasyprint 56.0
```

### 功能建议（Feature Requests）

如果你有新功能的想法，请创建一个 Issue 并说明：

1. **功能描述**：这个功能是什么
2. **使用场景**：在什么情况下需要这个功能
3. **实现思路**：你有什么想法吗（可选）
4. **相关的其他项目**：有没有类似的实现可以参考

示例：
```markdown
**功能描述**
支持导出为 Word 格式

**使用场景**
用户需要编辑生成的报告，PDF 不方便编辑

**实现思路**
使用 python-docx 库转换 Markdown 为 Word

**相关项目**
- Pandoc（多格式转换）
- python-docx（Word 生成）
```

### 提交代码（Pull Requests）

#### 准备工作

1. **Fork 项目**
   ```bash
   git clone https://github.com/yourusername/Ethan-skills.git
   cd Ethan-skills
   ```

2. **创建功能分支**
   ```bash
   git checkout -b feature/your-feature-name
   # 或者修复分支
   git checkout -b fix/bug-description
   ```

3. **安装开发依赖**
   ```bash
   pip install -r requirements-dev.txt  # 如果有的话
   pip install weasyprint markdown pytest  # 最基础的依赖
   ```

#### 开发规范

##### 代码风格

- **Python 代码**：遵循 PEP 8 标准
  - 使用 4 空格缩进
  - 最大行长 120 字符
  - 使用有意义的变量名

- **Markdown 文档**：清晰有序
  - 使用 2 空格缩进代码块
  - 保持一致的标题级别
  - 在代码块指定语言

示例：

```python
# ✅ 好的
def generate_pdf_report(markdown_content, output_path, title="", author=""):
    """
    将 Markdown 内容转换为 PDF 报告。
    
    Args:
        markdown_content (str): Markdown 格式的内容
        output_path (str): 输出 PDF 文件的路径
        title (str): 报告标题（可选）
        author (str): 作者名称（可选）
    
    Returns:
        bool: 成功返回 True，失败返回 False
    """
    pass

# ❌ 不好的
def gen_pdf(mc, op, t="", a=""):
    """generate pdf"""
    pass
```

##### 提交信息

使用 Conventional Commits 格式：

```bash
# 新功能
git commit -m "feat: 添加 Word 格式导出支持"

# 缺陷修复
git commit -m "fix: 修复 PDF 生成时的中文显示问题"

# 文档更新
git commit -m "docs: 更新 PDF 生成的使用说明"

# 代码重构
git commit -m "refactor: 简化 Markdown 解析逻辑"

# 性能优化
git commit -m "perf: 优化大文件的 PDF 转换速度"

# 测试相关
git commit -m "test: 添加 PDF 生成的单元测试"

# 依赖更新
git commit -m "chore: 更新 weasyprint 到 56.0"
```

#### 提交 PR

1. **推送你的分支**
   ```bash
   git push origin feature/your-feature-name
   ```

2. **创建 Pull Request**
   在 GitHub 上创建 PR 时，请包含：
   - **标题**：简洁地说明改动内容
   - **描述**：
     - 改动的内容是什么
     - 为什么需要这个改动
     - 如何测试这个改动
     - 相关的 Issue 号（如有）
   - **检查清单**：
     - [ ] 代码遵循项目风格规范
     - [ ] 包含必要的代码注释
     - [ ] 包含或更新了相关文档
     - [ ] 添加了测试（如适用）
     - [ ] 所有测试都通过了

PR 描述示例：

```markdown
## 改动内容
修复了 PDF 生成时中文字体显示为方块的问题。

## 改动原因
WeasyPrint 默认配置不支持中文字体，需要在 CSS 中指定字体 fallback 链。

## 测试方法
1. 创建含有中文的 Markdown 文件
2. 运行 `python md_to_pdf.py test.md output.pdf`
3. 检查 PDF 中的中文是否显示正常

## 关联 Issue
Closes #123

## 检查清单
- [x] 代码遵循项目风格
- [x] 包含代码注释
- [x] 已更新相关文档
- [x] 通过了测试
```

---

## 📋 代码审查标准

PR 会根据以下标准进行审查：

### 功能完整性
- [ ] 功能实现完整，达到预期目标
- [ ] 处理了边界情况和错误
- [ ] 没有引入新的 bug

### 代码质量
- [ ] 代码清晰易读，遵循命名规范
- [ ] 有必要的注释和文档字符串
- [ ] 避免重复代码，复用现有工具函数
- [ ] 性能合理，没有明显的优化空间

### 测试覆盖
- [ ] 添加了单元测试（如适用）
- [ ] 所有现有测试仍然通过
- [ ] 测试覆盖了主要的代码路径

### 文档完整性
- [ ] 更新了 README 或其他相关文档
- [ ] 代码注释清晰准确
- [ ] 如有 API 变化，文档已同步

---

## 🧪 测试

### 运行测试

```bash
# 运行所有测试
pytest

# 运行特定测试文件
pytest tests/test_pdf_generation.py

# 带覆盖率的测试
pytest --cov=hv_skills tests/
```

### 编写测试

示例：

```python
import pytest
from hv_skills.scripts.md_to_pdf import md_to_html

def test_md_to_html_basic():
    """测试基础 Markdown 到 HTML 的转换"""
    md_content = "# 标题\n\n这是正文。"
    html = md_to_html(md_content, title="测试标题")
    
    assert "测试标题" in html
    assert "<h1>" in html
    assert "这是正文" in html

def test_md_to_html_with_author():
    """测试带作者信息的 HTML 生成"""
    md_content = "# 标题"
    html = md_to_html(md_content, author="张三")
    
    assert "张三" in html

def test_md_to_html_empty_author():
    """测试不显示空作者"""
    md_content = "# 标题"
    html = md_to_html(md_content, author="")
    
    assert "研究者:" not in html or "研究者: </div>" in html
```

---

## 📚 资源

### 项目文档
- [README.md](README.md) - 项目概览
- [hv-skills/SKILL.md](hv-skills/SKILL.md) - 纵横双轴分析 Skill 文档
- [REFACTOR_SUMMARY.md](REFACTOR_SUMMARY.md) - 最近改造总结

### 技术参考
- [WeasyPrint 文档](https://doc.courtbouillon.org/weasyprint/)
- [Python Markdown 文档](https://python-markdown.github.io/)
- [PEP 8 Python 风格指南](https://www.python.org/dev/peps/pep-0008/)
- [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

---

## ❓ 常见问题

**Q: 我是新贡献者，该从哪里开始？**
A: 
1. 查看 [Issues](https://github.com/yourrepo/Ethan-skills/issues) 找一个标记为 `good-first-issue` 的任务
2. 在 Issue 下评论表明你想要处理它
3. Fork 项目并按照上面的流程提交 PR

**Q: 提交 PR 后多久会被审查？**
A: 通常在 1-3 天内会有人审查。如果没有及时反馈，可以在 PR 下留言提醒。

**Q: 代码风格有什么工具可以自动检查？**
A: 你可以使用：
- `black` - 代码格式化
- `flake8` - 风格检查
- `pylint` - 代码分析

```bash
pip install black flake8 pylint

# 格式化代码
black hv_skills/

# 检查风格
flake8 hv_skills/
```

**Q: 我的改动影响很大，应该先讨论吗？**
A: 对于大的改动（如重构整个模块、改变 API），建议先创建一个讨论 Issue，获得维护者的反馈后再实施。

---

## 📞 联系方式

- 创建 GitHub Issue
- 提交讨论主题
- 发送邮件（待补充）

---

感谢你的贡献！🎉
