<template>
  <div class="text-center">
    <h2 class="mb-6 text-4xl font-bold">Register for Vaccine</h2>
    <p class="text-lg">You will just need your NID Card, Phone number and filling up some info </p>
    <div class="flex my-16 -mx-6">
      <div class="flex-1 px-6">
        <div class="flex items-center justify-center h-32">
          <img class="mx-auto" src="~/static/img/promo-1.svg" alt="">
        </div>
        <div class="relative w-6 h-6 mx-auto mt-8 mb-4 border-4 border-green-600 rounded-full tika-step"></div>
        <p class="text-lg font-bold">NID</p>
      </div>

      <div class="flex-1 px-6">
        <div class="flex items-center justify-center h-32">
          <img v-if="theme == 'homepage' || theme == 'step_2' || theme == 'step_3'" class="mx-auto" src="~/static/img/promo-2.svg" alt="">
          <img v-if="theme == 'step_1'" class="mx-auto" src="~/static/img/promo-2-disabled.svg" alt="">
        </div>
        <div v-bind:class="theme == 'homepage' || theme == 'step_2 ' || theme == 'step_3' ? 'border-green-600' : 'border-gray-400'" class="relative w-6 h-6 mx-auto mt-8 mb-4 border-4 rounded-full tika-step"></div>
        <p class="text-lg font-bold">Phone</p>
      </div>

      <div class="flex-1 px-6">
        <div class="flex items-center justify-center h-32">
          <img v-if="theme == 'homepage' || theme == 'step_3' " class="mx-auto" src="~/static/img/promo-3.svg" alt="">
          <img v-if="theme == 'step_1' || theme == 'step_2'" class="mx-auto" src="~/static/img/promo-3-disabled.svg" alt="">
        </div>
        <div v-bind:class="theme == 'homepage' || theme == 'step_3' ? 'border-green-600' : 'border-gray-400'" class="relative w-6 h-6 mx-auto mt-8 mb-4 border-4 rounded-full tika-step"></div>
        <p class="text-lg font-bold">Information</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "VaccineSteps",
  props: ["theme"]
}
</script>

<style scoped>
</style>
