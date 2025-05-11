<template>
    <button class="fancy-button" @click="handleClick">
      {{ buttonText }}
      <slot />
    </button>
  </template>
  
  <script>
  export default {
    props: {
      buttonText: {
        type: String,
        required: true
      }
    },
    methods: {
      handleClick() {
        this.$emit('customClick')
      }
    }
  }
  </script>
  
  <style scoped>
  .fancy-button {
    background-color: #42b983;
    color: white;
    border: none;
    padding: 1rem 1.5rem;
    margin-top: 1rem;
    border-radius: 10px;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s ease;
  }
  
  .fancy-button:hover {
    background-color: #2c8f6f;
  }
  </style>