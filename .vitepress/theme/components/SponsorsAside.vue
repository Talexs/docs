<script setup lang="ts">
import SponsorsGroup from './SponsorsGroup.vue'
import { useData } from 'vitepress'
const { frontmatter } = useData()
</script>

<template>
  <div v-if="frontmatter.sponsors !== false">
    <a class="sponsors-aside-text" href="https://test.pvpin.net">独家支持</a>
    <SponsorsGroup tier="pvpin" />
  </div>
</template>

<style>
a.sponsors-aside-text {
  color: var(--vt-c-text-3);
  display: block;
  margin: 3em 0 1em;
  font-weight: 700;
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.4px;
}
</style>
