<script setup>
import { computed, reactive } from 'vue';
import TableColumn from './components/table-column/wrapper.vue'
import TableRowTitle from './components/table-row/wrapper.vue'
import TableCell from './components/table-cell/index.vue'
const permitions = ['none', 'read', 'create', 'execute', 'delete']

const {dataColumnSizeWidht, dataRowSizeHeight, columnData, rowTitle} = reactive({
    dataColumnSizeWidht: [],
    dataRowSizeHeight: [],
    columnData:{
       firstItem: [
            {
            style: {
                width: '226px',
                backgroundColor: '#E4F2FF',
            },
            template: {
                name: 'text',
                title: 'Событие',
                info: {
                    state: false,
                    title: '',         
                },
            },
            },
        ],
        basic: [
    {
            style: {
                width: '400px',
                backgroundColor: '#F7F4EF',
            },
            template: {
                name: 'text',
                title: 'Имеет права на просмотр событий',
                info: {
                    state: true,
                    title: 'Пользователь сможет устанавливать статус «обработано», означающий, что событие болеене требует внимания.',         
                },
            },
            id: 22
        },
        {
            style: {
                width: '226px', 
                backgroundColor: '#F7F4EF',
            },
            template: {
                name: 'text',
                title: 'Имеет права на создание событий',
                info:{
                    state: true,
                    title: 'Пользователь сможет устанавливать статус «обработано», означающий, что событие более не требует внимания.',         
                },
            },
            id: 23
        },
        {
            style: {
                width: '226px', 
                backgroundColor: '#F7F4EF',
            },
            template: {
                name: 'text',
                title: 'Имеет права на установку статуса «обработано»',
                info:{
                    state: true,
                    title: 'Пользователь сможет устанавливать статус «обработано», означающий, что событие более не требует внимания.',         
                },
            },
            id: 24
        },
        {
            style: {
                width: '226px', 
                backgroundColor: '#F7F4EF',
            },
            template: {
                name: 'text',
                title: 'Имеет права на удаление события',
                info:{
                    state: true,
                    title: 'Пользователь сможет устанавливать статус «обработано», означающий, что событие более не требует внимания.',         
                },
            },
            id: 25
        },
        {
            style: {
                width: '226px',
                backgroundColor: '#F7F4EF',
            },
            template: {
                name: 'text',
                title: 'Имеет права на просмотр событий',
                info: {
                    state: true,
                    title: 'Пользователь сможет устанавливать статус «обработано», означающий, что событие болеене требует внимания.',         
                },
            },
            id: 26
        },
        {
            style: {
                width: '226px',
                backgroundColor: '#F7F4EF',
            },
            template: {
                name: 'text',
                title: 'Имеет права на просмотр событий',
                info: {
                    state: true,
                    title: 'Пользователь сможет устанавливать статус «обработано», означающий, что событие болеене требует внимания.',         
                },
            },
            id: 27
        },
        {
            style: {
                width: '226px',
                backgroundColor: '#F7F4EF',
            },
            template: {
                name: 'text',
                title: 'Имеет права на просмотр событий',
                info: {
                    state: true,
                    title: 'Пользователь сможет устанавливать статус «обработано», означающий, что событие болеене требует внимания.',         
                },
            },
            id: 28
        },
        {
            style: {
                width: '226px',
                backgroundColor: '#F7F4EF',
            },
            template: {
                name: 'text',
                title: 'Имеет права на просмотр событий',
                info: {
                    state: true,
                    title: 'Пользователь сможет устанавливать статус «обработано», означающий, что событие болеене требует внимания.',         
                },
            },
            id: 29
        },
        {
            style: {
                width: '226px',
                backgroundColor: '#F7F4EF',
            },
            template: {
                name: 'text',
                title: 'Имеет права на просмотр событий',
                info: {
                    state: true,
                    title: 'Пользователь сможет устанавливать статус «обработано», означающий, что событие болеене требует внимания.',         
                },
            },
            id: 30
        },
        ],
    } ,
    rowTitle: [
    {
        style: {
            width: '226px', 
            backgroundColor: '#E4F2FF',
        },
        cell:[
            {
                template: 'checkbox',
                value: 'read',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'create',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'execute',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
        ],
        title: 'Нарушение платежной дисциплины (сроки и суммы платежей)',
        id: 33
    },
    {
        style: {
            width: '226px', 
            backgroundColor: '#E4F2FF',
        },
        cell:[
        {
                template: 'checkbox',
                value: 'read',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'create',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'execute',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
        ],
        id: 34,
        title: 'Поступление на сумму, превышающую сумму выставленного счета'
    },
    {
        style: {
            width: '226px', 
            backgroundColor: '#E4F2FF',
        },
        cell:[
        {
                template: 'checkbox',
                value: 'read',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'create',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'execute',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
        ],
		id: 35,
        title: 'Платеж на сумму, превышающую заданную'
    },
    {
        style: {
            width: '226px', 
            backgroundColor: '#E4F2FF',
        },
            cell:[
            {
                template: 'checkbox',
                value: 'read',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'create',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'execute',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
        ],
        id: 36,
        title: 'Возникновение дебиторской задолженности выше определенной для контрагента (размер рассчитывается автоматически)'
    },
    {
        style: {
            width: '226px', 
            backgroundColor: '#E4F2FF',
        },
        cell:[
        {
                template: 'checkbox',
                value: 'read',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'create',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'execute',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
        ],
        id: 37,
        title: 'Отклонения от стандартных коммерческих условий договоров'
    },
    {
        style: {
            width: '226px', 
            backgroundColor: '#E4F2FF',
        },
        cell:[
        {
                template: 'checkbox',
                value: 'read',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'create',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'execute',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
        ],
        id: 38,
        title: 'Изменение коммерческих условий договоров'
    },
    {
        style: {
            width: '226px', 
            backgroundColor: '#E4F2FF',
        },
        cell:[
        {
                template: 'checkbox',
                value: 'read',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'create',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'execute',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
            {
                template: 'checkbox',
                value: 'delete',
                checked: false
            },
        ],
        id: 38,
        title: 'Изменение коммерческих условий договоров'
    }
]

})

// const permitions = {
// 	none: 0,
// 	read: 1,
// 	create: 2,
// 	execute: 3,
// 	delete: 4
// }

// const columnData = [
//         {
//             style: {
//                 width: '226px',
//                 backgroundColor: '#E4F2FF',
//             },
//             template: {
//                 name: 'text',
//                 title: 'Событие',
//                 info: {
//                     state: false,
//                     title: '',         
//                 },
//             },
//         },
//         {
//             style: {
//                 width: '226px',
//                 backgroundColor: '#F7F4EF',
//             },
//             template: {
//                 name: 'text',
//                 title: 'Имеет права на просмотр событий',
//                 info: {
//                     state: true,
//                     title: 'Пользователь сможет устанавливать статус «обработано», означающий, что событие болеене требует внимания.',         
//                 },
//             },
//             id: 22
//         },
//         {
//             style: {
//                 width: '226px', 
//                 backgroundColor: '#F7F4EF',
//             },
//             template: {
//                 name: 'text',
//                 title: 'Имеет права на создание событий',
//                 info:{
//                     state: true,
//                     title: 'Пользователь сможет устанавливать статус «обработано», означающий, что событие более не требует внимания.',         
//                 },
//             },
//             id: 23
//         },
//         {
//             style: {
//                 width: '226px', 
//                 backgroundColor: '#F7F4EF',
//             },
//             template: {
//                 name: 'text',
//                 title: 'Имеет права на установку статуса «обработано»',
//                 info:{
//                     state: true,
//                     title: 'Пользователь сможет устанавливать статус «обработано», означающий, что событие более не требует внимания.',         
//                 },
//             },
//             id: 24
//         },
//         {
//             style: {
//                 width: '226px', 
//                 backgroundColor: '#F7F4EF',
//             },
//             template: {
//                 name: 'text',
//                 title: 'Имеет права на удаление события',
//                 info:{
//                     state: true,
//                     title: 'Пользователь сможет устанавливать статус «обработано», означающий, что событие более не требует внимания.',         
//                 },
//             },
//             id: 25
//         }
//     ]


// const rowTitle = [
//     {
//         style: {
//             width: '226px', 
//             backgroundColor: '#E4F2FF',
//         },
//         cell:[
//             {
//                 template: 'checkbox',
//                 value: 'read',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'create',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'execute',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'delete',
//                 checked: false
//             },
//         ],
//         title: 'Нарушение платежной дисциплины (сроки и суммы платежей)',
//         id: 33
//     },
//     {
//         style: {
//             width: '226px', 
//             backgroundColor: '#E4F2FF',
//         },
//         cell:[
//             {
//                 template: 'checkbox',
//                 value: 'read',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'create',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'execute',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'delete',
//                 checked: false
//             },
//         ],
//         id: 34,
//         title: 'Поступление на сумму, превышающую сумму выставленного счета'
//     },
//     {
//         style: {
//             width: '226px', 
//             backgroundColor: '#E4F2FF',
//         },
//         cell:[
//             {
//                 template: 'checkbox',
//                 value: 'read',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'create',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'execute',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'delete',
//                 checked: false
//             },
//         ],
// 		id: 35,
//         title: 'Платеж на сумму, превышающую заданную'
//     },
//     {
//         style: {
//             width: '226px', 
//             backgroundColor: '#E4F2FF',
//         },
//             cell:[
//             {
//                 template: 'checkbox',
//                 value: 'read',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'create',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'execute',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'delete',
//                 checked: false
//             },
//         ],
//         id: 36,
//         title: 'Возникновение дебиторской задолженности выше определенной для контрагента (размер рассчитывается автоматически)'
//     },
//     {
//         style: {
//             width: '226px', 
//             backgroundColor: '#E4F2FF',
//         },
//         cell:[
//             {
//                 template: 'checkbox',
//                 value: 'read',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'create',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'execute',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'delete',
//                 checked: false
//             },
//         ],
//         id: 37,
//         title: 'Отклонения от стандартных коммерческих условий договоров'
//     },
//     {
//         style: {
//             width: '226px', 
//             backgroundColor: '#E4F2FF',
//         },
//         cell:[
//             {
//                 template: 'checkbox',
//                 value: 'read',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'create',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'execute',
//                 checked: false
//             },
//             {
//                 template: 'checkbox',
//                 value: 'delete',
//                 checked: false
//             },
//         ],
//         id: 38,
//         title: 'Изменение коммерческих условий договоров'
//     }
// ]

function columnSizeWidth(val) {
    dataColumnSizeWidht.push(val)
}

function rowSizeHeight(val) {
    dataRowSizeHeight.push(val)
}

const sizeCell = computed(() => {
    return {
        width: dataColumnSizeWidht,
        height: dataRowSizeHeight
    }
})
</script>
<template>
    <div class="bebra">
        <div class="column-wr">
            <TableColumn
                :columnData="columnData"
                @columnSizeWidth="columnSizeWidth"
            />
        </div>
        <div class="fufufuf">
            <TableRowTitle
                    :rowTitle="rowTitle"
                    @rowSizeHeight="rowSizeHeight"
                />
            <div class="table-role">
                <div class="table-body">
                    <div>
                        <TableCell
                            :mode="'permition'"
                            :permitionCell="rowTitle"
                            :sizeCell="sizeCell"
                        />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style>
.fufufuf {
    display: flex;
    position: relative;
}
.column-wr {
    overflow: hidden;
    width: 100%
}
.bebra {
    display: flex;
    flex-wrap: wrap;
    background-color: #fff;
    width: 1160px;
    padding: 16px 16px 16px 16px;
    box-sizing: border-box;
    /* overflow: hidden; */
}
.table-body {
	display: flex;
}
/* .table-column__list {
    display: flex;
    flex-wrap: nowrap;
    margin-bottom: 6px;
	margin-right: 6px;
    padding: 0;
    width: fit-content;
} */
.table-column__item {
    min-width: 185px;
    min-height: 92px;
    margin-right: 6px;
    border: 1px dotted #D7CFC6;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 10px;
    box-sizing: border-box;
    text-align: center;
    background-color: #F7F4EF;
}
/* .table-column__item:nth-child(2) {
    margin-left: 232px;
} */
.first-table-column__item {
    min-width: 185px;
    min-height: 92px;
    margin-right: 6px;
    border: 1px dotted #D7CFC6;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 10px;
    box-sizing: border-box;
    text-align: center;
    background-color: #F7F4EF;
    z-index: 1;
    position: relative;
}
.first-table-column__item::before {
    position: absolute;
    content: "";
    width: 5px;
    height: 103%;
    background-color: #ffffff;
    right: -6px;
    z-index: 222;
}
.table-column__item:last-child {
    margin-right: 0;
}
.table-column__item:first-child {
    background-color: #E4F2FF;
    min-width: 201px;
}
.table-column__item-title {
    font-family: 'Noto IKEA Latin';
    font-weight: 700;
    font-size: 16px;
    line-height: 24px;
    color: #474747;
}
.table-role {
    /* margin-left: 196px; */
    /* padding: 16px; */
    border-radius: 0 15px 15px 0;
    background-color: #fff;
    /* width: 940px; */
    /* width: 2x; */
    /* overflow: scroll; */
    /* overflow-x: hidden; */

}

/* ---------------------------------------------------- */

.table-line__cell-list{
    display: flex;
}
/* .table-line__cell-item{
    min-width: 185px;
    border: 1px dotted #D7CFC6;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-right: 6px;
    margin-bottom: 6px;


} */
/* .table-line__cell-item:last-child {
    margin-right: 0;
   
} */
</style>