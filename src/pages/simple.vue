<script setup lang="ts">
import AfficheFilm from '@/components/AfficheFilm.vue';
import type { SchemaFilm } from '@/types';

    const monFilm :SchemaFilm = {
        nom_film: "Titre du film",
        annee_film: 1000,
        description_film: "123 rue de la maison",
        note_film: 2,
        image_film: "\public\pexels-binyamin-mellish-106399.jpg",
      
    };
</script>

<template>
    <div class="grid grid-cols-3 gap-4">
        <AfficheFilm :nom_Film="monFilm.nom_film" :description_film="monFilm.description_film" :note="monFilm.note_film" :annee_films="monFilm.annee_film" :img_film="monFilm.image_film"/>
    </div>
    <AfficheFilm nom-maison="Maison" :favori="true" image="\pexels-binyamin-mellish-106399.jpg"/>
</template>