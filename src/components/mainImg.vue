<template>
    <img v-bind:src="img" class="user-photo">
</template>

<script>
    export default {
        name: 'UserImg',
        props: ['img']
    }
</script>

<style>
    .user-photo {
        box-sizing: border-box;
        height: 150px;
        margin-top: -100px;
        border-radius: 50%;
        border: 3px solid #ccc;
    }
</style>