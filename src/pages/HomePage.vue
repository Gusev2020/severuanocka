<script setup lang="ts">
import Header from '@/widgets/header/index.vue'
import typography from '@/shared/typography/index.vue'
</script>

<template>
  <main>
    <Header></Header>
    <typography tagName="p" size="xl" :bold="true">test</typography>
  </main>
</template>
