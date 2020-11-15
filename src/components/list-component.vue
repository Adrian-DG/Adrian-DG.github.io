<template>
    <b-container>
        <h4 class="text-center">{{ title }}</h4>
        <hr>
        <b-row class="list">
            <b-col :cols="column" :sm="phone" :md="tablet" :lg="laptop" class="item" v-for="(item,index) in list" :key="index">
                <product-card-component v-if="item.price" :item="item"/>
                <card-component v-else :item="item"/>
            </b-col>
        </b-row>
    </b-container>
</template>

<script>
import CardComponent from './card-component.vue'
import ProductCardComponent from './product-card-component.vue'



export default {
    name: 'list-component',
    props: ['title','list', 'column', 'phone', 'tablet', 'laptop'],
    components: { CardComponent, ProductCardComponent }
}
</script>

<style scoped>
    .container {
        margin-top: 2.5em;
    }
    .text-center {
        color: #303841;
    }
    .list {
        overflow-x: auto;
        flex-wrap: nowrap;
    }
    .item {
        margin-bottom: 1em;
    }
</style>