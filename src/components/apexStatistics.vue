<template>
  <div>
    <div bar-stats>
      <p class="stats-title">TOTAL OPEX Budget Statistics</p>
      <p class="stats-sub-title">Total Budget Spent vs Total Budget Balance</p>
      <div stats>
        <span>Total Spent</span>
        <span class="spent">N 8,282,289</span>
        <span>Total Balance</span>
        <span class="balance">N 8,282,289</span>
      </div>
      <div>
        <canvas id="apex-bar" class="w-full" height="300"></canvas>
        <ul class="flex justify-center">
          <li class="spent-key flex items-center">
            <div></div>Spent
          </li>
          <li class="balance-key flex items-center">
            <div></div>Balance
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import Chart from "chart.js";
export default {
  data() {
    return {};
  },
  methods: {
    createOpexGraph() {
      var barChartData = {
        labels: [
          "jan",
          "feb",
          "mar",
          "april",
          "may",
          "june",
          "july",
          "aug",
          "sept",
          "oct",
          "nov",
          "dec"
        ],
        datasets: [
          {
            label: "Balance",
            backgroundColor: "#e95957",
            borderWidth: 0,
            data: [3, 1, 4, 3, 3, 4.7, 2, 1, 3, 1, 4, 3]
          },
          {
            label: "Spent",
            backgroundColor: "#17c7bf",
            borderWidth: 0,
            data: [2, 2.5, 3, 4, 2, 3, 1, 3, 2, 2, 3, 2]
          }
        ]
      };

      var ctx = document.getElementById("apex-bar").getContext("2d");
      new Chart(ctx, {
        type: "bar",
        data: barChartData,
        options: {
          responsive: false,
          legend: {
            display: false
          },
          scales: {
            xAxes: [
              {
                gridLines: {
                  display: false
                }
              }
            ],
            yAxes: [
              {
                ticks: {
                  beginAtZero: true
                },
                gridLines: {
                  display: false
                }
              }
            ]
          }
        }
      });
    }
  },
  mounted() {
    this.createOpexGraph();
  }
};
</script>

<style>
#apex-bar,
#opex-bar {
  margin: auto;
  padding: 30px 14px;
}
</style>
