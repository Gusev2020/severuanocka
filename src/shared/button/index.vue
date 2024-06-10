<script lang="ts" setup>
import Typography from '@/shared/typography/index.vue'

interface Props {
  color?: 'primary' | 'secondary' | 'grayscale' | 'error'
  decoration?: 'none' | 'outline' | 'default'
  size?: 'm' | 'l' | 's'
  disabled?: boolean
}

const props = defineProps<Props>()

const { color = 'primary', decoration = 'none', size = 'm', disabled = false } = props
const classes = ['button', `size_${size}`, `decoration_${decoration}`, `color_${color}`]
</script>
<template>
  <button :class="classes" :disabled="disabled">
    <slot name="leftIcon"></slot>
    <Typography class="button__text" tagName="span" size="s"><slot /></Typography>
  </button>
</template>
<style scoped>
.button {
  display: flex;
  align-items: center;
  border: none;
  border-radius: 4px;
  width: 100%;
  cursor: pointer;
}

.button__text {
  width: 100%;
  text-align: center;
}

.button.size_m {
  gap: 8px;
  padding: 8px;
}

.button.color_secondary {
  background-color: var(--main-secondary);
  color: var(--main-on-secondary);
}
</style>
