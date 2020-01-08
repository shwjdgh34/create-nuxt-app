<template>
  <header>
    <ul class="nav-items">
      <li>
        <nuxt-link to="/users">Users</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/">Home</nuxt-link>
      </li>
    </ul>
  </header>
</template>

<style>
.header {
  width: 100%;
  height: 60px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.nav-items {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.nav-items a {
  text-decoration: none;
  color: black;
}
.nav-items a:hover,
.nav-items a:active {
  color: blue;
}
</style>