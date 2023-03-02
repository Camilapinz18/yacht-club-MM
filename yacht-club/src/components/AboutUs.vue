<script setup>

</script>

<template>
    <h1>Abprt</h1>
    <div class="about-cont">
        <div>
            <img class="side-img" src="../assets/images/yacth-side.jpg">
        </div>
        <div class="side-text">

            <div class="text-cont">
                <h3> We are delighted to have you here and look forward to sharing our passion for the open sea with you.
                </h3>
                <p>Whether you're a seasoned sailor or a newcomer to the world of boating, Nautica offers something for
                    everyone. From our state-of-the-art facilities and top-of-the-line equipment to our expert instructors
                    and friendly community, we strive to provide an unparalleled experience for all members.</p>
                <div class="numbers-cont">
                    <div>
                        <h1>20+</h1>
                        <span>years</span>
                    </div>
                    <div>
                        <h1>60+</h1>
                        <span>yachts</span>
                    </div>
                    <div>
                        <h1>500+</h1>
                        <span>members</span>
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
    justify-content: space-around;
    align-items: center;
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
   
    display: flex;
    flex-direction: row;
    justify-content: space-around;
}</style>
