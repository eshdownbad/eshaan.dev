<template>
  <div class="container mx-auto">
    <section
      class="mx-auto mt-10 flex w-full flex-row gap-8 rounded-xl bg-slate-400 p-8 shadow-lg shadow-slate-700 md:w-3/4"
    >
      <div
        class="flex flex-1 flex-col justify-center rounded-2xl bg-gray-800 text-center text-white"
      >
        <h1 class="text-3xl">Eshaan</h1>
      </div>
      <div class="flex-1">
        <div class="flex flex-col gap-2">
          <a
            v-for="linkData in LINKS"
            :key="linkData.link"
            class="rounded-2xl border-2 border-gray-800 p-3 text-center text-xl font-bold text-gray-800 transition-colors duration-300 hover:bg-gray-800 hover:text-white"
            :href="linkData.link"
          >
            {{ linkData.title }}
          </a>
        </div>
      </div>
    </section>
  </div>
</template>
<script lang="ts" setup>
const LINKS = [
  {
    title: 'Twitter',
    link: 'https://twitter.com/eshdownbad',
  },
  {
    title: 'Github',
    link: 'https://github.com/eshdownbad',
  },
  {
    title: 'Email',
    link: 'mail:contact@eshaan.dev',
  },
] as const;
useHead({
  bodyAttrs: {
    class: 'dark:bg-gray-900',
  },
});
</script>
