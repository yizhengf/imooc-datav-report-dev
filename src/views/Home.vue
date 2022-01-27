<template>
  <div class="home">
    <top-view></top-view>
    <bottom-view></bottom-view>
    <sales-view></sales-view>
    <map-view></map-view>
  </div>
</template>

<script>
import TopView from '../components/TopView'
import SalesView from '../components/SalesView'
import BottomView from '../components/BottomView'
import MapView from '../components/MapView'

export default {
  name: 'Home',
  components: {
    TopView,
    BottomView,
    SalesView,
    MapView
  }
}
</script>

<style>
.home {
  width: 100%;
  height: 100%;
  padding: 20px;
  background: #eee;
  box-sizing: border-box;
}
</style>
