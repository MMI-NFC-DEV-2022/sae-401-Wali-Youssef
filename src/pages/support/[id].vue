<script setup lang="ts">
import { useRoute } from 'vue-router/auto';
import { supabase } from '@/supabase';
import Affichesupport from '../../components/Affichesupport.vue';
const route = useRoute('/support/[id]');
let {data : Support, error} = await supabase
    .from('Support')
    .select(`
    *,
    Films(*)
    `)
    .eq('id', route.params.id)
    .single();
console.log("data film",Support);
</script>

<template>
    <div>
        <Affichesupport v-bind="Support" />
    </div>
</template>