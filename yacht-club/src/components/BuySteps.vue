<template>
  <div class="main-buy-cont">
    <div class="steps-cont">
      <n-steps v-model:current="current">
        <n-step title="Membership" description="Select the membership you would like to purchase."
          @click="setIsMembership" />
        <n-step title="Payment method" description="Select the payment method to use" @click="setIsPaymentMethod" />
        <n-step title="Payment confirmation" description="Here come old flat top He come grooving up slowly"
          @click="setIsConfirmation" />
      </n-steps>
    </div>

    <div class="radios" v-if="isMembership">
      <strong>Select the membership you would like to purchase:</strong>
      <n-radio-group v-model:value="value" name="radiogroup">
        <n-space>
          <n-radio class="radio" v-for="song in songs" :key="song.value" :value="song.value" :label="song.label" />
        </n-space>
      </n-radio-group>
    </div>

    <div class="payment-method" v-if="isPaymentMethod">
      <n-collapse default-expanded-names="1" accordion>
        <n-collapse-item title="Credit card" name="1">
          <div>
            <n-input v-model:value="value" type="text" placeholder="Cardholder Name" />
            <n-input v-model:value="value" type="text" placeholder="Card Number" />
            <n-input v-model:value="value" type="text" placeholder="Expiration Date" />
            <n-input v-model:value="value" type="text" placeholder="CVV" />
            <n-input v-model:value="value" type="text" placeholder="Billing Address" />

            <n-radio-group v-model:value="value" name="radiogroup">
              <n-space>
                <n-radio class="radio" v-for="method in methods" :key="method.value" :value="method.value"
                  :label="method.label" />
              </n-space>
            </n-radio-group>
          </div>
        </n-collapse-item>
        <n-collapse-item title="PayPal" name="2">
          <div>
            <n-input v-model:value="value" type="text" placeholder="Email" />
            <n-input v-model:value="value" type="text" placeholder="Password" />

            <n-button type="info">
              Login with PayPal
            </n-button>

          </div>
        </n-collapse-item>
      </n-collapse>

    </div>


    <div v-if="isConfirmation">
      <n-list class="profile-info" hoverable clickable>
        <n-list-item>
          <n-thing title="Membership" content-style="margin-top: 10px;">
            <span>Crew Member</span>
          </n-thing>
        </n-list-item>

        <n-list-item>
          <n-thing title="Payment Method" content-style="margin-top: 10px;">
            <span>credit card</span>
          </n-thing>
        </n-list-item>

        <n-list-item>
          <n-thing title="Purchase date" content-style="margin-top: 10px;">
            <span>02/02/2023</span>
          </n-thing>
        </n-list-item>

        <n-list-item>
          <n-thing title="Status" content-style="margin-top: 10px;">
            <span>Successfully acquired</span>
          </n-thing>
        </n-list-item>

      </n-list>

      <n-button @click="" type="info">
        Confirm data
      </n-button>


    </div>
  </div>
</template>

<script setup>
import { ref, computed, onMounted } from "vue";
import Memberships from '../components/Memberships.vue'

const current = ref(0);
const value = ref(null);

const isMembership = ref(false);
const isPaymentMethod = ref(false);
const isConfirmation = ref(false);
const hasMembership = ref(false)



function setIsMembership() {
  isPaymentMethod.value = false
  isConfirmation.value = false
  isMembership.value = true
}

function setIsPaymentMethod() {
  isMembership.value = false
  isConfirmation.value = false
  isPaymentMethod.value = true

}

function setIsConfirmation() {
  isMembership.value = false
  isPaymentMethod.value = false
  isConfirmation.value = true

}

function syncLocalStorage() {


  hasMembership.value = localStorage.getItem('hasMembership')
  console.log("hasMem", hasMembership.value)
}






const songs = [
  {
    value: "crew",
    label: "Crew Member"
  },
  {
    value: "cruise",
    label: "Cruise Member"
  },
  {
    value: "honor",
    label: "Honorable Member"
  }
].map((s) => {
  s.value = s.value.toLowerCase();
  return s;
});

const methods = [
  {
    value: "master",
    label: "Master Card"
  },
  {
    value: "visa",
    label: "Visa"
  },
  {
    value: "amex",
    label: "American Express"
  }
].map((s) => {
  s.value = s.value.toLowerCase();
  return s;
});





onMounted(() => syncLocalStorage())


</script>

<style scoped>
.steps-cont {}

.main-buy-cont {

  width: 100%;
}

.radios {
  display: flex;
  flex-direction: column;

}

.radios strong {
  font-size: 20px;
  margin: 10px;
}

.radio {

  margin: 10px;
}

.payment-method .n-input {
  margin-top: 5px;
}
</style>
