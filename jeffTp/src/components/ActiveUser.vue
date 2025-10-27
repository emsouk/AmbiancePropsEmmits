<template>
  <div class="flex justify-center items-center bg-base-50">
    <div class="card w-96 shadow-xl bg-primary text-primary-content">
      <div class="card-body text-center">
        <h1 class="text-2xl font-bold">Composant affichage des données</h1>
        <div class="border:solid 5px white">  
        {{ props.user.name }}
        {{ props.user.age }}
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="js" setup>
import { ref } from 'vue';

const props = defineProps({
  user :
  {
    name:{type: String, required: true}, 
    age:{type:Number, required: true}
  }
});
console.log("ma props",props.user);
</script>



<style>
/* Conservation de ton violet personnalisé */
.bg-primary {
  background-color: rgb(75, 23, 166) !important;
}
</style>


