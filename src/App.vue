<script>
export default {
  data() {
    return {
      activeMenu: "home",
    };
  },
  methods: {
    setActiveMenu(menu) {
      this.activeMenu = menu;
    },
  },
}
</script>

<template>
  <div class="header">
    <div class="logo">
      <i class="bx bx-menu menu-icon"></i>
      <span class="logo-name">Dashboard</span>
    </div>
    <div class="header-right">
      <div class="bx bx-search"></div>
      <div class="bx bx-bell"></div>
    </div>
  </div>

  <div class="sidebar" id="sidebar">
    <h1 class="logo">Dashboard</h1>
    <ul>
      <li
        :class="{ active: activeMenu === 'home' }"
        @click="setActiveMenu('home')"
      >
        <a href="#"><i class="bx bxs-dashboard"></i>Home</a>
      </li>
      <li
        :class="{ active: activeMenu === 'profile' }"
        @click="setActiveMenu('profile')"
      >
        <a href="#"><i class="bx bxs-user"></i>User Profile</a>
      </li>
      <li
        :class="{ active: activeMenu === 'tickets' }"
        @click="setActiveMenu('tickets')"
      >
        <a href="#"><i class="bx bxs-comment-dots"></i>Tickets</a>
      </li>
      <li
        :class="{ active: activeMenu === 'settings' }"
        @click="setActiveMenu('settings')"
      >
        <a href="#"><i class="bx bxs-cog"></i>Settings</a>
      </li>
      <li
        :class="{ active: activeMenu === 'statistics' }"
        @click="setActiveMenu('statistics')"
      >
        <a href="#"><i class="bx bx-stats"></i>Statistics</a>
      </li>
      <li
        :class="{ active: activeMenu === 'products' }"
        @click="setActiveMenu('products')"
      >
        <a href="#"><i class="bx bxs-shopping-bag"></i>Products</a>
      </li>
    </ul>
  </div>

</template>

<style scoped>
.sidebar {
  position: fixed;
  top: 0;
  left: 0;
  width: 225px;
  height: 100vh;
  background-color: #f0f0f0;
  padding: 20px;
}

.sidebar .logo {
  font-size: 24px;
  font-weight: 700;
  margin-bottom: 20px;
  color: #333;
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 2px;
  border-bottom: 1px solid #bdbdbd;
  padding-bottom: 10px;
  margin-bottom: 20px;
  text-decoration: none;
}

.sidebar ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

.sidebar li {
  margin-bottom: 10px;
}

.sidebar li a {
  display: block;
  padding: 10px;
  border-radius: 10px;
  color: #333;
  text-decoration: none;
}

.sidebar li.active {
  background-color: #d1d1d1;
  border-radius: 10px;
}

.sidebar li a i {
  margin-right: 10px;
  color: #333;
  text-decoration: none;
  font-size: 20px;
  vertical-align: middle;
  text-align: center;
  line-height: 20px;
  width: 20px;
  height: 20px;
  border-radius: 50%;
  display: inline-block;
  margin-right: 10px;
  text-decoration: none;
}

.sidebar li a:hover {
  background-color: #e0e0e0;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: #f0f0f0;
  height: 50px;
}

.header-right {
  display: flex;
  align-items: center;
}
</style>
