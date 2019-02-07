<template>
  <div class="columns is-mobile is-multiline is-centered">
    <div v-for="p in products" :key="p.id" class="column is-one-third-desktop">
      <small-product :product="p" />
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import SmallProduct from '~/components/SmallProduct.vue'

export default {
  components: {
    SmallProduct
  },
  async asyncData({ env, params }) {
    const { data } = await axios.get(`${env.wp.baseUrl}${env.wp.apiUrl}`)

    const products = await Promise.all(await data.map(p => p))
    console.log(products)
    return {
      products
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
