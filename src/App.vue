<template>
  <div id="main">
    <navbar-component/>
    <header-component/>
    <list-component :column="12" :phone="12" :tablet="4" :laptop="3" :title="'Categories'" :list="categories"/>
    <list-component :column="12" :phone="10" :tablet="6" :laptop="4" :title="'Our Deals'" :list="deals"/>
  </div>
</template>

<script>
import Popper from 'popper.js';
Popper.Defaults.modifiers.computeStyle.gpuAcceleration = false;

// Components
import NavbarComponent from './components/navbar-component.vue';
import HeaderComponent from './components/header-component.vue';
import ListComponent from './components/list-component.vue';


export default {
  name: 'App',
  data: function(){
    return {
      categories: [
        { name: 'Tablets', image: 'tablet.jpg' },
        { name: 'Laptop', image: 'laptop.jpg' },
        { name: 'accesories', image: 'accesories.jpg' },
        { name: 'accesories', image: 'accesories.jpg' }
      ],
      deals: [
        { image: 'headphones.jpg', name: 'Beats headphones', brand: 'Beats Inc.', price: 120.95 },
        { image: 'controller.jpg', name: 'Xbox Controller', brand: 'Microsoft Inc.', price: 40.95 },
        { image: 'tripod.jpg', name: 'Professional Camera', brand: 'Sony Inc.', price: 150.95 },
        { image: 'headphones.jpg', name: 'Beats headphones', brand: 'Beats Inc.', price: 120.95 },
        { image: 'tripod.jpg', name: 'Professional Camera', brand: 'Sony Inc.', price: 150.95 },
        { image: 'controller.jpg', name: 'Xbox Controller', brand: 'Microsoft Inc.', price: 40.95 }        
      ]
    }
  },
  components: {
    NavbarComponent,
    HeaderComponent,
    ListComponent,
  }
}
</script>

<style>
  #main {
    width: 100%;
  }
</style>
