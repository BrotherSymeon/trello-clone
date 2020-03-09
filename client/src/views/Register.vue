

<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
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
    <v-text-field
      v-model="confirmPassword"
      :rules="confirmPasswordRules"
      label="Confirm Password"
    ></v-text-field>
    <v-text-field
      v-model="displayName"
      :counter="10"
      :rules="displayNameRules"
      label="Display Name"
    ></v-text-field>
    <v-text-field
      v-model="imageUrl"
      :counter="10"
      :rules="imageUrlRules"
      label="Avatar"
    ></v-text-field>


<v-btn class="mr-4" @click="register">Register</v-btn>


  </v-form>
      </v-col>
    </v-row>

  </v-container>
</template>

<script>
/* eslint-disable */
export default {
name: 'register',
        data() {  
          return {
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
       confirmPassword: '',
       confirmPasswordRules: [
         v => (v === this.password) || 'Passwords must match'
       ],
       displayName: '',
       imageUrl: '',
          }
        }
}
</script>
