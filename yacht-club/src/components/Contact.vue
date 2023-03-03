<script setup>
import Title from './Title.vue';
</script>

<template>
    <Title title="Contact" />
    <div class="contact-cont">

        <div class="text-cont">
            <div class="contact-text">
                We are thrilled that you are interested in learning more about us. If you have any questions, comments, or
                concerns, please don't hesitate to contact us. Our team is here to help you with anything you may need.
            </div>
            <n-space vertical class="inputs-cont">
                <n-input v-model:value="value" type="text" placeholder="Your name" />
                <n-input v-model:value="value" type="number" placeholder="Your phone" />
                <n-input v-model:value="value" type="email" placeholder="Your email" />
                <n-input v-model:value="value" type="textarea" placeholder="Your message" />

                <n-button type="info">
                    Send
                </n-button>
            </n-space>
        </div>

        <div class="img-cont">
            <img class="side-img" src="../assets/images/contact.jpg">
        </div>


    </div>
</template>

<style scoped>
.contact-cont {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-evenly;

    width: 100%;
}

.contact-text {
    font-size: 20px;
    margin-bottom: 20px;
}

.text-cont {
    width: 50%;
    height: 100%;
}

.inputs-cont {

    width: 100%;
}

.inputs-cont .n-input {

    margin-top: 10px;
}

.img-cont {
    width: 40%;
}

.side-img {
    width: 100%;
}
</style>
