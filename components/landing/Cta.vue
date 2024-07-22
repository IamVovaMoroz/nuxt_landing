<!-- When hovering, the text is white and the background is black. only the text moves -->
<!-- 
<template>
  <div
    class="bg-black px-20 py-20 mt-[32px] mx-auto max-w-5xl rounded-lg flex flex-col items-center text-center"
  >
    <h2 class="text-white text-2xl sm:text-4xl md:text-6xl typing-animation-unique">Build products, faster.</h2>
    <div class="flex mt-5">
      <LandingLink class="button" href="#" styleName="inverted" data-hover-text="Started">
        <span class="button-text">Get Started</span>
      </LandingLink>
    </div>
  </div>
</template>


<style scoped>


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

.button {
  position: relative;
  overflow: hidden;
  display: inline-block;
  padding: 10px 20px;
  color: white;
  background-color: black;
  border: 4px solid white; /* Added white border */
  cursor: pointer;
  text-align: center;
  transition: background-color 0.3s, color 0.3s;
}

.button .button-text {
  position: relative;
  display: inline-block;
  transition: transform 0.3s;
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
  color: white;
  background-color: black;
  border: 1px solid black;
  transition: transform 0.3s;
  transform: translateY(-100%);
}

</style> -->

<!-- 2) when hovering, the text changes to black and the background is white -->


 <template>
  <div class="bg-black px-20 py-20 mt-[32px] mx-auto max-w-5xl rounded-lg flex flex-col items-center text-center">
    <h2 class="text-white text-2xl sm:text-4xl md:text-6xl typing-animation-unique">Build products, faster.</h2>
    <div class="flex mt-5">
      <LandingLink class="button" href="#" data-hover-text="Started">
        <span class="button-text">Get Started</span>
      </LandingLink>
    </div>
  </div>
</template>

<style scoped>
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

.button {
  position: relative;
  overflow: hidden;
  display: inline-block;
  padding: 10px 20px;
  color: white; /* Text color for default state */
  background-color: black; /* Background color for default state */
  border: 2px solid white; /* White border for default state */
  cursor: pointer;
  text-align: center;
  transition: background-color 0.3s, color 0.3s, border-color 0.3s; /* Transition for background, text color, and border color */
}

.button .button-text {
  position: relative;
  display: inline-block;
  transition: transform 0.3s; /* Transition for text movement */
}

.button:hover {
  background-color: white; /* Background color on hover */
  color: black; /* Text color on hover */
  border-color: black; /* Border color on hover */
  
}

.button:hover .button-text {
  transform: translateY(-124%); /* Move text up on hover */
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
  color: black; /* Text color on hover */
  background-color: white; /* Background color on hover */
  border: 2px solid white; /* Border color on hover */
  transition: transform 0.3s; /* Transition for the sliding effect */
  transform: translateY(-100%); /* Move the hover text into view */
}
</style>
