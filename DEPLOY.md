# GitHub Pages 部署指南

## 📋 部署步骤

### 1. 创建GitHub仓库
1. 登录 [GitHub](https://github.com)
2. 点击右上角的 "+" 按钮，选择 "New repository"
3. 仓库名建议：`ios-style-shared-calendar`
4. 设置为 Public（GitHub Pages免费版需要公开仓库）
5. 点击 "Create repository"

### 2. 上传代码到GitHub
```bash
# 在项目目录中执行以下命令
git init
git add .
git commit -m "Initial commit: iOS style shared calendar"
git branch -M main
git remote add origin https://github.com/你的用户名/ios-style-shared-calendar.git
git push -u origin main
```

### 3. 配置GitHub Pages
1. 进入你的GitHub仓库页面
2. 点击 "Settings" 选项卡
3. 在左侧菜单中找到 "Pages"
4. 在 "Source" 部分选择 "GitHub Actions"
5. 保存设置

### 4. 等待部署完成
- 代码推送后，GitHub Actions会自动开始部署
- 在仓库的 "Actions" 选项卡可以查看部署状态
- 部署完成后，你的网站将在以下地址可用：
  `https://你的用户名.github.io/ios-style-shared-calendar/`

## 🔄 更新应用

每次修改代码并推送到main分支时，GitHub Pages会自动重新部署：

```bash
git add .
git commit -m "更新描述"
git push
```

## 🌐 自定义域名（可选）

如果你有自己的域名：

1. 在仓库根目录创建 `CNAME` 文件
2. 文件内容写入你的域名，如：`calendar.yourdomain.com`
3. 在域名DNS设置中添加CNAME记录指向：`你的用户名.github.io`

## 🚀 部署完成后

你的iOS风格共享日历将可以通过以下方式访问：
- **GitHub Pages链接**: `https://你的用户名.github.io/ios-style-shared-calendar/`
- **永久可用**: 只要GitHub仓库存在，网站就会一直运行
- **免费托管**: GitHub Pages完全免费
- **自动HTTPS**: 自动提供SSL证书

## 📱 分享给朋友

部署完成后，你可以将链接分享给朋友和同事，大家都可以：
- 注册自己的用户名
- 创建和查看事项
- 与你共享日程安排
- 设置私人事项

## ⚠️ 注意事项

1. **数据存储**: 当前版本使用浏览器本地存储，不同设备间不会同步
2. **用户管理**: 用户数据存储在各自的浏览器中
3. **备份建议**: 重要数据建议定期导出备份

## 🔧 故障排除

如果部署失败：
1. 检查GitHub Actions日志
2. 确保仓库是公开的
3. 确认GitHub Pages设置正确
4. 等待几分钟让DNS生效