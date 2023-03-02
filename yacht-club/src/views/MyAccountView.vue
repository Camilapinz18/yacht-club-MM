<script setup>
import SideMenu from '../components/SideMenu.vue'
import BuySteps from '../components/BuySteps.vue';

</script>

<template>
    <div class="bg-cont">
        <div class="main-cont">
           <SideMenu/>
           <BuySteps/>
            
            
        </div>

    </div>
</template>

<style scoped>
.bg-cont {
    /* background-image: url('../assets/images/login-bg.jpg'); */
    background-color: #24466B;
    background-size: cover;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.main-cont {
    width: 80%;
    background-color: white;
    height: 90%;
    border-radius: 10px;
    display: flex;
    flex-direction: row;
}
</style>
