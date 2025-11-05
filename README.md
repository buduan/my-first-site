# 🌟 我的第一个个人网站

欢迎来到个人网站 Workshop！这是一个专为零基础学员设计的项目模板，你将在 1 小时内创建属于自己的个人介绍网站。

## 📚 目录

- [开始之前](#-开始之前)
- [项目结构](#-项目结构)
- [开发指南](#-开发指南)
- [Helper 组件使用](#-helper-组件使用)
- [部署到 Vercel](#-部署到-vercel)
- [常见问题](#-常见问题)

---

## 🚀 开始之前

### 1. 环境准备

在开始之前，请确保你的电脑已安装以下工具：

- **Node.js**（版本 20.19.0 或更高）
  - 下载地址：https://nodejs.org/
  - 验证安装：在终端运行 `node -v`

- **pnpm**（包管理工具）
  - 安装命令：`npm install -g pnpm`
  - 验证安装：在终端运行 `pnpm -v`

- **代码编辑器**
  - 推荐使用 VS Code：https://code.visualstudio.com/

### 2. 安装项目依赖

打开终端（Terminal），在项目文件夹中运行：

```bash
pnpm install
```

### 3. 启动开发服务器

安装完成后，运行以下命令启动项目：

```bash
pnpm dev
```

然后在浏览器中打开 `http://localhost:5173`，你就能看到网站了！

---

## 📁 项目结构

```
my-first-site/
├── src/
│   ├── views/              # 页面文件
│   │   ├── HomeView.vue    # 首页 - 展示头像和姓名
│   │   ├── AboutView.vue   # 关于我 - 详细介绍
│   │   └── FavoriteView.vue # 兴趣爱好 - 兴趣展示
│   ├── components/         # 组件文件夹
│   │   ├── Navigation.vue  # 导航栏组件
│   │   └── helper/         # 辅助组件（布局工具）
│   │       ├── Column.vue  # 垂直布局组件
│   │       ├── Row.vue     # 水平布局组件
│   │       └── Grid.vue    # 网格布局组件
│   ├── assets/             # 静态资源（图片、CSS等）
│   ├── router/             # 路由配置
│   ├── App.vue             # 根组件
│   └── main.js             # 入口文件
├── public/                 # 公共资源
├── package.json            # 项目配置
└── README.md               # 项目说明文档
```

---

## 💻 开发指南

### 修改网站内容的步骤

1. **打开对应的页面文件**
   - 首页：`src/views/HomeView.vue`
   - 关于我：`src/views/AboutView.vue`
   - 兴趣爱好：`src/views/FavoriteView.vue`

2. **阅读文件中的注释**
   - 每个文件都有详细的注释说明
   - 找到标有 `❗️` 的地方，这些是可以修改的内容

3. **修改文字和图片**
   - 直接在代码中修改文字
   - 更换图片地址或上传本地图片

4. **保存并查看效果**
   - 按 `Ctrl + S`（Windows）或 `Cmd + S`（Mac）保存
   - 浏览器会自动刷新显示新内容

### 常用的样式修改

#### 文字颜色

```html
<p class="text-blue-500">这是蓝色文字</p>
<p class="text-red-500">这是红色文字</p>
<p class="text-green-500">这是绿色文字</p>
```

#### 文字大小

```html
<p class="text-sm">小号文字</p>
<p class="text-base">普通文字</p>
<p class="text-lg">大号文字</p>
<p class="text-2xl">超大文字</p>
```

#### 字体粗细

```html
<p class="font-light">细体</p>
<p class="font-normal">正常</p>
<p class="font-bold">粗体</p>
```

---

## 🎨 Helper 组件使用

为了让零基础学员更容易理解网页布局，我们提供了三个辅助组件：

### 📐 Column 组件 - 垂直排列

**作用**：让内容从上到下排列（纵向布局）

**使用方法**：

```vue
<Column align="center">
  <div>第一项内容</div>
  <div>第二项内容</div>
  <div>第三项内容</div>
</Column>
```

**参数说明**：

- `align="left"` - 内容靠上对齐
- `align="center"` - 内容居中对齐（默认）
- `align="right"` - 内容靠下对齐
- `align="between"` - 内容两端对齐
- `align="around"` - 内容周围均匀分布
- `align="evenly"` - 内容完全均匀分布

**示例效果**：

```
┌─────────┐
│  内容1  │
│  内容2  │
│  内容3  │
└─────────┘
```

---

### 📏 Row 组件 - 水平排列

**作用**：让内容从左到右排列（横向布局）

**使用方法**：

```vue
<Row align="center">
  <div>项目1</div>
  <div>项目2</div>
  <div>项目3</div>
</Row>
```

**参数说明**：

- `align="left"` - 内容靠左对齐
- `align="center"` - 内容居中对齐（默认）
- `align="right"` - 内容靠右对齐
- `align="between"` - 内容两端对齐
- `align="around"` - 内容周围均匀分布
- `align="evenly"` - 内容完全均匀分布

**示例效果**：

```
┌─────────────────────┐
│ 内容1  内容2  内容3 │
└─────────────────────┘
```

---

### 🎯 Grid 组件 - 网格布局

**作用**：创建网格布局，自动排列卡片（类似相册）

**使用方法**：

```vue
<Grid :cols="2" gap="4">
  <div>卡片1</div>
  <div>卡片2</div>
  <div>卡片3</div>
  <div>卡片4</div>
</Grid>
```

**参数说明**：

- `:cols` - 每行显示几列
  - `:cols="1"` - 每行1个（占满整行）
  - `:cols="2"` - 每行2个
  - `:cols="3"` - 每行3个
  - `:cols="4"` - 每行4个
  - 最多支持 12 列

- `gap` - 卡片之间的间距
  - `gap="2"` - 小间距
  - `gap="4"` - 中等间距
  - `gap="6"` - 大间距
  - 可选值：`"0"`, `"1"`, `"2"`, `"3"`, `"4"`, `"5"`, `"6"`, `"8"`, `"10"`

**示例效果（2列）**：

```
┌──────────┬──────────┐
│  卡片1   │  卡片2   │
├──────────┼──────────┤
│  卡片3   │  卡片4   │
└──────────┴──────────┘
```

**示例效果（3列）**：

```
┌──────┬──────┬──────┐
│ 卡片1│ 卡片2│ 卡片3│
├──────┼──────┼──────┤
│ 卡片4│ 卡片5│ 卡片6│
└──────┴──────┴──────┘
```

---

### 🎨 组件组合使用

你可以灵活组合这些组件来实现复杂的布局：

```vue
<!-- 外层垂直排列，内层水平排列 -->
<Column align="center">
  <h1>我的标题</h1>
  <Row align="center">
    <img src="photo1.jpg" />
    <img src="photo2.jpg" />
  </Row>
</Column>
```

```vue
<!-- 网格布局中嵌套其他内容 -->
<Grid :cols="2" gap="4">
  <div>
    <Row align="left">
      <span>图标</span>
      <span>标题</span>
    </Row>
    <p>描述文字</p>
  </div>
  <div>第二个卡片</div>
</Grid>
```

---

## 🚀 部署到 Vercel

完成网站开发后，你可以将它免费部署到互联网上，让全世界都能访问！

### 方法一：通过 Vercel 网站部署（推荐新手）

#### 1. 准备 GitHub 账号

- 访问 https://github.com 注册账号（如果没有的话）
- 登录你的 GitHub 账号

#### 2. 上传项目到 GitHub

**方式 A：使用 VS Code 图形界面**

1. 在 VS Code 左侧点击"源代码管理"图标（三个小圆点连线的图标）
2. 点击"初始化存储库"按钮
3. 输入提交消息（例如："首次提交"）并点击"提交"
4. 点击"发布分支"，选择"发布到 GitHub"
5. 选择"公开"（Public）或"私有"（Private）
6. 等待上传完成

**方式 B：使用命令行**

在项目文件夹打开终端，依次运行：

```bash
# 初始化 Git 仓库
git init

# 添加所有文件
git add .

# 提交更改
git commit -m "首次提交：完成个人网站"

# 连接到 GitHub（替换成你的用户名和仓库名）
git remote add origin https://github.com/你的用户名/my-first-site.git

# 推送到 GitHub
git branch -M main
git push -u origin main
```

#### 3. 在 Vercel 部署

1. **访问 Vercel 官网**
   - 打开 https://vercel.com
   - 点击右上角"Sign Up"（注册）

2. **使用 GitHub 登录**
   - 选择"Continue with GitHub"
   - 授权 Vercel 访问你的 GitHub 账号

3. **导入项目**
   - 点击"Add New Project"（添加新项目）
   - 选择你刚才上传的 `my-first-site` 仓库
   - 点击"Import"（导入）

4. **配置项目**
   - **Project Name**：可以使用默认名称或自定义
   - **Framework Preset**：Vercel 会自动检测为 Vite
   - **Build Command**：`pnpm build`（通常会自动填写）
   - **Output Directory**：`dist`（通常会自动填写）
   - 点击"Deploy"（部署）

5. **等待部署完成**
   - 部署过程大约需要 1-3 分钟
   - 完成后会显示一个网址（例如：`https://my-first-site-xxx.vercel.app`）
   - 点击网址即可访问你的网站！

6. **分享你的网站**
   - 复制这个网址，分享给朋友和家人
   - 每次你修改代码并推送到 GitHub，Vercel 会自动重新部署

---

### 方法二：使用 Vercel CLI（命令行工具）

如果你熟悉命令行，可以使用更快速的方式：

#### 1. 安装 Vercel CLI

```bash
npm install -g vercel
```

#### 2. 登录 Vercel

```bash
vercel login
```

按照提示完成登录。

#### 3. 部署项目

在项目文件夹中运行：

```bash
# 第一次部署
vercel

# 后续部署到生产环境
vercel --prod
```

按照提示操作：

- 设置项目名称
- 选择部署范围（个人或团队）
- 确认项目设置

部署完成后会显示网站地址！

---

### 🔄 更新网站内容

部署后如果你想修改网站内容：

**使用 GitHub + Vercel（自动部署）：**

1. 在本地修改代码
2. 保存并提交到 GitHub：
   ```bash
   git add .
   git commit -m "更新内容描述"
   git push
   ```
3. Vercel 会自动检测到更新并重新部署
4. 等待 1-2 分钟后刷新网站即可看到新内容

**使用 Vercel CLI：**

1. 在本地修改代码
2. 运行 `vercel --prod` 重新部署
3. 完成！

---

### 🎯 自定义域名（可选）

如果你有自己的域名（例如 `www.yourname.com`），可以在 Vercel 中绑定：

1. 进入 Vercel 项目设置页面
2. 点击"Domains"（域名）
3. 输入你的域名
4. 按照提示在域名服务商处添加 DNS 记录
5. 等待验证完成

---

## ❓ 常见问题

### Q1: 修改代码后网页没有变化？

**A:**

- 确保你已经保存了文件（Ctrl+S 或 Cmd+S）
- 检查终端是否有报错信息
- 尝试在浏览器中强制刷新（Ctrl+Shift+R 或 Cmd+Shift+R）

### Q2: 如何更换头像图片？

**A:** 有两种方法：

方法1：使用在线图片

```html
<img src="https://你的图片地址.jpg" />
```

方法2：使用本地图片

1. 将图片拖到 `src/assets` 文件夹
2. 修改图片路径：

```html
<img src="/src/assets/你的图片名.jpg" />
```

### Q3: 如何添加更多兴趣爱好卡片？

**A:**

1. 打开 `src/views/FavoriteView.vue`
2. 找到 Grid 组件内的卡片代码
3. 复制一个卡片的完整代码块（从 `<div class="bg-white...">` 到 `</div>`）
4. 粘贴到 Grid 标签内
5. 修改 emoji、标题和描述

### Q4: 网站部署后显示 404 错误？

**A:**

- 检查 Vercel 项目设置中的构建命令是否正确
- 确保 `Output Directory` 设置为 `dist`
- 查看 Vercel 的部署日志，看是否有构建错误

### Q5: 如何修改网站标题（浏览器标签上的文字）？

**A:**
打开 `index.html`，找到 `<title>` 标签，修改其中的文字：

```html
<title>我的个人网站</title>
```

### Q6: 如何添加更多页面？

**A:**

1. 在 `src/views` 文件夹中创建新的 `.vue` 文件
2. 在 `src/router/index.js` 中添加路由配置
3. 在 `src/components/Navigation.vue` 中添加导航链接

### Q7: 代码出错了怎么办？

**A:**

- 检查终端（Terminal）中的错误信息
- 确保所有的标签都正确闭合（`<div>` 要有对应的 `</div>`）
- 检查引号是否配对
- 如果实在不行，可以用 Git 恢复到之前的版本

---

## 📖 学习资源

- **Vue.js 官方文档**：https://cn.vuejs.org/
- **Tailwind CSS 文档**：https://tailwindcss.com/docs
- **MDN Web 文档**：https://developer.mozilla.org/zh-CN/
- **Emoji 查找**：https://emojipedia.org/

---

## 🎉 祝贺

恭喜你完成了第一个个人网站！继续探索和学习，你可以：

- 添加更多页面和功能
- 学习更多 CSS 样式
- 添加动画效果
- 集成第三方服务（评论、统计等）

**记住：每个伟大的开发者都是从这里开始的！** 🚀

---

## 📞 需要帮助？

如果在开发过程中遇到问题：

1. 仔细阅读代码中的注释
2. 查看本文档的常见问题部分
3. 向讲师或助教寻求帮助
4. 在网上搜索相关问题（Stack Overflow、GitHub Issues）

**Happy Coding! 💻✨**
