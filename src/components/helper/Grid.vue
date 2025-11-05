<template>
  <div :class="containerClass">
    <slot></slot>
  </div>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  cols: {
    type: Number,
    default: 2,
    validator: (value) => value >= 1 && value <= 12,
  },
  gap: {
    type: String,
    default: '2',
    validator: (value) => ['0', '1', '2', '3', '4', '5', '6', '8', '10'].includes(value),
  },
})

const containerClass = computed(() => {
  const classes = ['grid-container']

  // 列数
  classes.push(`grid-cols-${props.cols}`)

  // 间距
  classes.push(`gap-${props.gap}`)

  return classes.join(' ')
})
</script>

<style scoped>
.grid-container {
  display: grid;
}

/* 列数定义 */
.grid-cols-1 {
  grid-template-columns: repeat(1, minmax(0, 1fr));
}

.grid-cols-2 {
  grid-template-columns: repeat(2, minmax(0, 1fr));
}

.grid-cols-3 {
  grid-template-columns: repeat(3, minmax(0, 1fr));
}

.grid-cols-4 {
  grid-template-columns: repeat(4, minmax(0, 1fr));
}

.grid-cols-5 {
  grid-template-columns: repeat(5, minmax(0, 1fr));
}

.grid-cols-6 {
  grid-template-columns: repeat(6, minmax(0, 1fr));
}

.grid-cols-7 {
  grid-template-columns: repeat(7, minmax(0, 1fr));
}

.grid-cols-8 {
  grid-template-columns: repeat(8, minmax(0, 1fr));
}

.grid-cols-9 {
  grid-template-columns: repeat(9, minmax(0, 1fr));
}

.grid-cols-10 {
  grid-template-columns: repeat(10, minmax(0, 1fr));
}

.grid-cols-11 {
  grid-template-columns: repeat(11, minmax(0, 1fr));
}

.grid-cols-12 {
  grid-template-columns: repeat(12, minmax(0, 1fr));
}

/* 间距定义 */
.gap-0 {
  gap: 0;
}

.gap-1 {
  gap: 0.25rem; /* 4px */
}

.gap-2 {
  gap: 0.5rem; /* 8px */
}

.gap-3 {
  gap: 0.75rem; /* 12px */
}

.gap-4 {
  gap: 1rem; /* 16px */
}

.gap-5 {
  gap: 1.25rem; /* 20px */
}

.gap-6 {
  gap: 1.5rem; /* 24px */
}

.gap-8 {
  gap: 2rem; /* 32px */
}

.gap-10 {
  gap: 2.5rem; /* 40px */
}
</style>
