<template>
  <div id="app">
    <ejs-grid :dataSource="data" :allowPaging="true" :allowSorting="true" :allowFiltering="true" :allowGrouping='true' :pageSettings='pageSettings'>
      <e-columns>
        <e-column field='OrderID' headerText='Order ID' textAlign='Right'></e-column>
        <e-column field='CustomerID' headerText='Customer ID'></e-column>
        <e-column field='Price' headerText='Price' format='C2'></e-column>
      </e-columns>
    </ejs-grid>
  </div>
</template>

<script>
import Vue from 'vue';
import { GridPlugin, Page, Sort, Filter, Group } from '@syncfusion/ej2-vue-grids';
Vue.use(GridPlugin);

export default {
  data () {
    return {
       data: [
          { OrderID: 10248, CustomerID: 'VINET', Price: 32.38 },
          { OrderID: 10250, CustomerID: 'HANAR', Price: 65.83 },
          { OrderID: 10251, CustomerID: 'VICTE', Price: 41.34 },
          { OrderID: 10252, CustomerID: 'SUPRD', Price: 51.3 },
          { OrderID: 10253, CustomerID: 'HANAR', Price: 58.17 },
          { OrderID: 10254, CustomerID: 'CHOPS', Price: 22.98 },
          { OrderID: 10255, CustomerID: 'RICSU', Price: 148.33 },
          { OrderID: 10256, CustomerID: 'WELLI', Price: 13.97 },
          { OrderID: 10249, CustomerID: 'TOMSP', Price: 11.61 },],
       pageSettings: { pageSize: 5 }
    }
  },
  provide: {
    grid: [Page, Sort, Filter, Group]
  }
}
</script>

<style>
  @import url("https://cdn.syncfusion.com/ej2/material.css");
</style>