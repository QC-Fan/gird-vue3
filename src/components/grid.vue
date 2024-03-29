<template>
    <ag-grid-vue :rowData="rowData" :columnDefs="colDefs" class="grid ag-theme-quartz">
    </ag-grid-vue>
</template>
<script setup>
import { ref } from 'vue';
import "ag-grid-community/styles/ag-grid.css";
import "ag-grid-community/styles/ag-theme-quartz.css";
import { AgGridVue } from "ag-grid-vue3";
import ButtonRenderer from './ButtonRenderer.vue'
const rowData = ref([
    { make: '123', bz: 'Toyota', kcbm: 'Celica', kc: 35000, pz: 35000, pf: 35000, ls: 35000, ck: 35000 },
    { make: '123', bz: 'Toyota', kcbm: 'Celica', kc: 35000, pz: 35000, pf: 35000, ls: 35000, ck: 35000 },
    { make: '123', bz: 'Toyota', kcbm: 'Celica', kc: 35000, pz: 35000, pf: 35000, ls: 35000, ck: 35000 },
    { make: '123', bz: 'Toyota', kcbm: 'Celica', kc: 35000, pz: 35000, pf: 35000, ls: 35000, ck: 35000 },
]);

const colDefs = ref([
    {
        headerName: '客户需求',
        cellEditor: 'agRichSelectCellEditor',
        field: "make",
        editable: true,
        cellEditor: "agSelectCellEditor",
        cellEditorParams: { values: ["活塞", "连杆瓦", "连杆瓦", "连杆瓦"] }
    },
    { headerName: '标准名称及OE', field: "bz", },

    { headerName: "库存编码", field: "kcbm" },
    { headerName: "库存", field: "kc" },
    { headerName: "品质", field: "pz" },
    { headerName: "批发", field: "pf" },
    { headerName: "零售", field: "ls" },
    { headerName: "查库", field: "ck" },
    {
        headerName: "操作",
        cellRenderer: ButtonRenderer,
    },

]);

</script>
<style scoped>
.grid {
    height: 500px;
    width: 100%;
}
</style>