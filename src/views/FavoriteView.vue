<template>
  <!-- 
  ==============================================
  📌 兴趣爱好页面 - Favorite Page
  ==============================================
  这个页面用来展示你的兴趣爱好和座右铭
  使用卡片式布局，让内容更清晰美观
  -->
  <div class="px-6">
    <!-- 
    ==============================================
    📝 标题区域
    ==============================================
    -->
    <div class="mb-8">
      <!-- ❗️ 修改页面 emoji -->
      <div class="text-6xl mb-4">⭐</div>

      <!-- ❗️ 修改页面标题 -->
      <h2 class="text-4xl font-bold text-gray-800">兴趣爱好</h2>

      <!-- ❗️ 修改页面副标题 -->
      <p class="text-xl text-gray-600">生活不止眼前的代码，还有诗和远方</p>
    </div>

    <!-- 
    ==============================================
    🎨 兴趣爱好卡片展示区域
    ==============================================
    使用 Grid 组件实现卡片网格布局
    
    💡 Grid 组件说明：
    - Grid 用于创建网格布局，自动排列卡片
    - :cols="2" 表示每行显示 2 个卡片
      可以改成 :cols="3"（3列）或 :cols="1"（1列，竖着排）
    - gap="4" 表示卡片之间的间距
      可以改成 gap="2"（更小）或 gap="6"（更大）
    
    ❗️ 修改卡片内容：
    每个卡片包含：emoji、标题、描述文字
    直接修改对应的文字即可
    
    ❗️ 添加新卡片：
    1. 复制整个 <div class="bg-white p-3 rounded-2xl">...</div> 块
    2. 粘贴到 Grid 标签内的任意位置
    3. 修改 emoji、标题和描述
    
    ❗️ 删除卡片：
    删除对应的整个 <div class="bg-white p-3 rounded-2xl">...</div> 块
    -->
    <div class="mb-8">
      <h3>我喜欢的事情</h3>
      <Grid :cols="2" gap="4" class="mt-4">
        <!-- 卡片 1 -->
        <div class="bg-white p-3 rounded-2xl">
          <!-- ❗️ 修改卡片图标 -->
          <div class="text-4xl mb-3">💻</div>

          <!-- ❗️ 修改卡片标题 -->
          <h4 class="text-xl font-bold text-gray-800 mb-2">编程开发</h4>

          <!-- ❗️ 修改卡片描述 -->
          <p class="text-gray-700">
            热爱编写代码，探索新技术，享受创造的乐趣。特别喜欢前端开发和用户体验设计。
          </p>
        </div>

        <!-- 卡片 2 -->
        <div class="bg-white p-3 rounded-2xl">
          <div class="text-4xl mb-3">🎮</div>
          <h4 class="text-xl font-bold text-gray-800 mb-2">电子游戏</h4>
          <p class="text-gray-700">
            喜欢各种类型的游戏，从策略游戏到动作冒险，游戏是放松和娱乐的好方式。
          </p>
        </div>

        <!-- 卡片 3 -->
        <div class="bg-white p-3 rounded-2xl">
          <div class="text-4xl mb-3">📚</div>
          <h4 class="text-xl font-bold text-gray-800 mb-2">阅读</h4>
          <p class="text-gray-700">喜欢阅读技术书籍和科幻小说，通过阅读不断充实自己，拓展视野。</p>
        </div>

        <!-- 卡片 4 -->
        <div class="bg-white p-3 rounded-2xl">
          <div class="text-4xl mb-3">🎵</div>
          <h4 class="text-xl font-bold text-gray-800 mb-2">音乐</h4>
          <p class="text-gray-700">
            音乐是生活的调味剂，喜欢在编程时听各种风格的音乐，提高效率和灵感。
          </p>
        </div>

        <!-- 
        💡 想添加更多爱好？复制上面的卡片，粘贴到这里！
        常用 emoji 参考：
        🏀 运动  🎬 电影  🍕 美食  ✈️ 旅行  
        📷 摄影  🎨 绘画  🎸 音乐  🐱 宠物
        -->
      </Grid>
    </div>

    <!-- 
    ==============================================
    💭 座右铭区域
    ==============================================
    展示一句激励自己的名言
    
    ❗️ 修改座右铭：
    1. 修改第一个 <p> 标签中的引语内容
    2. 修改第二个 <p> 标签中的作者信息
    
    💡 样式说明：
    - italic: 斜体字
    - text-center: 文字居中
    - text-2xl: 文字大小
    -->
    <div class="bg-linear-to-r from-indigo-50 to-purple-50 p-8 rounded-2xl text-center mb-8">
      <!-- ❗️ 修改座右铭文字 -->
      <p class="text-2xl font-light text-gray-700 italic">"Stay hungry, stay foolish."</p>

      <!-- ❗️ 修改作者 -->
      <p class="text-gray-500 mt-2">— Steve Jobs</p>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Grid from '@/components/helper/Grid.vue'
</script>

<style scoped></style>
