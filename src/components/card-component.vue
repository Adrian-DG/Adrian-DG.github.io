<template>
    <div class="card">
        <img :src="require(`@/assets/${item.image}`)" class="card-img"/>
        <p class="card-text">{{ item.name }}</p>
    </div>
</template>

<script>
export default {
    name: 'card-component',
    props: ['item']
}
</script>

<style scoped>
    .card {
        max-height: 15vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .card-img {
        width: 100%;
        height: auto;
    }
    .card-text {
        font-size: 1.3rem;
        position: absolute;
        color: whitesmoke;
        font-weight: 800;
        filter: drop-shadow(1em 2em 1.5em #000);
    }
</style>