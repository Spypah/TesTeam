<template>
    <div class="detalle-producto">
      <div class="imagen">
        <img :src="card.imageSrc" :alt="'Imagen de la carta' + card.id">
      </div>
      <div class="detalles">
        <h2>{{ card.nombre }}</h2>
        <p>Descripción: {{ card.descripcion }}</p>
        <p>Valor: ${{ card.valor }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'DetalleProducto',
    props: {
      card: Object // Recibe la información de la carta como prop
    }
  }
  </script>
  
  <style scoped>
  .detalle-producto {
    display: flex;
    align-items: center;
  }
  
  .imagen {
    flex: 1;
    text-align: center;
  }
  
  .imagen img {
    max-width: 100%;
    max-height: 400px; /* Ajusta la altura máxima según tus necesidades */
  }
  
  .detalles {
    flex: 1;
    padding: 20px;
  }
  
  h2 {
    font-size: 24px;
    margin-bottom: 10px;
  }
  
  p {
    font-size: 16px;
    margin-bottom: 5px;
  }
  </style>
  