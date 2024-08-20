<template>
    <div>
        <form @submit.prevent>
            <h4>Create a post</h4>
            <my-input  v-model="post.title" type="text" placeholder="Type a title" />
            <my-input class="input" v-model="post.body" type="text" placeholder="Type a body" />
            <my-button @click="createPost" style="margin-top: 15px;">Create</my-button>
        </form>
    </div>
</template>

<script>
    import MyButton from "@/components/UI/MyButton.vue"

export default {
    components:{
        MyButton
    },
    data() {
        return {
            post: {
                title: '',
                body: '',
            }
        }
    },
    methods: {
        createPost() {
            this.post.id = Date.now();
            this.$emit('create', this.post)
            this.post = {
                title: '',
                body: '',
            }

        },
    }
}
</script>

<style>
form {
    display: flex;
    flex-direction: column
}

</style>