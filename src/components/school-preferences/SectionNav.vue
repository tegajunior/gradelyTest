<template>
  <div class="d-flex justify-space-between root">
    <div class="navItem"><span>My School</span></div>
    <div class="navItem"><span>Subjects</span></div>
    <div class="navItem currentNavItem"><span>Users</span></div>
    <div class="navItem"><span>Account</span></div>
  </div>
</template>

<script>
export default {
  name: "SectionNav"
}
</script>

<style scoped>
  .root {
    padding: 21px;
    width: 300px;
  }
  .root span {
    color: #959595;
    font-style: normal;
    font-size: 14px;
  }

  .navItem:hover, .currentNavItem {
    cursor: pointer;
    border-bottom: 3px solid #FAA017;
    font-weight: 500;
  }
</style>