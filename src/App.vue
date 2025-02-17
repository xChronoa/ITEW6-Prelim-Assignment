<script setup>
import { RouterLink, RouterView } from 'vue-router'
import PageFooter from './components/PageFooter.vue'
</script>

<template>
  <header>
    <nav class="bg-purple-800 text-white flex justify-center items-center gap-8 uppercase py-4">
      <RouterLink
        class="text-lg tracking-[.2rem] relative after:bg-yellow-500 after:absolute after:h-0.5 after:w-0 after:bottom-[-0.4rem] after:left-0 hover:after:w-full after:duration-300 transition-all cursor-pointer font-medium hover:text-yellow-500"
        to="/"
      >
        Home
      </RouterLink>
      <RouterLink
        class="text-lg tracking-[.2rem] relative after:bg-yellow-500 after:absolute after:h-0.5 after:w-0 after:bottom-[-0.4rem] after:left-0 hover:after:w-full after:duration-300 transition-all cursor-pointer font-medium hover:text-yellow-500"
        to="/skills"
        >Skills</RouterLink
      >
      <RouterLink
        class="text-lg tracking-[.2rem] relative after:bg-yellow-500 after:absolute after:h-0.5 after:w-0 after:bottom-[-0.4rem] after:left-0 hover:after:w-full after:duration-300 transition-all cursor-pointer font-medium hover:text-yellow-500"
        to="/contact"
        >Contact</RouterLink
      >
    </nav>
  </header>
  <RouterView class="flex flex-col justify-center items-center min-h-screen" />
  <PageFooter />
</template>

<style>
.router-link-active,
.router-link-exact-active {
  color: oklch(0.795 0.184 86.047);
  position: relative; /* Ensure correct positioning */
}

.router-link-active::after,
.router-link-exact-active::after {
  content: '';
  position: absolute;
  bottom: -0.4rem;
  left: 0;
  width: 100%;
  height: 2px;
  background-color: oklch(0.795 0.184 86.047);
  transition: width 300ms ease;
}

.router-link-active:hover,
.router-link-exact-active:hover {
  color: oklch(0.795 0.184 86.047);
}
</style>
