<template>
    <div class="flex w-vh bg-slate-50">
        <the-sidebar class="w-1/6 h-screen bg-slate-600"></the-sidebar>
        <div class="w-full flex flex-col border">
            <div class="flex w-full justify-end bg-white">
                <img src="../../public/images/sairil-headshot.jpeg" alt="" class="w-10 h-10 m-2 rounded-full">
            </div>
            <div class="flex flex-col m-3">
                <h1 class="text-2xl uppercase">Monthly Reports</h1>
                <div class="flex w-full m-3">
                    <div class="w-1/2">
                        <p><font-awesome-icon icon="plus"></font-awesome-icon> Monthly Reports</p>
                        <bar-chart class="w-2/3"></bar-chart>
                    </div>
                    <div class="w-1/2">
                        <p><font-awesome-icon icon="check"></font-awesome-icon> Resolved Reports</p>
                        <line-chart class="w-2/3"></line-chart>
                    </div>
                </div>
                <p class="mt-3"><font-awesome-icon icon="bars"></font-awesome-icon> Latest Reports</p>
                <div class="w-full">
                    <table class="w-full mt-3">
                        <thead class="bg-slate-700">
                            <tr class="">
                                <th class="text-sm font-normal text-white py-2 uppercase">Name</th>
                                <th class="text-sm font-normal text-white py-2 uppercase">Last Name</th>
                                <th class="text-sm font-normal text-white py-2 uppercase">Phone</th>
                                <th class="text-sm font-normal text-white py-2 uppercase">Email</th>
                            </tr>
                        </thead>
                        <tbody class="text-center text-sm">
                            <tr>
                                <td class="py-1">Sairil</td>
                                <td class="py-1">Seberiaga</td>
                                <td class="py-1">0928292820280</td>
                                <td class="py-1">sairil@gmail.com</td>
                            </tr>
                            <tr>
                                <td class="py-1">Jermaine</td>
                                <td class="py-1">Seberiaga</td>
                                <td class="py-1">09290282928</td>
                                <td class="py-1">jermaine@gmail.com</td>
                            </tr>
                            <tr>
                                <td class="py-1">Atat</td>
                                <td class="py-1">TenTaw</td>
                                <td class="py-1">098892829292</td>
                                <td class="py-1">atat_dswd@dswd.com</td>
                            </tr>
                            <tr>
                                <td class="py-1">Jerlyn</td>
                                <td class="py-1">Ramos</td>
                                <td class="py-1">092982882929</td>
                                <td class="py-1">singgitanay@ict-guimaras.com</td>
                            </tr>
                            <tr>
                                <td class="py-1">Daniel</td>
                                <td class="py-1">Gepolongca</td>
                                <td class="py-1">0927289292928</td>
                                <td class="py-1">pwd@ict-guimaras.com</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
        </div>
    </div>
    
</template>

<script>


import TheSidebar from './UI/TheSidebar.vue';
import TopPanel from './UI/TopPanel.vue';
import BarChart from './Charts/BarCharts.vue';
import LineChart from './Charts/LineCharts.vue';

export default {
   components: {
    'the-sidebar': TheSidebar,
    'top-panel': TopPanel,
    'bar-chart': BarChart,
    'line-chart': LineChart,
   },
}
</script>