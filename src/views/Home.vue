<template>
  <div>
    <h1>Home</h1>

    <button @click="increment">
      You clicked me {{ count }} {{ count === 1 ? "time" : "times" }}
    </button>
  </div>
</template>

<style lang="scss">
button {
  background: #41b883;
  color: white;
  border: 0;
  padding: 0.5rem 1rem;
  font-size: 0.9rem;
  font-family: monospace;
  border-radius: 1.5rem;
  transition: 0.25s ease-in-out;
  cursor: pointer;
  outline: none;

  &:hover {
    background: darken(#41b883, 5);
  }
}
</style>

<script>
import { ref } from "vue"

export default {
  setup() {
    const count = ref(0)

    const increment = () => count.value++

    return { count, increment }
  }
}
</script>
