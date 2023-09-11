<template>
  <div class="all">
    <a v-bind:href="url">Ini button ke bimay</a>
    <br>
    <button :disabled="disabled">
      Button
    </button>
  </div>
</template>

<script>
  export default {
    component: true,
    name: 'AboutPage',
    disabled: true,
    data() {
      return {
        url: 'https://newbinusmaya.binus.ac.id/lms/dashboard'
      }
    },
    mounted() {
      this.$nextTick(() => {
        this.$nuxt.$loading.start()
        setTimeout(() => this.$nuxt.$loading.finish(), 500);
      })
    }
  }
</script>
