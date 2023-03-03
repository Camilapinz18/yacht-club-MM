<script setup>
import SideMenu from '../components/SideMenu.vue'
import BuySteps from '../components/BuySteps.vue';
import ProfileInfo from '../components/ProfileInfo.vue';

import { ref, onMounted } from "vue";
import {RouterLink} from 'vue-router'
const showBuyStepsRef = ref(false);
const showAlertRef = ref(true);
const hasMembership = ref(false)

let showBuySteps = false
function purchaseMembership() {

    showBuyStepsRef.value = true
    showAlertRef.value = false
    console.log("ghola", showBuyStepsRef.value)
}

function checkIfUserHasMembership() {
    let randNumber = Math.round(Math.random() * 1)
    console.log("randNumber", randNumber)

    if (randNumber === 1) {
        hasMembership.value = true
        localStorage.setItem('hasMembership', true)
    } else if (randNumber === 0) {
        hasMembership.value = false
        localStorage.setItem('hasMembership', false)
    }

    console.log("has", hasMembership.value)
}

function logout(){
   
}

onMounted(() => checkIfUserHasMembership())
</script>

<template>
    <div class="bg-cont">
        <div class="main-cont">
            <n-collapse>
                <n-collapse-item title="My account" name="1">
                    <div class="account-cont">
                        <div class="img-cont">
                            <img class="profile-img" src="../assets/images/profile.jpg" />
                        </div>
                        <div class="account-info">
                            <ProfileInfo />
                        </div>
                    </div>
                </n-collapse-item>

                <n-collapse-item title="My membership" name="2">
                    <div class="membership-cont" v-if="!hasMembership">
                        <n-alert title="Membership not found" type="info">
                            It seems like you dont have a membership yet. Purchase one now!
                        </n-alert>
                        <n-button @click="purchaseMembership" type="info">
                            Purchase my membership!
                        </n-button>
                    </div>
                    <div v-if="showBuyStepsRef">
                        <BuySteps />
                    </div>
                    <div v-if="hasMembership">
                        <n-card title="Crew Member" class="card-membership">
                            <template #cover>
                                <div class="image-container">
                                    <img class="membership-img" src="../assets/images/crew-y.jpg">
                                </div>

                            </template>
                            <div>
                                <n-list class="profile-info" hoverable clickable>
                                    <n-list-item>
                                        <n-thing title="Purchase date" content-style="margin-top: 10px;">
                                            <span>02/02/23</span>
                                        </n-thing>
                                    </n-list-item>

                                    <n-list-item>
                                        <n-thing title="Period" content-style="margin-top: 10px;">
                                            <span>02/02/24</span>
                                        </n-thing>
                                    </n-list-item>


                                </n-list>
                            </div>
                            <n-button @click="logout" type="info">
                                Change my membership
                            </n-button>
                        </n-card>


                    </div>

                </n-collapse-item>
                <n-button type="error">
                    <RouterLink to="/">Logout</RouterLink> 
            </n-button>
            </n-collapse>

           
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

.membership-cont {

    display: flex;
    flex-direction: column;

    align-items: center;
}

.profile-img {
    width: 100%;
    border-radius: 50%;
}

.img-cont {
    width: 30%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.account-info {
    width: 50%;
    padding-left: 3%;
}

.account-cont {
    display: flex;
    flex-direction: row;
    width: 100%;

    justify-content: space-evenly;
}

.membership-cont .n-button {
    margin: 20px;
}

.main-cont {
    width: 80%;
    background-color: white;
    height: fit-content;
    border-radius: 10px;
    display: flex;
    flex-direction: row;
    padding: 20px;
}

.membership-img {
    height: fit-content
}

.card-membership {
    width: 50%;


}

.image-container {
    width: 300px;

    height: 100px;

    overflow: hidden;

}
</style>
