<script setup lang="ts">
import AfficheFilm from '@/components/AfficheFilm.vue';
import type { SchemaFilm } from '@/types';
import { supabase } from '@/supabase';
 
console.log(supabase);
    
let {data : tableaufilm, error} = await supabase
    .from('Films')
    .select('*');
    if (error) console.log("n'a pas pu charger la table Film :", error);
</script>

<template>
    <div class="banner">
 <h1 class="text-3xl font-bold text-center text-black my-8">Films</h1>
</div>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 bg-gray-900" >
        <AfficheFilm v-for="film in tableaufilm" v-bind="film" />
    </div>


</template>

<style>
.banner {
  /* Définir l'image de fond */
  background-image: url('/src/assets/banniere.png');
  /* Définir la taille de l'image */
  background-size: cover;
  /* Centrer l'image horizontalement et verticalement */
  background-position: center;
  /* Définir la hauteur de la bannière */
  height: 300px; /* Ajustez la hauteur selon vos besoins */
  /* Autres styles */
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}
</style>