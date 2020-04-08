<template>
    <div id="app">
        <input type="checkbox" @change="handleChange" v-model="isAllChecked">
        <ul>
            <li v-for="data in dataList" :key="data.id">
                <input type="checkbox" v-model="checkedGroup" :value="data" @change="handleItemChange" />{{data}}
                <button @click="handleDelClick(data)">删除</button>
                <input type="number" style="width:40px" v-model="data.number"/>
                <button @click="data.number+data.number">增加</button>
            </li>
        </ul>
        总金额：{{getSum()}} 
    </div>
</template>
<script>
export default {
    name: 'Demo07',
    data(){
        return {
            checkedGroup: [],
            isAllChecked: false,
            dataList: [
                {
                    name: '商品1',
                    price: 10,
                    number: 1,
                    id: 1
                },
                {
                    name: '商品2',
                    price: 20,
                    number: 2,
                    id: 2
                },
                {
                    name: '商品3',
                    price: 30,
                    number: 3,
                    id: 3
                }
            ]
        }
    },
    methods: {
        getSum(){
            var sum = 0;
            for (var data of this.checkedGroup) {
                sum += data.price * data.number;
            }
            return sum;
        },
        handleDelClick(data){
            if (data.number > 1) {
                data.number--;
            }
        },
        handleChange(ev){
            // 如果为true 则是全选
            if(this.isAllChecked){
                this.checkedGroup = this.dataList;
            } else {
                this.checkedGroup = [];
            }
        },
        handleItemChange(ev){
            if(this.checkedGroup.length === this.dataList.length){
                this.isAllChecked = true;
            } else {
                this.isAllChecked = false;
            }
        }
    }
}
</script>