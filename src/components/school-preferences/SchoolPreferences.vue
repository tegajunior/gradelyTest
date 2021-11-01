<template>
  <div class="sectionContainer">
    <div class="sectionHeadingWrapper">
      <span class="sectionHeading">School Preferences</span>
      <SectionNav />
      <hr />
    </div>
    <AdminUsers />
    <div class="userInfoSection">
      <UserInfo :user="user1" />
      <UserInfo :user="user2" />
      <UserInfo :user="user3" />
    </div>
    <div class="pendingUsersSection">
      <h5 class="pendingUsersHeader">PENDING USERS</h5>
      <UserInfo :user="user4" />
      <UserInfo :user="user5" />
    </div>
  </div>
</template>

<script>
import SectionNav from "./SectionNav";
import AdminUsers from "./AdminUser";
import UserInfo from "./UserInfo";
export default {
  name: "School Preferences",
  components: {
    SectionNav,
    AdminUsers,
    UserInfo,
  },
  data() {
    return {
      user1: {
        id: 1,
        initials: "BO",
        fullname: "Boye Oshinaga",
        email: "boye@gradely.ng",
        role: "Owner",
        status: "active",
      },
      user2: {
        id: 2,
        initials: "BC",
        fullname: "Babatunde Calebs",
        email: "cahylebs@gradely.ng",
        role: "Principal",
        status: "active",
      },
      user3: {
        id: 3,
        initials: "FS",
        fullname: "Francis Sanni",
        email: "francis@gradely.ng",
        role: "School Administrator",
        status: "active",
      },
      user4: {
        id: 4,
        initials: "FI",
        fullname: "Femi Ibiwoye",
        email: "femi@gradely.ng",
        role: "IT Director",
        status: "inactive",
      },
      user5: {
        id: 5,
        initials: "SA",
        fullname: "Seyi Adelaju",
        email: "seyi@gradely.ng",
        role: "School Administrator",
        status: "inactive",
      },
    };
  },
};
</script>
<style scoped>
hr {
  background-color: #d5d5d5;
  height: 1px;
  opacity: 0.5;
  margin-top: -22px;
}
.sectionContainer {
  background: #fff;
  border-radius: 10px;
  /* height: 730px; */
  width: 770px;
  padding: 30px;
  padding-bottom: 40px;
  margin-top: 50px;
}
.sectionHeading {
  font-size: 21px;
  font-weight: 700;
  margin-bottom: 30px;
  color: #113255;
}
.userInfoSection {
  margin-top: 30px;
}
.pendingUsersSection {
  padding-top: 50px;
}
.pendingUsersHeader {
  margin-bottom: 20px;
  text-transform: uppercase;
  color: #555555;
  font-size: 16px;
  font-weight: bold;
}
@media (max-width: 800px) {
  .sectionContainer {
    max-width: 100%;
  }
}
</style>
