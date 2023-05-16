

<template>
    <display-card style="height: 100vh" id="chrono-card">

        <div class="title"> <h1>About me.</h1> <hr> </div>
        <div style="height: 50px"></div>
        <div class="chronology">
            <div class="history" style="margin-right: 5px">
                <h2> Education </h2>
                <chronology-point title="Instituto Superior Técnico"
                                  desc="Bachelor in Electrical and Computer Engineering" date="2019 - 2024">
                </chronology-point>
            </div>
            <div class="history" style="margin-left: 5px">
                <h2> Experience </h2>
                <chronology-point title="CELFOCUS"
                                  desc="Intern trainee - Software Developer" date="March 2022 - September 2022">
                </chronology-point>
                <chronology-point title="Freelance"
                                  desc="Web Developer" date="June 2021 - September 2021">
                </chronology-point>
                <chronology-point title="Freelance"
                                  desc="Flutter Developer" date="January 2021 - June 2021">
                </chronology-point>
                <chronology-point title="General Assembly"
                                  desc="Teaching Assistant" date="September 2019">
                </chronology-point>
            </div>
        </div>
    </display-card>
</template>

<script>

import displayCard from "@/components/display-card.vue";
import ChronologyPoint from "@/components/chronology-components/chronology-point.vue";

export default {
    mounted() {
        const maxWidth = document.getElementById('chrono-card').offsetWidth;
        this.maxWidth = maxWidth + "px";
    },
    data(){
        return{
            maxWidth: ""
        }
    },
    components: {
        ChronologyPoint,
        displayCard
    }
}

</script>

<style scoped>
    h1 {
        font-weight: normal;
    }

    .title{
        justify-self: center;
        height: auto;
    }

    .chronology {
        display: flex;
        flex-direction: row;

        justify-content: space-around;
        justify-items: start;
        width: v-bind(maxWidth);
    }

    .history {
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
    }

    .history h2{
        font-weight: normal;
        text-decoration-line: underline;
    }


</style>