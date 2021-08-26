<template>
<div class="relative">
    <div class="pt-2 pb-24 primary-bg">
        <div class="container mx-auto">
            <div class="flex items-center">
                <div class="w-full">
                    <h1 class="mb-6 font-bold leading-none text-white uppercase hero-heading">Vaccine</h1>
                    <h2 class="mb-10 font-medium text-white text-7xl">Registration</h2>
                    <p class="text-2xl text-white">Complete the registration by verifying your national identity card and mobile number</p>
                </div>
                <div class="min-w-max">
                    <img width="600" src="~/static/img/vaccine-header.png" alt="" />
                </div>
            </div>
        </div>
    </div>
    <div class="relative">
        <div class="absolute dots-1 left-10 top-10"></div>
        <div class="container py-20 mx-auto text-center small-container">
            <div class="">
                <vaccine-steps theme="homepage" />

                <div class="mb-16 text-left">
                    <h2 class="mb-6 text-4xl font-bold">Get Updates</h2>
                    <p class="text-lg">Check Your Registration Status, Vaccine card, Certificate and See Faqs .</p>
                </div>

                <div class="flex -mx-4">
                    <div class="flex-1 px-4">
                        <nuxt-link to="" class="relative block px-6 pt-16 pb-10 border border-gray-200 shadow-xl">
                            <div class="flex items-center justify-center h-32">
                                <img src="~/static/img/box-1.svg" class="" alt="" />
                            </div>
                            <p class="mt-6 text-lg font-semibold">Check Status</p>

                            <div class="absolute left-0 w-full -bottom-5">
                                <img class="mx-auto" src="~/static/img/enter-1.svg" alt="" />
                            </div>
                        </nuxt-link>
                    </div>

                    <div class="flex-1 px-4">
                        <nuxt-link to="" class="relative block px-6 pt-16 pb-10 border border-gray-200 shadow-xl">
                            <div class="flex items-center justify-center h-32">
                                <img src="~/static/img/box-2.svg" class="" alt="" />
                            </div>
                            <p class="mt-6 text-lg font-semibold">Vaccine card</p>

                            <div class="absolute left-0 w-full -bottom-5">
                                <img class="mx-auto" src="~/static/img/enter-2.svg" alt="" />
                            </div>
                        </nuxt-link>
                    </div>

                    <div class="flex-1 px-4">
                        <nuxt-link to="" class="relative block px-6 pt-16 pb-10 border border-gray-200 shadow-xl">
                            <div class="flex items-center justify-center h-32">
                                <img src="~/static/img/box-3.svg" class="" alt="" />
                            </div>
                            <p class="mt-6 text-lg font-semibold">Certificate</p>

                            <div class="absolute left-0 w-full -bottom-5">
                                <img class="mx-auto" src="~/static/img/enter-3.svg" alt="" />
                            </div>
                        </nuxt-link>
                    </div>

                    <div class="flex-1 px-4">
                        <nuxt-link to="" class="relative block px-6 pt-16 pb-10 border border-gray-200 shadow-xl">
                            <div class="flex items-center justify-center h-32">
                                <img src="~/static/img/box-4.svg" class="" alt="" />
                            </div>
                            <p class="mt-6 text-lg font-semibold">FAQs</p>

                            <div class="absolute left-0 w-full -bottom-5">
                                <img class="mx-auto" src="~/static/img/enter-4.svg" alt="" />
                            </div>
                        </nuxt-link>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="container mx-auto">
        <div class="px-16 py-20 mx-auto text-white primary-bg rounded-3xl">
            <div class="flex items-center">
                <div class="w-1/3 mr-10 font-bold">
                    <h3 class="uppercase text-7xl">Hotline</h3>
                    <p class="text-4xl">Numbers</p>
                </div>
                <div class="w-2/3">
                    <div class="flex flex-wrap -mx-8">
                        <div class="w-1/2 px-8 mb-8">
                            <div class="p-4 text-black bg-white rounded-lg">
                                <div class="flex items-center">
                                    <div class="mr-2 min-w-max">
                                        <img src="~/static/img/phone-pink.svg" alt="" />
                                    </div>
                                    <div class="w-full">
                                        <h4 class="text-4xl font-bold tika-text-pink">333</h4>
                                        <p class="text-xl">National Call Center</p>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="w-1/2 px-8 mb-8">
                            <div class="p-4 text-black bg-white rounded-lg">
                                <div class="flex items-center">
                                    <div class="mr-2 min-w-max">
                                        <img src="~/static/img/phone-green.svg" alt="" />
                                    </div>
                                    <div class="w-full">
                                        <h4 class="text-4xl font-bold tika-text-primary">16263</h4>
                                        <p class="text-xl">Health Portal</p>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="w-1/2 px-8">
                            <div class="p-4 text-black bg-white rounded-lg">
                                <div class="flex items-center">
                                    <div class="mr-2 min-w-max">
                                        <img src="~/static/img/phone-orange.svg" alt="" />
                                    </div>
                                    <div class="w-full">
                                        <h4 class="text-4xl font-bold tika-text-orange">10655</h4>
                                        <p class="text-xl">IEDCR</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="w-1/2 px-8">
                            <div class="p-4 text-black bg-white rounded-lg">
                                <div class="flex items-center">
                                    <div class="mr-2 min-w-max">
                                        <img src="~/static/img/phone-blue.svg" alt="" />
                                    </div>
                                    <div class="w-full">
                                        <h4 class="text-4xl font-bold tika-text-blue">09666777222</h4>
                                        <p class="text-xl">Covid-19 Telehealth</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <ThreeSteps />
    </div>

    <div class="py-20 text-2xl font-bold text-center text-white primary-bg">
        <div class="container mx-auto">
            <div class="flex">
                <div class="flex-1 px-10">
                    <h3 class="mb-4 text-5xl font-bold">10,000,000</h3>
                    <p>Registered</p>
                </div>

                <div class="flex-1 px-10">
                    <h3 class="mb-4 text-5xl font-bold">8,000,000</h3>
                    <p>Vaccinated</p>
                </div>

                <div class="flex-1 px-10">
                    <h3 class="mb-4 text-5xl font-bold">7,000,000</h3>
                    <p>Certificate Issued</p>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
import ThreeSteps from '../components/ThreeSteps.vue'
import VaccineSteps from '../components/VaccineSteps.vue'
export default {
  components: {ThreeSteps, VaccineSteps},
  data() {
    return {

    }

  },
  mounted() {


  },
  methods: {

  }
}
</script>
