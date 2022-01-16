<template>
  <div class="mar2">
      <v-container>
          <p class="font-regular orange--text font size-12 text-center" >TESTIMONIALS</p>
          <p class="font-bold font-size-2 text-center mb-n1">Our Client Reviews</p>
       
           <div class="mar3">
        <carousel loop    dots nav items="3" autoWidth class="carousel">
         <v-card v-for="i in testimonials" :key="i.title"  flat class=" mr-3 carousel-card" width="230" :style="`border-radius:20px;position:relative;margin:15%;background:url(${i.bg});
    background-size: cover;`"  >
            <!-- <div class="" > -->
               
            <!-- </div> -->
            <div style="position:absolute;height:60%;bottom:0;width:100%;">
                <div style="margin:3%;height:90%;border-radius:20px" class="white">
                        <div style="position:absolute;top:-20%;width:95%" class="pa-4">
                            <v-row no-gutters>
                                <v-spacer></v-spacer>
                                <v-avatar color="white">
                                    <v-img eager :src="i.icon"></v-img>
                                </v-avatar>
                                <v-spacer></v-spacer>
                            </v-row>
                        </div>
                        <br>
                      
                        <p class="text-center font-bold font-size-12 mb-n1">{{i.name}}</p>
                        <p class=" text-center grey--text " style="font-size:10px">{{i.title}}</p>
                    
                        <p class="text-center " style="font-size:10px">{{i.desc}}</p>
                       <v-row class="mt-n1" no-gutters>
                           <v-spacer></v-spacer>
                            <v-rating small color="orange" background-color="orange" dense value="4"></v-rating>
                            <v-spacer></v-spacer>
                       </v-row>
                </div>
            </div>
           
         </v-card>
        </carousel>
      </div>
      </v-container>
  </div>
</template>

<script>
import carousel from "vue-owl-carousel2";
export default {
    components:{
        carousel
    },
    data(){
        return {
            testimonials:[
        {name:"Bang Upin",title:"Pedagang Asongan",desc:"“Terimakasih banyak, kini ruanganku menjadi lebih mewah dan terlihat mahal“",bg:require("../../assets/images/a1.png"),icon:require("../../assets/images/i1.png")},
        {name:"Ibuk Sukijan",title:"Ibu Rumah Tangga",desc:"“Makasih Panto, aku sekarang berasa tinggal di apartment karena barang-barang yang terlihat mewah“",bg:require("../../assets/images/a5.png"),icon:require("../../assets/images/i2.png")},
        {name:"Mpok Ina",title:"Karyawan Swasta",desc:"“Sangat terjangkau untuk kantong saya yang tidak terlalu banyak“",bg:require("../../assets/images/a4.png"),icon:require("../../assets/images/i3.png")}
    ]
        }
    }
}
</script>

<style>
.mar2{
    margin-top:40%;
}
.carousel-card{
    height:55vh;
    /* background:url('../../assets/images/a1.png');
    background-size: cover; */
    
}
 .mar3{
     margin-top: 0.5em;
 }   
@media screen and (max-width: 500px){
 .mar3{
     margin-top: 5%;
 }   
.mar2{
    margin-top:190% !important;
}
.carousel-card{
    height:45vh;
    /* background:url('../../assets/images/a1.png');
    background-size: cover; */
    
}
}
</style>