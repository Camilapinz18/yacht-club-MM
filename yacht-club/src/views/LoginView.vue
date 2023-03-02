<script setup>
import {RouterLink} from 'vue-router'

</script>

<template>
    <div class="bg-cont">

        <div class="login-cont">
            <div class="image-cont">
                <img class="image-side" src="../assets/images/login-side.jpg" />
            </div>
            <div class="inputs">
                <img class="logo-img" src="../assets/images/logoB.png" />



                <div class="memberships-cont">
                    <n-card content-style="padding: 0;" class="accordion">
                        <n-tabs type="line" size="large" :tabs-padding="20" pane-style="padding: 20px;">
                            <n-tab-pane name="Login">

                                <div class="card-cont">

                                    <n-input class="input" size="large" round placeholder="Email" />
                                    <n-input class="input" size="large" round placeholder="Password" />

                                </div>
                                <n-button type="info">
                                    <RouterLink to="/account">Login</RouterLink>
                                </n-button>


                            </n-tab-pane>
                            <n-tab-pane name="Sign up">

                                <div class="card-cont">

                                    <n-input class="input" size="large" round placeholder="Full name" />
                                    <n-input class="input" size="large" round placeholder="Email" />
                                    <n-input class="input" size="large" round placeholder="Password" />
                                    <n-input class="input" size="large" round placeholder="Phone" />
                                    <n-input class="input" size="large" round placeholder="Address" />

                                </div>
                                <n-button type="info">
                                    Sign up
                                </n-button>


                            </n-tab-pane>

                        </n-tabs>
                    </n-card>
                </div>
            </div>
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

.login-cont {
    width: 80%;
    background-color: white;
    height: 70%;
    border-radius: 10px;
    display: flex;
    flex-direction: row;
}

.image-side {
    height: 100%;
    border-bottom-left-radius: 10px;
    border-top-left-radius: 10px;
}

.image-cont {
    width: 50%;
}

.logo-img {
    width: 80%;
}

.inputs {
    display: flex;
    flex-direction: column;

    /* justify-content: center; */
    align-items: center;
    padding-top: 5%;

}

.input {
    width: 100%;
    margin: 5px;
}
</style>
