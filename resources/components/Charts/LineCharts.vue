<template>
    <line-chart
    :chard-id="chartID"
    :chart-options="chartOptions"
    :chart-data="chartData"
    :width="width"
    :height="height"
    :css-styles="cssStyles"
    :plugins="plugins"
    ></line-chart>
</template>

<script>

import {Line} from 'vue-chartjs';
import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  LineElement,
  LinearScale,
  PointElement,
  CategoryScale,
} from 'chart.js'

ChartJS.register(
  Title,
  Tooltip,
  Legend,
  LineElement,
  LinearScale,
  PointElement,
  CategoryScale
)
export default {
    components: {
        'line-chart': Line
    },
    props: {
        chartId: {
        type: String,
        default: 'line-chart'
    },
    // datasetIdKey: {
    //     type: String,
    //     default: 'label'
    // },
    width: {
        type: Number,
        default: 400
    },
    height: {
        type: Number,
        default: 400
    },
    cssClasses: {
        default: '',
        type: String
    },
    styles: {
        type: Object,
        default: () => {}
    },
    plugins: {
        type: Array,
        default: () => []
    },
    },
    data(){
        return{
chartData: {
            labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
            datasets: [{
                label: 'Number of Clients',
                data: [40, 20, 12, 20, 33, 12, 35],
                backgroundColor: ['#0000FF', '#f87979'],
                }]
        },
        chartOptions: {
            responsive: true
        }
        }
    }
}
</script>