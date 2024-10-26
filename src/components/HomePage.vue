<template>
  <v-container>
    <v-row class="d-flex justify-center">
      <v-col cols="12" lg="10" class="body pa-0 my-lg-16 my-5 px-3">
        <v-col class="head d-flex align-center px-0">
          <div class="logo d-flex align-center">
            <img src="/src/assets/logo.svg" alt="" />
          </div>
          <v-spacer></v-spacer>
          <div class="link pa-0 d-none d-md-flex">Home</div>
          <div class="link mx-9 d-none d-md-flex">New</div>
          <div class="link d-none d-md-flex">Popular</div>
          <div class="link mx-9 d-none d-md-flex">Trending</div>
          <div class="link d-none d-md-flex">Categories</div>
          <!-- BURGER -->
          <div>
            <img
              src="/src/assets/icon-menu.svg"
              alt="Menu Icon"
              class="menu-icon d-flex flex-column d-md-none"
              @click="dialog = true"
            />

            <v-dialog
              v-model="dialog"
              fullscreen
              class="custom-dialog d-flex d-md-none"
              transition="dialog-right-transition"
            >
              <v-sheet class="dialog-content" height="100%">
                <img
                  src="/src/assets/icon-menu-close.svg"
                  alt="Close Icon"
                  class="close-icon"
                  @click="dialog = false"
                />

                <v-list class="burger-list">
                  <v-list-item
                    v-for="link in links"
                    :key="link.text"
                    class="pa-0 pl-2"
                  >
                    <v-list-item-title>
                      <a href="">{{ link.text }}</a>
                    </v-list-item-title>
                  </v-list-item>
                </v-list>
              </v-sheet>
            </v-dialog>
          </div>
          <!--  -->
        </v-col>
        <v-col class="d-flex flex-wrap mt-4 px-0">
          <v-col
            cols="12"
            md="8"
            class="left pa-0 d-flex flex-wrap flex-column"
          >
            <v-col class="pa-0 d-none d-md-flex">
              <img
                class="img1"
                src="/src/assets/image-web-3-desktop.jpg"
                alt=""
              />
            </v-col>
            <v-col class="pa-0 d-flex d-md-none">
              <img
                class="img1"
                src="/src/assets/image-web-3-mobile.jpg"
                alt=""
              />
            </v-col>
            <v-col class="lower mt-6 d-flex flex-md-row flex-column pa-0">
              <v-col class="left1 pa-0 mb-4">
                <div class="heading">The Bright Future of Web 3.0?</div>
              </v-col>
              <v-col class="right1 d-flex flex-column pa-0 pl-md-1">
                <div class="para">
                  We dive into the next evolution of the web that claims to put
                  the power of the platforms back into the hands of the people.
                  But is it really fulfilling its promise?
                </div>
                <div class="btn mt-6 mb-10 mb-md-0">
                  <v-btn
                    rounded="0"
                    elevation="0"
                    class="read-more px-6 py-5 d-flex align-center"
                    >READ MORE</v-btn
                  >
                </div>
              </v-col>
            </v-col>
          </v-col>
          <v-col cols="12" md="4" class="right py-0 pr-0 pl-md-7 pl-0">
            <v-col class="right-body text-white d-flex flex-column pa-0 px-2">
              <div class="new px-3 pt-5 pb-1">New</div>
              <v-col class="blogs">
                <div class="heading1">Hydrogen VS Electric Cars</div>
                <div class="para1">
                  Will hydrogen-fueled cars ever catch up to EVs?
                </div>
              </v-col>
              <v-col class="px-3 my-1">
                <div class="line px-10"></div>
              </v-col>
              <v-col class="blogs">
                <div class="heading2">The Downsides of Al Artistry</div>
                <div class="para2">
                  What are the possible adverse effects of on-demand Al image
                  generation?
                </div>
              </v-col>
              <v-col class="px-3 my-1">
                <div class="line px-10"></div>
              </v-col>
              <v-col class="blogs">
                <div class="heading3">Is VC Funding Drying Up?</div>
                <div class="para3 mb-5">
                  Private funding by VC firms is down 50% YOY. We take a look at
                  what that means.
                </div>
              </v-col>
            </v-col>
          </v-col>
        </v-col>
        <v-col class="d-flex flex-wrap pa-0 mt-12">
          <v-col cols="12" sm="6" md="4" class="d-flex pa-0 my-5 my-md-0">
            <v-col cols="3" class="pa-0 left3"> </v-col>
            <v-col cols="9" class="ml-2 py-0 d-flex flex-column">
              <div class="num1 py-0 pos">01</div>
              <div class="heading4 pos1">Reviving Retro PCs</div>
              <div class="para4 pr-0 pr-md-7">
                What happens when old PCs are given modern upgrades?
              </div>
            </v-col>
          </v-col>
          <v-col cols="12" sm="6" md="4" class="d-flex pa-0 my-5 my-md-0">
            <v-col cols="3" class="pa-0 left4"> </v-col>
            <v-col cols="9" class="ml-2 py-0 d-flex flex-column">
              <div class="num1 py-0 pos">02</div>
              <div class="heading4 pos1">Top 10 Laptops of 2022</div>
              <div class="para4 pr-0 pr-md-7">
                Our best picks for various needs and budgets.
              </div>
            </v-col>
          </v-col>
          <v-col cols="12" sm="6" md="4" class="d-flex pa-0 my-5 my-md-0">
            <v-col cols="3" class="pa-0 left5"> </v-col>
            <v-col cols="9" class="ml-2 py-0 d-flex flex-column">
              <div class="num1 py-0 pos">03</div>
              <div class="heading4 pos1">The Growth of Gaming</div>
              <div class="para4 pr-0 pr-md-7">
                How the pandemic has sparked fresh opportunities.
              </div>
            </v-col>
          </v-col>
        </v-col>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { ref } from "vue";

