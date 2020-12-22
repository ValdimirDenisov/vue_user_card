<template>
    <p class="user-info-item">
        <img src="../assets/img/mail.png"> 
        {{mail}}
    </p>
</template>

<script>
    export default {
        name: 'UserMail',
        props: ['mail']
    }
</script>
    
<style>
    .user-info-item img {
        vertical-align: middle;
        margin-right: 5px;
    }
</style>