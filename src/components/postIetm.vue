<template lang="">
   <div class="post">
      <h5>{{ post.title }}</h5>
      <p>{{ post.body }}</p>
      <my-button @click="$emit('removeItem',post)">Удалить</my-button>
   </div>

</template>
<script>

export default {
   props:{
      post:{
         type:Object,
         required:true
      }
   },
   methods: {
      // remote(){
      //   console.log(key); 
      // }
   },
}
</script>
<style>
     .post{
    margin:10px ;
    border: solid 1px rgb(85, 116, 252);
    padding:10px;
  }
</style>