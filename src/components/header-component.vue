<template>
   <b-jumbotron fluid header="Back to School" lead="Be Sure to be Prepared">
       <b-button variant="default" href="#">Check Our Catalog >></b-button>
   </b-jumbotron>
</template>

<script>
    export default {
        name: 'header-component'
    }
</script>

<style scoped>
    .jumbotron {
        min-height: 70vh;
        background-image: url('../assets/slider.jpg');
        background-position: center center;
        background-size: cover;
        opacity: 0.95;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .container {
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        align-items: center;
    }

    h1 {
        padding: 0.2em 0.5em;
        font-size: 3rem;
        color: white;
        background-color: #303841;
        text-align: center;
    }
    .lead, .btn {
        font-size: 1.5rem;
        color: whitesmoke;
        font-weight: 600;
        filter: drop-shadow(1em 1em 1em  #303841);
    }
    .btn {
        text-decoration: underline;
    }
</style>