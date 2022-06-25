<template>
  <div>
    <Home-Nav :navindex="0"></Home-Nav>
    <Home-Swiper></Home-Swiper>
    <Home-Product :list="list1"></Home-Product>
    <Home-Product :list="list2"></Home-Product>
    <Home-Product :list="list3"></Home-Product>
    <Home-Footer></Home-Footer>
  </div>
</template>

<script>
import HomeNav from '../common/Nav'
import HomeSwiper from './components/Swiper'
import HomeProduct from '../common/Product'
import HomeFooter from '../common/Footer'

export default {
  name: 'Home',
  components: {
    HomeNav, HomeSwiper, HomeProduct, HomeFooter
  },
  data () {
    return {
      list1: [
        {id: 1, p: 'それは、人と人をつなぐ、世代を超えたコミュニティづくりをサポートすること。樹々の温もりを感じる、上質な住まいをつくること。暮らしにあったらうれしい商品やサービスを提供すること。いざという時でも家族が安心できる住まいをつくること。そして、住まわれてからの家族の将来設計を支える仕組みをつくること。', src: require('./../../assets/image/lead_img01.jpg')}
      ],
      list2: [],
      list3: []
    }
  },
  mounted () {
  }
}
</script>

<style scoped>

</style>
