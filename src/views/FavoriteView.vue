<template>
  <div class="px-6">
    <!-- 标题部分 -->
    <div class="mb-8">
      <div class="text-6xl mb-4">⭐</div>
      <h2 class="text-4xl font-bold text-gray-800">兴趣爱好</h2>
      <p class="text-xl text-gray-600">生活不止眼前的代码，还有诗和远方</p>
    </div>

    <!-- 兴趣爱好卡片展示 -->
    <div class="mb-8">
      <h3>我喜欢的事情</h3>
      <Grid :cols="2" gap="4" class="mt-4">
        <div class="bg-white p-3 rounded-2xl">
          <div class="text-4xl mb-3">💻</div>
          <h4 class="text-xl font-bold text-gray-800 mb-2">编程开发</h4>
          <p class="text-gray-700">
            热爱编写代码，探索新技术，享受创造的乐趣。特别喜欢前端开发和用户体验设计。
          </p>
        </div>

        <div class="bg-white p-3 rounded-2xl">
          <div class="text-4xl mb-3">🎮</div>
          <h4 class="text-xl font-bold text-gray-800 mb-2">电子游戏</h4>
          <p class="text-gray-700">
            喜欢各种类型的游戏，从策略游戏到动作冒险，游戏是放松和娱乐的好方式。
          </p>
        </div>

        <div class="bg-white p-3 rounded-2xl">
          <div class="text-4xl mb-3">📚</div>
          <h4 class="text-xl font-bold text-gray-800 mb-2">阅读</h4>
          <p class="text-gray-700">喜欢阅读技术书籍和科幻小说，通过阅读不断充实自己，拓展视野。</p>
        </div>

        <div class="bg-white p-3 rounded-2xl">
          <div class="text-4xl mb-3">🎵</div>
          <h4 class="text-xl font-bold text-gray-800 mb-2">音乐</h4>
          <p class="text-gray-700">
            音乐是生活的调味剂，喜欢在编程时听各种风格的音乐，提高效率和灵感。
          </p>
        </div>
      </Grid>
    </div>

    <!-- 座右铭 -->
    <div class="bg-linear-to-r from-indigo-50 to-purple-50 p-8 rounded-2xl text-center mb-8">
      <p class="text-2xl font-light text-gray-700 italic">"Stay hungry, stay foolish."</p>
      <p class="text-gray-500 mt-2">— Steve Jobs</p>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Grid from '@/components/helper/Grid.vue'
</script>

<style scoped></style>
