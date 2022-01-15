<template>
  <div style="margin-top:10%;position:relative;margin-bottom:10%">
      <div class="bg-shape" style="width:35%;background-color:#F7F7F7;border-bottom-right-radius:20px;border-top-right-radius:20px;">

      </div>
       <div style="width:45%;background-color:#F7F7F7;height:40vh;position:absolute;top:20%;border-bottom-right-radius:20px;border-top-right-radius:20px;">

      </div>
      <v-row  style="position:absolute;width:100%;top:0" no-gutters>
          <v-col cols="12" xl="6" lg="6" class="">
              <br>
              <br>
              <v-img eager class="shadow" width="80%" contain src="../../assets/images/experience.png">

              </v-img>
          </v-col>
          <v-col class="" cols="12" xl="6" lg="6">
            <v-row no-gutters align="center" justify="center" style="height:100%">
                 <v-container style="padding-right:20%">
                  <p class=" font-size-12 font-regular" style="color:#E58411">EXPERIENCES</p>
              <p class="font-size-2 font-bold" style="line-height:1" >We Provide You The Best Experience</p>
              <p class="" style="margin-right:10%">You don’t have to worry about the result because all of these interiors are made by people who are professionals in their fields with an elegant and lucurious style and with premium quality materials</p>
              <p><v-btn text plain style="text-transform:none" class="font-size-12" small color="orange darken-5">More info <v-icon>mdi-arrow-right</v-icon></v-btn></p>
             </v-container>
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
.shadow{
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    border-radius: 20px;
    border-bottom-left-radius:0;
    border-top-left-radius:0;
}
.bg-shape{
    height:70vh;

}
@media screen and (max-width: 500px){
    .bg-shape{
    height:30vh;

}
}
</style>