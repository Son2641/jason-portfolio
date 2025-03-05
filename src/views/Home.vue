<script setup lang="ts">
import AppAbout from "../components/AppAbout.vue";
import { projects } from "../projects";
</script>

<template>
  <main>
    <app-about class="my-16"></app-about>
    <!-- #Projects -->
    <div class="flex flex-col gap-2">
      <p class="text-3xl font-bold main-header text-white">Projects</p>
      <p class="italic text-sm">
        Note: Due to confidentiality, the codebase for some projects is private,
        and live links may not be publicly accessible. However, the projects
        below provide an overview of my contributions.
      </p>
      <div class="flex flex-col gap-6 my-4">
        <div
          v-for="project in projects"
          :key="project.name"
          class="flex md:flex-row flex-col gap-6 w-full"
        >
          <img
            :src="project.imgSrc"
            :alt="project.name"
            class="rounded-xl shadow-xl md:h-60 sm:h-72 h-48 md:w-[56%] w-full"
          />

          <div class="flex flex-col gap-2">
            <p class="main-header font-bold text-lg text-white">
              {{ project.name }}
            </p>
            <p>{{ project.overview }}</p>
            <p class="text-sm">Contribution: {{ project.contribution }}</p>
            <p class="text-sm">Technology used: {{ project.techStacks }}</p>
            <div class="w-full flex gap-2">
              <a
                v-if="project.link"
                :href="project.link"
                target="_blank"
                rel="noopener noreferrer"
                class="p-2 bg-slate-500 text-white rounded-lg hover:opacity-90 cursor-pointer font-bold"
                >Demo Site</a
              >
              <a
                v-if="project.github"
                :href="project.github"
                target="_blank"
                rel="noopener noreferrer"
                class="p-2 bg-stone-400 text-white rounded-lg hover:opacity-90 cursor-pointer font-bold"
                >Github Repository</a
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
