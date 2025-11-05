<template>
  <!-- 
  ==============================================
  📌 关于我页面 - About Page
  ==============================================
  这个页面用来展示更详细的个人信息
  包括：个人介绍、技能展示、照片墙等
  
  💡 px-6 表示左右内边距为 6 单位，让内容不要紧贴边缘
  -->
  <div class="px-6">
    <!-- 
    ==============================================
    👤 个人介绍区域
    ==============================================
    包含 emoji 表情、姓名和一句话介绍
    -->
    <div class="mb-8">
      <!-- 
      ❗️ 修改表情符号：
      直接修改 emoji，可以从这里复制：https://emojipedia.org/
      常用 emoji: 👨‍💻 👩‍💻 🎓 🚀 ⚡ 🌟 💡
      -->
      <div class="text-6xl mb-4">🧑‍💻</div>

      <!-- 
      ❗️ 修改姓名：
      直接修改 <h2> 标签中的文字
      可以是中文、英文或中英文结合
      -->
      <h2 class="text-4xl font-bold text-gray-800">肖遥 Hunter Xiao</h2>

      <!-- 
      ❗️ 修改个人简介：
      在 <p> 标签中写一句话介绍自己
      可以包括：学校、专业、年级、兴趣爱好等
      -->
      <p class="text-xl text-gray-600">
        宁波诺丁汉大学计算机系大三学生，热爱编程与技术,学习成绩十分优异。
      </p>
    </div>

    <!-- 
    ==============================================
    ⭐ 技能展示区域
    ==============================================
    使用 Row 组件横向排列你的技能标签
    
    💡 Row 组件说明：
    - Row 用于水平排列内容
    - align="left" 表示内容靠左对齐
    - 也可以改为 align="center" 居中，或 align="right" 靠右
    -->
    <div class="mb-16">
      <h3>我擅长的</h3>

      <!-- 
      ❗️ 添加或修改技能：
      1. 复制下面的 <div> 块（从 <div class="text-center"> 到 </div>）
      2. 粘贴到合适位置
      3. 修改 emoji 和文字内容
      
      💡 可以添加更多技能，例如：
      - 🎨 设计
      - 📸 摄影
      - ✍️ 写作
      - 🎵 音乐
      -->
      <Row align="left">
        <div class="text-center w-12">
          <div class="text-2xl mb-2">📑</div>
          <p class="text-gray-700">学习</p>
        </div>
        <div class="text-center w-12">
          <div class="text-2xl mb-2">💻</div>
          <p class="text-gray-700">编程</p>
        </div>
        <div class="text-center w-12">
          <div class="text-2xl mb-2">🎮</div>
          <p class="text-gray-700">游戏</p>
        </div>
      </Row>
    </div>

    <!-- 
    ==============================================
    📷 照片墙区域
    ==============================================
    展示你的生活照片或作品集
    
    ❗️ 修改图片方法 1：使用在线图片
    将 src 中的网址替换成你的图片地址
    
    ❗️ 修改图片方法 2：使用本地图片
    1. 将图片拖到 src/assets 文件夹
    2. 修改 src，例如：src="/src/assets/photo1.jpg"
    
    💡 添加更多图片：
    复制 <img> 这一行，粘贴在下面，然后修改图片地址
    
    💡 调整图片大小：
    修改 class 中的 w-5/12
    - w-3/12: 占 25% 宽度（更小）
    - w-5/12: 占 42% 宽度（中等）
    - w-6/12: 占 50% 宽度（一半）
    - w-full: 占 100% 宽度（全宽）
    -->
    <div class="mb-16">
      <h3>照片</h3>
      <Row align="left">
        <img src="https://picsum.photos/300/200?random=1" class="rounded-lg shadow-md w-5/12" />
        <img src="https://picsum.photos/300/200?random=2" class="rounded-lg shadow-md w-5/12" />
      </Row>
    </div>
  </div>
</template>
