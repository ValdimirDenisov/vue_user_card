<template>
    <p class="user-info-item">
        <img src="../assets/img/location.png">
        {{location}}
    </p>
</template>

<script>
    export default {
        name: 'UserLocation',
        props: ['location']
    }
</script>

<style>
    .user-info-item img {
        vertical-align: middle;
        margin-right: 5px;
    }   
</style>