<template>
    <div id="app">
        <input @input="handleInput()" v-model="myText" />
        <ul v-for="data in dataList" :key="data">
            <li>{{data}}</li>
        </ul>
    </div>
</template>
<script>
export default {
    name: 'Demo04',
    data(){
        return{
            dataList: ['aaa','bbb','ccc','ddd','add','cee','eee'],
            list: ['aaa','bbb','ccc','ddd','add','cee','eee'],
            myText: ''
        }
    },
    methods: {
        handleInput(){
            // console.log(this.myText)
            // 过滤
            this.dataList = this.list.filter(item => item.indexOf(this.myText) > -1);
        }
    }
}
</script>