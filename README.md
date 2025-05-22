# LaunchBox

一个用于快速启动和管理各类工具的图形化工具箱，支持多种类型工具的统一管理和快速启动。
<img width="850" alt="image" src="https://github.com/user-attachments/assets/46522e6e-8272-49b4-a73e-74525a627afc" />



## 功能特点

- 支持多种工具类型：
  - macOS 应用程序 (.app)
  - Java JAR 程序
  - Python 脚本
  - 可执行程序
  - shell 脚本
- 支持工具分类管理
- 支持环境配置管理（Java/Python）
- 支持模糊搜索工具
- 支持自定义启动命令
- macOS 下优先使用 iTerm2 终端（如果安装）

## 环境要求

- 支持的操作系统：
  - macOS
  - Linux
  - Windows
- 如果运行 JAR 文件需要 Java 环境
- 如果运行 Python 脚本需要 Python 环境

## 使用说明
**注意：如果是直接使用 可执行程序 和 EXE ，请先创建一个空的config.yaml文件再运行**

### 环境配置

1. 切换到"环境配置"标签页
2. 可以配置 Java 和 Python 环境：
   - Java 环境：配置 Java 可执行文件路径（如：/usr/bin/java）
   - Python 环境：配置 Python 解释器路径（如：/usr/bin/python3）
<img width="850" alt="image" src="https://github.com/user-attachments/assets/ccaab239-c02a-487b-a699-d5afe06a9323" />



### 工具分类管理

1. 在"环境配置"标签页的"工具分类"选项卡中
2. 可以添加、编辑、删除工具分类
3. 分类用于对工具进行归类管理
<img width="850" alt="image" src="https://github.com/user-attachments/assets/b3d011a5-2c48-41b1-9321-dccd5341dc46" />



### 添加工具

1. 在主界面点击"添加工具"按钮
2. 填写工具信息：
   - 名称：工具的显示名称
   - 类型：选择工具类型（app/jar/python/executable）
   - 路径：工具的完整路径
   - 环境：选择运行环境（仅 jar/python 类型需要）
   - 完整命令：自定义启动命令（可选）
   - 分类：选择工具分类


<img width="850" alt="image" src="https://github.com/user-attachments/assets/a680b583-94e4-4f6f-91cc-6203d8a26ab1" />



### 完整命令模板说明

不同类型工具支持不同的命令模板：

1. JAR 文件：
   - 默认模板：`环境 -javaagent:"路径" -jar "路径"`
   - "环境"会被替换为选择的 Java 环境路径
   - "路径"会被替换为 JAR 文件路径

2. Python 脚本：
   - 默认模板：`环境 "路径"`
   - "环境"会被替换为选择的 Python 环境路径
   - "路径"会被替换为 Python 脚本路径

3. 可执行程序：
   - 默认：直接执行程序
   - 可以通过完整命令自定义启动参数，如：`路径 -h`
   - "路径"会被替换为程序的实际路径

### 工具管理

- 搜索：在搜索框输入关键字可以快速查找工具
- 编辑：右键点击工具可以编辑工具信息
- 删除：右键点击工具可以删除工具
<img width="800" alt="image" src="https://github.com/user-attachments/assets/2a5d32b1-9d20-4205-858d-54f705353d68" />


## 配置文件

配置信息存储在 `config.yaml` 文件中，包含：
- 环境配置
- 工具分类
- 工具信息

## 注意事项

1. 路径建议使用绝对路径
2. JAR 和 Python 工具需要先配置对应的环境
3. 在 macOS 中如果安装了 iTerm2，会优先使用 iTerm2 打开终端
4. 可执行程序和 Python 脚本会在新的终端窗口中运行

## 贡献

欢迎提交 Issue 和 Pull Request！
