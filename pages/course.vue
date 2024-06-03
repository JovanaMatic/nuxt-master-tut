<template>
  <div class="main">
    <div class="heading">
      <h1>Course: <strong>Mastering Nuxt</strong></h1>
    </div>
    <div class="col">
      <div class="aside">
        <h3>Chapters</h3>
      </div>
      <div class="content">
        <NuxtPage />
      </div>
    </div>
  </div>
</template>

<script setup>

</script>

<style scoped>

.main {
  display: flex;
  height: 100vh;
  flex-direction: column;
}

.col {
  display: flex;
  height: 100%;
}

.aside {
  width: 20%;
  background-color: #f8f7f7;
  padding: 20px;
  margin: 20px;
  border-radius: 5px;
  box-shadow: 0 2px 4px 0 rgb(90 90 90 / 40%)
}

.content {
  width: 80%;
  background-color: #f8f7f7;
  padding: 20px;
  margin: 20px;
  border-radius: 5px;
  box-shadow: 0 2px 4px 0 rgb(90 90 90 / 40%)
}

.heading {
  text-align: center;
}

.heading h1 {
  font-weight: 400;
}

</style>