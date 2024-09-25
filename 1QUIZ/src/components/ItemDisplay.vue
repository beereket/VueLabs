<template>
  <div class="item">
    <h2 class="item-title">{{ item.title }}</h2>
    <p class="item-description">{{ item.description }}</p>
  </div>
</template>

<script>
export default {
  name: 'ItemDisplay',
  props: {
    item: Object
  }
}
</script>

<style scoped>
.item {
  padding: 15px;
  margin: 10px 0;
  background: #e9e9e9;
  border-left: 5px solid #C71585;
  border-radius: 4px;
  transition: background 0.3s;
}

.item:hover {
  background: #f1f1f1;
}

.item-title {
  font-size: 1.5em;
  margin: 0;
  color: #333;
}

.item-description {
  margin: 5px 0 0 0;
  color: #666;
}
</style>
