# Changelog / 更新日志

## [0.0.5] - 2025-03-30

### New Features / 新功能
- Editor Framework Upgrade
  - Migrated from ReactMarkdown to TipTap Editor
  - Implemented enhanced rich text editing capabilities
  - Optimized editor performance and stability
  - Provided improved real-time preview experience
- 升级编辑器框架
  - 从ReactMarkdown迁移至TipTap Editor
  - 实现更强大的富文本编辑功能
  - 优化编辑器性能和稳定性
  - 提供更好的实时预览体验

- Enhanced Markdown Rendering
  - Added inline Markdown syntax real-time rendering
  - Supported more Markdown extension syntax
  - Optimized rendering performance and display effects
  - Provided more intuitive editing experience
- 增强Markdown渲染能力
  - 新增行内Markdown语法实时渲染
  - 支持更多Markdown扩展语法
  - 优化渲染性能和显示效果
  - 提供更直观的编辑体验

- Enhanced Note Block Features
  - Added note block quick action toolbar
  - Supported quick note content copying
  - Implemented note block deletion functionality
  - Provided multiple format conversion options
  - Optimized note block management experience
- 新增笔记块功能增强
  - 添加笔记块快捷操作菜单栏
  - 支持笔记内容快速复制
  - 实现笔记块删除功能
  - 提供多种格式转换选项
  - 优化笔记块管理体验

### Optimizations / 优化
- Interaction Experience Optimization
  - Implemented quick note block creation with Enter key
  - Optimized transition animations between note blocks
  - Improved note block selection and focus management
  - Enhanced overall operation fluidity
- 交互体验优化
  - 实现回车键快速创建新笔记块
  - 优化笔记块之间的过渡动画
  - 改进笔记块选择和焦点管理
  - 提升整体操作流畅度

- Performance Optimization
  - Optimized editor rendering performance
  - Improved large document loading speed
  - Reduced unnecessary re-renders
  - Optimized memory usage
- 性能优化
  - 优化编辑器渲染性能
  - 改进大型文档的加载速度
  - 减少不必要的重渲染
  - 优化内存占用

## [0.0.4] - 2025-03-03

### New Features / 新功能
- Added Ubuntu deployment documentation
  - Added DEPLOY_UBUNTU.md file
  - Detailed EC2 environment configuration steps
  - Comprehensive project deployment process guide
  - Optimized external access configuration guide
  - Added common troubleshooting solutions
- 新增Ubuntu部署文档
  - 添加DEPLOY_UBUNTU.md文件
  - 详细记录EC2环境配置步骤
  - 完善项目部署流程说明
  - 优化外部访问配置指南
  - 添加常见问题解决方案

### Optimizations / 优化
- Deployment Process Optimization
  - Simplified environment dependency installation
  - Optimized project configuration management
  - Improved service startup scripts
  - Enhanced security configuration
- 部署流程优化
  - 简化环境依赖安装
  - 优化项目配置管理
  - 改进服务启动脚本
  - 增强安全性配置

### Documentation / 文档
- Enhanced Deployment Documentation
  - Added detailed environment requirements
  - Optimized configuration step descriptions
  - Added troubleshooting guide
  - Added performance optimization suggestions
- 完善部署文档
  - 添加详细的环境要求说明
  - 优化配置步骤的描述
  - 补充故障排除指南
  - 添加性能优化建议

## [0.0.3] - 2025-03-02

### New Features / 新功能
- Added note file drag and drop functionality
  - Implemented long-press to trigger drag operations
  - Added real-time sorting visual feedback
  - Optimized performance during dragging
  - Implemented server-side sorting persistence
  - Added error handling and rollback mechanism for drag operations
- 新增笔记文件拖曳功能
  - 实现长按触发拖曳操作
  - 添加实时排序视觉反馈
  - 优化拖曳过程中的性能
  - 实现服务端排序持久化
  - 添加拖曳操作的错误处理和回滚机制

## [0.0.2] - 2025-03-01

### New Features / 新功能
- Added left sidebar navigation for better document organization
  - Implemented hierarchical directory structure
  - Added collapsible section support
  - Integrated smooth scrolling to sections
  - Enhanced keyboard navigation support
- 新增左侧导航目录，优化文档组织
  - 实现了层级目录结构
  - 添加了章节折叠功能
  - 集成平滑滚动定位
  - 增强键盘导航支持
- Refactored and enhanced documentation sync tool
  - Renamed sync_readme.py to sync_docs.py
  - Added support for CHANGELOG file synchronization
  - Improved script documentation and usage instructions
  - Optimized debounce handling for file change detection
  - Enhanced extraction and merging logic for Chinese and English content
