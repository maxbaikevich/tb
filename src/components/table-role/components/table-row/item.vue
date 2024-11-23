<script setup>
  import { ref, onMounted, watch } from 'vue'
const {rowTitleItem} = defineProps({
    rowTitleItem:{
        type: Object,
        default:() => ({})
    }
})
const emit = defineEmits(['rowSizeHeight'])

const tableRowElement = ref(null)

onMounted(() => {
// Вычисляем высоту строки
    setTimeout(()=> {
        emit('rowSizeHeight', tableRowElement.value.offsetHeight)
    }, 100)
})

</script>
<template>
    <li class="table-row__wrapper" :style="rowTitleItem.style">
        <p class="table-row__title" ref="tableRowElement">
            {{ rowTitleItem.title }}
        </p>
    </li>
</template>
<style>
.table-row__wrapper {
    display: flex;
    flex-wrap: nowrap;
    margin-bottom: 6px;
    margin-right: 6px;
}

.table-row__title{
    border: 1px dotted #D7CFC6;
    padding: 10px;
    background-color: #e4f2ff;
    font-family: 'Noto IKEA Latin';
}
</style>