<template>
  <div class="container">
    <div class="form-wrapper">
      <div class="form-title">
        Send your data
      </div>
      <form>
        <input placeholder="First Name" type="text" v-model="firstName" :class="{'error': !firstNameValid}">

        <input placeholder="Last Name" type="text" v-model="lastName" :class="{'error': !lastNameValid}">

        <input placeholder="Email" type="email" v-model="email" :class="{'error': !emailValid}">

        <input placeholder="Address" v-model="address" :class="{'error': !addressValid}">

        <button type="submit" @click.prevent="submitForm">Submit</button>
      </form>
    </div>
  </div>

</template>

<script setup>
import {ref} from 'vue'

const firstName = ref('')
const lastName = ref('')
const email = ref('')
const address = ref('')
const firstNameValid = ref(true)
const lastNameValid = ref(true)
const emailValid = ref(true)
const addressValid = ref(true)

function submitForm() {
  if (validateForm()) {
    // Do something with the form data
    console.log({
      firstName: firstName.value,
      lastName: lastName.value,
      email: email.value,
      address: address.value,
    })
    clearForm()
    alert('Form submitted successfully!')
  }
}

function clearForm() {
  firstName.value = ''
  lastName.value = ''
  email.value = ''
  address.value = ''
  firstNameValid.value = true
  lastNameValid.value = true
  emailValid.value = true
  addressValid.value = true
}

function validateForm() {
  firstNameValid.value = firstName.value !== ''
  lastNameValid.value = lastName.value !== ''
  emailValid.value = /\S+@\S+\.\S+/.test(email.value)
  addressValid.value = address.value !== ''
  return firstNameValid.value && lastNameValid.value && emailValid.value && addressValid.value
}
</script>
<style lang="scss">

.form-wrapper {
  margin-top: 123px;
  margin-bottom: 100px;
  width: 100%;
  height: 100%;
  border-radius: 14px;
  background-position: center;
  object-fit: cover;
  background-repeat: no-repeat;
  background-image: url("../assets/images/bg-form.png");
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding: 60px 0;

  .form-title {
    color: #FFFFFF;
    margin-bottom: 17px;
    text-align: center;
    font-weight: 700;
    font-size: 50px;
    line-height: 61px;
  }

  form {
    width: 395px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    input {
      margin-bottom: 16px;
      padding: 15px 30px;
      background: #FFFFFF;
      border: 1px solid #C8C2C6;
      border-radius: 38px;
      width: 100%;
      line-height: 28px;

      &::placeholder {
        font-size: 18px;
        color: #888888;

      }

    }

    .error {
      border: 1px solid #ff0000;
    }

    button {
      margin-top: 24px;

    }
  }
}


</style>
