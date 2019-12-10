<template functional>
  <div :class="{red: props.rng > .5, blue: props.rng <= .5}">
    <div v-if="props.rng">I am functional
      <functional />
    </div>
    <div v-else>
      I am child
    </div>
  </div>
</template>

<script>

import Functional from './Functional.vue'

export default {
  name: 'Functional',
  components: Functional
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