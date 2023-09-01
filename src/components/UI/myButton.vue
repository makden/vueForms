<template>dddd
   <myButtons><slot></slot></myButtons>
</template>

<script>
    export default{
      name:'myButtons'
    }
</script>

<style scoped>
   myButton{
      border:solid 1px #aaa;
      background-color: rgb(214, 20, 101);
      padding:5px 10px;
      border-radius: 5px;
   }
   myButton:hover{
      background-color: rgb(191, 223, 241);
      cursor: pointer;
   }
</style>