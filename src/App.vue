<template>
    <div class="container">
        <nav class="navbar justify-content-between mt-3">
            <router-link class="nav-item" :to="{ name: 'home'}">home</router-link>
            <router-link class="nav-item" :to="{ name: 'projects'}">projects</router-link>
            <a href="https://www.github.com/provmawn" target="_blank">github</a>
        </nav>
        <router-view/>
    </div>
</template>

<style>
* {
    background-color: #000000;
    font-family: 'Courier New', Courier, monospace;
    color:#e2e2e2;
    font-size:20px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #a40000;
}

nav a:hover {
  color: #ff0000;
}
</style>
