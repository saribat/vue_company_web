<template>
  <div id="app">
    <transition name="fade">
      <div id="loadingSec" v-if="load_show">
        <div class="loadingLogo">
          <img src="../src/assets/svg/toplogo.svg" alt="">
          <span class="loadingBar" style="height: 0%;"></span>
        </div>
      </div>
    </transition>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      load_show: true
    }
  },
  mounted () {
    let _this = this
    setTimeout(function () {
      _this.load_show = false
    }, 1000)
  }
}
</script>

<style>
#loadingSec {
  position: fixed;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  z-index: 9999;
  background: #ee7800;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 1s
}

.fade-enter,
.fade-leave-active {
  opacity: 0
}

</style>
