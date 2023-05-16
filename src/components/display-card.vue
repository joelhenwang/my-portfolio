<script>

</script>

<template>
  <div class="card">
      <slot/>
  </div>
</template>

<style scoped>
  .card{
      display: grid;
      box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
      padding: 10px;
      justify-content: center;
      align-content: start;
  }
</style>