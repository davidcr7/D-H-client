# HTTP Client Desktop Application

一个功能完整的HTTP客户端桌面应用，基于Electron构建。

## 功能特性

- ✅ 支持输入HTTP请求（URL、Method、Headers、Params、Body）
- ✅ 支持从剪贴板解析cURL命令
- ✅ 发送请求并展示响应
- ✅ 响应JSON以树状结构展示（保留所有key+value）
- ✅ 显示原始响应文本
- ✅ 支持主题切换（多种背景色可选）
- ✅ Body JSON实时校验 + 高亮

## 安装和运行

### 前置要求
- Node.js (v14或更高版本)
- npm

### 安装依赖
```bash
npm install
```

### 运行应用
```bash
npm start
```

或者使用启动脚本：
```bash
./start.sh
```

### 开发模式
```bash
npm run dev
```

## 使用说明

### 基本请求
1. 选择HTTP方法（GET、POST、PUT等）
2. 输入请求URL
3. 添加Headers（可选）
4. 添加Query参数（可选）
5. 设置请求Body（可选）
6. 点击"发送"按钮

### cURL解析
1. 复制cURL命令到剪贴板
2. 点击"解析cURL"按钮或使用快捷键 Ctrl+Shift+V
3. 应用会自动填充URL、Headers和Body

### 主题切换
- 点击"切换主题"按钮在不同主题间切换
- 支持亮色、暗色和蓝色主题

### JSON验证
- 当选择JSON Body类型时，应用会实时验证JSON格式
- 有效的JSON会显示绿色验证标记
- 无效的JSON会显示红色错误标记

### 响应查看
- **Preview标签**: 以树状结构查看JSON响应
- **Raw标签**: 查看原始响应文本
- 显示HTTP状态码和响应时间

## 快捷键

- `Ctrl+N`: 新建请求
- `Ctrl+Shift+V`: 解析剪贴板中的cURL
- `Ctrl+T`: 切换主题
- `Ctrl+R`: 重新加载应用

## 项目结构

```
src/
├── main.js              # 主进程
├── preload.js           # 预加载脚本
├── request-handler.js   # 请求处理逻辑
├── renderer/
│   ├── index.html       # 界面HTML
│   └── app.js           # 渲染进程逻辑
└── styles/
    └── main.css         # 样式文件
```

## 技术栈

- **Electron**: 桌面应用框架
- **Axios**: HTTP客户端库
- **Vanilla JavaScript**: 前端逻辑
- **CSS3**: 样式和主题系统

## 构建

```bash
npm run build
```

## 许可证

MIT License