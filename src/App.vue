<template>
  <div id="app">
    <customTable :tableList="tableList" :tableHeaders="tableHeaders" :properties="propertiesTable">
      <i class="fas fa-times"></i>
      <i class="far fa-edit"></i>
    </customTable>
  </div>
</template>

<script>
import customTable from './components/table.vue';

export default {
  name: 'app',
  components: {
    customTable
  },
  data () {
    return {
      tableList: [{
        date: '12/12/19',
        concept: 'House taxes',
        category: 'Fixed',
        cost: '80'
        }, {
        date: '13/12/19',
        concept: 'SuperMarket',
        category: 'Food',
        cost: '55'
        }, {
        date: '20/12/19',
        concept: 'Christmas gifts: sunglasses for mom, jumper for dad, jewelery for aunt, toys for the kids.',
        category: 'Gifts',
        cost: '150'
      }],
      tableHeaders: ["Date", "Concept", "Category", "Cost", "Actions"],
      propertiesTable: ["date", "concept", "category", "cost"]
    }
  }
}
</script>

<style>
  html, body {  
    margin: 0;
    padding: 0;
    font-family: 'Product Sans',Arial,sans-serif;
    height: 100%;
    width: 100%;
  }

  #app {
    background-color: #F2F2F2;
    height: 100%;
    width: 100%;
  }

</style>
