<template>
    <div id="app">
        <p>{{count}}</p>
        <button @click="handleClick1()">click1-通过函数调用</button>
        <button @click="handleClick2">click2-通过函数名调用</button>
        <button @click="count++">click3-通过表达式</button>
        
        <!-- 阻止事件冒泡 -->
        <ul @click="handleUlClick()">
            <li @click.stop="handleLiClick1()">11111</li>
        </ul>
        <!-- 阻止默认行为 -->
        <a href="http://www.baidu.com" @click.prevent="handleAClick()">跳转页面</a>
    </div>
</template>
<script>
export default {
    name: 'Demo05',
    data(){
        return{
            count: 0
        }
    },
    methods: {
        handleClick1(){
            this.count++;
        },
        handleClick2(){
            this.count++;
        },
        handleUlClick(){
            console.log('handleUlClick');
        },
        handleLiClick1(){
            console.log('handleLiClick1');
        },
        handleAClick(){
            console.log('handleAClick');
        }
    }
}
</script>