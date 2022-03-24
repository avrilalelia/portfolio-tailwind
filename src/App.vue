<template>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&family=Zen+Antique&display=swap"
    rel="stylesheet"
  />
  <HeaderPart />
  <HeroPart />
  <MyWorkPart />
  <ClientsPart />
  <HireMePart />
</template>

<script>
function updateList() {
	const titles = [...document.querySelectorAll('h1, h2')].sort((a, b) => {
		return Math.abs(a.getBoundingClientRect().top) - Math.abs(b.getBoundingClientRect().top);
	});

	document.querySelectorAll(".selected-circle").forEach(c => c.classList.remove("selected-circle"));
	
	document.querySelectorAll(".nav-dot")[[...document.querySelectorAll('h1, h2')].indexOf(titles[0])].classList.add("selected-circle");
}

updateList();
window.addEventListener('scroll', () => {
    updateList();
})

import HeaderPart from "./components/Header.vue";
import HeroPart from "./components/Hero.vue";
import MyWorkPart from "./components/MyWork.vue";
import ClientsPart from "./components/Clients.vue";
import HireMePart from "./components/HireMe.vue";

export default {
  name: "App",
  components: {
    HeaderPart, HeroPart, MyWorkPart, ClientsPart, HireMePart
  },
  mounted() {
    document.body.classList.add("bg-body", "text-white", "font-poppins", "pb-12");
  },
};
</script>
