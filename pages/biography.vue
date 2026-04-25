<script setup lang="ts">
useHead({ title: 'Biography' })
</script>

<template>
  <div>
    <h1 class="font-mono font-semibold text-gray-900 dark:text-zinc-100 text-xl mb-8 tracking-tight">Biography</h1>

    <div class="space-y-4 text-sm text-gray-700 dark:text-zinc-300 leading-relaxed max-w-prose">

      <p>
        Kosuke Ukita is a first-year PhD student in Computer Science and Systems Engineering
        at the
        <a href="https://www.kyutech.ac.jp/english/" target="_blank" rel="noopener" class="text-primary hover:underline underline-offset-2">Kyushu Institute of Technology</a>,
        advised by Associate Professor
        <a href="https://sites.google.com/view/okita-lab" target="_blank" rel="noopener" class="text-primary hover:underline underline-offset-2">Tsuyoshi Okita</a>.
        He is supported by the JST SPRING fellowship (JPMJSP2154).
      </p>

      <p>
        His research lies at the intersection of generative modelling and representation learning,
        with a particular focus on flow matching and its applications to sensor data.
        He is interested in developing efficient inference algorithms for continuous normalizing flows,
        leveraging generative pre-training for self-supervised learning,
        and building multimodal foundation models for human activity recognition.
      </p>

      <p>
        Kosuke received his MSc (2026) and BSc (2024) from Kyushu Institute of Technology.
        His master's thesis investigated sensor foundation models trained jointly with flow matching,
        leading to publications at
        AISTATS 2026 (Spotlight, top 3%) and PAKDD 2026 (Oral Presentation).
        He received the PAKDD 2026 Student Travel Award in recognition of this work.
      </p>

      <p>
        Beyond his primary research, he maintains a broad interest in the mathematical foundations
        of machine learning — particularly probabilistic modelling, optimal transport, and score-based methods —
        and enjoys following developments across the wider machine learning community.
      </p>

    </div>

    <!-- Placeholder note -->
    <p class="mt-10 text-[0.7rem] text-gray-300 dark:text-zinc-600 font-mono italic">
      * note placeholder.
    </p>
  </div>
</template>
