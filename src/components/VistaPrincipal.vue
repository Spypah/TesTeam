<template>
  <div>
    <router-link
      v-for="card in cards"
      :key="card.id"
      :to="'/detalle-producto/' + card.id"
    >
      <div class="card">
        <img :src="card.imageSrc" :alt="'Imagen de la carta ${card.id}'">
        <button @click="handleButtonClick(card)">{{ card.buttonText }}</button>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CardComponent',
  data() {
    return {
      cards: [
        {
          id: 1,
          imageSrc: 'https://upload.wikimedia.org/wikipedia/commons/b/b8/Chinese_vase.jpg',
          buttonText: 'Pujar producto'
        },
        {
          id: 2,
          imageSrc: 'https://upload.wikimedia.org/wikipedia/commons/b/b8/Chinese_vase.jpg',
          buttonText: 'Pujar producto'
        },
      ]
    };
  },
  methods: {
    handleButtonClick() {
      alert('Pujaste en ${card.id}');
    }
  }
}
</script>

<style scoped>
.card {
  width: 300px;
  border: 1px solid #ccc;
  padding: 50px;
  text-align: center;
  margin: 10px;
}

img {
  max-width: 100%;
}

button {
  background-color: #007bff;
  color: #fff;
  padding: 10px 20px;
  border: none;
  cursor: pointer;
  margin-top: 10px;
}

button:hover {
  background-color: #0056b3;
}
</style>
