<template>
  <div class="main">
    <!-- <ul>
      <li v-for="(product, index) in products" :key="index">
        {{product.titolo}}
      </li>
    </ul> -->
<div class="main-center">
<ProductCard 
      v-for="(card, index) in cards" 
      :key="index"
      :card="card"
    />
</div>
    

        <button>LOAD MORE</button>
  </div>
</template>

<script>
import ProductCard from '@/components/ProductCard.vue'
import cards from '@/assets/data/dc-comics.js'
export default {
  name: 'Products',
  components: {
    ProductCard
  },
  data() {
    console.log(cards)

    return {
      cards: cards
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .main {
        display: flex;
        position: relative;
        justify-content: center;
        background: black;

        button {
            display: flex;
            position: absolute;
            bottom: 0;
            right: 50%;
            left: 50%;
            transform: translate(-50% , -50%);
            width: 10vw;
            padding: 5px;
            justify-content: center;
            color: white;
            text-transform: uppercase;
            background: blue;
        }

        .main-center {
          display: flex;
          color: white;
          padding-top: 20px;
          padding-bottom: 80px;
          justify-content: center;
          flex-flow: row wrap;
        }
    }
</style>