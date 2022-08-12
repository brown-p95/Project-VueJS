<template>
  <h1><button @click="accion" :disabled="disabled">{{text}}</button></h1>
</template>

<script>

export default {
    props: {
        text: String,
        disabled:{
            type:Boolean,
            default: false
        } 
    },
    methods: {
        accion(){
            this.$emit('accion')
        }
    },

}
</script>

<style scoped>
 h1{
    background-color: transparent;
 }
</style>