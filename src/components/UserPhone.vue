<template>
   <p class="user-info-item">
        <img src="../assets/img/phone.png">
        {{number}}
    </p>
</template>

<script>
    export default {
        name: 'UserPhone',
        props: ['number']
    }
</script>

<style>
    .user-info-item img {
        vertical-align: middle;
        margin-right: 5px;
    }
</style>