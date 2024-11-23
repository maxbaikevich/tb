<script setup>
import {computed} from 'vue'
 const {item} = defineProps({
    item: {
        type: Object,
        default:()=> ({})
    }
})
const emit = defineEmits(['choisenItem'])

const checkedData = computed({
  get() {
    return item.checked
  },
  
  set(value) {
    item.checked = value
    emit('choisenItem', item)
  }
})

</script>
<template>
    <label class="checkbox-label">
	    <input 
            :type="item.template" 
            :value="item"
            :checked="item.checked"
            v-model="checkedData"
        >
    </label>
</template>
<style>

.checkbox-label {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
}


</style>