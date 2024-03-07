<template>
  <div class="home">
    <h1>Bienvenue dans notre boutique de vélos</h1>
    <p>Découvrez notre sélection de vélos à vendre :</p>
    <div class="bike-list">
      <div v-for="bike in bikes" :key="bike.id" class="bike">
        <img :src="bike.image" :alt="bike.name" class="bike-image">
        <h2>{{ bike.name }}</h2>
        <p>{{ bike.description }}</p>
        <p>Prix: {{ bike.price }} €</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      bikes: [
        {
          id: 1,
          name: 'Vélo de ville',
          description: 'Vélo élégant et confortable pour vos déplacements en ville.',
          price: 300,
          image: '/assets/velo-ville.jpg'
        },
        {
          id: 2,
          name: 'VTT',
          description: 'Vélo tout terrain robuste pour vos aventures en pleine nature.',
          price: 500,
          image: '/assets/vtt.jpg'
        },
        {
          id: 3,
          name: 'Vélo de course',
          description: 'Vélo léger et rapide pour les passionnés de cyclisme sur route.',
          price: 800,
          image: '/assets/velo-course.jpg'
        }
      ]
    };
  }
}
</script>

<style scoped>
.home {
  text-align: center;
  padding: 20px;
}

.bike-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}

.bike {
  width: 300px;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 10px;
}

.bike-image {
  width: 100%;
  border-radius: 10px;
}
</style>