const dialog = ref(false);

const links = [
  { text: "Home" },
  { text: "New" },
  { text: "Popular" },
  { text: "Trending" },
  { text: "Categories" },
];

const openDialog = () => {
  dialog.value = true;
};

const closeDialog = () => {
  dialog.value = false;
};
</script>


<style scoped>
@font-face {
  font-family: f1;
  src: url(/src/assets/Inter-Bold.ttf);
}
@font-face {
  font-family: f2;
  src: url(/src/assets/Inter-ExtraBold.ttf);
}
@font-face {
  font-family: f3;
  src: url(/src/assets/Inter-Regular.ttf);
}
.logo img {
  width: 89%;
}
.link {
  color: hsl(248, 3%, 45%);
  cursor: pointer;
  font-size: 14px;
}
.link:hover {
  color: hsl(2, 62%, 75%);
}
.img1 {
  width: 100%;
}
.heading {
  color: hsl(240, 100%, 5%);
  font-family: f2;
  font-size: 48px;
  line-height: 51px;
  letter-spacing: 0.7px;
}
.para {
  color: hsl(270, 2%, 47%);
  font-size: 14px;
  font-weight: 500;
  line-height: 25px;
  letter-spacing: 0.3px;
}
.read-more {
  background-color: hsl(4, 86%, 64%);
  color: hsl(240, 100%, 5%);
  font-family: f1;
  font-size: 12px;
  letter-spacing: 3px;
}
.read-more:hover {
  background-color: hsl(240, 100%, 5%);
  color: hsl(249, 24%, 94%);
}
.right-body {
  background-color: hsl(240, 100%, 5%);
}
.new {
  font-family: f1;
  color: hsl(35, 75%, 62%);
  font-size: 40px;
}
.heading1,
.heading2,
.heading3 {
  color: white;
  font-family: f1;
  font-size: 18px;
}
.heading1:hover,
.heading2:hover,
.heading3:hover {
  color: hsl(38, 76%, 69%);
}
.para1,
.para2,
.para3 {
  color: hsl(240, 30%, 76%);
  font-family: f3;
  font-size: 12px;
  letter-spacing: 0.1px;
  margin-top: 5px;
  line-height: 22px;
}
.line {
  height: 1.5px;
  background-color: hsl(240, 17%, 29%);
  width: 100%; /* Adjust width as needed */
}
.num1 {
  color: hsl(5, 84%, 63%);
  font-family: f1;
  font-size: 28px;
}
.left3 {
  width: 100%; /* Adjust width as needed */
  background-image: url("/src/assets/image-retro-pcs.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
.left4 {
  width: 100%; /* Adjust width as needed */
  background-image: url("/src/assets/image-top-laptops.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
.left5 {
  width: 100%; /* Adjust width as needed */
  background-image: url("/src/assets/image-gaming-growth.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.heading4,
.heading5,
.heading6 {
  color: hsl(240, 100%, 5%);
  font-family: f2;
  font-size: 16px;
  cursor: pointer;
}
.heading4:hover,
.heading5:hover,
.heading6:hover {
  color: hsl(5, 84%, 63%);
}
.para4 {
  color: hsl(249, 3%, 56%);
  font-size: 14px;
}
.pos {
  position: relative;
  top: -10px;
}
.pos1 {
  position: relative;
  top: -5px;
}
.menu-icon {
  width: 40px;
  height: 40px;
  cursor: pointer;
}
.dialog-content {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  position: relative;
  padding: 20px;
  background-color: white;
}
.burger-list {
  color: black;
  background-color: #fff;
}
.burger-list a {
  text-decoration: none;
  color: hsl(248, 16%, 10%);
}
.burger-list a:hover {
  color: hsl(2, 62%, 75%);
}
.close-icon {
  position: absolute;
  top: 30px;
  right: 30px;
  width: 30px;
  height: 30px;
  cursor: pointer;
}
.blogs {
  cursor: pointer;
}
/* Dialog Animation */
.dialog-right-transition-enter-active,
.dialog-right-transition-leave-active {
  transition: transform 0.3s ease-in-out;
}

.dialog-right-transition-enter {
  transform: translateX(100%);
}
.dialog-right-transition-leave-to {
  transform: translateX(100%);
}
.custom-dialog {
  width: 70vw;
  left: 100px;
}
@media (min-width: 430px) and (max-width: 619.5px) {
  .custom-dialog {
    width: 70vw;
    left: 155px;
  }
}
@media (min-width: 619.5px) and (max-width: 735.5px) {
  .custom-dialog {
    width: 70vw;
    left: 190px;
  }
}
@media (min-width: 735.5px) and (max-width: 959.5px) {
  .custom-dialog {
    width: 70vw;
    left: 300px;
  }
  .close-icon {
    position: absolute;
    top: 30px;
    right: 100px;
    width: 30px;
    height: 30px;
    cursor: pointer;
  }
}
</style>