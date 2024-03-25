<template>
  <main class="container mx-auto px-4 py-8">
    <!-- Section Films à l'actualité -->
    <section class="mb-8">
      <h2 class="text-2xl font-bold mb-4">Films à l'actualité</h2>
      <!-- Contenu de la section -->
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
        <!-- Exemple de film -->
        <div class="bg-gray-200 p-4 rounded-lg">
          <img src="https://via.placeholder.com/300x400" alt="Image de film" class="mb-2">
          <h3 class="text-xl font-semibold mb-2">Titre du Film</h3>
          <p class="text-gray-700">Description du film</p>
        </div>
        <!-- Ajoutez d'autres films ici -->
      </div>
    </section>

    <!-- Section Films populaires -->
    <section class="mb-8">
      <h2 class="text-2xl font-bold mb-4">Films populaires</h2>
      <!-- Contenu de la section -->
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
        <!-- Exemple de film -->
        <div class="bg-gray-200 p-4 rounded-lg">
          <img src="https://via.placeholder.com/300x400" alt="Image de film" class="mb-2">
          <h3 class="text-xl font-semibold mb-2">Titre du Film</h3>
          <p class="text-gray-700">Description du film</p>
        </div>
        <!-- Ajoutez d'autres films ici -->
      </div>
    </section>

    <!-- Section Les plus vus -->
    <section class="mb-8">
      <h2 class="text-2xl font-bold mb-4">Les plus vus</h2>
      <!-- Contenu de la section -->
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
        <!-- Exemple de film -->
        <div class="bg-gray-200 p-4 rounded-lg">
          <img src="https://via.placeholder.com/300x400" alt="Image de film" class="mb-2">
          <h3 class="text-xl font-semibold mb-2">Titre du Film</h3>
          <p class="text-gray-700">Description du film</p>
        </div>
        <!-- Ajoutez d'autres films ici -->
      </div>
    </section>

    <!-- Section Les incontournables -->
    <section>
      <h2 class="text-2xl font-bold mb-4">Les incontournables</h2>
      <!-- Contenu de la section -->
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
        <!-- Exemple de film -->
        <div class="bg-gray-200 p-4 rounded-lg">
          <img src="https://via.placeholder.com/300x400" alt="Image de film" class="mb-2">
          <h3 class="text-xl font-semibold mb-2">Titre du Film</h3>
          <p class="text-gray-700">Description du film</p>
        </div>
        <!-- Ajoutez d'autres films ici -->
      </div>
    </section>

    <!-- Carrousel -->
    <section class="mt-8">
      <h2 class="text-2xl font-bold mb-4">Carrousel</h2>
      <div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="https://via.placeholder.com/1200x600" class="d-block w-100" alt="...">
          </div>
          <div class="carousel-item">
            <img src="https://via.placeholder.com/1200x600" class="d-block w-100" alt="...">
          </div>
          <div class="carousel-item">
            <img src="https://via.placeholder.com/1200x600" class="d-block w-100" alt="...">
          </div>
          <!-- Ajoutez d'autres images pour le carrousel ici -->
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
    </section>
  </main>
</template>


<style scoped>
/* Ajoutez vos styles personnalisés ici */
.carousel-inner img {
  max-height: 400px; /* ajuste la hauteur maximale des images du carrousel */
  object-fit: cover; /* assure que les images du carrousel remplissent l'espace défini */
}
</style>

<script setup lang="ts">

import { useRouter } from "vue-router";

const router = useRouter();
router.replace ('/films');
</script>
