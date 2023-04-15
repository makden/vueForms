<template>
   fff
   <input type="text" :value="modelValue" @input="updateInput" >
</template>

<script>
   export default {
      
      props:{
         mdoelValue:[String,Number]
      },
      methods: {
         updateInput(event){
            this.$emit('update:modelValue',event.target.value)
         }
      },
   }
</script>
<style scoped>
   input[type="text"]{
      border:solid 1px rgb(67, 59, 140);
      background-color: #eee;
      padding:5px 10px;
      border-radius: 5px;
   }
</style>