<template>
  <common-card
    title="累计订单量"
    value="2,157,420">
    <template>
      <v-chart :option="getOptions()"/>
    </template>
    <template v-slot:footer>

      <span>昨日订单量 </span>
      <span class="emphasis">20，000 </span>

    </template>
  </common-card>

</template>

<script>

import commonCardMixin from '../../mixins/commonCardMixin'

export default {
  mixins: [commonCardMixin],
  methods: {
    getOptions () {
      return {
        xAxis: {
          type: 'category',
          show: false,
          boundaryGap: false
        },
        yAxis: {
          show: false
        },
        series: [{
          type: 'line',
          data: [620, 340, 430, 560, 715, 480, 390, 190, 835, 220, 170, 260, 310, 560, 880],
          areaStyle: {
            color: 'purple'
          },
          lineStyle: {
            width: 0
          },
          itemStyle: {
            opacity: 0
          },
          smooth: true

        }],
        grid: {
          top: 0,
          bottom: 0,
          left: 0,
          right: 0
        }
      }
    }
  }
  }
</script>
