<template>
  <div class="home">
    <b-card bg-variant="light" header="Table" class="text-left">
      <Table v-bind:data="data" v-bind:tableConfig="tableConfig" />
    </b-card>
  </div>
</template>

<script>
// @ is an alias to /src
import Table from '@/components/Table.vue'
export default {
  name: 'home',
  data: function () {
    return {
      tableConfig: {
        sortBy: 'age',
        sortDesc: false,
        currentPage: 1,
        totalRows: 1,
        perPage: 5,
        columns: [
          { key: 'last_name', sortable: true },
          { key: 'first_name', sortable: true },
          { key: 'age', sortable: true }
        ]
      },
      data: [
        { age: 40, first_name: 'Dickerson', last_name: 'Macdonald' },
        { age: 21, first_name: 'Larsen', last_name: 'Shaw' },
        { age: 89, first_name: 'Geneva', last_name: 'Wilson' },
        { age: 38, first_name: 'Jami', last_name: 'Carney' },
        { age: 40, first_name: 'Dickerson', last_name: 'Macdonald' },
        { age: 21, first_name: 'Larsen', last_name: 'Shaw' },
        { age: 89, first_name: 'Geneva', last_name: 'Wilson' },
        { age: 38, first_name: 'Jami', last_name: 'Carney' },
        { age: 40, first_name: 'Dickerson', last_name: 'Macdonald' },
        { age: 21, first_name: 'Larsen', last_name: 'Shaw' },
        { age: 89, first_name: 'Geneva', last_name: 'Wilson' },
        { age: 38, first_name: 'Jami', last_name: 'Carney' },
        { age: 40, first_name: 'Dickerson', last_name: 'Macdonald' },
        { age: 21, first_name: 'Larsen', last_name: 'Shaw' },
        { age: 89, first_name: 'Geneva', last_name: 'Wilson' },
        { age: 38, first_name: 'Jami', last_name: 'Carney' }
      ]
    }
  },
  mounted() {
    // Initial number of rows
    this.tableConfig.totalRows = this.data.length
  },
  components: {
    Table
  }
}
</script>
