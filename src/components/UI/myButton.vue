<template>
   
   <button><slot></slot></button>
</template>

<script>
   export default {
      components:{
         "name":myButton
      }
   }
</script>

<style scoped>
   my-button{
      border:solid 1px #aaa;
      background-color: #eee;
      padding:5px 10px;
      border-radius: 5px;
   }
   my-button:hover{
      background-color: rgb(191, 223, 241);
      cursor: pointer;
   }
</style>