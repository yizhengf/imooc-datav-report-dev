<template>
<ve-wordcloud :data="chartData"
              :settings="chartSettings"
              height="100%"/>
</template>

<script>
export default {
data () {
  return {
    chartData:{
      columns:['name','value'],
      rows:[{
        name:'imooc',
        value:100 * Math.random()
      },
        {
          name:'imooc1',
          value:100 * Math.random()
        },
        {
          name:'imooc2',
          value:100 * Math.random()
        },
        {
          name:'imooc4',
          value:100 * Math.random()
        },
        {
          name:'imooc3',
          value:100 * Math.random()
        },
        {
          name:'imooc5',
          value:100 * Math.random()
        }]
    },
    chartSettings:{
      color: ['rgba(97,216,0,.7)', 'rgba(204,178,26,.7)', 'rgba(245,166,35,.7)', 'rgba(156,13,113,.7)']
    }
  }
}
}
</script>

<style scoped>

</style>
