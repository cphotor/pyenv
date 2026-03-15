# uv-init

一个增强版的 Python 项目初始化脚本，基于 `uv` 工具，自动添加开发环境配置。

## 功能特性

- 🚀 基于 `uv init` 快速创建 Python 项目
- 📚 支持库项目布局（`--lib` 选项）
- 🐍 支持指定 Python 版本（`--python` 选项）
- ⚙️ 自动配置 Ruff（代码格式化和检查）
- 📝 自动配置 Pyright（类型检查）
- 💻 自动配置 VS Code 设置
- 🎯 一键设置完整的开发环境

## 安装

1. 下载脚本：
```bash
curl -O https://raw.githubusercontent.com/yourusername/uv-init/main/uv-init
```

2. 添加执行权限：
```bash
chmod +x uv-init
```

3. 移动到系统路径（可选）：
```bash
mv uv-init ~/.local/bin/
```

## 使用方法

### 基本用法

```bash
# 创建普通 Python 项目
uv-init my-project

# 创建库项目
uv-init --lib my-library

# 指定 Python 版本
uv-init --python 3.11 my-project

# 组合使用
uv-init --lib --python 3.12 my-awesome-lib
```

### 命令行选项

- `--lib`: 创建库项目布局（src 目录结构）
- `--python <version>`: 指定 Python 版本
- `--help, -h`: 显示帮助信息

## 自动配置的内容

### 1. VS Code 配置 (`.vscode/settings.json`)
- 配置 Python 虚拟环境路径
- 启用保存时格式化
- 设置 Ruff 为默认格式化工具
- 配置保存时自动整理导入和修复问题

### 2. Pyright 配置 (`pyrightconfig.json`)
- 设置 Python 版本
- 标准类型检查模式
- 优化的错误报告配置

### 3. Ruff 配置 (追加到 `pyproject.toml`)
- 代码行长度限制：88 字符
- 目标 Python 版本：自动检测
- 全面的代码检查规则
- 自动修复所有可修复的问题

## 示例

创建一个名为 `my-app` 的项目：

```bash
uv-init my-app
cd my-app
```

这将创建：
- 完整的 Python 项目结构
- 配置好的开发环境
- 可以直接开始编码的环境

## 依赖要求

- [uv](https://github.com/astral-sh/uv): Python 包管理工具
- Python 3.8+（推荐 3.11+）

## 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

## 贡献

欢迎提交 Issue 和 Pull Request！

## 为什么选择这个脚本？

标准的 `uv init` 只创建基本的项目结构，这个脚本在此基础上：

1. **开箱即用**：无需手动配置开发环境
2. **最佳实践**：预设了现代 Python 开发的最佳配置
3. **工具集成**：完美集成 VS Code、Ruff、Pyright
4. **灵活配置**：支持不同类型的项目和 Python 版本

让您专注于编码，而不是环境配置！
