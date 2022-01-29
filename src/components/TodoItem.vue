<template lang="">
     <v-card
    class="px-16 mx-auto justify-space-between d-flex align-center"
    max-width="500"
    tile
  >
  <div>
    <v-list-item>
      <v-list-item-content>
        <v-list-item-title>{{todo.text}}</v-list-item-title>
        <v-list-item-subtitle>{{todo.time}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
  </div>
  <div @click="onClick()">
    <v-icon large>mdi-delete-empty</v-icon>
  </div>

     </v-card>
</template>
<script>
export default {
  props: {
    todo: Object
  },
  methods: {
    onClick() {
      console.log("click")
    }
  }
}
</script>
<style lang="">
    
</style>