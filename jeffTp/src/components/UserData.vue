
<template>
  <div class="flex justify-center items-center min-h-screen bg-base-200">
    <form action="" class="card w-96 bg-base-100 shadow-xl p-6 space-y-4"  @submit.prevent="submitData">
      <h1 class="text-2xl font-bold text-center mb-4">Composant Formulaire d'édition ! </h1>

      <label class="form-control w-full">
        <span class="label-text">Votre nom</span>
        <input type="text" v-model="name" name="name" value="Entrez votre nom" class="input input-bordered w-full" />
      </label>

      <label class="form-control w-full">
        <span class="label-text">Votre âge</span>
        <input type="number" v-model="age" name="age" value="Entrez votre âge" class="input input-bordered w-full" />
      </label>

      <input type="submit"  value="Mettre à jour" class="btn btn-primary w-full" />
    </form>
  </div>
</template>

<script lang="js" setup>

import { ref } from 'vue';

let age = ref(0);
let name = ref("");
// defineEmits({name:{type:String}, age:{type:Number}});

const emit = defineEmits(['set-data']);

// Émission des données au parent
function submitData() {
    // on émet l’évènement
    // ⚠️ En Composition API, on définit emit :
    emit('set-data', name.value, age.value)
   
}

console.log(age);
console.log(name);
</script>

