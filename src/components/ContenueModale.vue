<template>
    <div class="container">

        <modale :revele="revele" :toggleModale="toggleModale"></modale>
    <!--  props name: 'bonjour'/ bind la donnée revele && lie la methode toggleModale en props-->
        <div v-on:click="toggleModale" class="btn-success">Ourve la modale</div>
        <!-- Quand clique active la methode toggleModale -->

    </div>
    

</template>

<script>

import FenetreModale from './FenetreModale.vue'

export default {
    name: 'ContenuModale',
    data() {
      return {
        revele: false
      } 
    },
    methods: {
        toggleModale: function() {
            this.revele = !this.revele
        }
    },
    components: {
        'modale': FenetreModale
    }
}

</script>


<style>

.btn-success {
    background-color: #4CAF50;
    width: 140px;
    color: white;
    padding: 10px;
    cursor:pointer;
    margin: 0 auto;
}

</style>