- 重构并增强了文档同步工具
  - 将sync_readme.py重命名为sync_docs.py
  - 添加了对CHANGELOG文件的同步支持
  - 完善了脚本的文档注释和使用说明
  - 优化了文件变更检测的防抖处理
  - 改进了中英文内容的提取和合并逻辑
- Added note file management features
  - Support for quick note deletion
  - Implemented instant visual feedback for delete operations
  - Optimized state updates and UI refresh after deletion
- 新增笔记文件管理功能
  - 支持快速删除笔记
  - 实现删除操作的即时视觉反馈
  - 优化删除后的状态更新和界面刷新

### Optimizations / 优化
- Project Architecture Optimization
  - Backend Modular Design
    - Separated core modules like models and routes
    - Optimized database model structure
    - Standardized API interface design
  - Frontend Code Refactoring
    - Adopted component-based development approach
    - Implemented layered design with hooks and services
    - Unified state management solution
  - Project Configuration Management
    - Added configuration file management system
    - Optimized environment variable configuration
    - Standardized project dependency management
  - Test Framework Enhancement
    - Added test directory structure
    - Implemented unit testing framework
    - Supported automated testing process
- 项目架构优化
  - 后端模块化设计
    - 分离models、routes等核心模块
    - 优化数据库模型结构
    - 规范化API接口设计
  - 前端代码重构
    - 采用组件化开发方式
    - 实现hooks和services的分层设计
    - 统一状态管理方案
  - 项目配置管理
    - 添加配置文件管理系统
    - 优化环境变量配置
    - 规范化项目依赖管理
  - 测试框架完善
    - 添加测试目录结构
    - 实现单元测试框架
    - 支持自动化测试流程

- User Experience Optimization
  - Note File Creation
    - Implemented automatic handling of duplicate filenames
    - Added filename suffix counting feature
    - Optimized user feedback prompts
  - Note Editing Features
    - Added edit button for toggling editor display state
    - Implemented smooth transition effects for editor state changes
    - Improved editor focus management and keyboard interaction
    - Optimized editor performance through conditional rendering
  - Drag and Drop Sorting
    - Optimized drag indicator position calculation logic
    - Implemented optimistic update strategy for instant visual feedback
    - Added error handling and rollback mechanism
    - Used throttling to optimize dragging performance
- 用户体验优化
  - 笔记文件创建
    - 实现文件名重复自动处理机制
    - 添加文件名后缀计数功能
    - 优化用户反馈提示
  - 笔记编辑功能
    - 添加编辑按钮用于切换编辑器显示状态
    - 实现编辑器状态切换的平滑过渡效果
    - 改进编辑器焦点管理和键盘交互
    - 通过条件渲染优化编辑器性能
  - 拖拽排序功能
    - 优化拖拽指示器的位置计算逻辑
    - 实现乐观更新策略，提供即时视觉反馈
    - 添加错误处理和回滚机制
    - 使用节流优化拖拽性能

### Bug Fixes / 修复
- Fixed high-frequency API request issues
  - Implemented request debouncing for search operations
  - Added request cancellation for obsolete searches
  - Optimized backend API response caching
- 修复高频API请求问题
  - 实现搜索操作的请求防抖
  - 添加过时搜索请求的取消机制
  - 优化后端API响应缓存
- Fixed potential data synchronization issues after drag-and-drop sorting
- Enhanced visual feedback during dragging with transition animations
- 修复了拖拽排序后可能出现的数据不同步问题
- 优化了拖拽时的视觉反馈，添加了过渡动画效果

### Other / 其他
- Added error logging functionality
  - Created ERROR_LOG.md file for system error recording
  - Implemented structured error logging
  - Added first error record about note file retrieval failure
- 添加错误日志记录功能
  - 创建ERROR_LOG.md文件用于记录系统错误
  - 实现了错误日志的结构化记录
  - 添加了第一条关于笔记文件获取失败的错误记录

## [0.0.1] - 2025-02-28

### New Features / 新功能
- Implemented basic note management functionality
  - Support for creating, editing, and deleting notes
  - Implemented note drag-and-drop sorting
  - Integrated Markdown editing with real-time preview
- 实现了基础的笔记管理功能
  - 支持创建、编辑、删除笔记
  - 实现了笔记的拖拽排序功能
  - 集成了Markdown编辑和实时预览
- Implemented frontend-backend separation architecture
  - Built modern UI with React and Material-UI
  - Implemented Flask backend API
  - Used SQLite for data persistence
- 实现了前后端分离架构
  - 使用React和Material-UI构建现代化前端界面
  - 实现了Flask后端API
  - 使用SQLite进行数据持久化
- Added performance optimization features
  - Implemented real-time note saving
  - Optimized API request frequency with debouncing
  - Enhanced note list rendering performance
- 添加了性能优化特性
  - 实现了笔记内容的实时保存
  - 使用防抖优化了API请求频率
  - 优化了笔记列表的渲染性能