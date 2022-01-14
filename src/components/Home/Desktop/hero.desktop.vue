<template>
  <div>
    <div class="hero-bg" style="height:170vh">
     <v-container style="height:100%">
        <v-row align="center" justify="center" style="height:110vh" no-gutters>
          <v-col cols="12">
              <p class="font-bold white--text text-center font-size-1 " style="line-height:1">Make your interior more minimalistic & modern</p>
              <p class="white--text font-size-5 text-center" >Turn your room with panto into a lot more minimalist <br> and modern with ease and speed</p>
             <v-row no-gutters>
               <v-col cols="12" xl="4" lg="4" />
               <v-col cols="12" xl="4" lg="4">
                  <div class="" style="border-radius:40px;height:9vh;position:relative">
                    <v-text-field dark   placeholder="Search furniture"  class="shrink white--text  text-field-transparent search-field font-bold" height="9vh" color="white" rounded></v-text-field>
                    <v-row class="" align="center" justify="center"  no-gutters style="position:absolute;right:0;top:0;height:100%;padding-right:4%">
                      <v-spacer></v-spacer>
                       <v-btn small   icon><v-avatar color="#E58411" size="40"><v-icon color="white">mdi-magnify</v-icon></v-avatar></v-btn>
                    </v-row>
                   
                  </div>
               </v-col>
                <v-col cols="12" xl="4" lg="4" />
             </v-row>
          </v-col>
      </v-row>
     </v-container>
    </div>
  </div>
</template>

<script>
  

  export default {
    name: 'Desktop',

    components: {
      
    },
  }
</script>
<style scoped>
.hero-bg{
  background: url('../../../assets/images/hero.jpg');
  background-size: cover;
} 
.v-input {
    align-items: flex-start;
    display: flex;
    flex: 1 1 auto;
    font-size: 16px !important;
    letter-spacing: normal;
    max-width: 100%;
    text-align: left;
    
}
.theme--light.v-input.search-field input::placeholder {
  color: white !important;
  
}
.v-text-field {
    padding-top: 0 !important;
    margin-top: 0 !important;
}
.v-text-field--rounded{
  border-radius: 40px !important;
}

.text-field-transparent  .v-input__slot {
  background: linear-gradient(45deg, rgba(255,255,255,0.3), rgba(255,255,255,0.3)) !important;
  color: white !important;
}
.v-input.input-field .v-label {
  pointer-events: auto;
}

</style>
