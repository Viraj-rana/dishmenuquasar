<template>
  <q-page>
    <div class="q-pa-md row items-start ">
    <q-card class="my-card">
      <q-card-section class="bg-primary text-white">
        <div class="text-h10">Menu</div>
        <div class="text-subtitle5">Indian dishes</div>
      </q-card-section>

      <q-separator />

      <q-card-actions vertical align="center">
        <q-btn link ref="../layouts/BlankLayout.vue" type="menu dishes" href="http://localhost:8084/#/menu/login">Menu of dishes</q-btn>
        <q-btn flat>Guests</q-btn>
      </q-card-actions>
    </q-card>
    <div class="q-pa-md row items-start "></div>
    <div class="q-pa-md row items-start "></div>
    <div class="q-pa-md row items-start "></div>
    <div class="text-h3">Guests</div>
    <div class="q-pa-md example-break-row">
<div class="row items-start example-container">
  <q-btn class="example-cell bg-standard text-red" tabindex="0">Guest registration</q-btn>
  <div class="q-pa-md row items-start "></div>
    <div class="q-pa-md row items-start "></div><div class="q-pa-md row items-start "></div>
    <div class="q-pa-md row items-start "></div>
  <q-btn class="example-cell" tabindex="0">Guest Table</q-btn>
</div>

</div>
    </div>
    <div class="row">
      <div class="col-12 col-md-4 col-lg-4 q-pa-xl">
        <div class="text-center">
          <q-img class="logo" src="~/src/assets/menu.jpg" />
        </div>
<div class="text-h4 text-bold q-mt-lg">Spa web</div>
        <div class="text-grey-7">Guest registration</div>
        <div class="column">
          <q-input
            outlined
            label="Enter email*"
            v-model="form.email.value"
            :error="form.email.error"
            :error-message="form.email.msg"
          >
            <template v-slot:append>
              <q-icon name="email"></q-icon>
            </template>
          </q-input>

          <q-input
            class="q-mt-sm"
            label="Enter password*"
            outlined
            v-model="form.Password.value"
            :error="form.Password.error"
            :error-message="form.Password.msg"
            >
            <template v-slot:append>
              <q-icon name="lock"></q-icon>
            </template>
          </q-input>
          <q-input
            class="q-mt-sm"
            outlined
            label="Enter Surname*"
            v-model="form.Surname.value"
            :error="form.Surname.error"
            :error-message="form.Surname.msg"
          >
            <template v-slot:append> <q-icon name="face"></q-icon></template>
          </q-input>
          <q-input
            class="q-mt-sm"
            outlined
            label="Enter Name*"
            v-model="form.Name.value"
            :error="form.Name.error"
            :error-message="form.Name.msg"
          >
            <template v-slot:append> <q-icon name="boy"></q-icon></template>
          </q-input>
          <q-input
            class="q-mt-sm"
            outlined
            label="Enter DOB*"
            v-model="form.DateofBirth.value"
            :error="form.DateofBirth.error"
            :error-message="form.DateofBirth.msg"
          >
            <template v-slot:append> <q-icon name="lan"></q-icon></template>
          </q-input>
          <q-input
            class="q-mt-sm"
            outlined
            label=" Paul*"
            v-model="form.Paul.value"
            :error="form.Paul.error"
            :error-message="form.Paul.msg"
          >
            <template v-slot:append> <q-icon name="man"></q-icon></template>
          </q-input>
          <q-input
            class="q-mt-sm"
            outlined
            label="Enter Address*"
            v-model="form.Address.value"
            :error="form.Address.error"
            :error-message="form.Address.msg"
          >
            <template v-slot:append> <q-icon name="home"></q-icon> </template>
          </q-input>
          <q-input
            class="q-mt-sm"
            outlined
            label="Enter phone*"
            v-model="form.phone.value"
            :error="form.phone.error"
            :error-message="form.phone.msg"
          >
            <template v-slot:append> <q-icon name="phone"></q-icon></template>
          </q-input>
        </div>
        <div class="column q-mt-sm">
            <q-btn label="Guest Registration" color="primary" @click="alert = true"/>
             <q-dialog v-model="alert">
      <q-card>
        <q-card-section>
          <div class="text-h6">Registration success</div>
        </q-card-section>
        <q-card-section class="q-pt-none">
        Please minimize the page with CTRL+- to exit</q-card-section>
        <q-card-actions align="right">
          <q-btn link flat label="OK" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
         <q-btn>
              <q-btn color="primary" label="Save" />
            </q-btn>
        </div>
      </div>
      </div>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'
const form = ref({
  email: {
    value: '',
    email: true,
    required: true
  },
  Password: {
    value: '',
    Password: true,
    required: true
  },
  Surname: {
    value: '',
    Surname: true,
    required: true
  },
  Name: {
    value: '',
    Name: true,
    required: true
  },
  DateofBirth: {
    value: '',
    DateofBirth: true,
    required: true
  },
  Paul: {
    value: '',
    Paul: true,
    required: true
  },
  Address: {
    value: '',
    Address: true,
    required: true
  },
  phone: {
    value: '',
    phone: true,
    required: true
  }
})
// const Save = () => {}
</script>
<style lang="sass">
.example-break-row
  .flex-break
    flex: 1 0 100% !important
    height: 0 !important

  .example-container
    .example-cell
      margin: 1px
      padding: 8px 18px
      box-shadow: inset 0 0 0 2px #9e9e9e
</style>
<style scoped>
.logo {
  width: 100%;
  margin-left: 250;
}
</style>
<script>
export default {
  setup () {
    return {
      alert: ref(false)
    }
  }
}
</script>
