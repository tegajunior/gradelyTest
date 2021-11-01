<template>
  <div class="root d-flex align-center">
    <div
      class="initials"
      :class="
        user.id === 1
          ? 'id-1'
          : user.id === 2
          ? 'id-2'
          : user.id === 3
          ? 'id-3'
          : user.id === 4
          ? 'id-4'
          : user.id === 5
          ? 'id-5'
          : ''
      "
    >
      <span>{{ user.initials }}</span>
    </div>
    <div class="userBio ml-3">
      <h5 class="userName">{{ user.fullname }}</h5>
      <span class="userEmail">{{ user.email }}</span>
    </div>

    <div class="userRole">
      <span>{{ user.role }}</span>
    </div>

    <div class="userStatus">
      <h5
        :class="user.status === 'active' ? 'activeUser' : 'inactiveUser'"
        class="useStatusDefault"
      >
        {{ user.status }}
      </h5>
    </div>

    <div class="moreIcon"><span>&mldr;</span></div>
  </div>
</template>

<script>
export default {
  name: "UserInfo",
  props: ["user"],
  data() {
    return {};
  },
};
</script>

<style scoped>
.root {
  width: 710px;
  height: 68px;
  background: #ffffff;
  box-shadow: 0px 1px 4px rgba(0, 0, 0, 0.15);
  border-radius: 3px;
  padding: 10px 15px;
}
.root .initials {
  width: 48px;
  height: 48px;
  border-radius: 5px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.initials {
  color: rgba(245, 245, 245, 1);
  font-weight: 700;
}
.id-1 {
  background: #f6515b;
}
.id-2 {
  background: #004680;
}
.id-3 {
  background: #DBF5F8;
  color: #000000;
}
.id-4 {
  background: #000000
}
.id-5 {
  background: #AC2858;
}

.userBio {
  width: 200px;
}
.userName {
  color: #353535;
  font-size: 16px;
  line-height: 22px;
}
.userEmail {
  color: #757575;
  font-size: 13px;
}
.userRole {
  width: 370px;
  padding-left: 100px;
}
.userRole span {
  color: #555555;
  font-size: 14px;
  line-height: 19px;
}
.userStatus {
  width: 100px;
  padding-left: 20px;
}
.useStatusDefault {
  font-size: 12px;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  font-weight: normal;
  line-height: 12px;
  color: #959595;
}
.userStatus .activeUser {
  color: #00e29f;
  font-weight: bold;
}
.moreIcon {
  width: 32px;
  height: 32px;
  background: #f5f5f5;
  border-radius: 4px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.moreIcon span {
  font-size: 20px;
}
@media (max-width: 800px) {
  .root {
    max-width: 100%;
    justify-content: space-between;
  }
  .userBio {
    display: none;
  }
  .userRole {
    width: 100px;
    padding-left: 10px
  }
}
</style>
