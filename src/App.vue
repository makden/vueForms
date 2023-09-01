<template>
    <postForm
      @addPost="addPost"
    />
    <postList
      :posts="posts"
      @removeItem="removePost"
    />

</template>

<script>
  import  postForm  from "./components/postForm.vue";
  import  postList  from "./components/postList.vue";
  export default{
    components:{
      postForm,
      postList
    },
    data(){
      return {
        posts:[
          {id:1, title:'Title 1', body: 'Text decoraion 1'},
          {id:2, title:'Title 2', body: 'Text decoraion 2'},
          {id:3, title:'Title 3', body: 'Text decoraion 3'},
          {id:4, title:'Title 4', body: 'Text decoraion 4'},
          {id:5, title:'Title 5', body: 'Text decoraion 5'},
        ]
      }
    },
    methods:{
      addPost(post){
        this.posts.push(post);
      },
      removePost(post){
        this.posts = this.posts.filter(item => item.id !== post.id)
      }
    }
  }
</script>



<style scoped>
</style>
