<template>
  <v-app>
        <v-app-bar
        app
        color="black"
        dark
        inverted-scroll
        >
        <!--inverted-scrol, think about it for the app-bar -->
          <!-- <v-toolbar-title color="white">Affra Technology</v-toolbar-title> -->
          <v-img
          src="./assets/Huvudbild.jpg"
          max-height="100"
          max-width="100"></v-img>
          <v-spacer></v-spacer>
        </v-app-bar>
        
        <v-main>
          <div id="bg" onscroll="blur()"></div>
          <v-container class="pa-0">
            <!--<v-img
            class="fill-height"
              lazy-src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
              max-height="450"
              width=150%
              src="./assets/AFFRA AB.jpg"
              ></v-img> -->
          </v-container>
          <v-container class="px-0">
            <!-- cards are an option, though they seem to be built horizontally-->
            <div class="d-flex flex-no-wrap">
              <v-img align=left src="./assets/Annons bild.jpg"
              max-height="272"
              max-width="448"></v-img>
              <v-card align=right elevation-1 height="272" width="741">
              <v-card-title class=".text-h5">Introduction</v-card-title>
              <v-card-text>
                  <p class="intro">We are a consulting company specializing in engineering and we have a even deeper focus on CI, HIL, autonomous drive and much else. <br>
                    We strive to keep up with our customers needs while keeping our co-workers wishes intact. Our goal is to be simple to work with and for.
                  </p>
                </v-card-text>
            </v-card>
            </div>
          </v-container>
          <v-container class="px-0">
            <div class="d-flex flex-no-wrap">
              <v-card align=left elevation-1 height="272" width="741">
              <v-card-title class=".text-h5">Hardware In Loop</v-card-title>
              <v-card-text>
                  <p class="hil">Hardware in Loop or HIL testing is a method to test software running on the hardware it was designed for. It is widely used in embedded system testing. The HIL is the final testing stage before the SW product is released to the intended unit and is tested in the final product or prototypes of the product.<br> 
Depending on the complexity of the SW tested, the test system needs to release electric, network and physical signals. This is done using simple arduino circuts or scalable real-time tools from major suppliers like National Instruments, Vector or dSpace and modelling tools like Simulink,  GT-suite or CarMaker.
                  </p>
                </v-card-text>
            </v-card>
            <v-img align=right src="./assets/bulb.jpg"
            max-height="272"
            max-width="448">
            </v-img>
            </div>
          </v-container>
          <v-container class="px-0 mb-6">
            <div class="d-flex flex-no-wrap">
              <v-img align=left src="./assets/sommar2021.png"
            max-height="272"
            max-width="448"
            ></v-img>
            <v-card align=right elevation-1 height="272" width="741">
              <v-card-title class=".text-h5">Who we are</v-card-title>
              <v-card-text>
                  <p class="intro">We are hardworking, fun loving, and dedicated developers with our goal set on a healthy worplace and relation between co-workers.
                  </p>
                </v-card-text>
            </v-card>
            </div>
          </v-container>
          <v-container class="px-0">
            <div class="d-flex flex-no-wrap">
              <v-card align=left elevation-1 height="272" width="741">
              <v-card-title class=".text-h5">Our services</v-card-title>
              <v-card-text><p class="services">We offer services in: <br>
                              - HIL development, complete and domain level <br>
                              - Function development in simulink and python <br>
                              - Vehicle/engine testing and calibration, electric vehicles
</p></v-card-text>
            </v-card>
            <v-img align=right src="./assets/engine.jpg"
            max-height="272"
            max-width="448">
            </v-img>
            </div>
          </v-container>
          <v-footer
        color="White"
        height="100">
        <v-list two-line>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>+46708 18 41 37</v-list-item-title>
              <v-list-item-subtitle>William Bruun</v-list-item-subtitle>
            </v-list-item-content>
            <v-list-item-avatar>
                <v-img src="https://static.vecteezy.com/system/resources/previews/000/422/862/original/avatar-icon-vector-illustration.jpg"></v-img>
              </v-list-item-avatar>
          </v-list-item>
        </v-list>
        </v-footer>
        </v-main>
      </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
    
  }),
};
window.onscroll = function() {blur()}

function blur(){
  if (document.body.scrollTop > 50 || document.documentElement.scrollTop > 50) {
    document.getElementById("bg").className ="blur";
  } else {
    document.getElementById("bg").className = "";
  }
}
</script>

<style scoped lang="scss">

#bg {
  background-image: url("./assets/AFFRA AB.jpg");
  min-height: 80%;

  /* Parallax effect*/
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.blur{
  filter: blur(4px);
  -webkit-filter: blur(4px);
  transition: 0.5s ease-in-out
}

 .services{
   font-size: 1.2rem;
 }

 .hil{
   font-size: 1.1rem;
 }

 .intro{
   font-size: 1.2rem;
   text-align: left;
 }
</style>
