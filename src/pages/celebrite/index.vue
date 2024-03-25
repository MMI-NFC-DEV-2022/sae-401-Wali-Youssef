<script setup lang="ts">
import { useRoute } from 'vue-router/auto';
import { supabase } from '@/supabase';
import AfficheCelebrite from '@/components/AfficheCelebrite.vue';
const route = useRoute('/celebrite/[id]');
let {data : celebrite, error} = await supabase
    .from('Celebrite')
    .select('*')
console.log("data film",celebrite);
</script>

<template>
   <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 bg-gray-900" >
        <AfficheCelebrite v-for="Celebrite in celebrite" v-bind="Celebrite" />
    </div>
</template>