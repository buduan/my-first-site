<template>
  <!-- 
  ==============================================
  📌 首页 - Home Page
  ==============================================
  这是网站的首页，展示你的头像、姓名和简单介绍
  
  💡 使用了 Column 组件来实现垂直居中布局
  - Column 是一个辅助组件，用于垂直排列内容
  - align="center" 表示内容在垂直方向上居中对齐
  - class="mt-20" 表示距离顶部有一定的外边距
  -->
  <Column align="center" class="mt-20">
    <!-- 
    ==============================================
    🖼️ 头像图片部分
    ==============================================
    ❗️ 修改方法 1：使用在线图片地址
    将 src 中的网址替换成你自己的头像地址
    例如：src="https://github.com/你的用户名.png"
    
    ❗️ 修改方法 2：使用本地图片
    1. 在左侧文件列表中，找到 src/assets 文件夹
    2. 将你的头像图片拖拽到这个文件夹中
    3. 修改下面的 src，例如：src="/src/assets/你的图片名.jpg"
    
    ----------------------------------
    💡 样式说明（class 中的内容）：
    - size-36: 设置图片宽度和高度为 36 单位
    - rounded-2xl: 设置圆角，让图片看起来更柔和
    - border-2: 设置边框粗细
    - transition-all: 添加过渡动画效果
    - hover:border-blue-100: 鼠标悬停时显示蓝色边框
    -->
    <img
      class="size-36 rounded-2xl border-2 border-transparent transition-all hover:border-blue-100"
      src="https://github.com/xiaoook.png"
    />

    <!-- 
    ==============================================
    📝 标题和介绍文字部分
    ==============================================
    ❗️ 修改标题文字：
    直接修改 <h1> 标签中的文字即可
    例如：<h1>👋 Hi, 我是张三</h1>
    
    💡 修改文字颜色：
    在 class 中添加 text-颜色名-亮度
    常用颜色：
    - text-blue-500: 蓝色
    - text-red-500: 红色
    - text-green-500: 绿色
    - text-purple-500: 紫色
    - text-pink-500: 粉色
    
    💡 修改文字大小：
    在 class 中添加 text-大小
    可选大小：text-xs, text-sm, text-base, text-lg, text-xl, 
             text-2xl, text-3xl, text-4xl, text-5xl, text-6xl
    
    示例：<h1 class="mt-8 text-blue-500 text-5xl">我的标题</h1>
    -->
    <h1 class="mt-8">👋 Hi, 这里是肖遥</h1>

    <!-- 
    ❗️ 修改副标题：
    直接修改 <p> 标签中的文字
    font-light 表示字体较细，你可以改成 font-bold（粗体）
    -->
    <p class="text-2xl font-light">这是一个我的个人网站</p>

    <!-- 
    ==============================================
    🔗 添加链接（可选）
    ==============================================
    如果你想添加社交媒体链接，可以取消下面的注释
    将 href 中的网址改成你自己的
    
    示例：
    <a href="https://github.com/你的用户名" class="text-blue-500 hover:underline">
      访问我的 Github
    </a>
    -->

    <!-- <a href="https://github.com/xiaoook">Github</a> -->

    <!--
    ==============================================
    💡 高级技巧：局部文字样式
    ==============================================
    如果你想让一段文字中的某几个字有不同的颜色，
    可以用 <span> 标签包裹起来
    
    示例：
    <p>
      这是一个<span class="text-red-500 font-bold">重点内容</span>的文本
    </p>
    -->
  </Column>
</template>
