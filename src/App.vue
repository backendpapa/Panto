<template>
  <v-app>
    <v-app-bar id="nav-bar" class="pa-4" :color="color" flat fixed>
      <div class="d-flex align-center">
        <p class="font-heavy font-title" :style="`color:${colo}`">Panto</p>
      </div>

      <v-spacer></v-spacer>
      <div class="d-none d-sm-flex mt-n5">
        <div class="d-flex align-center">
          <v-btn
            text
            :style="`text-transform:none;color:${colo}`"
            class="font-bold"
            plain
            >Furniture <v-icon>mdi-chevron-down</v-icon></v-btn
          >
          <v-btn
            text
            :style="`text-transform:none;color:${colo}`"
            class="font-bold"
            plain
            >Shop</v-btn
          >
          <v-btn
            text
            :style="`text-transform:none;color:${colo}`"
            class="font-bold"
            plain
            >About Us</v-btn
          >
          <v-btn
            text
            :style="`text-transform:none;color:${colo}`"
            class="font-bold"
            plain
            >Contact</v-btn
          >
        </div>
      </div>
      <v-spacer></v-spacer>

      <v-btn plain icon class="mt-n5">
        <v-icon :color="colo">mdi-shopping</v-icon>
        <v-avatar
          size="15"
          color="orange"
          style="font-size: 108; position: absolute; right: 15%; top: -20%"
          class="white--text font-bold"
          >2</v-avatar
        >
      </v-btn>
      <v-app-bar-nav-icon
        :style="`color:${colo}`"
        class="mt-n5 d-flex d-sm-none"
      ></v-app-bar-nav-icon>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>

     <v-footer padless>
   <v-container>
      <v-col
      
      style="padding:5% 0"
      cols="12"
    >
      <v-row align="center" justify="center" no-gutters>
        <v-col cols="12" xl="5" lg="5">
          <p class="font-bold font-size-2">Panto</p>
          <p class="font-size-12">The advantage of hiring a workspace with us is that givees you comfortable service and all-around facilities.</p>
        </v-col>
        <v-col cols="4" xl="2" lg="2">
          <p class="orange--text font-size-12 font-bold">Services</p>
          <a href="" style="text-decoration:none;" class="black--text font-size-12">Email Marketing</a><br>
          <a href="" style="text-decoration:none;" class="black--text font-size-12">Campaigns</a><br>
          <a href="" style="text-decoration:none;" class="black--text font-size-12">Branding</a><br>
        </v-col>
         <v-col cols="4" xl="2" lg="2">
          <p class="orange--text font-size-12 font-bold">Furniture</p>
          <a href="" style="text-decoration:none;" class="black--text font-size-12">Beds</a><br>
          <a href="" style="text-decoration:none;" class="black--text font-size-12">Chair</a><br>
          <a href="" style="text-decoration:none;" class="black--text font-size-12">All</a><br>
        </v-col>
         <v-col cols="4" xl="2" lg="2">
          <p class="orange--text font-size-12 font-bold">Follow us</p>
          <a href="" style="text-decoration:none;" class="black--text font-size-12"><v-icon size="15" class="mt-n1">mdi-facebook</v-icon> Facebook</a><br>
         <a href="" style="text-decoration:none;" class="black--text font-size-12"><v-icon size="15" class="mt-n1">mdi-twitter</v-icon> Twitter</a><br>
         <a href="" style="text-decoration:none;" class="black--text font-size-12"><v-icon size="15" class="mt-n1">mdi-instagram</v-icon> Instagram</a><br>
        </v-col> 
        <v-col cols="12" xl="1" lg="1" />
      </v-row>

    </v-col>
    <v-row align="center" no-gutters>
      <v-col cols="12" xl="3" lg="3"><p class="mb-n1 centraled"  style="font-size:10px">Copyright &#169; 2022</p></v-col>
      <v-col cols="12" xl="6" lg="6"></v-col>
      <v-col cols="12" xl="3" lg="3">
        <div style="display:flex;justify-content:center;align-item:center;height:100%">
          <a href="" style="text-decoration:none;font-size:10px" class="black--text font-bold mr-4">Terms & Conditiions</a>
          <a href="" style="text-decoration:none;font-size:10px" class="black--text font-bold">Privacy Policy</a>
        </div>
      </v-col>

    </v-row>
   </v-container>
  </v-footer>
  </v-app>
</template>

<script>
import "./css/fonts.css";
import "./css/Animation.css";

export default {
  name: "App",

  data: () => ({
    //
    color: "transparent",
    colo: "#faedcb",
  }),
  mounted() {
    const navbar = document.getElementById("nav-bar");
    window.addEventListener("scroll", () => {
      if (window.scrollY > 20) {
        this.color = "#faedcb";
        this.colo = "black";
        navbar.classList.add("scale-in-center");
      } else {
        this.color = "transparent";
        this.colo = "#faedcb";
        navbar.classList.remove("scale-in-center");
        navbar.classList.add("scale-out-center");
      }
    });
  },
};
</script>
<style>
.centraled{
    text-align: left;
  }
@media screen  and (max-width:500px) {
  .centraled{
    text-align: center;
    padding-bottom: 7px !important;
  }
}
</style>
