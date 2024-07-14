<script setup>
const features = [
  {
    title: "Accelerated Product Development",
    description:
      "Achieve your product goals faster than ever with our automated solutions and dedicated team, ensuring efficient transitions from concept to reality.",
    icon: "bx:rocket",
  },
  {
    title: "Open-Source Automation Tools",
    description:
      "Streamline your publishing process with our open-source tools, bringing your product to market swiftly within a transparent, community-driven environment.",
    icon: "bx:world",
  },
  {
    title: "Focused on SaaS Product Delivery",
    description:
      "Specializing in SaaS product delivery, our automated tools help reduce costs while ensuring secure, scalable, and high-quality products.",
    icon: "bx:package",
  },
  {
    title: "Self-Maintenance with Open-Source Tools",
    description:
      "Our open-source tools provide the flexibility to maintain and customize your product independently after deployment.",
    icon: "bx:wrench",
  },
  {
    title: "Plugin Management",
    description:
      "Effortlessly create, configure, and manage plugins with our intuitive system, making it simple to extend your product's functionality.",
    icon: "bx:cog",
  },
  {
    title: "Automated Screen Building",
    description:
      "Customize your product with ease using our visual WYSIWYG editor, enabling screen and interface modifications without coding.",
    icon: "bx:desktop",
  },
  {
    title: "Self-Hosted or Managed Solutions",
    description:
      "Choose between fully managed services or self-hosting options, allowing you to host the entire SaaS solution or manage specific microservices.",
    icon: "bx:globe",
  },
  {
    title: "Customized Development Solutions",
    description:
      "Our expert team offers tailored software solutions to meet your unique needs, delivering new features and custom integrations using our tools and expertise.",
    icon: "bx:sort",
  },
  
];
</script>
<!-- https://boxicons.com/ for icons -->

<!-- <template>
  <div class="mt-16 md:mt-0">
    <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight mb-[30px]">
      How QELOS Enhances Your SaaS Development Experience
    </h2>

<div class="relative w-full px-4 md:px-0 max-w-[90%] md:max-w-full mx-auto overflow-hidden">
      <img class="transition-transform duration-300 ease-in-out hover:scale-105 object-cover w-full h-auto"
    src="~/assets/img/laptop_big.webp"
    alt="Laptop image" loading="eager" format="avif" />
</div>

 
  </div>

  <div class="grid sm:grid-cols-2 md:grid-cols-3 mt-16 gap-16">
    <div v-for="item of features" class="flex gap-4 items-start">
      <div class="mt-1 bg-black rounded-full p-2 w-8 h-8 shrink-0">
        <Icon class="text-white" :name="item.icon" />
      </div>
      <div>
        <h3 class="font-semibold text-lg">{{ item.title }}</h3>
        <p class="text-slate-500 mt-2 leading-relaxed">
          {{ item.description }}
        </p>
      </div>
    </div>
  </div>
</template> -->

<template>
  <div class="mt-16 md:mt-0">
    <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight mb-[30px]">
      How QELOS Enhances Your SaaS Development Experience
    </h2>


    <img class="w-full h-96 "
         src="~/assets/img/3.jpg"
         alt="server image"
         loading="eager"
         format="avif"
         width="1920"
         height="1080" />


    <div class="grid sm:grid-cols-2 md:grid-cols-3 mt-16 gap-16 fade-in-container">
      <div
        v-for="(item, index) in features"
        :key="index"
        :style="{ '--index': index }"
        class="fade-in card"
      >
        <div class="flex gap-4 items-start">
          <div class="mt-1 bg-black rounded-full p-2 w-8 h-8 shrink-0">
            <Icon class="text-white" :name="item.icon" />
          </div>
          <div>
            <h3 class="font-semibold text-lg">{{ item.title }}</h3>
            <p class="text-slate-500 mt-2 leading-relaxed">
              {{ item.description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>


@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.fade-in {
  opacity: 0;
  animation: fadeIn 0.9s ease-in-out forwards;
  animation-delay: calc(var(--stagger) * 0.1s);
}

.fade-in-container > div {
  --stagger: var(--index);
}

.card {
  position: relative;
  perspective: 1000px;
  overflow: hidden;
  background: #ffffff;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transform-style: preserve-3d;
  transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
  transform: rotateX(0) rotateY(0);
}

.card:hover {

  background-color: #f0f4f8;
  transition: transform 0.3s ease-in-out;
  /* box-shadow: 0 15px 25px rgba(0, 0, 0, 0.3); */
  cursor: pointer;
}

.card:hover h3,
.card:hover p {
  color: #4b5563;
}

.card h3 {
  transition: color 0.3s ease-in-out;
}

.card p {
  transition: color 0.3s ease-in-out;
}

.card:hover .text-slate-500 {
  color: #4b5563;
}
</style>



