<template>
  <div class="app">
    <h1>Selamat datang</h1>
    <h1>Halo, {{ name }}</h1>
    <input v-model="name" type="text" />
  </div>
</template>

<script>
  export default {
    el: '#app',
    name: 'DashboardPage',
    data() {
      return {
        name: '',
      }
    }
  }
</script>
