<template>
   <div class="input_search">
      <input type="text" :value="val" @input="updateInput">
      <ul class="list_data" v-if="displayListData">
         <li v-for="arrVal in arrVals" @click="selectItem"> {{ arrVal }}</li>
      </ul>
   </div>
</template>

<script>
export default {
   name: 'myInput',
   props: {
      modelValue: Array,

   },
   data() {
      return {
         arrVals: Array,
         val: "",
         displayListData: false
      }
   },
   methods: {
      updateInput(event) {
         
         this.arrVals = this.modelValue.filter(function (book) {
            return book.indexOf(event.target.value) !== -1;
         })
         this.displayListData = this.arrVals.length <=3; // Покать подсказу когда мешьше или = 3
         
         this.val = event.target.value;
      },
      selectItem(e) {
         this.val = e.target.innerText
         this.displayListData = false;
      }
   },
}
</script>
<style scoped>
.input_search {
   border: solid 1px #def;
   display: inline-block;
}

.input_search input[type="text"] {
   border: solid 1px #aaa;
   border-bottom: none;
   background-color: #eee;
   padding: 5px 10px;
}

ul.list_data {
   margin: 0px;
   padding: 0px;
   list-style: none;
   border: solid 1px #aaa;

}

ul.list_data li {
   line-height: 22px;
   padding: 5px;
}

ul.list_data li:hover {
   background-color: #eee;
}
</style>