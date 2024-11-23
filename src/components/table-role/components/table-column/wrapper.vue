<script setup>
import TableColumnItem from './item.vue'
import { reactive, computed } from 'vue';
const emit = defineEmits(['columnSizeWidth'])
const {columnData} = defineProps({
    columnData:{
        type: Object,
        default: ()=>({})
    }
})
const firstItem = computed(() => {
    return columnData[0]
})
// const columnDataFix = computed(()=> {
//     return columnData
// })
// const {dataColumnSizeWidht} = reactive({
//     dataColumnSizeWidht: []
// })
// function columnSizeWidth(val) {
//     dataColumnSizeWidht.push(val)
// }

</script>
<template>
    <ul class="table-column__list">
        <!-- <TableColumnItem  v-for="(item, index) of columnData" 
            :class="[index === 0 ? 'first-table-column__item' : 'table-column__item',]"
            :key="item.id"
            :index="index"
            :columnItem="item"
            @columnSizeWidth="(val) => emit('columnSizeWidth', val)"
        /> -->
        <TableColumnItem 
            class="first-table-column__item"
            :columnItem="columnData.firstItem[0]"
        />
        <li class="table-column__basic-wrapper">
            <ul class="table-column__list-basic">
                <TableColumnItem  v-for="item of columnData.basic" 
                    class="table-column__item"
                    :key="item.id"
                    :columnItem="item"
                    @columnSizeWidth="(val) => emit('columnSizeWidth', val)"
                />
            </ul>
        </li>
        
    </ul> 
</template>
<style>
.table-column__list {
    display: flex;
    flex-wrap: nowrap;
    margin-bottom: 6px;
	margin-right: 6px;
    padding: 0;
    width: fit-content;
    z-index: 1;
}
.table-column__list-basic {
    margin-bottom: 0;
    display: flex;
    flex-wrap: nowrap;
	/* margin-right: 6px; */
    padding: 0;
    width: fit-content;
    position: absolute;
}
.table-column__basic-wrapper {
    list-style: none;
    position: relative;
}

</style>