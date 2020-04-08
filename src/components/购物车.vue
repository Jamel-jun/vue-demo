<template>
    <div id="app">
        <ul>
            <li v-for="data in dataList" :key="data.id">
                <input type="checkbox" v-model="checkedGroup" :value="data" />{{data}}
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
        }
    }
}
</script>