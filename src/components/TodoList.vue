<template>
    <ul>
        <li v-for="(todo, index) in todos" v-on:click="deleteTodo(index)" v-bind:key="index">{{ todo }}</li>
    </ul>
</template>

<script>
export default {
    props: ['todos'],
    methods: {
        deleteTodo(index){
            this.$emit('delete-todo', index);
        }
    }
}
</script>
<style>li{width: 200px; border: solid; font-family: cursive; text-decoration: none; text-align: center; list-style: none; margin: auto; margin-top: 15px;}</style> 