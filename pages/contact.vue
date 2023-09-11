<template>
  <div class="app">
    <h3 v-if="ganteng">Gw ganteng</h3>
    <h3 v-else>Gw ttp ganteng</h3>
  </div>
</template>

<script>
  export default {
    el: '#app',
    name: 'ContactPage',
    data() {
      return {
        ganteng: true
      }
    }
  }
</script>
