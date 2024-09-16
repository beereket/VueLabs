<template>
  <header class="header">
    <div class="logo">
      <img src="../assets/jojo.webp" alt="Logo" class="logo-image">
      <h1 class="title">MiniBlog</h1>
    </div>

    <nav class="nav">
      <ul class="nav-list">
        <li class="nav-item"><a href="#bereket" class="nav-link">Home</a></li>
        <li class="nav-item"><a href="#bereket" class="nav-link">About</a></li>
        <li class="nav-item"><a href="#bereket" class="nav-link">Posts</a></li>
        <li class="nav-item"><a href="#bereket" class="nav-link">Contact</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: `Header`
}

</script>

<style scoped>
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

.nav {
  display: flex;
}

.nav-list {
  display: flex;
  list-style: none;
}

.nav-item {
  margin-left: 1.5rem;
}

.nav-link {
  color: #C71585;
  text-decoration: none;
  font-size: 1.1rem;
  transition: color 0.3s;
}

.nav-link:hover {
  color: #f0a500;
}
</style>
