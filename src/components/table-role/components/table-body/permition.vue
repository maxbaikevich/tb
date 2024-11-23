<script setup>
import WrapperCell from '../table-cell/wrapper.vue'
import templateA from '../table-cell/text.vue'

const {permitionCell} = defineProps({
    permitionCell:{
        type: Array,
        default: []
    },
    sizeCell: {
        type: Object,
        default:()=> ({})
    },
})

function dataCell(data, index) {
    const id = data.id
    let zzz = data.cell.map((el)=> {
      
        return {
            ...el,
            id
        }
    })
    return zzz[index]
    
}
function choisenItem(value) {
    console.log(value)
    console.log('permitionCell',permitionCell)
    const choisenPermition = permitionCell.find(el => el.id === value.id).cell
    if(choisenPermition) {
        // let cjcjcj = null
        // choisenPermition.forEach((el, index) => {
           
        //     if(el.value === value.value) {
        //         el.checked = value.checked
        //         cjcjcj = index
                
        //     }
        
        //    if( cjcjcj !== null ) {
        //         console.log('zalupa', index)
        //         el.checked = true
        //     }
        // })
        // for (let item of choisenPermition) {
        //     if(item.value === value.value) {
        //         item.checked = value.checked
        //     }
        // }
        // for(let i = 0; i < choisenPermition.length; i++) {
        //     if(choisenPermition[i].name == value.name){
        //         choisenPermition[i].checked = value.checked
        //     }
        // }
    }
    // if(choisenPermition) {
    //     for (let item of choisenPermition.cell) {
    //         if(item.value !== value) {
    //             item.checked = true
    //         }else {
    //             break
    //         }
    //     }
    //     // choisenPermition.cell.forEach((el) => {
    //     //     console.log('el', el)
    //     // })
    // }
}
</script>
<template>
	<templateA 
        :sizeCell="sizeCell"
    >
    <template #bodyCell="bodyCellProps">
        <WrapperCell 
            :cellData="dataCell(permitionCell[bodyCellProps.index], bodyCellProps.cellIndex)"
            @choisenItem="choisenItem"
        />
    </template>
        
    </templateA>
</template>
<style>

/* ::-webkit-scrollbar {
	width: 16px;
    margin-left: 10px;
} 
::-webkit-scrollbar-track {
	box-shadow: inset 0 0 6px rgba(0,0,0,0.3); 
} 
::-webkit-scrollbar-thumb {
	box-shadow: inset 0 0 6px rgba(0,0,0,0.3); 
} */
.body-cell {
    /* margin-left: 189px; */
    /* overflow: scroll; */
    /* overflow: initial; */
    /* overflow: scroll; */
    /* margin-left: 272px; */
    /* overflow: scroll; */
    /* overflow: initial; */
    overflow: auto;
    width: 900px;
    display: flex;
    height: 615px;
    flex-wrap: wrap;
    padding: 0;
    margin-left: 232px;
}

</style>