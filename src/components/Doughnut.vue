<template>
  <Doughnut :data="chartData" :options="chartOptions" />
</template>

<script>
import { Chart as ChartJS, ArcElement, Tooltip, Legend } from "chart.js";
import { Doughnut } from "vue-chartjs";

ChartJS.register(ArcElement, Tooltip, Legend);
export default {
  components: { Doughnut },
  data: () => ({
    chartData: {
      labels: ["VueJs", "EmberJs", "ReactJs", "AngularJs"],
      datasets: [
        {
          backgroundColor: ["#418883", "#E46651", "#00D8FF", "#DD1816"],
          data: [40, 20, 80, 10],
        },
      ],
    },
    chartOptions: {
      responsive: true,
    },
  }),
};
</script>

<style></style>
