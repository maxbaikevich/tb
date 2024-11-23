<script setup>
import {computed, defineAsyncComponent} from 'vue'
 const {mode} = defineProps({
    permitionCell:{
        type: Array,
        default: []
    },
    sizeCell: {
        type: Object,
        default:()=> ({})
    },
    mode: String
})

const getCurrTemplate  = computed(()=> {
    const components = {
		permition: defineAsyncComponent(() => import(`../table-body/permition.vue`)),
	}
    return components[mode]
})
</script>
<template>
    <component
        :is="getCurrTemplate"
        :permitionCell="permitionCell"
        :sizeCell="sizeCell"
    >
    </component>
    

</template>
<style>

.table-row__item{
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 6px;
}

.table-row__cell {
    border: 1px dotted #D7CFC6;
    margin-right: 6px;
}

.table-row__cell:last-child{
    margin-right: 0;
}

</style>