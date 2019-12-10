
<template>
  <div :class="{red: rng > .5, blue: rng <= .5}">
    I am not
  </div>
</template>

<script>
export default {
    props: {
        rng: Number
    }
}
</script>

<style scoped>
  .red {
    background: red;
    color: white;
  }
  .blue {
    background: blue;
    color: white;
  }
</style>