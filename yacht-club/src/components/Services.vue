<script setup>
import Title from './Title.vue';
import ServiceCard from './ServiceCard.vue';
import services from '../assets/services.json';



console.log("SERVICES", services)
</script>

<template>
    <Title title="Services" />
    <div class="services-cont">
        <ServiceCard v-for="serviceInfo in services" :key="serviceInfo.id" :serviceInfo="serviceInfo.info"
        :serviceName="serviceInfo.service" 
        :serviceImage="serviceInfo.image" 
        />


    </div>
</template>

<style scoped>
.services-cont {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;

    justify-content: center;

}

.n-card {
    max-width: 300px;
    margin: 15px;
}

.card-content {
    display: flex;
    flex-direction: column;
}
</style>
