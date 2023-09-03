<template lang="">
   <div>
      <form action="">
         <my-input  :modelValue=arrVals></my-input>
         <hr>
            
         <my-button @click="addPost">Добавить</my-button>
      </form>
   </div>
</template>
<script>
import myinput from "./UI/myInput.vue";
export default {
   components:{
      myinput,
   },
   data(){
      return {
         arrVals:["Один","Два","Три","Тристо","Тари","Четыре","Пять","Двадцать","Одинадцать","Двенадцать","Пятьсот","Двести"],
         post:{
            title:'',
            body:''
         }
      }
   }, 
   methods:{

      vvv(){
            this.vvv="df"
      },

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