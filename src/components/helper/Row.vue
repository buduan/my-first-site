<!-- 
==============================================
📏 Row 组件 - 水平布局辅助组件
==============================================
这个组件用于将内容从左到右水平排列

使用示例：
<Row align="center">
  <div>内容1</div>
  <div>内容2</div>
  <div>内容3</div>
</Row>

参数说明：
- align: 控制内容的对齐方式
  - "left": 靠左对齐
  - "center": 居中对齐（默认）
  - "right": 靠右对齐
  - "between": 两端对齐
  - "around": 周围均匀分布
  - "evenly": 完全均匀分布
==============================================
-->
<template>
  <div :class="containerClass">
    <slot></slot>
  </div>
</template>

<script setup>
import { computed } from 'vue'

// 定义组件接收的参数
const props = defineProps({
  align: {
    type: String,
    default: 'center', // 默认居中对齐
    validator: (value) =>
      ['left', 'center', 'right', 'between', 'around', 'evenly'].includes(value),
  },
})

const containerClass = computed(() => {
  const classes = ['flex-row', 'gap-2']

  // 对齐方式
  switch (props.align) {
    case 'left':
      classes.push('justify-start')
      break
    case 'center':
      classes.push('justify-center')
      break
    case 'right':
      classes.push('justify-end')
      break
    case 'between':
      classes.push('justify-between')
      break
    case 'around':
      classes.push('justify-around')
      break
    case 'evenly':
      classes.push('justify-evenly')
      break
  }

  return classes.join(' ')
})
</script>

<style scoped>
.flex-row {
  display: flex;
  flex-direction: row;
  align-items: center;
}

.justify-start {
  justify-content: flex-start;
}

.justify-center {
  justify-content: center;
}

.justify-end {
  justify-content: flex-end;
}

.justify-between {
  justify-content: space-between;
}

.justify-around {
  justify-content: space-around;
}

.justify-evenly {
  justify-content: space-evenly;
}

.gap-2 {
  gap: 0.5rem; /* 8px */
}
</style>
