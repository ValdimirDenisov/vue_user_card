<template>
    <p class="user-nickname">{{nick}}</p>
</template>

<script>
    export default {
        name: 'UserNick',
        props: ['nick']
    }
</script>

<style>
    .user-nickname {
        color: #a0a9b3;
        font-size: 18px;
        margin: 5px 0;
        font-family: monospace;
    }
</style>