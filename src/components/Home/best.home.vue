<template>
  <div style="padding: 5%; background: #f7f7f7">
    <v-container>
      <p class="font-size-2 text-center font-bold">Best selling Product</p>
      <v-row no-gutters>
        <v-col cols="12" xl="4" lg="4" />
        <v-col cols="12" xl="4" lg="4">
          <v-tabs   background-color="#EEEEEE" color="black" grow  style="border-radius: 28px;text-transform:none;"   hide-slider>
            <v-tab active-class="no-bg" id="chair"  style="text-transform:none;" class="font-size-12 font-bold">Chair</v-tab>
            <v-tab id="bed" style="text-transform:none;" class="font-size-12 font-bold">Bed</v-tab>
            <v-tab id="sofa" style="text-transform:none;" class="font-size-12 font-bold">Sofa</v-tab>
            <v-tab id="lamp" style="text-transform:none;" class="font-size-12 font-bold">Lamp</v-tab>
          </v-tabs>
        </v-col>
        <v-col cols="12" xl="4" lg="4" />
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {

mounted(){
    const chair=document.getElementById("chair")
    const bed=document.getElementById("bed")
    const sofa=document.getElementById("sofa")
    const lamp=document.getElementById("lamp")

    chair.addEventListener("click",()=>{
        chair.classList.add("tab-button")
        bed.classList.remove("tab-button")
        sofa.classList.remove("tab-button")
        lamp.classList.remove("tab-button")
    })

    bed.addEventListener("click",()=>{
        bed.classList.add("tab-button")
        chair.classList.remove("tab-button")
        sofa.classList.remove("tab-button")
        lamp.classList.remove("tab-button")
    })

    sofa.addEventListener("click",()=>{
        sofa.classList.add("tab-button")
        bed.classList.remove("tab-button")
        chair.classList.remove("tab-button")
        lamp.classList.remove("tab-button")
    })
    lamp.addEventListener("click",()=>{
        lamp.classList.add("tab-button")
        bed.classList.remove("tab-button")
        sofa.classList.remove("tab-button")
        chair.classList.remove("tab-button")
    })
}
};

</script>

<style scoped>
.v-tab, .v-tab:hover{
    padding: none;
}
.tab-button{
    border-radius:28px;
    background:white;
    margin: 1.2% !important;
}

</style>
