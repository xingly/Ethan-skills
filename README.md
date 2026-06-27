# Ethan-skills

> 一个为 Claude Code 开发的高级 Skills 集合，包含深度研究和分析工具。

## 📋 项目概览

本项目是一个 Claude Code 自定义 Skills 开发库，包含专业级的分析框架和生成工具。

### 当前 Skills

#### 1. **纵横双轴分析法** (`hv-analysis`)

一个融合语言学、社会科学、商学院案例研究和竞争战略分析的系统化深度研究框架。

**核心能力：**
- 📊 双轴分析：纵轴追踪生命历程，横轴对标竞品
- 📝 学术级报告生成：自动生成排版精美的PDF研究报告
- 🔍 多维度对比分析：系统性地研究产品、公司、概念或人物
- 🎨 专业排版：内置CSS样式方案，支持中英文混排

**适用场景：**
- 深度研究产品演进与竞争格局
- 分析公司战略与商业模式
- 研究技术概念与创新范式
- 评估人物影响力与职业轨迹

**输出格式：**
- 高质量 PDF 研究报告（10,000-30,000字）
- 清晰的逻辑结构：纵向发展 → 横向对比 → 交汇洞察
- 专业的排版和易读的叙事风格

---

## 🚀 快速开始

### 系统要求

- Python 3.7+
- 依赖包：`weasyprint`、`markdown`

### 安装依赖

```bash
pip install weasyprint markdown --break-system-packages
```

### 使用示例

#### 纵横双轴分析

```bash
# 使用脚本生成PDF报告
python hv-skills/scripts/md_to_pdf.py research.md output.pdf \
  --title "研究对象名称" \
  --author "研究者名称"
```

**参数说明：**
- `research.md`：Markdown 格式的研究报告
- `output.pdf`：输出的PDF文件路径
- `--title`：报告标题（会用于封面和页眉）
- `--author`：作者/研究者名称（可选，省略则不显示）

#### 报告写作指南

详见 `hv-skills/SKILL.md`，包含：
- 前置准备和环境设置
- 五步研究流程指导
- 信息收集策略
- 纵向分析方法
- 横向对标方法
- 深度报告的写作特征
- PDF生成和排版说明

---

## 📂 项目结构

```
Ethan-skills/
├── README.md                           # 项目说明文档
├── REFACTOR_SUMMARY.md                 # 重构改造总结
├── .gitignore                          # Git 忽略规则
├── .editorconfig                       # 编辑器配置
│
└── hv-skills/                          # 纵横双轴分析 Skill
    ├── SKILL.md                        # Skill 完整文档
    ├── references/
    │   └── schema.json                 # 数据框架定义
    └── scripts/
        └── md_to_pdf.py                # PDF 生成脚本
```

---

## 🛠️ 开发指南

### 代码风格

本项目使用 `.editorconfig` 规范代码风格：
- Python: 4 空格缩进，最大行长 120 字符
- Markdown: 2 空格缩进
- JSON: 2 空格缩进

### Git 工作流

```bash
# 创建功能分支
git checkout -b feature/your-feature-name

# 提交更改（遵循 conventional commits）
git commit -m "feat: 添加新的Skill"
git commit -m "fix: 修复PDF生成问题"
git commit -m "docs: 更新文档"

# 推送到远程
git push origin feature/your-feature-name
```

### 提交规范

使用 Conventional Commits 格式：
- `feat:` 新功能
- `fix:` 缺陷修复
- `docs:` 文档更新
- `refactor:` 代码重构
- `test:` 测试相关
- `chore:` 构建、依赖更新等

---

## 📝 最近更新

### v1.0 - 2026-06-27

✅ **项目完善**
- 添加完整的 `.gitignore` 文件
- 添加 `.editorconfig` 编辑器配置
- 更新和扩展 README 文档

✅ **hv-analysis Skill 改造**
- 移除所有个人署名相关内容
- 改造为独立、原创的学术框架
- 支持用户自定义作者署名
- 完整的方法论和功能保留

---

## 📄 文件说明

| 文件 | 说明 |
|------|------|
| `.gitignore` | Git 忽略规则，用于管理不需要版本控制的文件 |
| `.editorconfig` | 编辑器配置，统一代码风格 |
| `REFACTOR_SUMMARY.md` | 详细的项目改造总结和验证报告 |
| `hv-skills/SKILL.md` | 纵横双轴分析 Skill 的完整文档 |
| `hv-skills/references/schema.json` | 数据框架和分析结构定义 |
| `hv-skills/scripts/md_to_pdf.py` | Markdown 转 PDF 生成脚本 |

---

## 🔄 更新和改进

### 已知的未来计划

- [ ] 添加 Skill 的单元测试
- [ ] 支持更多的输出格式（HTML、Word 等）
- [ ] 添加国际化支持（英文、日文等）
- [ ] 优化 PDF 生成性能
- [ ] 扩展数据框架支持更多分析维度

---

## 📞 支持和反馈

如有问题或建议，欢迎通过以下方式反馈：
- 创建 GitHub Issue
- 提交 Pull Request
- 发送讨论信息

---

## 📄 许可证

本项目开源发布。具体许可证信息待补充。

---

## 🙏 致谢

感谢所有贡献者和使用者的支持。

---

*最后更新: 2026-06-27*