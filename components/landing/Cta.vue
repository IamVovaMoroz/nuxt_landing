<template>
  <div
    class="bg-black px-20 py-20 mt-20 mx-auto max-w-5xl rounded-lg flex flex-col items-center text-center"
  >
    <h2 class="text-white text-3xl md:text-6xl typing-animation-unique">Build products, faster.</h2>
    <!-- <p class="text-slate-500 mt-4 text-lg md:text-xl">
      Static or Dynamic, the choice is yours with Nuxts hybrid rendering modes.
    </p> -->
    <div class="flex mt-5">
      <LandingLink href="#" styleName="inverted">Get Started</LandingLink>
    </div>
  </div>
</template>

<style>

@keyframes typing-unique {
  from {
    width: 0;
  }
  to {
    width: 100%;
  }
}

@keyframes blink-caret-unique {
  from, to {
    border-color: transparent;
  }
  50% {
    border-color: white;
  }
}

.typing-animation-unique {
  overflow: hidden;
  border-right: .1em solid white;
  white-space: nowrap;
  letter-spacing: .15em;
  animation:
    typing-unique 3.5s steps(30, end),
    blink-caret-unique 1.5s step-end infinite;
}
</style>
