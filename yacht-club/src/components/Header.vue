<script setup>
import Navbar from './Navbar.vue';
</script>

<template>
    <div class="main-img">
        <Navbar />
        <div class="welcome-cont">
            <h1 class="welcome-text">Welcome to Nautica, the premier yacht club for boating enthusiasts</h1>
            <n-space>
            <n-button type="info">
                Get started
            </n-button>
        </n-space>
        </div>
        

    </div>
</template>

<style scoped>
.main-img {
    background-image: url('../assets/images/main.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    height: 100vh;

}

.welcome-cont {

    width: 50%;
    margin-top: 20%;
    margin-left: 2%;

}

.welcome-text {
    color: white;
    font-size: 40px;
    text-shadow: 1px 1px 2px black;

}
</style>
