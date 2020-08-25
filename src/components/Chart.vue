<template>
  <div class="hello">
    <BarChart :chart-data="datacollection" class="graph" />
  </div>
</template>

<script>
import BarChart from "./BarChart.js";
export default {
  data() {
    return {
      datacollection: null,
    };
  },
  components: {
    BarChart,
  },
  mounted() {
    this.fillData();
  },
  methods: {
    fillData() {
      this.datacollection = {
        labels: ["A", "B", "C", "D"],
        maxWidth: "50px",
        datasets: [
          {
            label: "データセットラベルA",
            data: [20, 30, 40, 50],
            backgroundColor: "#f87979",
            pointBackgroundColor: "white",
            borderWidth: 1,
            pointBorderColor: "#249EBF",
          },
        ],
      };
    },
  },
};
</script>
