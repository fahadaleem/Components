<template>
  <div class="side-drawer">
    <div id="mySidenav" :class="{ sidenav: true, active: isOpen }">
      <div
        class="round-btn close-btn m section-gap-bottom"
        @click="$emit('handleCloseDrawer')"
      >
        close
      </div>

      <div class="menu-links text-align-center">
        <router-link to="/" class="m round-btn link-btn"> Home </router-link>
        <router-link to="/" class="m round-btn link-btn"> Blog </router-link>
        <router-link to="/" class="m round-btn link-btn"> About </router-link>
        <router-link to="/" class="m round-btn link-btn"> Request </router-link>
      </div>
    </div>

    <!-- Use any element to open the sidenav -->
  </div>
</template>
<script>
export default {
  name: "MenuDrawer",
  props: {
    isOpen: {
      type: Boolean,
      default: true,
    },
  },
};
</script>
<style scoped>
/* The side navigation menu */
.sidenav {
  height: 100%; /* 100% Full-height */
  width: 0; /* 0 width - change this with JavaScript */
  position: fixed; /* Stay in place */
  z-index: 1; /* Stay on top */
  top: 0; /* Stay at the top */
  left: 0;
  background-color: #ededed; /* Black*/
  overflow-x: hidden; /* Disable horizontal scroll */
  transition: 0.5s; /* 0.5 second transition effect to slide in the sidenav */
}

/* The navigation menu links */
.sidenav a {
  text-decoration: none;
  font-size: 25px;
  color: #818181;
  display: block;
  transition: 0.3s;
}

/* When you mouse over the navigation links, change their color */
.sidenav a:hover {
  color: #f1f1f1;
}

/* Position and style the close button (top right corner) */
.sidenav .closebtn {
  position: absolute;
  top: 0;
  right: 25px;
  font-size: 36px;
  margin-left: 50px;
}

.active {
  width: 100%;
}

/* Style page content - use this if you want to push the page content to the right when you open the side navigation */
#main {
  transition: margin-left 0.5s;
  padding: 20px;
}

.close-btn {
  background-color: #191a19;
  color: #ededed;
}

.link-btn {
  border: 1px solid;
}
/* On smaller screens, where height is less than 450px, change the style of the sidenav (less padding and a smaller font size) */
@media screen and (max-height: 450px) {
  .sidenav {
    padding-top: 15px;
  }
  .sidenav a {
    font-size: 18px;
  }
}
</style>
