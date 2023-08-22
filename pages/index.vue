<script setup lang="ts">
useHead({
  title: 'FXJZZ',
})

const items = [
  { label: '介绍', route: '/intro' },
  { label: '开始', route: 'resume' },
  { label: 'github', route: 'https://github.com' },
]
</script>

<template>
  <div class="bg-#27292d w-full h-screen flex flex-col items-center c-white">
    <div class="w-600px flex-auto flex items-center flex-col mt-200px">
      <img src="/logo.png" alt="resume-logo" />
      <span class="font-size-28px">VisResumeMook</span>
      <span class="mt-40px font-size-16px">一个模板简历制作平台，轻松打造精美简历~</span>
      <div class="mt-16px w-280px flex justify-between bg-transparent">
        <NuxtLink v-for="item in items" :key="item.label" :to="item.route">
          <a-button>
            {{ item.label }}
          </a-button>
        </NuxtLink>
      </div>
    </div>
    <div class="h-60px m-auto">
      Copyright © 2002-{{ new Date().getFullYear() }} All Rights Reserved. Copyright By fxjzz
    </div>
  </div>
</template>
