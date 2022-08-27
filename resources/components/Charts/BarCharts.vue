<template>
    <div>
        <bar-chart 
        :chart-options="chartOptions"
        :chart-data="chartData"
        :chart-id="chartId"
        :dataset-id-key="datasetIdKey"
        :plugins="plugins"
        :css-styles="cssStyles"
        :styles="styles"
        :width="width"
        :height="height"></bar-chart>
    </div>
</template>

<script>
import {Bar} from 'vue-chartjs';
import {Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale} from 'chart.js';
ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale)
export default {
    components: {
        'bar-chart': Bar,
    },
    props: {
    chartId: {
        type: String,
        default: 'bar-chart'
    },
    datasetIdKey: {
        type: String,
        default: 'label'
    },
    width: {
        type: Number,
        default: 200
    },
    height: {
        type: Number,
        default: 200
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

