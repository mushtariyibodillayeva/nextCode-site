<script setup></script>

<template>
  <header>
    <div class="wrapper">
      <HelloWorld msg="You did it!" />
      <nav class="links">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/login">Login</RouterLink>
      </nav>
      <h1>Onlayn IT kursidan ro'yhatdan o'ting!</h1>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
.wrapper h1 {
  color: crimson;
  margin-top: 50px;
  text-align: center;
}
.links {
  font-size: 20px;
  display: flex;
  justify-content: space-around;
  color: blue;
  background-color: bisque;
  padding: 13px;
}
</style>
