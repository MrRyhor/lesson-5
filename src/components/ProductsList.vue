<template>
    <div class="products-list">
        <product-item v-for="product in productsListData" :key="product.id" :item-data="product"/>
    </div>
</template>
<script>
import ProductItem from './ProductItem.vue'

export default {
    name: 'ProductsList',
    components: { ProductItem },

    props: {
        productsListData: {
            type: Array,
            default: () => []
        }
    },
    
    
}
</script>
<style lang="css" scoped>
    .products-list{
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-top: 50px;
        
    }
</style>