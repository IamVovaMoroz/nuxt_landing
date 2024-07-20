<script setup>
const menuitems = [
  {
    title: "Home",
    path: "/",
  },
  {
    title: "About",
    path: "/about",
  },
  {
    title: "Contact",
    path: "/contact",
  },
];

const open = ref(false);
</script>

<template>
  <LandingContainer>
    <header class="flex flex-col lg:flex-row justify-between items-center my-5">
      <div class="flex w-full lg:w-auto items-center justify-between">
        <a href="/" class="text-lg flex items-center">
          <img class="w-8 h-8 mr-2" src="~/assets/img/qelos_logo.jpg" alt="Qelos Logo" />
          <span class="font-bold text-slate-800">QELOS</span>
        </a>
        <div class="block lg:hidden">
          <button @click="open = !open" class="text-gray-800">
            <svg fill="currentColor" class="w-4 h-4" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
              <title>Menu</title>
              <path v-show="open" fill-rule="evenodd" clip-rule="evenodd"
                d="M18.278 16.864a1 1 0 01-1.414 1.414l-4.829-4.828-4.828 4.828a1 1 0 01-1.414-1.414l4.828-4.829-4.828-4.828a1 1 0 011.414-1.414l4.829 4.828 4.828-4.828a1 1 0 111.414 1.414l-4.828 4.829 4.828 4.828z">
              </path>
              <path v-show="!open" fill-rule="evenodd"
                d="M4 5h16a1 1 0 010 2H4a1 1 0 110-2zm0 6h16a1 1 0 010 2H4a1 1 0 010-2zm0 6h16a1 1 0 010 2H4a1 1 0 010-2z">
              </path>
            </svg>
          </button>
        </div>
      </div>
      <nav class="w-full lg:w-auto mt-2 lg:flex lg:mt-0" :class="{ block: open, hidden: !open }">
        <ul class="flex flex-col lg:flex-row lg:gap-3">
          <li v-for="item of menuitems" :key="item.title" class="relative group">
            <a :href="item.path" :target="item.target || '_self'"
              :rel="item.target === '_blank' ? 'noopener noreferrer' : ''"
              class="relative inline-block py-2 text-lg text-gray-600 hover:text-gray-900">
              {{ item.title }}
              <span class="underline-effect"></span>
            </a>
          </li>
        </ul>
        <div class="lg:hidden flex items-center mt-3 gap-4">
          <!-- Mobile menu -->
          <LandingLink href="https://docs.qelos.io/getting-started/intro.html" styleName="muted" block size="md">Docs
          </LandingLink>
          <LandingLink href="https://gitlab.com/qelos" size="md" block>Gitlab</LandingLink>
        </div>
      </nav>
      <div>
        <div class="hidden lg:flex items-center gap-4">
          <a href="https://docs.qelos.io/getting-started/intro.html" target="_blank"
            class="flex items-center text-lg text-gray-600 hover:text-gray-900">
            <IconsDocsIcon class="w-7 h-7 mr-2" />
            Docs
          </a>

          <a href="https://gitlab.com/qelos" target="_blank"
            class="flex items-center text-lg text-gray-600 hover:text-gray-900">
            <IconsGitlabIcon class="w-7 h-7 mr-2" />
            GitLab
          </a>

          <a href="https://discord.com/channels/1105863727854649464/1249006082660237434" target="_blank"
            class="flex items-center text-lg text-gray-600 hover:text-gray-900">
            <IconsDiscordIcon class="w-7 h-7 mr-2" />
            Discord
          </a>
        </div>
      </div>
    </header>
  </LandingContainer>
</template>

<style scoped>
.underline-effect {
  display: inline-block;
  width: 100%;
  height: 3px;
  background: currentColor;
  transform: scaleX(0);
  transform-origin: bottom right;
  transition: transform 0.3s ease-out;
  margin-top: -4px;
}

a:hover .underline-effect {
  transform: scaleX(1);
  transform-origin: bottom left;
}
</style>
