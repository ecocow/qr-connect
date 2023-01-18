<script setup lang="ts">
import logo from '@/assets/images/logo_white.png'
</script>

<template>
  <main>
    <div class="logo">
      <h1><img :src="logo" alt=""></h1>
    </div>
  </main>
</template>

<style scoped lang="scss">
.logo {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  h1 {
    text-align: center;
    img {
      width: 100%;
      max-width: 150px;
    }
  }
}
</style>

