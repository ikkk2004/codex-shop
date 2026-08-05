<script setup>
import { ref } from 'vue'

const isMenuOpen = ref(false)
const navigationItems = [
  { href: '#menu', label: '今日菜单' },
  { href: '#story', label: '关于我们' },
  { href: '#visit', label: '到店指南' },
]

function closeMenu() {
  isMenuOpen.value = false
}
</script>

<template>
  <header class="site-header">
    <a class="logo" href="#top" aria-label="橄榄巷首页">
      <svg viewBox="0 0 38 38" aria-hidden="true"><path d="M19 3.5c6.7 0 12.1 5.4 12.1 12.1S25.7 27.7 19 34.5C12.3 27.7 6.9 22.3 6.9 15.6S12.3 3.5 19 3.5Z" fill="none" stroke="currentColor" stroke-width="1.5"/><path d="M12.5 20.5c4.2-1.4 7.8-4.8 10.5-10.4M17 18.5c2.9.1 5.6 1.1 8 3.1M13.4 14.9c2.3.1 4.3.7 6.1 1.9" fill="none" stroke="currentColor" stroke-width="1.4" stroke-linecap="round"/></svg>
      <span>OLIVE<br /><em>LANE</em></span>
    </a>
    <button class="menu-toggle" :aria-label="isMenuOpen ? '关闭导航菜单' : '打开导航菜单'" :aria-expanded="isMenuOpen" @click="isMenuOpen = !isMenuOpen">
      <span></span><span></span>
    </button>
    <nav class="main-nav" :class="{ open: isMenuOpen }" aria-label="主导航">
      <a v-for="item in navigationItems" :key="item.href" :href="item.href" @click="closeMenu">{{ item.label }}</a>
    </nav>
    <a class="button button-small reservation-link" href="#reserve">预约餐桌 <span>↗</span></a>
  </header>
</template>
