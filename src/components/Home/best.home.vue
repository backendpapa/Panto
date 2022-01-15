<template>
  <div style="padding: 5%; background: #f7f7f7">
    <v-container>
      <p class="font-size-2 text-center font-bold">Best selling Product</p>
      <v-row no-gutters>
        <v-col cols="12" xl="4" lg="4" />
        <v-col cols="12" xl="4" lg="4">
          <v-tabs
            background-color="#EEEEEE"
            color="black"
            grow
            style="border-radius: 28px; text-transform: none"
            hide-slider
          >
            <v-tab
              active-class="no-bg"
              id="chair"
              style="text-transform: none"
              class="font-size-12 font-bold"
              >Chair</v-tab
            >
            <v-tab
              id="bed"
              style="text-transform: none"
              class="font-size-12 font-bold"
              >Bed</v-tab
            >
            <v-tab
              id="sofa"
              style="text-transform: none"
              class="font-size-12 font-bold"
              >Sofa</v-tab
            >
            <v-tab
              id="lamp"
              style="text-transform: none"
              class="font-size-12 font-bold"
              >Lamp</v-tab
            >
          </v-tabs>
        </v-col>
        <v-col cols="12" xl="4" lg="4" />
      </v-row>
<br>
      <div>
        <carousel loop    dots nav items="4" autoWidth class="carousel">
         <v-card v-for="i in products" :key="i.category" flat class=" mr-3 carousel-card" width="230" style="border-radius:20px;position:relative;margin:15%"  color="#FAFAFA">
            <!-- <div class="" > -->
               
            <!-- </div> -->
            <div style="height:45%;position:absolute;background-color:white;width:100%;bottom:0;border-top-left-radius:0;border-top-right-radius:0;border-bottom-right-radius:20px;border-bottom-left-radius:20px">
                    <div class="ma-5" style="position:relative;;height:80%">
                        <p class="font-size-12 mb-n1">{{i.category}}</p>
                        <p class="font-size-9 font-bold mb-n1">{{i.title}}</p>
                        <v-rating color="orange" background-color="orange" value="5" x-small dense></v-rating>
                        <v-row class="" style="position:absolute;bottom:0;width:100%"  align="center" justify="center" no-gutters>
                            <div style="display:flex;" >
                                <p class="font-size-12 mt-n1 font-bold">&#36;</p>
                                <p class="font-bold font-size-7 mb-n1">{{i.price}}</p>
                            </div>
                            <v-spacer></v-spacer>
                            <v-btn class="mt-n2" small style="background:black" icon rounded><v-icon color="white">mdi-plus</v-icon></v-btn>
                        </v-row>
                    </div>
            </div>
              <v-img eager width="200" style="position:absolute;top:-10%;z-index:2; " contain aspect-ratio="1"  :src="i.img" ></v-img>
         </v-card>
        </carousel>
      </div>
      <br>
      <p class="text-center"><v-btn color="orange" class="font-regular" style="text-transform:none" text>View all <v-icon>mdi-arrow-right</v-icon></v-btn></p>
    </v-container>
  </div>
</template>

<script>
import carousel from "vue-owl-carousel2";
export default {
  components: { carousel },
  data(){
      return {
          products:[
              {category:"Chair",title:"Sakarias Armchair",price:392,img:require('../../assets/images/chair1.png')},
              {category:"Chair",title:"Baltsar Chair",price:299,img:require('../../assets/images/chair2.png')},
              {category:"Chair",title:"Anjay Chair",price:519,img:require('../../assets/images/chair3.png')},
              {category:"Chair",title:"Nyantuy Chair",price:921,img:require('../../assets/images/chair4.png')},
              
          ]
      }
  },
  mounted() {
    const chair = document.getElementById("chair");
    const bed = document.getElementById("bed");
    const sofa = document.getElementById("sofa");
    const lamp = document.getElementById("lamp");

    chair.addEventListener("click", () => {
      chair.classList.add("tab-button");
      bed.classList.remove("tab-button");
      sofa.classList.remove("tab-button");
      lamp.classList.remove("tab-button");
    });

    bed.addEventListener("click", () => {
      bed.classList.add("tab-button");
      chair.classList.remove("tab-button");
      sofa.classList.remove("tab-button");
      lamp.classList.remove("tab-button");
    });

    sofa.addEventListener("click", () => {
      sofa.classList.add("tab-button");
      bed.classList.remove("tab-button");
      chair.classList.remove("tab-button");
      lamp.classList.remove("tab-button");
    });
    lamp.addEventListener("click", () => {
      lamp.classList.add("tab-button");
      bed.classList.remove("tab-button");
      sofa.classList.remove("tab-button");
      chair.classList.remove("tab-button");
    });
  },
};
</script>

<style scoped>
.v-tab,
.v-tab:hover {
  padding: none;
}
.tab-button {
  border-radius: 28px;
  background: white;
  margin: 1.2% !important;
}
.carousel-card{
    height:55vh;
    
}
.carousel{
    height:60vh !important;
}

@media screen and (max-width:500px) {
    .carousel-card{
    height:40vh !important;
}
.carousel{
    height:45vh !important;
}
}
</style>
