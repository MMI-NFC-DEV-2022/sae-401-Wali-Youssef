<script setup lang="ts">
import { supabase, user } from '../supabase';
</script>
<template>
    <div class="flex justify-center items-center h-screen">
      <div class="text-center">
        <button v-if="user"
                @pointerdown="supabase.auth.signOut()"
                class="bg-red-500 hover:bg-red-600 text-white font-semibold py-2 px-4 rounded-md shadow-md mr-4">
          Se déconnecter ({{ user.email }})
        </button>
        <button v-else
                @pointerdown="supabase.auth.signInWithOAuth({ provider: 'github' })"
                class="bg-gray-800 hover:bg-gray-700 text-white font-semibold py-2 px-4 rounded-md shadow-md">
          Se connecter avec Github
        </button>
      </div>
    </div>
  </template>