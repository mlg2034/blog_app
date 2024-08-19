<template>
    <div class="app">
       <post-form/>
       <post-list :posts="posts"/>
    </div>
</template>

<script>

import PostForm  from './components/PostForm.vue';
import PostList from './components/Postlist.vue'
export default {
    components:{
        PostList , PostForm
    },
    data() {
        return {
            posts: [
             ]
        };
    },
    methods: {
        createPost(){
            const newPost ={
                id:Date.now(),
                title:this.title,
                body:this.body
            }
            this.posts.push(newPost);
            this.title='';
            this.body = '';
        },
        inputTitle(event){
            this.title=event.target.value;
        },
        inputBody(event){
            this.body=event.target.value;
        }
    }
};
</script>



<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}




.app {
    padding: 20px;
}

</style>