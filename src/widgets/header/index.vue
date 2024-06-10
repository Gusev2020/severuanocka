<script setup lang="ts">
import Conatiner from '@/shared/container/index.vue'
import Logo from '@/shared/logo/index.vue'
import Button from '@/shared/button/index.vue'
import Icon from '@/shared/icon/index.vue'
</script>
<template>
  <header class="header">
    <Conatiner class="header__container">
      <Logo orientation="horizontal" :colorful="true" bg-color="white" :with-text="true" />
      <div class="header__catalog">
        <Button color="secondary">
          <template v-slot:leftIcon>
            <Icon type="menu" />
          </template>
          Каталог
        </Button>
      </div>
    </Conatiner>
  </header>
</template>
<style scoped>
.header {
  position: sticky;
  top: 0;
  left: 0;
  background-color: var(--main-surface);
  box-shadow: var(--shadow-default-s);
}

.header__container {
  display: flex;
  align-items: center;
  height: 72px;
}

.header__catalog {
  width: 140px;
  margin-left: 40px;
}
</style>
