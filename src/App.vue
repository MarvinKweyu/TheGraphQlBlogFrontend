<template>
  <div id="app">
    <header class="d-flex justify-content-center">
      <router-link to="/">
        <h1>Marvin's Blog</h1>
      </router-link>
    </header>
    <router-view />
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

body {
  margin: 0;
  padding: 1.5rem;
}

* + * {
  margin-top: 1.5rem;
}

#app {
  margin: 0;
  padding: 0;
}
</style>
