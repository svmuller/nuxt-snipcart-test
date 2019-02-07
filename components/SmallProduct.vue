<template>
  <div class="card">
    <header class="card-header">
      <div class="card-header-title is-centered">
        {{ product.title.rendered }}
      </div>
    </header>

    <div class="card-image">
      <img :src="product.better_featured_image.media_details.sizes.thumbnail.source_url">
    </div>

    <div class="card-content">
      <div class="content">
        {{ product.acf.product_description }}
      </div>
    </div>

    <div class="card-footer">
      <a
        href="#"
        class="snipcart-add-item card-footer-item"
        data-item-url="/"
        :data-item-name="product.title.rendered"
        :data-item-price="product.acf.product_price"
        :data-item-id="product.id"
        :data-item-description="product.acf.product_description"
      >
        <i class="fa fa-cart-plus" /> &nbsp;Add to cart
      </a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    product: {
      type: Object,
      required: true
    }
  }
}
</script>

<style>
  .card-content .content {
    min-height: 48px;
  }
</style>
