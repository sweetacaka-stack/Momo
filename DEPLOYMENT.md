# Vercel 部署指南

## 项目概述

这是一个3D数字人作品集网站，使用纯HTML、CSS和JavaScript构建，包含Three.js 3D渲染。

## 快速部署到 Vercel

### 方法1：使用 Vercel Dashboard（推荐）

1. **推送到 GitHub/GitLab/Bitbucket**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin <your-repository-url>
   git push -u origin main
   ```

2. **连接到 Vercel**
   - 访问 https://vercel.com
   - 点击 "New Project"
   - 导入你的GitHub仓库
   - 点击 "Deploy"

3. **完成！**
   - Vercel会自动检测这是一个静态网站
   - 几秒钟后部署完成
   - 获得一个类似 `your-project-name.vercel.app` 的域名

### 方法2：使用 Vercel CLI

1. **安装 Vercel CLI**
   ```bash
   npm i -g vercel
   ```

2. **登录**
   ```bash
   vercel login
   ```

3. **部署**
   ```bash
   vercel
   ```

4. **按照提示操作**
   - 设置项目名称
   - 链接到现有项目（可选）
   - 设置为生产环境：`vercel --prod`

## 项目结构

```
portfolio-3d/
├── index.html              # 主页面
├── pages/                  # 子页面
│   ├── pulse.html         # 画廊
│   ├── aurora.html        # 产品视频
│   ├── dragon.html        # 作品集
│   ├── echo.html          # 详情页
│   ├── galaxy.html        # C4D+OC渲染
│   └── flame.html         # 联系方式
├── assets/                 # 资源文件
│   ├── models/            # 3D模型
│   ├── images/            # 图片
│   └── videos/            # 视频
├── styles/                 # 样式文件
├── vercel.json            # Vercel配置
└── package.json           # 项目配置
```

## Vercel 配置说明

`vercel.json` 文件配置：

```json
{
  "version": 2,
  "builds": [
    {
      "src": "**",
      "use": "@vercel/static"
    }
  ],
  "routes": [
    {
      "src": "/(.*)",
      "dest": "/$1"
    }
  ],
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        { "key": "Cache-Control", "value": "public, max-age=31536000, immutable" }
      ]
    }
  ]
}
```

- `@vercel/static` - 使用Vercel的静态文件托管
- 所有路由直接映射到文件系统
- 启用了长期缓存策略

## 自定义域名

1. 在Vercel项目设置中添加域名
2. 在域名注册商处添加DNS记录
3. Vercel会自动提供SSL证书

## 本地开发

```bash
# 使用Python启动本地服务器
python -m http.server 5000 --bind 0.0.0.0

# 访问 http://localhost:5000
```

## 注意事项

1. **GLB模型文件** - 确保模型文件路径正确
2. **外部资源** - CDN链接确保可访问
3. **缓存策略** - 已设置长期缓存，更新文件时可能需要清除缓存
4. **部署预览** - 每次git push都会自动创建预览部署

## 技术栈

- HTML5
- CSS3
- JavaScript (ES6+)
- Three.js (3D渲染)
- Vercel (部署平台)

## 支持

如有问题，请访问：
- Vercel文档: https://vercel.com/docs
- 项目仓库: [你的仓库地址]
