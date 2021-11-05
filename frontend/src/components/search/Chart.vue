<template>
  <div>
    <div id="chart" ref="chartarea"/>
  </div>
</template>
<style lang="scss" scoped>
</style>
<script>
import Vue from 'vue'
import tuiChart from 'tui-chart'
Vue.use(tuiChart)
export default {
  name: 'Chart',
  mounted() {
    this.drawChart()
  },
  methods: {
    drawChart() {
      var container = this.$refs.chartarea
      var data = {
        categories: [
          '01/01/2020',
          '02/01/2020',
          '03/01/2020',
          '04/01/2020',
          '05/01/2020',
          '06/01/2020',
          '07/01/2020',
          '08/01/2020',
          '09/01/2020',
          '10/01/2020',
          '11/01/2020',
          '12/01/2020',
        ],
        series: [
          {
            name: '쿠팡',
            data: [-3.5, -1.1, 4.0, 11.3, 17.5, 21.5, 25.9, 27.2, 24.4, 13.9, 6.6, -0.6],
          }
        ]
      }
      var options = {
        chart: {
          width: 500,
          height: 400,
          title: '가격'
        },
        yAxis: {
          title: '가격(원)'
        },
        xAxis: {
          title: '날짜'
        }
      }
      tuiChart.lineChart(container, data, options)
// console.log(tuiChart) 찍어보면 차트 이름들이 나옴. 그중에 골라서씀.
    }
  }
}
</script>
