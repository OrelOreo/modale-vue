<template>

    <div class="bloc-modale" v-if="revele">
        <!-- Si revele est true alors affiche -->

        <div class="overlay" v-on:click="toggleModale"></div>
        <!-- Si clique alors applique la methode toggleModale -->

        <div class="modale">
            <div class="btn-modale btn btn-danger" v-on:click="toggleModale">X</div>
            <!-- pareil ici -->
            <h2>Le contenu de la modale</h2>
        </div>

    </div>


</template>

<script>

export default {
    name:'FenetreModale',
    props: ['revele','toggleModale']
}

</script>

<style>

.bloc-modale {
    position: fixed;
    top:0;
    bottom:0;
    left: 0;
    right: 0;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.overlay {
    background: rgba(0, 0, 0, 0.5);
    position: fixed;
    top:0;
    left: 0;
    right: 0;
    bottom: 0;
}

.modale {
    border: 1px solid gray;
    background-color: #f1f1f1;
    color: #333;
    padding: 30px;
    position: fixed;
}

.btn {
    background-color: red;
    padding: 10px;
    color: white;
    font-weight: 600;
    cursor: pointer;
    position: absolute;
    right: 10px;
    top: 10px;
}

</style>