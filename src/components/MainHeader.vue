<template>
  <div class="container">
    <div class="app-bar d-flex align-center justify-space-between">
      <div class="d-flex align-center">
        <v-img
          alt="Gradely logo"
          class="shrink ml-6"
          contain
          :src="logo"
          transition="scale-transition"
          width="80"
        />
      </div>

      <div class="d-lg-flex justify-space-around hidden-sm-and-down">
        <div class="mr-4 d-flex align-center currentMainNav">
          <img :src="home" alt="">
          <span class="mainHeaderLink ml-3">Home</span>
        </div>
        <div class="mr-4 d-flex align-center mainNav">
          <v-btn icon>
            <v-icon>mdi-flask-round-bottom</v-icon>
          </v-btn>
          <span class="mainHeaderLink">Teachers</span>
        </div>
        <div class="mr-4 d-flex align-center mainNav">
          <img :src="students" alt="">
          <span class="mainHeaderLink ml-3">Students</span>
        </div>
        <div class="mr-4 d-flex align-center mainNav">
          <v-btn icon>
            <v-icon>mdi-apps</v-icon>
          </v-btn>
          <span class="mainHeaderLink">Apps</span>
        </div>
      </div>

      
      <div class="d-lg-flex align-center hidden-sm-and-down">
        <div class="mr-5">
          <img :src="actBtn" alt="Activities button" class="far-left" />
        </div>
        <div>
          <img :src="notBtn" alt="Notification button" class="far-left" />
        </div>
      </div>

      <v-app-bar-nav-icon
        @click="drawer = true"
        class="hidden-md-and-up"
      ></v-app-bar-nav-icon>

    </div>
    <hr>
  </div>
</template>

<script>
import logo from "../assets/gradleylogo.png";
import home from "../assets/home.png";
import students from "../assets/students1.png";


import actBtn from "../assets/activitiesBtn.png";
import notBtn from "../assets/notificationButton.png";
export default {
  name: "MainHeader",
  data() {
    return {
      logo,
      actBtn,
      notBtn,
      home,
      students
    }
  },
};
//
</script>

<style scoped>
hr {
  background-color: #d5d5d5;
  height: 1px;
  opacity: 0.5;
  margin-top: -6px
}
.app-bar {
  padding-left: 3.8%;
  padding-right: 3.8%;
  padding-top: 16.5px;
  padding-bottom: 4.5px;
  width: 100%;
  max-width: 100%;
  background: #fff;
}
.currentMainNav,
.mainNav:hover {
  border-bottom: 3px solid #11bdcf;
}
.mainHeaderLink {
  font-size: 14px;
  color: #353535;
}
.currentMainNav:hover,
.mainNav {
  cursor: pointer;
}
.currentMainNav i.v-icon.v-icon,
.mainNav:hover i.v-icon.v-icon {
  color: #11bdcf !important;
}
.far-left {
  cursor: pointer;
}
</style>
