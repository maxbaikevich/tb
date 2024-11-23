<script setup>
import TableRowTitle from '../table-row/wrapper.vue'
const {rowTitle} = defineProps({
    rowTitle:{
        type: Array,
        default:() => ([])
    }
})
</script>
<template>
    <div class="">
        <TableRowTitle
            :rowTitle="rowTitle"
        />
    </div>
</template>
<style>
</style>