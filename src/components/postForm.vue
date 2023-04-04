<template lang="">
   <div>
      <form action="">
         <input type="text" placeholder="Введите заголовок" v-model="post.title">
         <input type="text" placeholder="Введите описание" v-model="post.body">
         <input type="button" @click="addPost" value="Add">
      </form>
   </div>
</template>
<script>
export default {
   data(){
      return {
         post:{
            title:'',
            body:''
         }
      }
   }, 
   methods:{
    addPost(){
      
      this.post.id = Date.now();

      if(this.post.title == ""){
         alert("Не ввели титле");
         return false
      }

      this.$emit('addPost',this.post)
      this.post={
         title:"",
         body:""
      }
    }
  }
}
</script>
<style lang="">
   
</style>