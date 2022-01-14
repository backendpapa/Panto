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
</style>
