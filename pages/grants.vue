<script setup lang="ts">
import { grants } from '~/data/grants'

useHead({ title: 'Grants' })
</script>

<template>
  <h1 class="font-mono font-semibold text-gray-900 dark:text-zinc-100 text-xl tracking-tight mb-10">Grants</h1>
  <section id="grants">
    <ul class="space-y-4">
      <li v-for="(grant, i) in grants" :key="i" class="flex gap-1 text-sm">
        <span class="text-gray-300 dark:text-zinc-600 shrink-0 mt-0.5 select-none">–</span>
        <div>
          <p><a :href="grant.url" target="_blank" rel="noopener" class="font-medium text-gray-800 dark:text-zinc-200 dark:hover:text-primary hover:text-primary transition-colors">{{ grant.name }}</a></p>
          <p><a :href="grant.orgurl" target="_blank" rel="noopener" class="text-[0.72rem] text-gray-400 dark:text-zinc-500 font-mono hover:underline">{{ grant.organization }}</a></p>
          <p class="text-[0.72rem] text-gray-400 dark:text-zinc-500 font-mono">{{ grant.year }}</p>
        </div>
      </li>
    </ul>
  </section>
</template>
