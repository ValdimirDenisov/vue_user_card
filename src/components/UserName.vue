<template>
    <p class="user-name">
        {{name}}
    </p>
</template>

<script>
    export default {
        name: 'UserName',
        props: ['name']
    }
</script>

<style>
    .user-name {
        font-size: 30px;
        font-weight: 900;
        line-height: 1.4;
        margin: 5px 0;
    }
</style>