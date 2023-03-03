<script setup>
import Title from './Title.vue';
</script>

<template>
    <div class="footer-cont">
        <div class="footer-info">
            <div>
                <img class="logo-img" src="../assets/images/logoW.png" />
                <div class="address-cont">
                    <div class="address">
                        <h3>Office</h3>
                        <span>25 Rue de la République</span>
                        <span>Bureau 7</span>
                        <span>Nice, 06000</span>
                        <span>France</span>
                        <span>+33 6 12 34 56 78</span>
                    </div>
                    <div class="address">
                        <h3>Club</h3>
                        <span>Nautica Club Méditerranée</span>
                        <span>Quai des Docks</span>
                        <span>Port de la Pointe Rouge</span>
                        <span>Marseille, 13008</span>
                        <span>France</span>
                        <span>+33 7 89 01 23 45</span>
                    </div>


                </div>
                <h3>contact@yachtclubprovence.fr</h3>
                <n-back-top :right="100" />
            </div>

            <!-- <img class="map-image" src="../assets/images/map.png" /> -->
        </div>

    </div>
</template>

<style scoped>
.footer-cont {
    background-color: #24466B;
    height: 30%;
    margin: 0 auto;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    padding-bottom: 40px;
    margin-top:20px
}

.footer-info {
    padding-top: 2%;
    width: 90%;
    display: flex;
    flex-direction: row;
    color: white;
    align-items: center;
}

.address {
    display: flex;
    flex-direction: column;
    margin: 10px;

}

.logo-img {
    width: 15%;
}

.address-cont {
    margin-top: 30px;
    display: flex;
    flex-direction: row;
    color: white;
}

.map-image {
    width: 30%;
}
</style>
