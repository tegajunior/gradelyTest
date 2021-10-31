<template>
  <v-app class="app">
      <MainHeader />
    <div class="appContainer">
      <v-main>
        <div class="d-flex justify-space-between">
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
.appContainer {
  background-color: #f5f5f5;
  padding-left: 135px;
  padding-right: 139px;
  padding-bottom: 60px;
}
</style>
