<template>
  <div class="container">
    <h1>Learning Components, Props, Emits, dan Slots</h1>

    <MyButton 
      buttonText="Klik Aku!" 
      @customClick="handleClick"
    >
      <template #default>
        <strong> - Slot: Ini isi dari induk - </strong>
      </template>
    </MyButton>

    <p class="message">{{ message }}</p>
  </div>
</template>

<script>
import MyButton from './components/MyButton.vue'

export default {
  components: {
    MyButton
  },
  data() {
    return {
      message: 'Belum diklik'
    }
  },
  methods: {
    handleClick() {
      this.message = 'Tombol diklik! Kamu keren!'
    }
  }
}
</script>

<style scoped>
.container {
  text-align: center;
  padding: 2rem;
  font-family: Arial, sans-serif;
}

.message {
  margin-top: 1rem;
  color: #2c3e50;
  font-weight: bold;
}
</style>