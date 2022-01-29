<template lang="">
    <div>
        <TodoItem class="mt-8 px-4 py-4" v-for="(todo, index) in todos" :todo="todo" :key="index"/>
    </div>
</template>
<script>
import TodoItem from "./TodoItem"

export default {
    props: {
        todos: Array
    },
    components: {
        TodoItem
    }
}
</script>
<style lang="">
  
</style>