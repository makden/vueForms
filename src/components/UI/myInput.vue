<template>
   <input type="text"  @input="updateInput" >
   <ul v-for="arrVal in modelValue" >
         <li> {{arrVal}}</li>
         </ul>

   <hr>
   
   <ul v-for="arrVal in arrVals" >
         <li> {{arrVal}}</li>
         </ul>
</template>

<script>
   export default {
      name:'myInput',
      props:{
         modelValue:Array,
         
      },
     data(){
      return {
         arrVals:Array
      }
     },
      methods: {
         updateInput(event){

             this.arrVals = this.modelValue.filter(function (language) {
              return language.startsWith(event.target.value)
            })

           
            
            //this.$emit('update:modelValue',event.target.value)
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