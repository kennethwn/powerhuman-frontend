<template>
  <div class="app">
    <Tutorial />
    <ol>
      <li v-for="todolist in todolists" v-bind:key="todolist.id">
        {{ todolist.ngapain }}
      </li>
    </ol>
  </div>
</template>

<script>
  export default {
    el: '#app',
    name: 'Index',
    data() {
      return {
        todolists: [
          {ngapain: 'makan'},
          {ngapain: 'mandi'},
          {ngapain: 'bobo'}
        ]
      }
    },
  }
</script>
