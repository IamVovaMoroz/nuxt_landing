<script setup>
definePageMeta({
  layout: "landing",
});
</script>

<template>
  <LandingContainer>
    <LandingSectionhead>
      <template v-slot:title>About</template>
      <template v-slot:desc>
        We are a passionate team dedicated to empowering the world with innovative SaaS solutions.
      </template>
    </LandingSectionhead>


    <div class="relative w-full h-64 md:h-[400px] lg:h-[500px] overflow-hidden mt-4">
      <img class="absolute inset-0 object-cover" src="~/assets/img/team.jpg" alt="team image" loading="eager"
        format="avif" />
    </div>

    <div class="flex flex-col gap-4 mx-auto max-w-4xl mt-4  px-4">
      <p class="text-lg leading-relaxed text-slate-600">
        We are a dedicated team of SaaS specialists focused on delivering high-quality products and exceptional customer
        service. Our diverse backgrounds and shared commitment to excellence drive us to provide solutions that are both
        innovative and effective. Discover the team that’s here to support you every step of the way.
      </p>
    </div>
  </LandingContainer>
</template>
