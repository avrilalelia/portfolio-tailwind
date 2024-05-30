<!-- eslint-disable no-unexpected-multiline -->
<template>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&family=Zen+Antique&display=swap"
    rel="stylesheet"
  />
  <HeaderPart />
  <HeroPart />
  <AboutPart />
  <ProjectsPart />
  <HireMePart />
</template>

<script>
import HeaderPart from "./components/Header.vue";
import HeroPart from "./components/Hero.vue";
import AboutPart from "./components/About.vue";
import ProjectsPart from "./components/Projects.vue";
import HireMePart from "./components/HireMe.vue";

export default {
  name: "App",
  components: {
    HeaderPart,
    HeroPart,
    AboutPart,
    ProjectsPart,
    HireMePart,
  },
  mounted() {
    document.body.classList.add(
      "bg-body",
      "text-white",
      "font-poppins",
      "pb-12"
    );

    // if (confirm("Apakah Anda yakin ingin mendownload resume?") == true) {
    //   showResume();
    //   alert("Resume telah didownload");
    // } else {
    //   alert("Download dibatalkan");
    // }

    // function showResume(){
    //   window.location.href = "https://avrilalelia.github.io/portfolio-tailwind/resume";
    // }

    // const d = new Date();
    // const bulan = ["January","February","March","April","May","June","July","August","September","October","November","December"];
    // const hari = ["Minggu", "Senin", "Selasa", "Rabu", "Kamis", "Jumat", "Sabtu"];
    // const time = {
    //   day: hari[d.getDay()],
    //   date: d.getDate(),
    //   month: bulan[d.getMonth()],
    //   year: d.getUTCFullYear()
    // };

    // alert("Selamat datang! Anda membuka website ini pada: "+time.day+", "+time.date+" "+time.month+" "+time.year);

    function updateList() {
      const titles = [...document.querySelectorAll("h1, h2")].sort((a, b) => {
        return (
          Math.abs(a.getBoundingClientRect().top) -
          Math.abs(b.getBoundingClientRect().top)
        );
      });

      document
        .querySelectorAll(".selected-circle")
        .forEach((c) => c.classList.remove("selected-circle"));

      document.querySelectorAll(".nav-dot")[
        // eslint-disable-next-line no-unexpected-multiline
        [...document.querySelectorAll("h1, h2")].indexOf(titles[0])
      ].classList.add("selected-circle");
    }
    updateList();
    window.addEventListener("scroll", () => {
      updateList();
    });
  },
};
</script>
