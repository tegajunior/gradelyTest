<template>
  <div class="root">
    <div class="d-flex justify-space-between align-center sectionWithCircle">
      <div class="leftSection">
        <h5 class="leftSectionHeader">ADMIN USERS</h5>
      </div>
      <div class="rightSection circle">+</div>
    </div>
    <p class="leftSectionText">
      Add more school adminstrators, manage their roles and activities
    </p>
  </div>
</template>

<script>
export default {
  name: "AdminUsers",
};
</script>

<style scoped>
.root {
  margin-top: 26px;
}
.sectionWithCircle {
  margin-bottom: 15px;
}
.leftSectionHeader {
  font-size: 16px;
  font-weight: 700;
  color: #555555;
}
.circle {
  width: 20px;
  height: 20px;
  line-height: 20px;
  border-radius: 50%;
  font-size: 10px;
  color: #353535;
  text-align: center;
  background: #faa017;
}
.leftSectionText {
  color: #555555;
  font-size: 14px;
}
</style>
