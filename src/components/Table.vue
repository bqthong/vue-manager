<template>
  <div class="table">
    <b-table striped hover show-empty
      :items="data"
      :fields="tableConfig.columns"
      :sort-by.sync="tableConfig.sortBy"
      :sort-desc.sync="tableConfig.sortDesc"
      :current-page="tableConfig.currentPage"
      :per-page="tableConfig.perPage">
    </b-table>
    <b-row>
      <b-col>
        <b-pagination
          v-model="tableConfig.currentPage"
          :total-rows="tableConfig.totalRows"
          :per-page="tableConfig.perPage"
          class="my-0"
        ></b-pagination>
      </b-col>
    </b-row>
  </div>
</template>

<script>
  export default {
    id: 'table',
    props: ['data', 'tableConfig']
  }
</script>