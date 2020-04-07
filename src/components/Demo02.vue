<template>
    <div id="app">
        <input type="text" v-model="myText" />
        <button @click="handleAdd()">add</button>
        <ul>
            <li v-for="(data,index) in dataList" :key="index" :class="current===index?'red':''"
            @click="handleClick(index)">
                {{data}}---<button @click="handleDel(index)">del</button>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    name: 'Demo02',
    data() {
        return{
            myText: null,
            dataList: [],
            current: 0
        }
    },
    methods: {
        handleAdd(){
            if (this.myText != '' && this.myText != null) {
                this.dataList.push(this.myText);
                this.myText = '';
            }
        },
        handleDel(index){
            this.dataList.pop(index);
        },
        handleClick(index){
            this.current = index;
        }
    }
}
</script>
<style>
    .red{
        background-color: red;
    }
</style>