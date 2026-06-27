# 变更日志

所有重要的项目变化都会在这个文件中记录。

格式基于 [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)，
遵循 [语义化版本](https://semver.org/lang/zh-CN/)。

## [Unreleased]

### 计划中
- 添加单元测试套件
- 支持 Word 格式导出
- 国际化支持（英文、日文等）
- 优化大文件 PDF 转换性能

---

## [1.0.0] - 2026-06-27

### 添加

- ✨ **新功能**：纵横双轴分析 Skill (`hv-analysis`)
  - 完整的深度研究框架文档
  - Python 脚本支持 Markdown 转 PDF
  - 自动化的 PDF 排版方案
  - 支持自定义作者署名

- 📄 **项目文件**
  - `.gitignore` - 完整的 Git 忽略规则
  - `.editorconfig` - 统一的编辑器配置
  - `CONTRIBUTING.md` - 详细的贡献指南
  - `requirements.txt` - 项目依赖
  - `requirements-dev.txt` - 开发依赖
  - `LICENSE` - MIT 许可证
  - GitHub Issues/PR 模板

- 📚 **文档**
  - 完善的 `README.md`
  - 项目改造总结 `REFACTOR_SUMMARY.md`
  - 数据框架 `schema.json`

### 改动

- ♻️ **重构**：将 hv-skills 改造为独立、原创的框架
  - 移除所有个人署名相关内容
  - 强调学术基础（语言学、社会科学、商学院、竞争战略）
  - 支持用户自定义作者署名
  - 核心方法论 100% 保留

### 修复

- 🐛 作者签名参数化（可选，支持用户自定义）
- 📄 PDF 副标题一致性

---

## 版本说明

### [1.0.0]

- **发布日期**：2026-06-27
- **状态**：稳定版本
- **主要特性**：纵横双轴分析 Skill，完整的项目配置

---

## 贡献者

感谢以下贡献者的支持：

- Claude Code - 初始开发和改造

---

## 许可证

本项目采用 MIT 许可证。详见 [LICENSE](LICENSE) 文件。
