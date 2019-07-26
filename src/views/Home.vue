<template>
  <div class="home">
    <Table v-bind:items="items" />
  </div>
</template>

<script>
// @ is an alias to /src
import Table from '@/components/Table.vue'
export default {
  name: 'home',
  data: function () {
    return {
      items: [
        { age: 40, first_name: 'Dickerson', last_name: 'Macdonald' },
        { age: 21, first_name: 'Larsen', last_name: 'Shaw' },
        { age: 89, first_name: 'Geneva', last_name: 'Wilson' },
        { age: 38, first_name: 'Jami', last_name: 'Carney' }
      ]
    }
  },
  components: {
    Table
  }
}
</script>
