<template>
    <div>
        <form @submit.prevent>
            <h4>Create a post</h4>
            <input class="input" @input="post.title=$event.target.value" v-bind:value="post.title" type="text" placeholder="Type a title">
            <input class="input" @input="post.body=$event.target.value" v-bind:value="post.body" type="text" placeholder="Type a body">
            <button class="btn" >Create</button>
        </form>
    </div>
</template>

<script>
export default {


    data(){
        return{
            post:{
                title:'',
                body:'',
            }
        }
    }
}
</script>

<style>
form {
    display: flex;
    flex-direction: column
}

.btn {
    align-self: flex-end;
    margin-top: 15px;
    padding: 10px 15px;
    background-color: none;
    color: teal;
    border: 1px solid teal;
    border-radius: 8px;

}

.input {
    width: 100%;
    padding: 10px 15px;
    border: 2px solid teal;
    margin-top: 10px;
}
</style>