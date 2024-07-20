<template>
  <main class="grid lg:grid-cols-2 place-items-center pt-16 pb-8 md:pt-8 ">
    <div class="p-24 md:order-1 hidden md:block">
      <!-- <img class="rounded-full transition-transform transform hover:scale-125" src="~/assets/img/laptop2.webp" -->
      <img class="rounded-full transition-transform transform hover:scale-125" src="~/assets/img/laptop2.webp"
        alt="laptop img" loading="eager" format="avif" width="512" height="512" />
    </div>

    <div>
      <h1 class="text-5xl lg:text-6xl xl:text-7xl font-bold lg:tracking-tight text-shadow-3d">
        The Future of SaaS Products is Here
      </h1>
      <p class="text-lg mt-4 text-slate-600 max-w-xl">
        Introducing Qelos, an innovative platform that revolutionizes the creation and management of SaaS products.
        Whether you're a developer or not, Qelos provides a comprehensive suite of tools that make building, editing,
        enhancing, and modifying your SaaS applications easier and faster than ever.
      </p>
      <div class="mt-6 flex flex-col sm:flex-row gap-3">
        <LandingLink class="button" href="#" target="_blank" rel="noopener" data-hover-text="Started">
          <span class="button-text">Get Started</span>
        </LandingLink>
        <LandingLink class="button outline" size="lg" styleName="outline" rel="noopener" href="https://gitlab.com/qelos"
          target="_blank" data-hover-text="Repo">
          <span class="button-text">View Repo</span>
        </LandingLink>
      </div>
    </div>
  </main>
</template>

<style scoped>
.button {
  position: relative;
  overflow: hidden;
  display: inline-block;
  padding: 10px 20px;
  color: white;
  background-color: black;
  border: 1px solid black;
  cursor: pointer;
  transition: background-color 0.3s, color 0.3s;
  text-align: center;

}

.button .button-text {
  position: relative;
  display: inline-block;
  transition: transform 0.3s;
}

.button:hover {
  background-color: rgb(255, 255, 255);
  color: black;
}

.button:hover .button-text {
  transform: translateY(-124%);
}

.button:hover::before {
  content: attr(data-hover-text);
  position: absolute;
  top: 100%;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid black;

  color: black;
  transition: transform 0.3s;
  transform: translateY(-100%);

}

.button.outline {
  background-color: white;
  color: black;

}

.button.outline:hover::before {
  content: attr(data-hover-text);
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  /* background-color: rgba(226, 225, 225, 0.836); */
  color: black;
  transition: transform 0.3s;
  transform: translateY(0);

}
</style>
