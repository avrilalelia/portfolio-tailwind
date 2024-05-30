<template>
  <header class="py-6">
    <div
      class="container flex justify-between items-center mx-auto px-8 md:px-14 lg:px-24 w-full"
    >
      <div class="text-lg font-bold">Avril Alelia</div>
      <div class="hidden md:flex space-x-12 items-center">
        <a href="#" class="text-selected-text">Home</a>
        <a href="#about">About</a>
        <a href="#projects">Projects</a>
        <a href="#hire"
          ><button class="px-6 py-2 bg-theme font-bold">Contact Me</button></a
        >
      </div>
      <div class="md:hidden">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          height="24px"
          viewBox="0 0 24 24"
          width="24px"
          fill="#FFFFFF"
        >
          <path d="M0 0h24v24H0V0z" fill="none" />
          <path d="M3 18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z" />
        </svg>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderPart",
  setup() {},
};
</script>
