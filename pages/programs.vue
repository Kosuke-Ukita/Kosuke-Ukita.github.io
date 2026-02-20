<script setup lang="ts">
import { profile } from '~/data/profile'
import { programs } from '~/data/programs'
</script>

<template>
  <main class="max-w-5xl mx-auto px-6 py-10">
    
    <div class="flex items-center gap-6 mb-12 border-b border-slate-100 pb-8">
      <div class="w-20 h-20 rounded-full overflow-hidden shadow-xl border-2 border-slate-100 shrink-0">
        <img src="/assets/photo.jpg" alt="Profile" class="w-full h-full object-cover" onerror="this.onerror=null; this.src='https://placehold.co/200x200?text=Photo'"/>
      </div>
      
      <div>
        <h1 class="text-2xl font-bold text-slate-900">{{ profile.name }}</h1>
        <p class="text-slate-500 text-sm flex items-center gap-2"><Icon name="heroicons:academic-cap" /> {{ profile.role }}</p>
      </div>
    </div>
    <section id="programs" class="scroll-mt-24">
      <h3 class="text-2xl font-bold text-slate-900 flex items-center gap-2 mb-8"><Icon name="heroicons:command-line" class="text-primary" /> Programs </h3>


      <div v-for="program in programs" :key="program.id"
        class="overflow-hidden transition-all duration-500 group relative backdrop-blur-md bg-white/80 hover:backdrop-blur-xl hover:bg-white/50">
        
        <!-- Background thumbnail with gradient fade -->
        <div v-if="program.thumbnail" class="absolute inset-0 -z-10 width=150%">
          <img :src="program.thumbnail" :alt="program.title"
            class="w-full h-full object-cover opacity-90 scale-105 transition-all duration-500 group-hover:opacity-40 group-hover:blur-sm" />
          <!-- Gradient overlay: transparent center → page background edges -->
          <div class="absolute inset-0 bg-gradient-to-r from-white via-transparent to-white"></div>
          <!-- <div class="absolute inset-0 bg-gradient-to-l from-white via-transparent to-white"></div> -->
        </div>

        <!-- Liquid glass highlight layer -->
        <div class="absolute inset-0 -z-10 bg-gradient-to-br from-white/10 via-white/5 to-transparent pointer-events-none transition-all duration-500 group-hover:from-white/10 group-hover:via-white/50"></div>

        <a :href="program.url" target="_blank" rel="noopener noreferrer" class="block">
        <div class="relative p-6 flex flex-col gap-3">
          <div class="flex flex-col gap-8
               px-3 py-3 rounded-xl
               bg-white/10 backdrop-blur-sm
               shadow-[inset_0_1px_0_rgba(255,255,255,0.4),0_4px_12px_rgba(0,0,0,0.15)]
               border border-white/20
               group-hover:bg-white/20 group-hover:border-white/30
               transition-all duration-300">
            <div class="flex items-start justify-between">
              <h4 class="text-xl font-semibold text-black/40 drop-shadow-[0_1px_4px_rgba(0,0,0,0.3)] group-hover:drop-shadow-[0_2px_8px_rgba(0,0,0,0.4)] group-hover:text-black/80 transition-all duration-300">
              {{ program.title }}
              </h4>
            <a :href="program.githubUrl" target="_blank" rel="noopener noreferrer"
               class="text-black/40 hover:text-black transition-colors drop-shadow-md ml-3 shrink-0"
               @click.stop>
              <Icon name="mdi:github" class="w-6 h-6" />
            </a>
            </div>

            <p class="text-sm
              text-black/40 drop-shadow-sm
              group-hover:text-black/80 group-hover:drop-shadow-lg
              transition-all duration-300 leading-relaxed">
            {{ program.description }}
            </p>
          </div>
        </div>
        </a>
      </div>
    </section>

  </main>
</template>