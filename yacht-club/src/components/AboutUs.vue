<script setup>
import Title from './Title.vue';
</script>

<template>
    <Title title="About Us" />
    <div class="about-cont">
        <div>
            <img class="side-img" src="../assets/images/yacth-side.jpg">
        </div>
        <div class="side-text">

            <div class="text-cont">
                <h3 class="about-title-text"> We are delighted to have you here and look forward to sharing our passion for
                    the open sea with you.
                </h3>
                <p class="about-content-text">Whether you're a seasoned sailor or a newcomer to the world of boating,
                    Nautica offers something for
                    everyone. From our state-of-the-art facilities and top-of-the-line equipment to our expert instructors
                    and friendly community, we strive to provide an unparalleled experience for all members.</p>
                <div class="numbers-cont">
                    <div class="number">
                        <span>20+</span>
                        <strong>years</strong>
                    </div>
                    <div class="number">
                        <span>60+</span>
                        <strong>yachts</strong>
                    </div>
                    <div class="number">
                        <span>500+</span>
                        <strong>members</strong>
                    </div>

                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.about-cont {

    display: flex;
    flex-direction: row;
    padding: 50px;

    align-items: center;
}

.about-title-text {
    font-size: 30px;


}

.side-text {

    width: 100%;
}



.about-content-text {
    font-size: 15px;
    text-align: justify;
    text-justify: inter-word;
}



.text-cont {

    display: flex;
    flex-direction: column;
    width: 100%;
}

.side-img {
    width: 80%;

}

.numbers-cont {
    margin-top: 5%;
    display: flex;
    flex-direction: row;
    justify-content: space-around;


}

.numbers-cont span {
    color: #2080F0;
    font-size: 45px;



}

.number {

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;


}
</style>
