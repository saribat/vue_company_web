<template>
  <div>
    <Home-Nav :navindex="2"></Home-Nav>
    <Home-Banner :list="list"></Home-Banner>
    <Home-Main></Home-Main>
    <Home-Footer></Home-Footer>
  </div>
</template>

<script>
import HomeNav from '../common/Nav'
import HomeBanner from '../common/Banner'
import HomeMain from './components/Main'
import HomeFooter from '../common/Footer'

export default {
  name: 'Home',
  components: {
    HomeNav, HomeFooter, HomeBanner, HomeMain
  },
  data () {
    return {
      list: [{
        id: 1,
        h2: '事業案内',
        p: 'xxxx'
      }]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
