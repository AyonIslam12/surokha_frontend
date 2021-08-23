<template>
<div class="relative">
    <div class="container py-32 mx-auto text-center text-black small-container">
        <div class="mx-auto top-small-container">
            <h1 class="text-4xl font-bold text-black">Register For Veccine</h1>
            <p class="pt-6 mb-20 text-lg">You will just need your NID Card, Phone number and fillup some information</p>
            <div class="flex">
                <div class="w-1/3">
                    <img class="mx-auto" src="~/static/img/promo-1.svg" alt="not-found" />
                    <div class="w-6 h-6 mx-auto mt-16 mb-4 border-4 border-green-600 rounded-full"></div>
                    <p class="text-lg font-bold">NID</p>
                </div>
                <div class="w-1/3">
                    <img class="mx-auto" src="~/static/img/promo-2.svg" alt="not-found" />
                    <div class="w-6 h-6 mx-auto mt-16 mb-4 border-4 border-green-600 rounded-full"></div>
                    <p class="text-lg font-bold">Phone</p>
                </div>
                <div class="w-1/3">
                    <img class="mx-auto" src="~/static/img/promo-3.svg" alt="not-found" />
                    <div class="w-6 h-6 mx-auto mt-16 mb-4 border-4 border-green-600 rounded-full"></div>
                    <p class="text-lg font-bold">Information</p>
                </div>
            </div>

            <div class="flex -mx-4">
                <div class="flex-1 px-4">
                    <nuxt-link to="/" class="relative block px-6 pt-16 pb-10 border border-gray-200 shadow-xl">
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
                    <nuxt-link to="/" class="relative block px-6 pt-16 pb-10 border border-gray-200 shadow-xl">
                        <div class="flex items-center justify-center h-32">
                            <img src="~/static/img/box-2.svg" class="" alt="" />
                        </div>
                        <p class="mt-6 text-lg font-semibold">Vaccine card</p>

                        <div class="absolute left-0 w-full -bottom-5"><img class="mx-auto" src="~/static/img/enter-2.svg" alt="" /></div>
                    </nuxt-link>
                </div>

                <div class="flex-1 px-4">
                    <nuxt-link to="/" class="relative block px-6 pt-16 pb-10 border border-gray-200 shadow-xl">
                        <div class="flex items-center justify-center h-32">
                            <img src="~/static/img/box-3.svg" class="" alt="" />
                        </div>
                        <p class="mt-6 text-lg font-semibold">Certificate</p>

                        <div class="absolute left-0 w-full -bottom-5"><img class="mx-auto" src="~/static/img/enter-3.svg" alt="" /></div>
                    </nuxt-link>
                </div>

                <div class="flex-1 px-4">
                    <nuxt-link to="/" class="relative block px-6 pt-16 pb-10 border border-gray-200 shadow-xl">
                        <div class="flex items-center justify-center h-32">
                            <img src="~/static/img/box-4.svg" class="" alt="" />
                        </div>
                        <p class="mt-6 text-lg font-semibold">FAQs</p>

                        <div class="absolute left-0 w-full -bottom-5"><img class="mx-auto" src="~/static/img/enter-4.svg" alt="" /></div>
                    </nuxt-link>
                </div>
            </div>
        </div>
    </div>
</div>


</template>

<script>
export default {
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
