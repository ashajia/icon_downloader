# 如席矢量图标下载工具

## 项目简介

如席矢量图标下载工具是一个基于PyQt5开发的桌面应用程序，用于搜索和下载来自iconfont.cn的SVG矢量图标。该工具提供了简洁美观的用户界面，支持关键词搜索、分页浏览和一键下载SVG图标文件。

## 功能特点

- 关键词搜索：支持通过关键词搜索iconfont.cn上的图标资源
- 分页浏览：支持多页浏览搜索结果
- 图标预览：直观展示SVG图标及其名称
- 一键下载：点击图标即可下载SVG文件到本地
- 美观界面：采用现代化UI设计，操作简单直观
- 日志记录：自动记录操作日志，方便问题排查

## 技术实现

### 核心技术栈

- Python 3.x
- PyQt5：用于构建桌面GUI界面
- Requests：处理HTTP请求
- BeautifulSoup4：解析HTML内容
- SVG渲染：使用PyQt5的QSvgRenderer实现SVG预览

### 实现逻辑

1. **用户界面**
   - 采用PyQt5构建现代化界面
   - 主界面包含搜索框、图标展示区和分页控制
   - 自定义SvgIconWidget组件用于图标预览和交互

2. **搜索功能**
   - 通过调用iconfont.cn的API接口获取图标数据
   - 支持关键词搜索和分页浏览
   - 使用Session保持会话状态，处理Cookie和CSRF令牌

3. **图标渲染**
   - 使用QSvgRenderer渲染SVG图标
   - 自定义绘制逻辑，支持悬停效果和点击交互
   - 优化显示布局，提供良好的视觉体验

4. **下载功能**
   - 点击图标触发下载对话框
   - 支持自定义保存路径和文件名
   - 直接保存原始SVG内容，保证图标质量

5. **日志系统**
   - 自动记录操作日志和API响应
   - 每次启动时清理历史日志，只保留当前会话日志
   - 详细记录API请求和响应信息，便于调试

## 使用说明

### 安装要求

- Python 3.6或更高版本
- 安装以下依赖库：
pip install PyQt5 requests beautifulsoup4

### 启动应用

直接运行icon_downloader.py文件：
python icon_downloader.py

### 使用步骤

1. **搜索图标**
   - 在搜索框中输入关键词（如"箭头"、"用户"、"设置"等）
   - 点击"搜索"按钮或按回车键开始搜索

2. **浏览图标**
   - 搜索结果将显示在主界面中
   - 使用"上一页"和"下一页"按钮浏览更多结果
   - 鼠标悬停在图标上可以看到高亮效果

3. **下载图标**
   - 点击任意图标将打开保存对话框
   - 选择保存位置和文件名（默认使用图标原名）
   - 点击"保存"完成下载
   - 下载成功后会显示成功提示

## 注意事项

- 本工具仅用于个人学习和非商业用途
- 下载的图标版权归原作者所有，请遵守iconfont.cn的使用条款
- 频繁请求可能导致IP被临时限制，请合理使用
- 部分图标可能需要登录iconfont.cn才能下载，本工具不支持账号登录功能

## 常见问题

1. **搜索无结果**
   - 检查网络连接是否正常
   - 尝试使用不同的关键词
   - 确认iconfont.cn网站是否可以正常访问

2. **下载失败**
   - 检查是否有写入权限
   - 确保文件名不包含非法字符
   - 查看日志文件了解详细错误信息

3. **界面显示异常**
   - 调整窗口大小
   - 确保系统安装了必要的字体
   - 重启应用程序

## 开发者信息

本工具基于Python和PyQt5开发，源代码结构清晰，欢迎学习和改进。如有问题或建议，请提交issue或联系开发者。

---

**免责声明**：本工具仅用于学习和个人使用，请勿用于商业目的。所有图标版权归原作者所有。