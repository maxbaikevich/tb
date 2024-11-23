<script setup>

defineProps({
    item:{
        type: Object,
        default:() => ({})
    },
})
</script>
<template>
   
        <p class="table-column__item-title">
           {{ item.title }}
        </p>
   
</template>
<style>

</style>

