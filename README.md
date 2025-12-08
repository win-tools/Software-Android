# 安卓逆向

欢迎查看本项目，这是一个专注于安卓逆向工程的工具集合。

## 项目简介

本项目提供了多种工具和资源，方便进行安卓应用程序的逆向分析。主要包含以下组件：

- **APKDB**: 用于 APK 文件的解包、打包、签名等操作。
- **JEB**: 强大的反编译与逆向分析工具，支持多种平台与文件格式。
- **QtScrcpy**: 用于安卓设备屏幕投射和控制的工具。
- **其他工具**: 包括 ADB、Fastboot、Signer、XML 编辑器等实用工具。

## 目录结构说明

- `APKDB/`: 包含 APK 解包、打包、签名等工具。
- `jeb/`: 提供 JEB 逆向工程工具及其相关插件、脚本、文档。
- `QtScrcpy/`: 包含 QtScrcpy 的相关依赖和可执行文件。
- `jadx/`: 包含 JADX 及其依赖库，用于 Android APK 的反编译。

## 工具介绍

### APKDB
用于 APK 文件的分析、解包、重新打包和签名等操作。包含以下主要工具：

- `ApkTool.exe`: APK 解包和打包工具。
- `Signer`: 用于 APK 的签名工具。
- `ADB`: Android Debug Bridge 工具，用于设备调试。
- `AndXml`: XML 编辑工具，用于编辑 Android 资源文件。

### JEB
JEB 是一个专业的逆向工程平台，支持 Android APK、DEX、原生代码、PDF、以太坊智能合约等多种格式的分析。

- 支持脚本扩展，可通过 Python 或 Java 编写插件。
- 提供详细的文档与示例脚本。
- 支持调试、反编译、符号解析等功能。

### QtScrcpy
用于将安卓设备的屏幕投射到电脑上，并进行鼠标和键盘控制。适用于逆向调试时实时查看设备操作。

### JADX
用于将 Android APK 文件反编译为 Java 源代码，支持图形界面操作。

- `jadx-gui`: 图形界面反编译工具。
- `jadx`: 命令行工具，支持批量反编译。

## 使用说明

### 安装步骤

1. 下载项目并解压。
2. 根据操作系统选择对应的工具运行：
   - Windows: 可直接运行 `jeb_wincon.bat` 或 `APKDB/Setup.exe`。
   - Linux: 使用 `jeb_linux.sh` 启动 JEB。
   - macOS: 使用 `jeb_macos.sh` 启动 JEB。
3. 使用 `jadx/jadx-gui-1.5.1.exe` 运行 JADX 反编译工具。

### 主要功能

- **APK 解包与重打包**: 使用 `ApkTool` 可对 APK 文件进行资源提取与重新打包。
- **签名**: 使用 `Signer` 工具对重打包后的 APK 进行签名。
- **反编译**: 使用 `JADX` 或 `JEB` 将 APK/Dex 文件反编译为 Java 代码。
- **调试**: 使用 JEB 的调试功能进行动态调试，支持断点、内存查看等功能。
- **脚本扩展**: 使用 JEB 提供的脚本 API 编写自定义分析脚本（Python/Java）。

## 文档资源

- `jeb/doc/manual/`: 包含 JEB 使用手册，涵盖调试、反编译、插件开发等内容。
- `jadx/README.md`: JADX 的使用说明和构建方法。

## 脚本开发

JEB 支持通过脚本扩展其功能，脚本目录位于 `jeb/scripts/samples/`。以下是一些常见脚本示例：

- `DecompileFile.py`: 对文件进行反编译。
- `ListUnits.py`: 列出所有解析的单元。
- `ASTReplStringsTest.py`: 操作 Java AST 树，替换字符串。
- `AndroidDbgCreate.py`: 创建 Android 调试会话。

## 插件开发

JEB 提供了丰富的插件开发接口，支持自定义解析器、前端界面、引擎插件等。

- `jeb/doc/manual/dev/`: 包含插件开发的详细教程。
- `jeb/coreplugins/`: 示例插件目录，可参考其结构进行开发。

## 许可证

本项目中所使用的第三方工具可能遵循各自的许可证，请参考对应目录下的 `LICENSE` 文件。

---

如需进一步了解每个工具的使用方法，可查阅对应目录下的文档或示例。欢迎贡献代码或提出改进建议！