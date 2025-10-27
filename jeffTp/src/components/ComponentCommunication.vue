<!-- parent -->

<template>
  <div class="flex flex-col items-center min-h-screen bg-base-200 p-6 space-y-6">
    <div class="card w-full max-w-4xl bg-warning text-warning-content shadow-xl p-6">
      <h1 class="text-2xl font-bold text-center mb-4">Composant gestion de l'utilisateur</h1>
      
      <!-- Composants enfants -->
      <div class="space-y-4">
        <ActiveUser :user/>
        <UserData @set-data="setUserData" class="my-4" />
            <div style="border: red 1px solid;"> 
                <p style="color:black;">{{ user?.name }}</p>
                <p style="color:black;"> {{user?.age}}</p>
            </div>
      </div>
    </div>
  </div>
</template>

<script lang="js" setup>
import { ref } from 'vue';
import ActiveUser from './ActiveUser.vue';
import UserData from './UserData.vue';

const name = ref('');
const age = ref('');

const user = ref({
    name: 'Emilie',
    age: 30,
})

// Fonction de mise à jour (appelée via @set-data)
const setUserData = (nameEvent, ageEvent) => {
    console.log(nameEvent,ageEvent);

    user.value = {
        name: nameEvent,
        age: ageEvent,
    }
}

</script>

<style>

.bg-warning {
  background-color: rgb(255, 191, 0) !important;
}
</style>
