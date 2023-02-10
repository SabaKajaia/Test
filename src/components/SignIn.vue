<!-- COMPONENTE BOILERPLATE -->
 
<template>

  <div class="container">
    <div class="header">
      <div class="header-description">
        <h3 class="header-title">Sign In to ToDo App</h3>
        <p class="header-subtitle">Get organized with your tasks!</p>
      </div>
    </div>

    <form @submit.prevent="signIn" class="form-sign-in p-8 flex flex-col bg-light-grey rounded-md">
      <div class="form flex flex-col mb-2">
        <div class="form-input">
          <label class="input-field-label mb-1 text-sm text-at-light-green">E-mail</label>
          <input type="email" class="input-field p-2 text-gray-500 focus:outline-one" placeholder="example@gmail.com"
            id="email" v-model="email" required />
        </div>
        <div class="form-input flex-col mb-2">
          <label class="input-field-label">Password</label>
          <input type="password" class="input-field p-2 text-gray-500 focus:outline-one" placeholder="**********"
            id="password" v-model="password" required />
        </div>
        <button
          class="button mt-6 py-2 px-6 rounded-sm self-start text-sm text-white bg-at-light-green duration-200 border border-transparent hover:border-white hover:bg-white hover:text-at-light-green"
          type="submit">Sign In</button>
        <p>
          Don't have an account?
          <PersonalRouter :route="route" :buttonText="buttonText" class="sign-up-link" />
        </p>
      </div>
    </form>

    <div v-show="errorMsg">{{ errorMsg }}</div>
  </div>
</template>

<script setup>
import PersonalRouter from "./PersonalRouter.vue";

// Route Variables
const route = "/auth/signup";
const buttonText = "Sign Up";

// Arrow function to Signin user to supaBase
const signIn = async () => {
  try { } catch (error) { }
};
</script>

<style>

</style>
