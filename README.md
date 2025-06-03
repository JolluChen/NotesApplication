# Notes - A Modern Note-Taking Application
# Notes 笔记应用

A modern note-taking application that supports rich text editing, Markdown syntax, real-time preview, and note drag-and-drop sorting functionality.

一个正在尝试的笔记应用，支持富文本编辑、Markdown语法、实时预览、笔记拖拽排序等功能。

## Features
## 功能特性

- ✨ Rich text editing with Markdown syntax support
- 🔄 Note drag-and-drop sorting
- 💾 Auto-save functionality
- 🎨 Clean and modern interface

- ✨ 富文本编辑与Markdown语法支持
- 🔄 笔记拖拽排序
- 💾 自动保存
- 🎨 简洁现代的界面

## Documentation
## 文档资源
For detailed update history, please check:
完整的更新历史请查看：

- [CHANGELOG.md](docs/CHANGELOG.md) (Bilingual / 双语)
- [CHANGELOG_CN.md](docs/CHANGELOG_CN.md) (Chinese / 中文)
- [CHANGELOG_EN.md](docs/CHANGELOG_EN.md) (English / 英文)

For deployment instructions, please check:
部署说明请查看：

- [DEPLOY_UBUNTU.md](docs/DEPLOY_UBUNTU.md) - Ubuntu Deployment Guide / Ubuntu部署指南
- [DOCKER_DEPLOY.md](docs/DOCKER_DEPLOY.md) - Docker Deployment Guide / Docker部署指南

Additional documentation resources:
其他文档资源：

- [ERROR_LOG.md](docs/ERROR_LOG.md) - Common Error Solutions / 常见错误解决方案
- [icons_summary.md](docs/icons_summary.md) - Icon Usage Summary / 图标使用概览
- [git-operations.md](docs/git-operations.md) - Git Operation Guide / Git操作指南
- [Unfinished_Features.md](docs/Unfinished_Features.md) - Unfinished Features List / 未完成功能清单

## How to Run
## 如何运行

1. Start backend server:<br>启动后端服务器：
```bash
python app.py
```

2. Enter the `frontend` directory then start the frontend application:<br>先进入 `frontend` 目录再启动前端应用：
```bash
cd frontend
npm run dev
```

3. Open browser and visit:<br>打开浏览器访问：
http://localhost:5173

## External Network Access (Testing Environment)
## 外网访问配置（测试环境）

To access the application from external networks, follow these steps:
要从外网访问应用程序，请按照以下步骤操作：

### 1. Network Configuration / 网络配置

**Windows Firewall Configuration:**
**Windows防火墙配置：**

```powershell
# Allow Flask port (5000) through firewall
# 允许Flask端口(5000)通过防火墙
netsh advfirewall firewall add rule name="Flask App Port 5000" dir=in action=allow protocol=TCP localport=5000

# Allow Frontend port (5173) through firewall  
# 允许前端端口(5173)通过防火墙
netsh advfirewall firewall add rule name="Vite Dev Server Port 5173" dir=in action=allow protocol=TCP localport=5173
```

### 2. Get Your IP Address / 获取IP地址

```powershell
# Get your local IP address
# 获取本机IP地址
ipconfig
```

### 3. Update Frontend Configuration / 更新前端配置

Edit `frontend/.env` file and replace `localhost` with your actual IP:
编辑 `frontend/.env` 文件，将 `localhost` 替换为您的实际IP：

```env
# Replace YOUR_EXTERNAL_IP with your actual IP address
# 将 YOUR_EXTERNAL_IP 替换为您的实际IP地址
VITE_API_URL=http://YOUR_EXTERNAL_IP:5000/api

# Example / 示例：
# VITE_API_URL=http://192.168.1.100:5000/api
```

### 4. Router Port Forwarding (If Behind Router) / 路由器端口转发（如果在路由器后面）

If your computer is behind a router, configure port forwarding in your router's admin panel:
如果您的电脑在路由器后面，需要在路由器管理界面设置端口转发：

- **Internal IP / 内部IP:** Your computer's LAN IP / 您电脑的局域网IP
- **Internal Port / 内部端口:** 5000 (Backend) and 5173 (Frontend) / 5000（后端）和5173（前端）
- **External Port / 外部端口:** 5000 and 5173 (or custom ports) / 5000和5173（或自定义端口）
- **Protocol / 协议:** TCP

### 5. Access from External Networks / 外网访问

After configuration, you can access the application using:
配置完成后，您可以使用以下地址访问应用：

- **Backend API:** `http://YOUR_IP:5000`
- **Frontend App:** `http://YOUR_IP:5173`

### 6. Testing Configuration / 测试配置

To verify external access is working:
要验证外网访问是否正常工作：

```powershell
# Test backend API health check
# 测试后端API健康检查
curl http://YOUR_IP:5000/api/health

# Or use browser to test
# 或使用浏览器测试
# http://YOUR_IP:5000/api/health
```

