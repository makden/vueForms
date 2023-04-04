<template>
   <h3>Список постов</h3>

   <PostIetm 
      v-for="post in posts"
      :post="post" 
   />
</template>
<script>
import PostIetm from './postIetm.vue';

export default {
    props: {
        posts: {
            type: Array,
            required: true
        }
    },
    components: { PostIetm }
}
</script>

<style>
   


</style>