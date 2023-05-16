<template>
    <header-bar class="hidden from-top"></header-bar>
    <div style="height: 100px"></div>
    <div class="grid-container">
        <top-grid class="hidden"></top-grid>
        <div style="height: 100px"></div>
        <chronology-card class="hidden from-bottom"></chronology-card>

    </div>
</template>

<script>

import TopGrid from "@/components/top-grid.vue";
import HeaderBar from "@/components/header-bar.vue";
import ChronologyCard from "@/components/chronology-components/chronology-card.vue";

export default {
    name: 'App',
    mounted() {
        const observer = new IntersectionObserver( (entries) => {
            entries.forEach((entry) => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('show');
                } else {
                    entry.target.classList.remove('show');
                }
            });
        });


        const hiddenElements = document.querySelectorAll('.hidden');
        hiddenElements.forEach((element) => observer.observe(element));

        setTimeout( () => {
            document.querySelector(".from-bottom").classList.add("show")
        }, 1500)
    },
    components: {
      ChronologyCard,
      HeaderBar,
      TopGrid,
    },
}
</script>

<style>
    @font-face {
        font-family: VT323;
        src: url("../public/fonts/VT323-Regular.ttf");
    }

    @font-face {
        font-family: Montserrat;
        src: url("../public/fonts/Montserrat-VariableFont_wght.ttf");
    }

    body {
        padding: 0;
        margin: 0;
        font-family: Montserrat, sans-serif;
        -ms-overflow-style: none;  /* IE and Edge */
        scrollbar-width: none;  /* Firefox */
    }
    body::-webkit-scrollbar {
        display: none;
    }


    .hidden {
        opacity: 0;
        filter: blur(5px);
        transition: all 1s;
    }

    .hidden.from-top{
        transform: translateY(-100%);
    }

    .hidden.from-bottom{
        transform: translateY(200%);
    }

    .show {
        opacity: 1;
        filter: blur(0);
    }

    .show.from-top{
        transform: translateY(0);
    }
    .show.from-bottom{
        transform: translateY(0);
    }
    .grid-container{
        display: grid;
        justify-content: center;
    }
</style>
