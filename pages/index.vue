<template>
<div>
  <button @click.prevent="getBackendRequest()">Request Api</button>
  <h1 v-if="apiValue" class="font-bold text-3xl">check: {{apiValue}}</h1>
   <Tutorial/>

</div>

</template>

<script>
export default {
  data() {
    return {
      apiValue: '',
    }

  },
  mounted() {


  },
  methods: {
    getBackendRequest(){
      this.$axios.get('/test').then(res => {
       this.apiValue = res.data;
      })
    }
  }
}
</script>
