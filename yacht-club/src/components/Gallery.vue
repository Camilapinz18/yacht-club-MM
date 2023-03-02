<script setup>

</script>

<template>
    <div class="gallery-cont">
        <n-carousel show-arrow>
            <img class="carousel-img" src="../assets/images/car1.jpg">
            <img class="carousel-img" src="../assets/images/car2.jpg">
            <img class="carousel-img" src="../assets/images/car3.jpg">
            <img class="carousel-img" src="../assets/images/car4.jpg">
            <img class="carousel-img" src="../assets/images/car5.jpg">
            <img class="carousel-img" src="../assets/images/car6.jpg">
        </n-carousel>
    </div>
</template>

<style scoped>
.gallery-cont {
    height: 100%;
}

.gallery-cont .n-carousel {
    height:fit-content;
    
}

.carousel-img {
    width: 100%;
    height: 80%;
    object-fit: cover;
}
</style>
