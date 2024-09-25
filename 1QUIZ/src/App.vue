<template>
  <div id="app">
    <AppHeader />

    <main class="main-content">
      <div class="input-container">
        <input v-model="newItem.title" placeholder="Title" class="input-field" />
        <input v-model="newItem.description" placeholder="Description" class="input-field" />
        <button @click="addItem" class="add-button">Add Item</button>
      </div>

      <div v-if="items.length === 0" class="no-items">No items available.</div>

      <div v-show="items.length > 0" class="item-list">
        <ItemDisplay
            v-for="(item, index) in items"
            :key="index"
            :item="item"
        />
      </div>

      <div class="counter">
        <p>Count: {{ count }}</p>
        <button @click="increment" class="counter-button">Increment</button>
        <button @click="decrement" class="counter-button">Decrement</button>
      </div>
    </main>

    <AppFooter />
  </div>
</template>

<script>
import ItemDisplay from './components/ItemDisplay.vue';
import { useCounter } from './composables/useCounter';
import { ref } from "vue";
import AppHeader from "@/components/AppHeader.vue";
import AppFooter from "@/components/AppFooter.vue";

export default {
  name: 'App',
  components: {
    AppHeader,
    AppFooter,
    ItemDisplay
  },
  setup() {
    const { count, increment, decrement } = useCounter();
    const items = ref([]);
    const newItem = ref({ title: '', description: '' });

    const addItem = () => {
      if (newItem.value.title && newItem.value.description) {
        items.value.push({ ...newItem.value });
        newItem.value.title = '';
        newItem.value.description = '';
      }
    };

    return { items, newItem, addItem, count, increment, decrement };
  }
}
</script>

<style>
html, body {
  height: 100%;
  margin: 0;
}

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh; /* Full viewport height */
}

.main-content {
  flex: 1; /* This allows the main content to grow and push the footer down */
  max-width: 800px;
  margin: 20px auto;
  padding: 20px;
  background: white;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.input-container {
  display: flex;
  margin-bottom: 20px;
}

.input-field {
  padding: 10px;
  margin-right: 10px;
  border: 1px solid #ddd;
  border-radius: 4px;
  flex: 1;
}

.add-button {
  padding: 10px 15px;

  background-color: #C71585;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.add-button:hover {
  background-color: #f0a500;
}

.no-items {
  margin: 20px 0;
  font-weight: bold;
  color: #999;
}

.item-list {
  margin-bottom: 20px;
}

.counter {
  display: flex;
  align-items: center;
  margin-top: 20px;
}

.counter p {
  margin-right: 10px;
}

.counter-button {
  padding: 10px 15px;
  background-color: #C71585;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  margin-left: 5px;
}

.counter-button:hover {
  background-color: #f0a500;
}
</style>
