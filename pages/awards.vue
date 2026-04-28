<script setup lang="ts">
import { awards } from '~/data/awards'

useHead({ title: 'Awards' })
</script>

<template>
  <h1 class="font-mono font-semibold text-gray-900 dark:text-zinc-100 text-xl tracking-tight mb-10">Awards</h1>
  <section id="awards">
    <ul class="space-y-4">
      <li v-for="(award, i) in awards" :key="i" class="flex gap-1 text-sm">
        <span class="text-gray-300 dark:text-zinc-600 shrink-0 mt-0.5 select-none">–</span>
        <div>
          <a :href="award.url" target="_blank" rel="noopener" class="font-medium text-gray-800 dark:text-zinc-200 dark:hover:text-primary hover:text-primary transition-colors">{{ award.title }}</a>
          <p class="text-[0.72rem] text-gray-400 dark:text-zinc-500 font-mono">{{ award.organization }}</p>
          <p class="text-[0.72rem] text-gray-400 dark:text-zinc-500 font-mono">{{ award.year }}</p>
        </div>
      </li>
    </ul>
  </section>
</template>
