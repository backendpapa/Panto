<template>
  <div class="mar" style="position:relative;">
      <div class="bg-shape" style="width:35%;background-color:#F7F7F7;border-bottom-left-radius:20px;border-top-left-radius:20px;border-top-right-radius:0;position:absolute;right:0;top:0">

      </div>
       <div style="width:45%;background-color:#F7F7F7;height:40vh;position:absolute;top:20%;right:0;border-bottom-left-radius:20px;border-top-left-radius:20px;margin-top:10%;">

      </div>
      <v-row  style="position:absolute;width:100%;top:0" no-gutters>
          
          <v-col class="" cols="12" xl="6" lg="6">
           <v-container style="padding:10%">
                <v-row  no-gutters align="center" justify="center" style="height:100%">
                
             <div>
                  <p class=" font-size-12 font-regular" style="color:#E58411">MATERIALS</p>
              <p class="font-size-2 font-bold" style="line-height:1" >Very Serious Materials For Making Furniture</p>
              <p class="" style="margin-right:10%">Because panto was very serious about designing furniture for our environment, using a very expensive and famous capital but at a relatively low price</p>
              <p><v-btn text plain style="text-transform:none" class="font-size-12 " small color="orange darken-5">More info <v-icon>mdi-arrow-right</v-icon></v-btn></p>
             </div>
            </v-row>    
           </v-container>
          </v-col>
          <v-col cols="12" xl="6" lg="6" class="">
             
              <v-row no-gutters>
                  <v-col cols="4">
                      <p><v-img eager style="border-radius:20px" src="../../assets/images/1.png"></v-img></p>
                      <p><v-img eager style="border-radius:20px" src="../../assets/images/2.png"></v-img></p>
                  </v-col>
                  <v-col cols="6">
                      <div style="margin-right:-30%">
                <v-row no-gutters>
                    <v-spacer></v-spacer>
                      <v-img   eager class="shadow2 im"    src="../../assets/images/materials.png">

              </v-img>
                </v-row>
              </div>
                  </v-col>
              </v-row>
          </v-col>
      </v-row>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.shadow2{
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    border-radius: 20px !important;
    border-bottom-right-radius:0 !important;
    border-top-right-radius:0 !important;
}
.bg-shape{
    height:70vh;

}
.mar{
    margin-top:0;
}
.im{
    height: 300;
}
@media screen and (max-width: 500px){
    .bg-shape{
    height:30vh;

}
.mar{
    margin-top:100%
}
.im{
    height: 200;
}
}
</style>