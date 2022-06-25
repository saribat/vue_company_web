<template>
  <div>
    <Home-Nav :navindex="1"></Home-Nav>
    <Home-Banner :list="list"></Home-Banner>
    <Business-Item :businessList="businessList"></Business-Item>
    <Home-Footer></Home-Footer>
  </div>
</template>

<script>
import HomeNav from '../common/Nav'
import HomeBanner from '../common/Banner'
import BusinessItem from '../common/BussinessItem'
import HomeFooter from '../common/Footer'
import axios from 'axios'
import url from '../../modules/api.js'
export default {
  name: 'Bussiness',
  components: {
    HomeNav, HomeFooter, HomeBanner, BusinessItem
  },
  data () {
    return {
      list: [{
        id: 1,
        h2: '企业情报',
        p: 'xxxxxxxx'
      }],
      businessList: []
    }
  },
  mounted () {
    axios.get(url.producDetailtList).then(res => {
      this.businessList = res.data.list
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
