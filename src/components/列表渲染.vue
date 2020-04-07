<template>
    <div id="app">
        <ul v-for="(data,index) in obj" :key="data">
            <li>{{data}}---{{index}}</li>
        </ul>
    </div>
</template>
<script>
export default {
    name: "Demo03",
    data() {
        return{
            dataList: ['aaa','bbb','ccc','ddd'],
            obj: {
                id: 1,
                name: 'name111',
                age: 111
            }
        }
    },
    methods: {

    }
}
</script>