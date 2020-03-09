

<template>
  <v-container fluid>
    <v-slide-y-transition mode="out-in">
      <v-layout column align-center>
      <div class="text-header">
        Login
      </div>
      <v-form
    ref="form"
    v-model="valid"
  >
    <v-text-field
      v-model="email"
      :counter="10"
      :rules="emailRules"
      label="Email"
    ></v-text-field>

    <v-text-field
      v-model="password"
      :rules="passwordRules"
      label="Password"
    ></v-text-field>


<v-btn class="mr-4" @click="register">Register</v-btn>


  </v-form>
    </v-layout>
    </v-slide-y-transition>
  </v-container>
</template>

<script>
/* eslint-disable */
export default {
name: 'login',
  data: () => ({
    valid: true,
    email:'',
    emailRules: [
      value => !!value || 'Email is required',
      value => /.+@.+\..+/.test(v) || 'Email must be valid'
    ],
    password: '',
    passwordRules: [
      value => (value && value.length < 20 && value.length > 12) || 'Password must have a length of greater than 12 and less than 20'
    ],
  }),
  methods: {
    
  }
}
</script>
