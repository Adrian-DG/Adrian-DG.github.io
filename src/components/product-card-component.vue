<template>
    <b-card :title="item.name" :img-src="require(`@/assets/${item.image}`)" img-top tag="deal">
        <small>{{ item.brand }}</small>
        <b-card-text>
            Some quick example text to build on the card title.
        </b-card-text>
        <b-row>
            <b-col cols="9">
                <p class="card-price text-success">+ US${{ item.price }}</p>
            </b-col>
            <b-col cols="3">
                <b-button href="#" variant="default">+</b-button>
            </b-col>
        </b-row>
        
    </b-card>
</template>

<script>
    export default {
        name: 'product-card-component',
        props: ['item']
    }
</script>

<style scoped>
    .card-title {
        font-size: 1.3rem;
    }
    .card {
        height: 70vh;
    }
    .card-img-top {
        width: 100%;
        height: 40vh;
    }
    .card-price {
        font-weight: 800;
    }
    .row {
        align-items: center;
    }
    .btn {
        border: 1.5px solid gainsboro;
        font-weight: bold;
        font-size: 1.3rem;
    }
</style>