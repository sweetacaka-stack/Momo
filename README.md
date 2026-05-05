# 3D Digital Human Portfolio

一个精美的3D数字人作品集网站，使用Three.js实现3D渲染效果。

## 🌟 特性

- 🤖 **3D数字人** - 使用GLB模型的3D数字人站在中央
- 🎨 **精美UI设计** - 金色、青色、深黑色的高端配色方案
- 🎯 **6个作品板块** - 画廊、产品视频、作品集、详情页、C4D+OC渲染、联系方式
- 🔄 **流畅交互** - 滚动切换、点击进入、双击返回
- ✨ **视觉效果** - 粒子特效、光晕、纹理背景

## 🚀 快速开始

### 本地开发

```bash
# 使用Python启动本地服务器
python -m http.server 5000 --bind 0.0.0.0

# 访问 http://localhost:5000
```

### 部署到 Vercel

#### 方法1：使用 Vercel Dashboard（推荐）

1. 推送到 GitHub/GitLab/Bitbucket
2. 访问 https://vercel.com，点击 "New Project"
3. 导入你的仓库，点击 "Deploy"

#### 方法2：使用 Vercel CLI

```bash
# 安装 Vercel CLI
npm i -g vercel

# 登录
vercel login

# 部署
vercel

# 生产环境部署
vercel --prod
```

详细部署指南请查看 [DEPLOYMENT.md](./DEPLOYMENT.md)

## 📁 项目结构

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
│   ├── models/            # 3D模型 (.glb)
│   ├── images/            # 图片
│   └── videos/            # 视频
├── styles/                 # 样式文件
├── vercel.json            # Vercel部署配置
├── package.json           # 项目配置
├── DEPLOYMENT.md          # 部署指南
└── README.md              # 项目说明
```

## 🎮 操作说明

- **滚动鼠标滚轮** - 切换作品板块
- **点击任意作品** - 进入详情页
- **双击空白处** - 返回主页
- **移动鼠标** - 查看3D效果

## 🌐 在线演示

部署后访问：`https://your-project-name.vercel.app`

## 🛠️ 技术栈

- HTML5
- CSS3
- JavaScript (ES6+)
- Three.js (3D渲染)
- Vercel (部署平台)

## 📝 注意事项

1. 确保GLB模型文件路径正确
2. 外部CDN链接确保可访问
3. 更新文件时可能需要清除浏览器缓存

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📄 许可证

MIT License

## 🔗 相关链接

- [Three.js 文档](https://threejs.org/docs/)
- [Vercel 文档](https://vercel.com/docs)
- [部署指南](./DEPLOYMENT.md)
