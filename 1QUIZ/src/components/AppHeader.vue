<template>
  <header class="header">

    <div class="logo">
      <img src="../assets/jojo.webp" alt="Logo" class="logo-image">
      <h1 class="title">QuizAnswer</h1>
    </div>

  </header>
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>

<style>

* {
  margin: 0;
  padding: 0;
}
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 5%;
  background-color: white;
  color: #C71585;
}

.logo {
  display: flex;
  align-items: center;
}

.logo-image {
  width: 50px;
  margin-right: 0.5rem;
}

.title {
  font-size: 1.3rem;
}

</style>