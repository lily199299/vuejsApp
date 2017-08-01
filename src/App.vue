<template>
  <div id="app">

      <v-header></v-header>

    <div class="tab">
      <div class="tab-item">
        <router-link to="/goods">商品</router-link>
      </div>
      <div class="tab-item">
        <router-link to="/ratings">评论</router-link>
      </div>
      <div class="tab-item">
        <router-link to="/seller">商家</router-link>
      </div>
    </div>

    <router-view>
      <v-goods></v-goods>
      <v-ratings></v-ratings>
      <v-seller></v-seller>
    </router-view>
    <div class="content">content</div>
  </div>
</template>

<script>
  import header from './components/header/header.vue';
  import goods from './components/goods/goods.vue';
  import ratings from './components/ratings/ratings.vue';
  import seller from './components/seller/seller.vue';
  export default {
    components: {
      'v-header': header,
      'v-goods': goods,
      'v-ratings': ratings,
      'v-seller': seller
    }
  };
</script>

<style>
.tab{
  display: flex;
  width:100%;
  height:40px;
  line-height: 40px;
  background-color: aquamarine;
}
  .tab-item{
    flex:1;
    text-align: center;
  }
.tab-item a{
  display: block;
}
</style>
