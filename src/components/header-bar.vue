

<template>
    <header>
        <div class="logo">
            JW
        </div>
        <div ref="options" class="options">
            <div>About</div>
            <div>Skills</div>
            <div>Portfolio</div>
            <div>Contact</div>
        </div>
    </header>
</template>

<script>
export default {
    data(){
            return {
                imgHeight: 0
        }
    },
    mounted() {
        this.imgHeight = this.$refs.options.clientHeight
    }
}

</script>

<style scoped>




    header {
        display: grid;
        grid-auto-flow: column;
        grid-template-columns: repeat(auto-fit, 1fr);
        justify-content: space-around;
        background: ghostwhite;
        padding: 5px 20px;
        border-bottom: 2px solid grey;
        width: 100vw;
    }

    header .logo{
        max-height: 75px;
        align-items: center;
        display: grid;
        font-size: 2em;
    }

    header .options {
        display: grid;
        grid-auto-flow: column;
        grid-template-columns: repeat(auto-fit, 1fr);
        align-items: center;
        gap: 30px;
        min-height: 50px;
    }



</style>