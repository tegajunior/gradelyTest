<template>
  <div class="leftSections">
    <span class="my-account-section-header">MY ACCOUNT</span>
    <div class="d-flex flex-column justify-space-between leftSideNav">
      <div class="list-group-item d-flex align-center">
        <v-btn icon class="leftSideNavBtn">
          <v-icon>mdi-home-outline</v-icon>
        </v-btn>
        <span class="ml-1">Home</span>
      </div>
      <div class="list-group-item d-flex align-center">
        <v-btn icon class="leftSideNavBtn">
          <v-icon>mdi-account-circle-outline</v-icon>
        </v-btn>
        <span class="ml-1">Personal Information</span>
      </div>
      <div class="list-group-item d-flex align-center currentItem">
        <v-btn icon class="leftSideNavBtn">
          <v-icon style="color: red">mdi-tune-vertical</v-icon>
        </v-btn>
        <span class="ml-1">School Preferences</span>
      </div>
      <div class="list-group-item d-flex align-center">
        <v-btn icon class="leftSideNavBtn">
          <v-icon>mdi-cog-outline</v-icon>
        </v-btn>
        <span class="ml-1">Settings</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LeftSectionNav",
};
</script>

<style scoped>
.leftSections {
  margin-top: 50px;
}
.my-account-section-header {
  font-size: 14px;
  font-weight: 400;
}
.leftSideNav {
  padding-left: 20px;
  height: 250px;
  width: 300px;
  margin-top: 20px;
}
.list-group-item {
  padding: 5px;
}
.list-group-item:hover {
  font-weight: bold;
  background-color: white;
  border-radius: 30px;
  cursor: pointer;
}
i.v-icon.v-icon {
  color: #959595 !important;
}
.list-group-item:hover i.v-icon.v-icon {
  color: #11bdcf !important;
}
.ml-1 {
  font-size: 14px;
  color: #757575;
}
.currentItem {
  font-weight: bold;
  background-color: white;
  border-radius: 30px;
}
.currentItem i.v-icon.v-icon {
  color: #11bdcf !important;
}
@media (max-width: 800px) {
  .my-account-section-header, .ml-1 {
    font-size: 10px
  }
  .leftSideNav {
    width: 200px;
    margin-left: 0;
  }
}
</style>
