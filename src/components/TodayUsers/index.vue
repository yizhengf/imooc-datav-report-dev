<template>
  <common-card title="今日交易用户数"
               value="81,014">

    <template>
      <div id="today-user-chart" :style="{width: '100%', height:'100%'}"/>
    </template>

    <template v-slot:footer>
      <span>退货率  </span>
      <span class="emphasis">5.14%</span>
    </template>
  </common-card>
</template>

<script>

import commonCardMixin from '../../mixins/commonCardMixin'

export default {
  mixins: [commonCardMixin],
  mounted () {
    const chartDom = document.getElementById('today-user-chart')
    const chart = this.$echarts.init(chartDom)
    chart.setOption({
      color: ['#3398DB'],
      series: [{
        type: 'bar',
        data: [410, 82, 330, 150, 239, 222, 333, 512, 521, 289],
        barWidth: '60%'
      }],
      xAxis: {
        type: 'category',
        data: ['0:00', '1:00', '2:00', '3:00', '4:00', '5:00', '6:00', '7:00', '8:00', '9:00'],
        show: false,
        boundaryGap: false
      },
      yAxis: {
        show: false
      },
      grid: {
        bottom: 0,
        top: 0,
        left: 0,
        right: 0
      }
    })
  }
}
</script>

<style scoped>

</style>