**⚠️ Security Warning / 安全警告:**
- This configuration is for **testing environments only**
- 此配置**仅适用于测试环境**
- Do not use in production without proper security measures
- 生产环境请勿在没有适当安全措施的情况下使用
- Consider adding authentication and HTTPS for production use
- 生产环境建议添加认证和HTTPS

### Network Access Troubleshooting / 网络访问故障排除

**Common Issues and Solutions / 常见问题与解决方案:**

1. **Cannot access from external network / 无法从外网访问:**
   - Check firewall settings / 检查防火墙设置
   - Verify router port forwarding / 验证路由器端口转发
   - Ensure applications are running with correct host configuration / 确保应用以正确的主机配置运行

2. **CORS errors in browser / 浏览器CORS错误:**
   - Backend CORS is already configured to allow all origins for testing
   - 后端CORS已配置为测试环境允许所有来源
   - Make sure frontend is accessing the correct backend URL
   - 确保前端访问正确的后端URL

3. **Application not starting with 0.0.0.0 / 应用无法以0.0.0.0启动:**
   - Check if ports 5000 and 5173 are already in use
   - 检查端口5000和5173是否已被占用
   - Use `netstat -an | findstr :5000` and `netstat -an | findstr :5173` to check
   - 使用命令检查端口占用情况

## Technology Stack
## 技术栈

### Frontend
### 前端

- React 18.2.0
- Material-UI (MUI) 5.13.0
- TipTap Editor 2.11.5
- React Beautiful DnD 13.1.1
- Axios 1.4.0
- Vite 4.3.5

### Backend
### 后端

- Flask 2.0.1
- Flask-CORS 3.0.10
- SQLAlchemy 1.4.23
- Flask-SQLAlchemy 2.5.1
- SQLite

## Installation
## 安装说明

### Backend Setup
### 后端设置

1. Install Python dependencies:<br>安装Python依赖：
```bash
pip install -r requirements.txt
```

2. Run Flask server:<br>运行Flask服务器：
```bash
python app.py
```
Server will start at http://127.0.0.1:5000
服务器将在 http://127.0.0.1:5000 启动

### Frontend Setup
### 前端设置

1. Enter frontend directory:<br>进入前端目录：
```bash
cd frontend
```

2. Install Node.js dependencies:<br>安装Node.js依赖：
```bash
npm install
```

3. Start development server:<br>启动开发服务器：
```bash
npm run dev
```
Application will start at http://localhost:5173
应用将在 http://localhost:5173 启动

## Usage Guide
## 使用说明

1. Create note: Click the "+" button in the top right corner
2. Edit note: Input directly in the text area, supporting rich text editing and Markdown syntax
3. Format conversion: Convert notes to different formats (text, headings, lists, quotes, etc.) via right-click menu
4. Sort: Drag notes using the handle on the left to adjust order
5. Delete: Click the delete icon in the top right corner of the note or use the right-click menu

1. 创建笔记：点击右上角的"+"按钮
2. 编辑笔记：直接在文本区域输入，支持富文本编辑和Markdown语法
3. 格式转换：可以通过右键菜单将笔记转换为不同格式（文本、标题、列表、引用等）
4. 排序：通过左侧拖动手柄拖拽笔记调整顺序
5. 删除：点击笔记右上角的删除图标或使用右键菜单

## Development Features
## 开发特性

- React Hooks for state management
- TipTap editor integration for rich text editing and Markdown syntax
- Debounce optimization for improved input performance
- RESTful API design
- SQLite data persistence
- Real-time note saving
- Custom drag-and-drop sorting implementation
- Support for multiple note formats (text, headings, lists, quotes, etc.)

- 使用React Hooks进行状态管理
- 集成TipTap编辑器，支持富文本编辑和Markdown语法
- 实现了防抖优化，提升输入性能
- RESTful API设计
- SQLite数据持久化
- 支持笔记实时保存
- 自定义拖拽排序实现
- 支持多种笔记格式（文本、标题、列表、引用等）

## Project Structure
## 项目结构

