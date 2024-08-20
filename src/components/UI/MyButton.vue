<template>
    <button class="btn">
        <slot></slot>
    </button>
</template>

<script>
export default {
    name: 'my-button'
}
</script>

<style>
.btn {
    align-self: flex-end;
    padding: 10px 15px;
    background-color: white;
    color: teal;
    border: 1px solid teal;
    border-radius: 8px;
}
</style>