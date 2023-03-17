<!-- <template>
  <div>
    <h1>Login page</h1>
    <button @click="login">Login</button>
  </div>
</template>

<script>
export default {
  methods: {
    login() {
      localStorage.setItem("isLoggedIn", true);
      this.$router.push("/");
    },
  },
};
</script>

<style scoped></style> -->

//example-2

<template>
  <div class="box">
    <h1>Login</h1>
    <form>
      <label> UserName: </label>
      <input type="text" v-model="username" /><br /><br />
      <label>Password:</label>
      <input type="password" v-model="password" />
      <br /><br />
      <button @click.prevent="login">Login</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: "",
      password: "",
    };
  },
  methods: {
    login() {
      if (this.username === "nextCode24" && this.password === "password") {
        localStorage.setItem("isLoggedIn", true);
        this.$router.push("/about");
      } else {
        alert("Sizning username yokiy parolingiz xato!");
      }
      // localStorage.setItem("isLoggedIn", true);
      // this.$router.push("/");
    },
  },
};
</script>

<style scoped>
.box {
  width: 400px;
  margin: 0 auto;
  text-align: center;
}
h1 {
  font-size: 20px;
  color: darkorange;
  margin-bottom: 10px;
}
label {
  font-weight: 1000;
  color: green;
}
button {
  width: 100px;
  height: 30px;
  background-color: darkmagenta;
  color: #fff;
  border: none;
}
</style>
