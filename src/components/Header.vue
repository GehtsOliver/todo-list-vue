<template lang="">
<header class="d-flex justify-space-between">
    <h3>Todo List App</h3>
    <v-btn @click="$emit('toggle-todo')">{{text}}</v-btn>
</header>
</template>
<script>
export default {
    name: "Header",
    props: {
        text: String,
    },
}

</script>
<style lang="">
    
</style>