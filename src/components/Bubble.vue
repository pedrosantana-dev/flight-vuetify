<template>
  <Bubble :data="chartData" :options="chartOptions" />
</template>

<script>
import {
  Chart as ChartJS,
  Tooltip,
  Legend,
  PointElement,
  LinearScale,
} from "chart.js";
import { Bubble } from "vue-chartjs";

ChartJS.register(LinearScale, PointElement, Tooltip, Legend);

export default {
  components: { Bubble },
  data: () => ({
    chartData: {
      labels: ["VueJs", "EmberJs", "ReactJs", "AngularJs"],
      datasets: [
        {
          label: "Data One",
          backgroundColor: "#f87979",
          data: [
            { x: 20, y: 30, r: 15 },
            { x: 20, y: 20, r: 10 },
            { x: 15, y: 8, r: 30 },
          ],
        },
        {
          label: "Data Two",
          backgroundColor: "#7c8cf8",
          data: [
            { x: 10, y: 30, r: 15 },
            { x: 20, y: 20, r: 10 },
            { x: 15, y: 8, r: 30 },
          ],
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