```
NotesApplication/
├── .dockerignore          # Docker ignore configuration / Docker忽略配置
├── .gitignore             # Git ignore configuration / Git忽略配置
├── Dockerfile             # Docker configuration for backend / 后端Docker配置文件
├── LICENSE                # License file / 许可证文件
├── README.md              # Project main documentation (this file) / 项目主文档 (本文档)
├── app.py                 # Flask backend application entry / Flask后端应用入口
├── docker-compose.yml     # Docker Compose configuration / Docker Compose配置文件
├── package-lock.json      # Node.js lock file for root / 根目录Node.js锁定文件
├── package.json           # Node.js dependencies for root (e.g., for tools) / 根目录Node.js依赖 (例如用于工具脚本)
├── requirements.txt       # Python dependencies / Python依赖
├── app/                   # Backend application main directory / 后端应用主目录
│   ├── __init__.py        # Package initialization and app factory / 包初始化和应用工厂
│   ├── api/               # API routes module / API路由模块
│   │   ├── __init__.py    # Routes package initialization / 路由包初始化
│   │   ├── files.py       # File routes / 文件路由
│   │   ├── folders.py     # Folder routes / 文件夹路由
│   │   ├── health.py      # Health check routes / 健康检查路由
│   │   └── notes.py       # Note routes / 笔记路由
│   ├── config/            # Configuration module / 配置模块
│   │   ├── __init__.py    # Config package initialization / 配置包初始化
│   │   └── config.py      # Configuration definitions / 配置定义
│   ├── extensions.py      # Extensions instantiation / 扩展实例化
│   ├── models/            # Database models / 数据库模型
│   │   ├── __init__.py    # Models package initialization / 模型包初始化
│   │   ├── folder.py      # Folder model / 文件夹模型
│   │   ├── note.py        # Note model / 笔记模型
│   │   └── note_file.py   # Note file model / 笔记文件模型
│   ├── services/          # Business logic services (currently empty) / 业务逻辑服务 (当前为空)
│   │   └── __init__.py    # Services package initialization / 服务包初始化
│   └── utils/             # Utility functions / 工具函数
│       └── __init__.py    # Utils package initialization / 工具包初始化
├── docs/                  # Documentation directory / 文档目录
│   ├── CHANGELOG.md       # Bilingual changelog / 双语更新日志
│   ├── CHANGELOG_CN.md    # Chinese changelog / 中文更新日志
│   ├── CHANGELOG_EN.md    # English changelog / 英文更新日志
│   ├── DEPLOY_UBUNTU.md   # Ubuntu deployment guide / Ubuntu部署指南
│   ├── DOCKER_DEPLOY.md   # Docker deployment guide / Docker部署指南
│   ├── ERROR_LOG.md       # Error logging and solutions / 错误日志与解决方案
│   ├── OnePage_Propsal_EN.md # 英文提案
│   ├── PPT_Content_Description.md # PPT内容描述
│   ├── PPT_Outline.md     # PPT大纲
│   ├── README_CN.md       # Chinese README / 中文README
│   ├── README_EN.md       # English README / 英文README
│   ├── Unfinished_Features.md # 未完成功能清单
│   ├── git-operations.md  # Git operation guide / Git操作指南
│   └── icons_summary.md   # Icons usage summary / 图标使用汇总
├── frontend/              # Frontend application (React + Vite) / 前端应用 (React + Vite)
│   ├── .env.development   # Development environment variables / 开发环境变量
│   ├── Dockerfile         # Docker configuration for frontend / 前端Docker配置文件
│   ├── index.html         # HTML entry point / HTML入口文件
│   ├── nginx.conf         # Nginx configuration for Docker deployment / Docker部署Nginx配置
│   ├── package-lock.json  # Node.js lock file / Node.js锁定文件
│   ├── package.json       # Node.js dependencies / Node.js依赖
│   ├── vite.config.js     # Vite configuration / Vite配置文件
│   └── src/               # Source code / 源代码
│       ├── App.jsx        # Main application component / 主应用组件
│       ├── components/    # Reusable UI components / 可复用UI组件
│       ├── hooks/         # Custom React hooks / 自定义React钩子
│       ├── index.css      # Global styles / 全局样式
│       ├── main.jsx       # Application entry point / 应用入口文件
│       ├── services/      # API interaction services / API交互服务
│       └── utils/         # Utility functions / 工具函数
├── tests/                 # Test files / 测试文件
│   └── test_app.py        # Backend application tests / 后端应用测试
└── tools/                 # Utility scripts / 工具脚本
    └── sync_docs.py       # Script to sync documentation / 文档同步脚本
```
*(Note: `notes.db` and `app_debug.log` are omitted as they are typically generated or gitignored)*
*(注意: `notes.db` 和 `app_debug.log` 文件被省略，因为它们通常是生成文件或被git忽略)*

## Development Plans
## 开发计划

### Optimizations
### 优化功能

- [x] Optimize adaptive width display of note blocks in the page
- [x] Optimize editing functionality with rich text editing and Markdown syntax
- [ ] Further optimize TipTap editor performance and user experience

- [x] 优化笔记块在页面内的自适应宽度显示
- [x] 优化编辑功能，支持富文本编辑和Markdown语法
- [ ] 进一步优化TipTap编辑器的性能和用户体验

### New Features
### 新增功能

- [x] Support multiple note formats (text, headings, lists, quotes, etc.)
- [x] Add note folder creation functionality in the left sidebar
- [ ] Add user authentication system
- [ ] Support note tags and categories
- [ ] Add note search functionality
- [ ] Support image upload and management
- [ ] Add note sharing functionality
- [ ] Support dark mode

- [x] 支持多种笔记格式（文本、标题、列表、引用等）
- [x] 新增左侧建立笔记文件夹功能
- [ ] 添加用户认证系统
- [ ] 支持笔记标签和分类
- [ ] 添加笔记搜索功能
- [ ] 支持图片上传和管理
- [ ] 添加笔记分享功能
- [ ] 支持深色模式

## Contribution Guide
## 贡献指南

Issues and Pull Requests are welcome!
欢迎提交Issue和Pull Request！

## License
## 许可证

Apache License 2.0
Apache 许可证 2.0 版本
