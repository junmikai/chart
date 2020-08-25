<template>
  <div class="hello">
    <BarChart :chart-data="datacollection" />
  </div>
</template>

<script>
import BarChart from "./BarChart.js";
export default {
  name: "Chart",
  props: {
    msg: String,
  },
  components: {
    BarChart,
  },
  data: () => ({
    datacollection: null,
  }),
  mounted() {
    this.fillData();
  },
  methods: {
    fillData() {
      this.datacollection = {
        labels: ["A", "B", "C", "D"],
        datasets: [
          {
            label: "データセットラベルA",
            data: [20, 30, 40, 50],
          },
        ],
      };
    },
  },
};
</script>
