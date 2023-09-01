<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class="head">

        <v-row>
          <v-col cols="5">
            <div style="position:relative" class="mt-16">
              <h1 class="text-grey">Hello,</h1>
              <h1 class="text-white">I'm TerezzaB</h1>
              <span class="text-grey">Web Developer</span>

              <br />
              <v-btn tile dark class="text-purple mt-8" variant="outlined">Contact me</v-btn>
            </div>
          </v-col>
  
          <v-col cols="2">
            <div class="arrow-down"> 
              <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>

          <v-col cols="5">
            <div class="image mt-16">
              <v-img src="myAvatar.svg" contain max-height="300"></v-img>
            </div>
          </v-col>     
        </v-row>

      </div>

      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" md="6">
              <div class="egg">
                <v-img src="map_pin.png" max-height="200"></v-img>
              </div>
            </v-col>

            <v-col cols="12" md="6">
              <h4 class="mt-16" style="font-size:20px">About me</h4>
              <div style="width:200px">
                <v-slider v-model="slider2" color="purple"></v-slider>
              </div>
              <h5 class="mt-5" style="font-size:16px">I'm creative full stack developer</h5>
              <p class="mt-5 text-grey">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat</p>
              <br />
              <p class="mt-5 text-grey">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat</p>
              <v-btn tile dark color="purple" class="mt-4">Download resume</v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>

      <div class="text-center mt-10">
        <h2>What we Do?</h2>
        <div style="width:200px;margin:0 auto;">
          <v-slider v-model="slider2" color="purple"></v-slider>
        </div>
      </div>
      <div class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12" sm="6" md="4">
              <div class="child">
                  <v-btn icon="fas fa-laptop" color="#efe3fd" class="text-white"></v-btn>
                  <h3 class="ml-3 mt-4">Front End Development</h3>
                  <p class="text-grey ml-3 mt-4 text-caption">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                    <br />
                    Aspernatur ipsa dicta soluta. 
                    <br />
                    Cumque atque voluptatum, us inventore.
                  </p>
              </div>
            </v-col>

            <v-col cols="12" sm="6" md="4">
              <div class="child">
                  <v-btn icon="fas fa-mobile-alt" color="#efe3fd" class="text-white"></v-btn>
                  <h3 class="ml-3 mt-4">Mobile Development</h3>
                  <p class="text-grey ml-3 mt-4 text-caption">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                    <br />
                    Aspernatur ipsa dicta soluta. 
                    <br />
                    Cumque atque voluptatum, us inventore.
                  </p>
              </div>
            </v-col>

            <v-col cols="12" sm="6" md="4">
              <div class="child">
                  <v-btn icon="fas fa-database" color="#efe3fd" class="text-white"></v-btn>
                  <h3 class="ml-3 mt-4">Back End Development</h3>
                  <p class="text-grey ml-3 mt-4 text-caption">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                    <br />
                    Aspernatur ipsa dicta soluta. 
                    <br />
                    Cumque atque voluptatum, us inventore.
                  </p>
              </div>
            </v-col>

          </v-row>
          <v-divider></v-divider>
        </div>
      </div>
      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <v-btn color="purple" class="mr-2">All</v-btn>
          <v-btn color="purple" class="mr-2" variant="tonal">Front End</v-btn>
          <v-btn color="purple" class="mr-2" variant="tonal">Back End End</v-btn>
        </div>
      </v-col>

      <v-col cols="12" class="imgHover">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4"></v-col>
            <v-hover v-slot="{ isHovering, props }">
              <v-card :elevation="isHovering ? 12:2" :class="{ 'on-hover' : isHovering }" v-bind="props">
                <v-img :src="item.img" height="225px" cover></v-img>
              </v-card>
            </v-hover>
          </template>
        </v-row>
      </v-col>

      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="purple" class="mt-4">Load More</v-btn>
        </div>
      </v-col>

      <v-col cols="12" id="page">
        <div class="pre">
          <v-row>
            <v-col cols="12" md="4">
              <v-card class="mx-auto" max-width="344px" height="">
                <v-img src="abstract.jpeg" height="200px" width="344" cover></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>By AAAE IdeaPro | 06 Sep 2023</v-card-subtitle>
                <v-card-text>Lorem ipsum dolor sit amet. Consectetur adipisicing elit</v-card-text>
              </v-card>
            </v-col>

            <v-col cols="12" md="4">
              <v-card class="mx-auto" max-width="344" height="">
                <v-img src="abstract.jpeg" height="200px" cover></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>By AAAE IdeaPro | 06 Sep 2023</v-card-subtitle>
                <v-card-text>Lorem ipsum dolor sit amet. Consectetur adipisicing elit</v-card-text>
              </v-card>
            </v-col>

            <v-col cols="12" md="4">
              <v-card class="mx-auto" max-width="344" height="">
                <v-img src="abstract.jpeg" height="200px" cover></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>By AAAE IdeaPro | 06 Sep 2023</v-card-subtitle>
                <v-card-text>Lorem ipsum dolor sit amet. Consectetur adipisicing elit</v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </v-col>


      <v-col cols="12" id="biog">
        <div class="hire">
          <v-row>
            <v-col cols="12" sm="8">
              <h3 class="mt-10">Hire me for your awesome project</h3>
              <p class="text-grey mt-3">
                Lorem ipsum dolor sit amet. Consectetur adipisicing elit aspernatur ipsa dicta soluta.
              </p>
            </v-col>

            <v-col cols="12" sm="4">
              <v-btn color="purple" class="mt-15">Hire me</v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>

      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>
          <v-col cols="12" sm="4">
            <div class="child">
              <h3 class="text-left">Contact info</h3>
              <v-divider></v-divider>
              <v-btn icon="fas fa-map-marker-alt" class="mt-10" variant="outlined"></v-btn>
              <br />
              <span class="text-caption">Street name, Area 13132</span>
              <br />
              <v-btn icon="fas fa-phone-alt" class="mt-10" variant="outlined"></v-btn>
              <br />
              <span class="text-caption">+1234567890</span>
              <br />
              <v-btn icon="fas fa-envelope" class="mt-10" variant="outlined"></v-btn>
              <br />
              <span class="text-caption">mail_example@gmail.com</span>
              <br />
            </div>
          </v-col>

          <v-col cols="12" sm="8">
            <h3 class="mt-8">Send your message</h3>
            <v-divider></v-divider>
            <span class="text-caption">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat</span>
            
            <v-row class="mt-10">
              <v-col cols="12" sm="6">
                <v-text-field label="First name" variant="outlined"></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-text-field label="Last name" variant="outlined"></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-text-field label="Phone" variant="outlined"></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-text-field label="Email" variant="outlined"></v-text-field>
              </v-col>
            </v-row>
            <v-textarea label="Message" variant="outlined"></v-textarea>
            <v-btn color="purple" class="mt-2">Submit</v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-container>
    <FooterView />
  </v-app>
