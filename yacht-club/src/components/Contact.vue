<script setup>

</script>

<template>
    <h1>COntact</h1>
    <div class="contact-cont">

        <div>

            <div class="text-cont">

                <n-space vertical class="inputs-cont">
                    <n-input v-model:value="value" type="text" placeholder="Your name" />
                    <n-input v-model:value="value" type="number" placeholder="Your phone" />
                    <n-input v-model:value="value" type="email" placeholder="Your email" />
                    <n-input v-model:value="value" type="textarea" placeholder="Your message" />
                </n-space>



            </div>
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
    padding: 50px;
    align-items: center;
    justify-content: space-around;
    
    width: 100%;
}

.text-cont {
   
    width: 100%;
    height: 100%;

}

.inputs-cont{
    background-color: rebeccapurple;
    width:100%;
}



.img-cont {
    width: 40%;
    background-color: yellow;
}

.side-img {
    width: 100%;


}
</style>
