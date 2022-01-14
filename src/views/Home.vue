<template>
  <div>
   
    <index />
  </div>

</template>

<script>
  
import Index from '../components/Home/index.vue'
  export default {
    name: 'Home',

    components: {
      Index
    },
  }
</script>
<style>


.text-field-transparent  .v-input__slot {
  background: linear-gradient(45deg, rgba(255,255,255,0.3), rgba(255,255,255,0.3)) !important;
  color: white !important;
}


</style>
