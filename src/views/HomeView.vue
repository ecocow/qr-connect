<script setup lang="ts">
import logo from '@/assets/images/logo_white.png'
import {onMounted} from "vue";
// user agent device check
const isMobile = /iPhone|iPad|iPod|Android/i.test(navigator.userAgent)
const isAndroid = /Android/i.test(navigator.userAgent)
const isIOS = /iPhone|iPad|iPod/i.test(navigator.userAgent)
const isTablet = /Tablet/i.test(navigator.userAgent)
const isDesktop = !isMobile && !isTablet
const isChrome = /Chrome/i.test(navigator.userAgent)
const isSafari = /Safari/i.test(navigator.userAgent)
const isFirefox = /Firefox/i.test(navigator.userAgent)
const isEdge = /Edge/i.test(navigator.userAgent)
const isIE = /MSIE|Trident/i.test(navigator.userAgent)
const isOpera = /Opera/i.test(navigator.userAgent)
const isMac = /Macintosh/i.test(navigator.userAgent)
const isWindows = /Windows/i.test(navigator.userAgent)
const isLinux = /Linux/i.test(navigator.userAgent)
const isChromeOS = /CrOS/i.test(navigator.userAgent)
const isWebOS = /webOS/i.test(navigator.userAgent)
const isBlackBerry = /BlackBerry/i.test(navigator.userAgent)
const isBada = /Bada/i.test(navigator.userAgent)

onMounted(() => {
  let vh = window.innerHeight * 0.01;
  document.documentElement.style.setProperty('--vh', `${vh}px`);

// resize
  window.addEventListener('resize', () => {
    let vh = window.innerHeight * 0.01;
    document.documentElement.style.setProperty('--vh', `${vh}px`);
  })
})
</script>

<template>
  <main>
    <div class="logo">
      <h1><img :src="logo" alt=""></h1>
    </div>
    <div class="action-box" v-if="isMobile">
      <a href="https://play.google.com/store/apps/details?id=app.ecocow.ecomap">에코맵 다운받기</a>
    </div>
    <div v-else class="action-msg">
      <p>애코맵은 모바일기기에서 확인 하실 수 있습니다.</p>
    </div>
  </main>
</template>

<style scoped lang="scss">
.logo {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  height: calc(var(--var, 1vh) * 100);
  h1 {
    text-align: center;
    img {
      width: 100%;
      max-width: 150px;
    }
  }
}
.action-box, .action-msg {
  position: absolute;
  left: 0;
  bottom: 0;
  right: 0;
  padding: 20px 20px;
  * {
    font-weight: 600;
    font-size: 16px;
  }
  a {
    display: block;
    width: 100%;
    height: 50px;
    line-height: 50px;
    text-align: center;
    color: #fff;
    border-radius: 10px;
    text-decoration: none;
    background-color: #000;
  }
}
</style>

