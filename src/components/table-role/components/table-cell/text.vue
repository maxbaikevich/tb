<script setup>
  defineProps({
    sizeCell: {
        type: Object,
        default:()=> ({})
    },

})

</script>
<template>
   <ul class="body-cell" >
        <li 
            class="table-row__item"
            v-for="(height, index) in sizeCell.height" 
            :key="index"
            :style="{height:`${height}px`}"
        >
            <div 
                class="table-row__cell"
                v-for="(width, cellIndex) in sizeCell.width" 
                :key="cellIndex"
                :style="{height:`${height}px`, minWidth:`${width}px`}" 
                >
                <slot 
                    name="bodyCell"  
                    :index="index" 
                    :cellIndex="cellIndex">
                </slot>
            </div>
        </li>
    </ul>
    

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