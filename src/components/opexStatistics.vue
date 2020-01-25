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
        <canvas id="opex-bar" class="w-full" height="300"></canvas>
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
  methods: {
    createOpexChart() {
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
            data: [3, 1, 4, 3, 3, 4.6, 2, 1, 3, 1, 4, 3]
          },
          {
            label: "Spent",
            backgroundColor: "#17c7bf",
            borderWidth: 0,
            data: [2, 2.5, 3, 4, 2, 3, 1, 3, 2, 2, 3, 2]
          }
        ]
      };

      var ctx = document.getElementById("opex-bar").getContext("2d");
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
    this.createOpexChart();
  }
};
</script>

<style>
.spent-key > div,
.balance-key > div {
  border-radius: 4px;
  margin-right: 4px;
  width: 8px;
  height: 8px;
}
.balance-key > div {
  background: #e95957;
}
.balance-key {
  color: #e95957;
}
.spent-key {
  background-color: #f2f2f2;
  color: #17c7bf;
}
.spent-key > div {
  background-color: #17c7bf;
}
.spent-key,
.balance-key {
  border-radius: 8px;
  font-family: OpenSans;
  font-size: 14px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;

  padding: 3px 10px;
}
[bar-stats] {
  border-radius: 6px;
  box-shadow: 0 7px 64px 0 rgba(19, 36, 78, 0.07);
  background-color: #ffffff;
  padding: 38px;
}
.spent {
  color: #4abba4 !important;
}
.balance {
  color: #c00202 !important;
}
.spent,
.balance {
  border-radius: 8.5px !important;
  background-color: #f2f2f2 !important;
  padding: 2px 9px;
}
[stats] {
  margin-top: 13px;
    font-family: SourceSansPro;
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.17px;
  color: #485465;

}
[stats] span {
  margin-right: 10px;
  border-radius: 6px;
  box-shadow: 0 7px 64px 0 rgba(19, 36, 78, 0.07);
  background-color: #ffffff;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.17px;
  color: #485465;
}
.stats-sub-title {
  font-family: SourceSansPro;
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.17px;
  color: #485465;
}
.stats-title {
  font-family: SourceSansPro;
  font-size: 18px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.22px;
  color: #253858;
}
</style>
