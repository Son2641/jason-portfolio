<script setup lang="ts">
import LayoutDefault from "./layouts/LayoutDefault.vue";

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: "smooth" });
};
</script>

<template>
  <layout-default class="antialiased">
    <nav class="flex justify-between items-center">
      <p
        class="main-header text-3xl font-bold cursor-pointer"
        @click.prevent="scrollToTop()"
      >
        Jason Miranda
      </p>
    </nav>
    <main>
      <router-view></router-view>
    </main>
    <nav class="mt-12 flex justify-between items-center">
      <p>© Jason Miranda</p>
      <div class="flex sm:gap-6 gap-4">
        <a
          href="https://www.linkedin.com/in/louie-jason-miranda-36ba2b158/"
          target="_blank"
          rel="noopener noreferrer"
          class="flex items-center sm:gap-2 gap-1 sm:text-sm text-xs hover-white"
        >
          <img
            src="/linkedin_icon.png"
            alt="linkedin icon"
            class="sm:size-6 size-5 hover:opacity-20"
        /></a>
        <a
          href="https://github.com/Son2641"
          target="_blank"
          rel="noopener noreferrer"
          class="flex items-center sm:gap-2 gap-1 sm:text-sm text-xs hover-white"
        >
          <img
            src="/github_icon.png"
            alt="github icon"
            class="sm:size-6 size-5 hover:opacity-20"
        /></a>
      </div>
    </nav>
  </layout-default>
</template>