</template>

<script>
import { defineComponent } from 'vue';

// Components
import NavBar from '@/components/NavBar.vue';
import FooterView from '@/components/FooterView.vue';

export default defineComponent({
  name: 'HomeView',
  setup(){
    return {
      slider2: 50,
      items: [
        {
          img: "p-img1.jpeg",
        },
        {
          img: "p-img2.jpeg",
        },
        {
          img: "p-img3.jpeg",
        },
        {
          img: "p-img4.jpeg",
        },
        {
          img: "p-img5.jpeg",
        },
        {
          img: "p-img6.jpeg",
        },
      ]
    }
  },

  components: {
    NavBar,
    FooterView
  },
});
</script>

<style scoped>
  .v-container { padding: 16px 0; }
  .head { position: relative; text-align: center; padding: 12px; margin-bottom: 6px; height: 400px; width: 100%; color: #FFF; }
  .head:before { content: ""; position: absolute; top: 0; left: 0; height: 100%; width: 50%; background: #000; transform: skew(0deg, 6deg); }
  .head:after { content: ""; position: absolute; top: 0; right: 0; height: 100%; width: 50%; background: #000; transform: skew(0deg, -6deg); }
  .arrow-down { position: absolute; z-index: 9999; bottom: 0; margin: 0 auto; left: 0; right: 0; text-align: center; }
  .image { position: relative; z-index: 9999; }
  .egg { display: grid; margin-left: 100px; margin-top: 50px; width: 356px; height: 300px; background-color: #efe3fd; border-radius: 50% 50% 50% 50% / 60% 60% 40% 0%; align-items: center; }
  .first { width: 100%; height: 280px; text-align: center; padding: 2rem 2rem; }
  .child { display: inline-block; padding: 2rem 1rem; vertical-align: middle; text-align: center; margin-right: 0 2000px; }
  .imgHover { padding: 0 200px; }
  .pre { width: 100%; height: 380px; text-align: center; padding: 0 200px; background-color: #F5F5F5; }
  .hire { width: 100%; height: 200px; padding: 0 200px; background-color: #E9E9E9; margin-top: -24px; }
</style>
