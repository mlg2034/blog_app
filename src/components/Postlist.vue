<template>
    <div>
        <div v-for="post in posts"  class="post">
            <div><strong>Title:</strong> {{ post.title }}</div>
            <div><strong>Description:</strong> {{ post.body }}</div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.post {
    padding: 15px;
    border: 2px solid teal;
    margin-top: 10px;
}
</style>