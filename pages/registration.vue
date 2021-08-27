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
          <vaccine-steps :theme="step" />

          <div class="py-10 bg-white border-gray-100 px-18">
            <!-- for Step 1 -->
          <div  v-if="step == 'step_1'" class="">
              <h3 class="mb-6 text-4xl font-bold text-center">Identity Verification</h3>

               <div v-if="peopleData.hasOwnProperty('success') && !peopleData.success"  class="p-4 mb-6 text-red-900 bg-red-200 rounded-3xl">
               {{ peopleData.message }}
              </div>
              <p class="mb-6">
                <label class="tika-label" for="category_id">Select category </label>
                <select v-model="verifyData.category_id" class="tika-input" id="category_id">
                  <option selected="selected" value="">Select a category</option>
                  <option v-for="item in categories" :key="item.id" :value="item.id">{{item.name}}</option>
                </select>
              </p>

              <div  v-if="verifyData.category_id" class="flex -mx-4">
                <div class="w-2/3 px-4">
                  <p class="mb-6">
                    <label for="id_no" class="tika-label">National ID Number</label>
                    <input v-model="verifyData.id_no" id="id_no" type="number" class="tika-input" placeholder="Type your national ID card number">
                  </p>
                </div>
                <div class="w-2/3 px-4">
                  <p class="mb-6">
                    <label for="dob" class="tika-label">Date of birth</label>
                    <input v-model="verifyData.dob" id="dob" type="date" class="tika-input" placeholder="Type your national ID card number">
                  </p>
                </div>
              </div>

              <p  v-if="verifyData.category_id"><button @click.prevent="checkMyInformation()" class="primary-btn">Check my information</button></p>
          </div>
          <!-- endfor Step 1 -->

          <!-- for Step 2 -->
          <div v-if="step == 'step_2'">
             <h3 class="font-bold text-4xl mb-6 text-center">User Information</h3>

              <p class="mb-6">
                <label class="tika-label" for="division_id">Select Division </label>
                <select @change.prevent="getAvailableDistricts" v-model="division_id"  class="tika-input" id="division_id">
                  <option selected="selected" value="">Select a division</option>
                  <option v-for="item in divisions" :key="item.id" :value="item.id">{{item.name}}</option>
                </select>
              </p>

              <p  v-if="districts.length" class="mb-6">
                <label class="tika-label" for="district_id">Select District </label>
                <select @change.prevent="getAvailableUpazilas()" v-model="district_id"  class="tika-input" id="district_id">
                  <option selected="selected" value="">Select a district</option>
                   <option v-for="item in districts" :key="item.id" :value="item.id">{{item.name}}</option>
                </select>
              </p>

              <p v-if="upazilas.length"  class="mb-6">
                <label class="tika-label" for="upazila_id">Select Upazila </label>
                <select @change.prevent="getAvailableCenters"  v-model="upazila_id" class="tika-input" id="upazila_id">
                  <option selected="selected" value="">Select a upazila</option>
                  <option v-for="item in upazilas" :key="item.id" :value="item.id">{{item.name}}</option>
                </select>
              </p>
              <p v-if="centers.length"  class="mb-6">
                <label class="tika-label" for="center_id">Select Vaccination Center </label>
                <select v-model="center_id" class="tika-input" id="center_id">
                  <option selected="selected" value="">Select a center</option>
                  <option v-for="item in centers" :key="item.id" :value="item.id">{{item.name}}</option>
                </select>
              </p>
              <p v-if="!centers.length && upazila_id">
                No center available
              </p>


              <div  class="">
                <p class="mb-6">
                  <label for="name" class="tika-label">Name</label>
                  <input id="name"  type="text" class="tika-input" placeholder="Type your name">
                </p>
                <p class="mb-6">
                  <label for="diabates" class="tika-label">Do you have diabates?</label>
                  <select  class="tika-input" id="diabates">
                    <option selected="selected" value="">Select a value</option>
                    <option value="1">Yes</option>
                    <option value="0">No</option>
                  </select>
                </p>
              </div>

              <p><button  class="primary-btn">Submit</button></p>
          </div>
          <!-- End for Step 2 -->

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
       step: 'step_1',
       peopleData: [],
       peopleData: [],
      verifyData: {
        category_id: '',
        id_no: '',
        dob: ''
      },
      divisions: [],
      division_id: '',
      districts: [],
      district_id: '',
      upazilas: [],
      upazila_id: '',
      centers: [],
      center_id: '',
    }
  },
    mounted() {
    this.getAvailableCategory();
    this.getAvailableDivisions();

  },
  methods:{
     getAvailableCategory() {
      this.$axios.get('/categories').then(res => {
        this.categories = res.data;
      })
    },
     checkMyInformation() {
      this.$axios.post('/verify', this.verifyData).then(res => {
        this.peopleData = res.data;
        if(res.data.success) {
           this.step = 'step_2'
        }
      })
    },
     getAvailableDivisions() {
      this.$axios.get('/divisions').then(res => {
        this.divisions = res.data;
      })
    },
    getAvailableDistricts() {
      this.$axios.get('/districts?division_id=' + this.division_id).then(res => {
        this.districts = res.data
      })
    },
    getAvailableUpazilas() {
      this.$axios.get('/upazilas?district_id=' + this.district_id).then(res => {
        this.upazilas = res.data
        })
    },
    getAvailableCenters() {
      this.$axios.get('/vaccination-centers?upazila_id=' + this.upazila_id).then(res => {
        this.centers = res.data
      })
    },

  }


}
</script>

<style>

</style>
