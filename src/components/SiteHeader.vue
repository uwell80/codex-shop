<template>
  <header class="site-header" id="top">
    <a class="brand" href="#top" aria-label="沸堂火锅首页"><span>沸堂</span><i>FEI TANG</i></a>
    <button
      class="menu-toggle"
      :aria-expanded="menuOpen"
      aria-controls="nav"
      @click="menuOpen = !menuOpen"
    >
      菜单 <span></span>
    </button>
    <nav class="nav-links nav-desktop" aria-label="主导航">
      <a v-for="item in navItems" :key="item.href" :href="item.href">{{ item.label }}</a>
      <a class="reserve-link" href="#reserve">订一桌热辣 <b>↗</b></a>
    </nav>
    <Transition name="menu">
      <nav
        v-if="menuOpen"
        id="nav"
        class="nav-links nav-mobile"
        aria-label="主导航"
        @click="menuOpen = false"
      >
        <a v-for="item in navItems" :key="item.href" :href="item.href">{{ item.label }}</a>
        <a class="reserve-link" href="#reserve">订一桌热辣 <b>↗</b></a>
      </nav>
    </Transition>
  </header>
</template>

<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)
const navItems = [
  { label: '沸堂之味', href: '#story' },
  { label: '招牌涮品', href: '#menu' },
  { label: '堂食氛围', href: '#space' },
]
</script>
