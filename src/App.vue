<template>
    <div class="app">
        <post-form @create="createPost" />
        <post-list :posts="posts" />
    </div>
</template>

<script>

import PostForm from './components/PostForm.vue';
import PostList from './components/Postlist.vue'
export default {
    components: {
        PostList, PostForm
    },
    data() {
        return {
            posts: [
            ]
        };
    },
    methods: {
        createPost(post) {
            this.posts.push(post);
        },
        inputTitle(event) {
            this.title = event.target.value;
        },
        inputBody(event) {
            this.body = event.target.value;
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