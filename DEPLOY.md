# MBTI 性格测试 - GitHub Pages 部署指南

## 快速部署步骤

### 第一步：在 GitHub 上创建仓库

1. 访问 https://github.com/new
2. 填写以下信息：
   - **Repository name**: `mbti-test`（或者你喜欢的名字）
   - **Description**: `MBTI 性格测试网页`
   - 选择 **Public**（GitHub Pages 免费使用需要公开仓库）
   - **不要**勾选 "Add a README file"
3. 点击 **Create repository**

### 第二步：将文件推送到 GitHub

在你刚创建的仓库页面，你会看到推送代码的指引。按照以下步骤操作：

打开终端，运行以下命令：

```bash
# 进入部署目录
cd /Users/tongxuan/.qoderwork/workspace/mnymr80fwmae1tmu/mbti-deploy

# 初始化 Git 仓库
git init

# 添加文件
git add index.html

# 提交
git commit -m "Initial commit: MBTI 性格测试网页"

# 添加远程仓库（将 <你的用户名> 替换为你的 GitHub 用户名）
git remote add origin https://github.com/<你的用户名>/mbti-test.git

# 推送到 GitHub
git branch -M main
git push -u origin main
```

### 第三步：启用 GitHub Pages

1. 推送完成后，访问你的仓库页面
2. 点击顶部的 **Settings** 标签
3. 在左侧菜单找到并点击 **Pages**
4. 在 **Source** 下拉菜单中选择 **main** 分支
5. 在 **/ (root)** 文件夹选项下点击 **Save**

### 第四步：访问你的网站

等待 1-2 分钟后，你的网站就可以在以下地址访问了：

```
https://<你的用户名>.github.io/mbti-test/
```

## 常见问题

### 如果页面没有立即显示

- GitHub Pages 可能需要几分钟来构建和部署
- 你可以访问 `https://<你的用户名>.github.io/mbti-test/index.html` 试试
- 在仓库的 **Actions** 标签页可以查看部署进度

### 如果想使用自定义域名

1. 在 Pages 设置页面，找到 **Custom domain**
2. 输入你的域名（例如 `mbti.example.com`）
3. 按照指示配置 DNS 记录

### 如果想更新内容

只需修改 `index.html` 文件，然后重新推送：

```bash
git add index.html
git commit -m "更新内容描述"
git push
```

## 替代方案

如果你不想使用 GitHub，也可以考虑：

### Cloudflare Pages
1. 访问 https://pages.cloudflare.com/
2. 连接你的 GitHub 账号
3. 选择仓库并部署

### Vercel
1. 访问 https://vercel.com/
2. 使用 GitHub 账号登录
3. 导入仓库并部署

### Netlify
1. 访问 https://www.netlify.com/
2. 直接拖拽 `mbti-deploy` 文件夹到他们的上传区域
3. 即刻获得一个公开链接
