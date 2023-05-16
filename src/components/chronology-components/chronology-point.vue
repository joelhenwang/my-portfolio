
<template>
    <div class="chrono-point">
        <div class="exp-breakpoint">
            <div class="circle"></div>
            <div class="exp-line"></div>
        </div>

        <div class="experience">
            <div class="exp-title">
                {{title}}
            </div>
            <div class="exp-desc">
                {{desc}}
            </div>
            <div class="exp-date">
                {{date}}
            </div>
        </div>
    </div>

</template>

<script>
    export default {
        props: {
            title: String,
            desc: String,
            date: String
        }
    }
</script>

<style scoped>
    .chrono-point{
        display: flex;
    }

    .experience{
        padding-left: 10px;
    }
    .exp-breakpoint{
        display: flex;
        width: 1.5em;
        height: 150px;
        flex-direction: column;
        justify-content: flex-start;
        align-content: center;
        justify-self: center;
        align-items: center;
    }

    .exp-breakpoint .circle{
        border-radius: 50%;
        background-color: #3d9c6c;
        width: 1.5em;
        height: 1.5em;
    }

    .exp-line{
        width: 2px;
        height: calc(150px - 1.5em);
        background: black;
    }

    .exp-title{
        font-size: 1.1em;
    }
    .exp-desc{
        font-size: 0.9em;
    }
    .exp-date{
        font-size: 0.8em;
        color: grey;
    }
</style>