<template>
  <div id="app">
    <div id="sidebar">
      <div class="logo">
        <router-link to="/">Vue Manager</router-link>
      </div>
      <div>
        <b-link><router-link to="/">Home</router-link></b-link>
      </div>
      <div>
        <b-link><router-link to="/about">About</router-link></b-link>
      </div>
    </div>
    <div id="main-panel">
      <b-navbar toggleable="lg" type="dark" variant="dark">
        <b-navbar-brand href="#">DASHBOARD</b-navbar-brand>
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav class="ml-auto">
            <b-nav-item-dropdown text="Lang" right>
              <b-dropdown-item href="#">EN</b-dropdown-item>
              <b-dropdown-item href="#">VI</b-dropdown-item>
            </b-nav-item-dropdown>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
      <div class="content">
        <router-view/>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
#app {
  position: relative;
  height: 100vh;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#sidebar {
  position: absolute;
  height: 100%;
  width: 280px;
  background-color: #2c3e50;
}
#main-panel {
  position: relative;
  float: right;
  width: calc(100% - 280px);
  min-height: 100%;
}
.content {
  margin: 30px;
}
.navbar {
  padding: 8px 30px !important;
}
</style>
