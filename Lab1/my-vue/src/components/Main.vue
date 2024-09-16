<template>
  <div class="container">
    <div class="image-container">
      <div class="image-item">
        <img src="../assets/mha.jpg" alt="image" class="image" width="480">
        <p class="text">Midoriya's on a mission to push beyond his limits!</p>
      </div>

      <div class="image-item">
        <img src="../assets/gumble.jpg" alt="image" class="image" width="480">
        <p class="text">Gumball, ready to crush it!</p>
      </div>

      <div class="image-item">
        <img src="../assets/batman.jpg" alt="image" class="image" width="480" height="800">
        <p class="text">Even heroes need strength training</p>
      </div>

      <div class="image-item">
        <img src="../assets/goku.jpg" alt="image" class="image" width="480">
        <p class="text">Goku never skips leg day!</p>
      </div>

      <div class="image-item">
        <img src="../assets/darwin.jpg" alt="image" class="image" width="480">
        <p class="text">Watch out, he's about to go Super Saiyan!</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: `Main`
}
</script>

<style scoped>
.container {
  padding: 2rem 5%;
}

.image-container {
  columns: 15rem 3;
  gap: 1.2rem;
}

.image-item {
  position: relative;
  margin-bottom: 1rem;
}

.image {
  width: 100%;
  border-radius: 0.7rem;
}

.text {
  position: absolute;
  bottom: 10px;
  left: 40%;
  transform: translateX(-50%);
  color: white;
  font-size: 20px;
  font-weight: bold;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
  text-align: center;
}

.image-item:hover {
  transform: scale(1.01);
}


</style>