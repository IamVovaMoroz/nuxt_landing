<template>
  <footer class="my-20">
    <div class="flex flex-col items-center">
      <!-- Copyright -->
      <p class="text-center text-sm text-slate-500">
        Copyright © {{ new Date().getFullYear() }} Qelos. All rights reserved.
      </p>

      <div class="flex gap-6 mt-6">
        <!-- LinkedIn -->
        <a href="https://www.linkedin.com/company/qelos/" target="_blank" rel="noopener"
          class="flex items-center text-gray-600 hover:text-gray-900">
          <IconsLinkedinIcon class="w-8 h-8" />
          <span class="sr-only">LinkedIn</span>
        </a>

        <!-- GitLab Repo -->
        <a href="https://gitlab.com/qelos" target="_blank" rel="noopener"
          class="flex items-center text-gray-600 hover:text-gray-900">
          <IconsGitlabIcon class="w-8 h-8" />
          <span class="sr-only">GitLab Repository</span>
        </a>
        <!-- Documentation -->
        <a href="https://docs.qelos.io/" target="_blank" rel="noopener"
          class="flex items-center text-gray-600 hover:text-gray-900">
          <IconsDocsIcon class="w-8 h-8" />
          <span class="sr-only">Documentation</span>
        </a>
        <!-- Discord -->
        <a href="https://discord.gg/5KvhSesM" target="_blank" rel="noopener"
          class="flex items-center text-gray-600 hover:text-gray-900">
          <IconsDiscordIcon class="w-8 h-8" />
          <span class="sr-only">Discord</span>
        </a>
      </div>
    </div>
  </footer>
</template>
