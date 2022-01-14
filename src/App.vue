<template>
  <v-app>
    <v-app-bar
      class="pa-4"
      color="transparent"
      flat
      fixed
    >
      <div class="d-flex align-center">
        <p class="font-heavy white--text font-title">Panto</p>
      </div>

      <v-spacer></v-spacer>
        <v-btn text  style="text-transform:none;color:white" class="font-weight-bold" plain>Furniture <v-icon>mdi-chevron-down</v-icon></v-btn>
         <v-btn text  style="text-transform:none;color:white" class="font-weight-bold" plain>Shop</v-btn>
         <v-btn text  style="text-transform:none;color:white" class="font-weight-bold" plain>About Us</v-btn>
         <v-btn text  style="text-transform:none;color:white" class="font-weight-bold" plain>Contact</v-btn>
      <v-spacer></v-spacer>

     <v-btn plain icon>
       
       <v-icon color="white">mdi-shopping</v-icon>
      <v-avatar size="15" color="orange" style="font-size:108;position:absolute;right:15%;top:-20%" class="white--text font-bold">2</v-avatar>
     </v-btn>
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import "./css/fonts.css"
// import "./css/size.css"

export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
<style>
v-application {
    font-family: 'Gilroy-Light', sans-serif !important;
    line-height: 1.5;
}
</style>
