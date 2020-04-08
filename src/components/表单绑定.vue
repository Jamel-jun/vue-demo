<template>
    <div id="app">
        <!-- 多选框 -->
        喜欢的编程语言：
        <input type="checkbox" v-model="checkedGroup" value="vue">Vue
        <input type="checkbox" v-model="checkedGroup" value="React">React
        <input type="checkbox" v-model="checkedGroup" value="JQuery">JQuery
        <textarea v-model="checkedGroup"></textarea>
        <input type="button" @click="handleClick()" value="666"/>
    </div>
</template>
<script>
export default {
    name: 'Demo06',
    data(){
        return {
            checkedGroup: []
        }
    },
    methods: {
        handleClick(){
            console.log(this.checkedGroup);
        }
    }
}
</script>