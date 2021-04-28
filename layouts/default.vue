<template>
  <div>
    <div class="container mt-5 mb-4">
      <div class="row">
        <div class="col-md-4">
          <nuxt-link to="/" style="color: #111;"><strong>$TRADESPY.cc</strong> </nuxt-link>
        </div>
        <div class="col-md-8 text-right">
          <nuxt-link to="/about">ABOUT</nuxt-link> | <nuxt-link to="/feed">FEED</nuxt-link> | <a href="/strategies">STRATEGIES</a> | <nuxt-link to="/books">BOOKS</nuxt-link> | <nuxt-link to="/websites">WEBSITES</nuxt-link> | <nuxt-link to="/people">PEOPLE</nuxt-link> | <nuxt-link to="/misc">OTHER RESOURCES (MISC)</nuxt-link>
        </div>
      </div>
    </div>
  
    <Nuxt />

    <div class="container mt-4">
      <div class="row">
        <div class="col-md-12 text-center">
          Unique View Count: 000<br>
          This website was built solely, and strictly for educational purposes. © 2021
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
</style>
