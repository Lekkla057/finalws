<template>
  <div id="app">
    <nav class="navbar navbar-expand navbar-dark bg-dark">
    <div id="nav navbar-nav">
      <router-link  to="/" class="navbar-item navbar-link active">Home</router-link> |
      <router-link  to="/about" class="navbar-item navbar-link ">About</router-link> | 
      <router-link to="/product"  class="navbar-item navbar-link ">Category</router-link> |
      <router-link  to="/user" class="navbar-item navbar-link ">User</router-link>|
      <router-link  to="/grap" class="navbar-item navbar-link ">Graph</router-link>
    </div>
    </nav>
    <router-view/>
  </div>
  
</template>
<!-- router-link จะมาคู่กับ router-view เสมอ คือการเอาข้อมูลไปแทนใน router-view -->
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>