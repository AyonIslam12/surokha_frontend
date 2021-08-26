<template>
 <div>
    <div class="pb-10 text-lg text-center text-white primary-bg">
      <div class="container mx-auto">
        <h2 class="mb-6 text-4xl font-bold">Vaccine Registration</h2>
        <p>Complete the registration by verifying your national identity card and mobile number in the form below. The place and date of delivery of the vaccine will be informed in due course through SMS message on the mobile phone.</p>
      </div>
    </div>
    <div class="py-20">
       <div class="mx-auto small-container">
          <vaccine-steps theme="step_1" />

          <div class="py-10 bg-white border-gray-100 px-18">
           <div class="">
              <h3 class="mb-6 text-4xl font-bold text-center">Identity Verification</h3>

              <!-- <div  class="p-4 mb-6 text-red-900 bg-red-200">
                Error Message
              </div> -->


              <p class="mb-6">
                <label class="tika-label" for="category_id">Select category </label>
                <select v-model="category_id" class="tika-input" id="category_id">
                  <option selected="selected" value="">Select a category</option>
                  <option v-for="item in categories" :key="item.id" :value="item.id">{{item.name}}</option>
                </select>
              </p>


              <div  v-if="category_id" class="flex -mx-4">
                <div class="w-2/3 px-4">
                  <p class="mb-6">
                    <label for="id_no" class="tika-label">National ID Number</label>
                    <input id="id_no" type="number" class="tika-input" placeholder="Type your national ID card number">
                  </p>
                </div>
                <div class="w-2/3 px-4">
                  <p class="mb-6">
                    <label for="dob" class="tika-label">Date of birth</label>
                    <input id="dob" type="date" class="tika-input" placeholder="Type your national ID card number">
                  </p>
                </div>
              </div>

              <p><button class="primary-btn">Check my information</button></p>
            </div>

          </div>
       </div>
    </div>
     <div class="container mx-auto">
      <ThreeSteps/>
    </div>
 </div>
</template>

<script>
import ThreeSteps from '../components/ThreeSteps.vue'
import VaccineSteps from '../components/VaccineSteps.vue'
export default {
  name: 'registration',
  components: { VaccineSteps,ThreeSteps },
  data(){
    return{
       categories: [],
       category_id: '',
    }
  },
    mounted() {
    this.getAvailableCategory();
  },
  methods:{
     getAvailableCategory() {
      this.$axios.get('/categories').then(res => {
        this.categories = res.data;
      })
    },
  }


}
</script>

<style>

</style>
