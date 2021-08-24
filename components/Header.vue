<template>
  <div>
    <div class="primary-bg">
      <div class="container pt-20 pb-10 mx-auto">
        <div class="bg-white">
          <div class="flex items-center">
            <div class="min-w-max">
              <h2 class="px-6 text-2xl font-bold text-black uppercase "><nuxt-link to="/">TIKA</nuxt-link></h2>
            </div>

            <div class="w-full">
              <ul class="flex justify-center">
                <li><nuxt-link class="menu-item" to="/">Home</nuxt-link></li>
                <li><nuxt-link class="menu-item" to="/registration">Registration</nuxt-link></li>
                <li><nuxt-link class="menu-item" to="/verify">Verify</nuxt-link></li>
                <li><nuxt-link class="menu-item" to="/tika-card">Tika Card</nuxt-link></li>
                <li><nuxt-link class="menu-item" to="/help">Help</nuxt-link></li>
                <li><nuxt-link class="menu-item" to="/faqs">Faqs</nuxt-link></li>
              </ul>
            </div>

            <div class="min-w-max">
              <div class="px-6">
                <nuxt-link class="primary-btn" to="/">Register Now</nuxt-link>
              </div>
            </div>
          </div>
        </div>
        <!-- <div class="flex items-center">
          <div class="w-full">
            <h1 class="mt-6 mb-6 font-bold leading-none text-white uppercase hero-heading">Vaccine</h1>
            <h2 class="mb-8 font-medium text-white uppercase text-7xl">Registration</h2>
            <p class="text-2xl text-white">Complete the registration by varifying your national identity card and mobile number</p>
          </div>
          <div class="min-w-max">
            <img src="~/static/img/vaccine-header.png" alt="not-found">
          </div>
        </div> -->
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>
