<script setup>
import {defineAsyncComponent} from 'vue'
 defineProps({
    cellData: {
        type: Object,
        default:()=> ({})
    }
})
const getCurrComponents = ({template}) => {
	const components = {
		checkbox: defineAsyncComponent(() => import(`./template/checkbox.vue`)),
	}
	if (!template) {
		template = 'checkbox'
	}
	return components[template]
}
</script>
<template>
	 <component 
            :is="getCurrComponents(cellData)"
            :item="cellData"
        >
		</component>
</template>
<style>



</style>