<script setup>
import {onMounted, ref, defineAsyncComponent} from 'vue'
const {columnItem} = defineProps({
    columnItem:{
        type: Object,
        default:() => ({}),
    },
})
const emit = defineEmits(['columnSizeWidth'])

const tableColumnElement = ref(null)
onMounted(() => {
    // Вычисляем ширену колонки
    if(tableColumnElement.value.className !== 'first-table-column__item') {
        setTimeout(()=> {
        emit('columnSizeWidth', tableColumnElement.value.offsetWidth)
        },100)
    }
})
// watch(tableColumnElement.value, (newValue) => {
//   console.log('zalupka', newValue)
// })
// watch( tableColumnElement, (newValue, oldValue) => {
    
//     if(tableColumnElement.value.className !== 'first-table-column__item') {
//         setTimeout(()=> {
//             emit('columnSizeWidth', tableColumnElement.value.offsetWidth)
//         }, 100)
       
//     }
// })
const getCurrComponents = ({template}) => {
	const components = {
		text: defineAsyncComponent(() => import(`../table-column/template/text.vue`)),
	}
	if (!template.name) {
		template.name = 'text'
	}
	return components[template.name]
}

</script>
<template>
    <li 
        ref="tableColumnElement" 
        :style="columnItem.style"
    >
        <component 
            :is="getCurrComponents(columnItem)"
            :item="columnItem.template"
        />
    </li>
</template>
<style>
</style>