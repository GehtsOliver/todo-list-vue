<template lang="">
      <form class="mt-6 d-flex flex-column justify-space-between px-8">
    <v-text-field
      v-model="todo"
      label="Todo"
      required
    ></v-text-field>
    <v-text-field
      v-model="time"
      label="Date & Time"
      required
    ></v-text-field>

    <v-checkbox
      v-model="reminder"
      label="Reminder"
    ></v-checkbox>

    <v-btn
      class="mr-4"
      @click="onAdd()"
      
    >
      Add
    </v-btn>
    <v-btn @click="onClear()">
      clear
    </v-btn>
  </form>
</template>
<script>
export default {
    methods: {
        onAdd() {
            console.log("add")
        },
        onClear() { console.log("clear") }
    },
    data() {
        return {
            todo: "",
            time: "",
            reminder: false,
        }
    }
}
</script>
<style lang="">
    
</style>