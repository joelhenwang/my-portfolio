<script>
    export default {
        data() {
            return {
                text1: "Hi, my name is Joel.\n" +
                    "I'm a Electrical and Computer Engineering student and aspiring to be a Software Engineer. Welcome!",
                i: 0,
                j: 0
            }
        },
        mounted() {

            this.typewriter1();

        },
        methods: {
            typewriter1(){
                if (this.i < this.text1.length){
                    document.getElementById("text1").innerHTML += this.text1.charAt(this.i);
                    this.i++;
                    setTimeout(this.typewriter1,30);
                }

            },
        }
    }
</script>

<template>
  <div class="top-grid">
      <div>
          <h2 class="text-writer" id="text1">

          </h2>

      </div>
      <div class="image"> <img alt="Vue logo" src="../assets/maleOnLaptop.png"> </div>
  </div>
</template>

<style scoped>
  .top-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(360px, 1fr));

      max-width: 1080px;
  }

  .top-grid .image{
      display: flex;
      align-items: flex-end;
      justify-content: flex-end;
  }

  h2.text-writer{
      font-family: VT323, monospace;
      font-weight: lighter;
      letter-spacing: 4px;
      font-size: 2em;
      color: #3d9c6c;
      overflow: hidden;
  }
  h2 span{
      font-weight: bold;
  }


</style>