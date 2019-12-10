<template functional>
  <div :class="{red: props.rng > .5, blue: props.rng <= .5}">
    {{props.rng}}
  </div>
</template>

<script>
export default {

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