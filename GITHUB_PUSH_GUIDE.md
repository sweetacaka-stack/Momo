# GitHub 推送指南

## 🔑 最简单的方法：直接在GitHub网页上操作

### 步骤1：清空你的GitHub仓库
1. 访问你的仓库：https://github.com/sweetacaka-stack/Momo
2. 点击仓库中的每个文件，点击右上角的 `...` → `Delete file`
3. 删除所有现有文件（保留 `.git` 目录，你不需要操作这个）
4. 提交删除

### 步骤2：上传我们准备好的文件

#### 需要上传的文件清单：

**在仓库根目录创建/上传：**

1. **`index.html`** ⭐ 最重要
   - 从沙箱环境的 `/workspace/projects/index.html` 复制内容
   - 或者我可以把完整内容展示给你

2. **`vercel.json`**
   ```json
   {
     "version": 2,
     "builds": [
       { "src": "index.html", "use": "@vercel/static" },
       { "src": "pages/**", "use": "@vercel/static" },
       { "src": "assets/**", "use": "@vercel/static" },
       { "src": "styles/**", "use": "@vercel/static" }
     ]
   }
   ```

3. **`package.json`**
   ```json
   {
     "name": "portfolio-3d",
     "version": "1.0.0",
     "description": "3D Digital Human Portfolio",
     "scripts": {
       "dev": "python -m http.server 5000 --bind 0.0.0.0",
       "build": "echo 'Build completed successfully'"
     },
     "keywords": ["portfolio", "3d", "digital-human"],
     "author": "",
     "license": "MIT"
   }
   ```

4. **`.gitignore`**
   ```
   node_modules
   .DS_Store
   *.swp
   __pycache__/
   *.pyc
   .venv/*
   *.o
   *.a
   /vendor
   *.egg-info/
   /.env
   .env
   ```

**创建目录结构：**

5. **创建 `pages/` 目录**，然后在里面上传：
   - `pulse.html`
   - `aurora.html`
   - `dragon.html`
   - `echo.html`
   - `flame.html`
   - `galaxy.html`

6. **创建 `assets/` 目录**，然后在里面创建 `models/` 子目录，上传：
   - `base_basic_pbr.glb`
   - `base_basic_shaded.glb`

7. **创建 `styles/` 目录**（如果有样式文件的话）

### 步骤3：在GitHub上操作

1. 访问你的仓库：https://github.com/sweetacaka-stack/Momo
2. 点击 `Add file` → `Create new file` 创建新文件
3. 或者点击 `Add file` → `Upload files` 上传文件
4. 按照上面的文件清单逐个创建/上传
5. 每次操作后点击 `Commit changes`

### 步骤4：在Vercel中重新部署

1. 访问：https://vercel.com/sweetacaka-stack/momo-murex-theta
2. 点击 `Deployments`
3. 点击最新的部署旁边的 `...` → `Redeploy`
4. 或者点击 `New Deployment` 重新部署

---

## 📋 关键要点

- ⭐ **最重要**：`index.html` 必须叫这个名字（不要叫作品集.html）
- 必须创建 `pages/` 和 `assets/` 目录
- GLB模型文件必须放在 `assets/models/` 目录下
- 所有文件都上传后，在Vercel中重新部署

---

## 💡 需要我展示某个文件的完整内容吗？

我可以把任何文件的完整内容展示给你，你只需要复制粘贴！
