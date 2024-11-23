<script setup>
import TableRowItem from './item.vue'
import {reactive} from 'vue'
const {rowTitle} = defineProps({
    rowTitle:{
        type: Array,
        default: []
    }
})
const emit = defineEmits(['rowSizeHeight'])

const {dataRowSizeHeight} = reactive({
    dataRowSizeHeight: []
})

function rowSizeHeight(val) {
    dataRowSizeHeight.push(val)
}
</script>
<template>
    <ul class="table-row__list">
        <TableRowItem  v-for="item of rowTitle" 
            :key="item.id"
            :rowTitleItem="item"
            @rowSizeHeight="(value) => emit('rowSizeHeight', value)"
       />
    </ul>

</template>
<style>
.table-row__list {
    display: flex;
    flex-direction: column;
    /* max-width: 228px; */
    display: flex;
    flex-direction: column;
    /* max-width: 228px; */
    position: absolute;
    height: 594px;
    overflow: hidden;
    padding: 0;
}


</style>
