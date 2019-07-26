<template>
  <div id="app">
    <div id="sidebar">
      <div class="logo">
        <img alt="Vue logo" src="./assets/logo.png" width="40" height="40">
        <router-link to="/">ue Manager</router-link>
      </div>
      <ul class="sidebar-nav">
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/about">About</router-link></li>
      </ul>
    </div>
    <div id="main-panel">
      <b-navbar toggleable="lg" variant="faded" type="light">
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
        <router-view />
      </div>
      <footer class="footer">
        <div class="copyright text-center">Designed by <a href="https://github.com/bqthong">Thong</a>.</div>
      </footer>
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
  height: 100%;
}
footer {
  background: #f5f5f5;
  padding: 10px;
}
.content {
  margin: 30px;
  min-height: calc(100% - 161px);
}
.navbar {
  border-bottom: 1px solid rgba(0,0,0,.1);
  padding: 8px 30px !important;
}
.logo {
  padding: 8px 5px;
  margin: 0 20px;
  border-bottom: 1px solid #ffffff33;
  position: relative;
  text-transform: uppercase;
  font-size: 18px;
  a{
    color: #ffffffff;
  }
}
.sidebar-nav {
  padding: 10px;
  text-align: left;
  a{
    color: #fff;
    margin: 5px 15px;
    border-radius: 4px;
    display: block;
    padding: 10px 15px;
  }
  a:hover{
    text-decoration: none;
    color: #333;
    background: #fff;
    margin: 5px 15px;
    padding: 10px 15px;
  }
}
</style>
