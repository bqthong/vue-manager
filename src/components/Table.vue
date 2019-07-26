<template>
  <div class="table">
    <b-table striped hover :items="items"></b-table>
  </div>
</template>

<script>
  export default {
    id: 'table',
    props: ['items']
  }
</script>