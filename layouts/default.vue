<template>
  <div>
    <section class="section">
      <Header />
      <div class="container">
        <nuxt />
      </div>
    </section>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.2.2/jquery.min.js" />
    <script id="snipcart" src="https://cdn.snipcart.com/scripts/2.0/snipcart.js" data-api-key="ZDlhMDVjMTAtMWMwNi00MzA0LWE2NTQtNjc4MDE2MGQ3ZDBjNjM2ODQ5MjMxOTI3MjA5NTk0" />
  </div>
</template>

<script>
import Header from '~/components/Header'
export default {
  components: {
    Header
  }
}
</script>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

</style>
