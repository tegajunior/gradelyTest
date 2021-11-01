<template>
  <v-app class="app">
      <MainHeader />
    <div class="appContainer">
      <v-main>
        <div class="d-flex justify-space-between flex-column flex-md-row">
          <LeftSectionNav />
          <SchoolPreferences />
        </div>
      </v-main>
    </div>
  </v-app>
</template>

<script>
import MainHeader from "./components/MainHeader";
import LeftSectionNav from "./components/LeftSectionNav";
import SchoolPreferences from "./components/school-preferences/SchoolPreferences";
export default {
  name: "App",

  components: {
    MainHeader,
    LeftSectionNav,
    SchoolPreferences,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
* {
  box-sizing: border-box;
}
.appContainer {
  background-color: #f5f5f5;
  padding-left: 5.5%;
  padding-right: 4%;
  padding-bottom: 60px;
}
</style>
