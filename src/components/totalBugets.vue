<template>
  <div>
    <div CAPPEX>
      <div class="flex items-center justify-between">
        <div cappex-title>
          <img src="images/image.png" class="inline mr-2" width="32" />
          Total Annual CAPEX Budget
          <button class="outline-none price">N 50,000,000</button>
        </div>
        <div>
          <button class="dropdown">
            Annual
            <span>⌄</span>
          </button>
        </div>
      </div>
      <section chart-holders class="flex items-center">
        <div class="w-1/2 relative">
          <div class="chart-details absolute">
            <p>64%</p>
            <p>REMAINING</p>
          </div>
          <canvas
            id="annex"
            class="w-100 m-auto"
            width="136"
            height="136"
          ></canvas>
        </div>
        <div>
          <div class="flex items-center">
            <img src="images/capex_spent.png" width="54px" class="m-4" />
            <div capex-details>
              <p>
                Total
                <b>CAPEX</b> Spent
              </p>
              <p>
                <b>N 18,000,000</b>
              </p>
            </div>
          </div>

          <div class="flex items-center">
            <img src="images/capex_balance.png" width="54px" class="m-4" />
            <div>
              <p capex-details>
                Total
                <b>CAPEX</b> Balance
              </p>
              <p capex-price>
                <b>N 32,000,000</b>
              </p>
            </div>
          </div>
        </div>
      </section>
    </div>

    <div CAPPEX>
      <div class="flex items-center justify-between">
        <div cappex-title>
          <img src="images/assignment2.png" class="inline mr-2" width="32" />
          Total Annual OPEX Budget
          <button class="outline-none price opex-price">N 20,000,000</button>
        </div>
        <div>
          <button class="dropdown">
            Annual
            <span>⌄</span>
          </button>
        </div>
      </div>
      <section chart-holders class="flex items-center">
        <div class="w-1/2 relative">
          <div class="chart-details absolute">
            <p>50%</p>
            <p>REMAINING</p>
          </div>
          <canvas
            id="opex"
            class="w-100 m-auto"
            width="136"
            height="136"
          ></canvas>
        </div>
        <div>
          <div class="flex items-center">
            <img src="images/Group 10798@3x.png" width="54px" class="m-4" />
            <div capex-details>
              <p>
                Total
                <b>OPEX</b> Spent
              </p>
              <p>
                <b>N 18,000,000</b>
              </p>
            </div>
          </div>

          <div class="flex items-center">
            <img src="images/opex_new.png" width="54px" class="m-4" />
            <div>
              <p capex-details>
                Total
                <b>OPEX</b> Balance
              </p>
              <p capex-price>
                <b>N 32,000,000</b>
              </p>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import Chart from "chart.js";
export default {
  methods: {
    annexChart() {
      var ctx = document.getElementById("opex");
      new Chart(ctx, {
        type: "pie",
        data: {
          labels: ["remianing", "used"],
          datasets: [
            {
              data: [50, 50],
              backgroundColor: ["#fb0091"],
              borderWidth: 0
            }
          ]
        },
        options: {
          cutoutPercentage: 85,
          responsive: false,
          legend: {
            display: false
          },
          tooltips: {
            callbacks: {
              label: function(tooltipItem) {
                return tooltipItem.yLabel;
              }
            }
          }
        }
      });
    },
    OpexChart() {
      var ctx = document.getElementById("annex");
      new Chart(ctx, {
        type: "pie",
        data: {
          labels: ["remianing", "used"],
          datasets: [
            {
              label: "# of Tomatoes",
              data: [64, 26],
              backgroundColor: ["#6915cf"],
              borderWidth: 0
            }
          ]
        },
        options: {
          cutoutPercentage: 85,
          responsive: false,
          legend: {
            display: false
          },
          tooltips: {
            callbacks: {
              label: function(tooltipItem) {
                return tooltipItem.yLabel;
              }
            }
          }
        }
      });
    }
  },
  mounted() {
    this.OpexChart();
    this.annexChart();
  }
};
</script>

<style>
.dropdown span {
  /* transform: rotate(90deg); */
  position: absolute;
  font-weight: bold;
  font-size: 17px;
  top: -1.5px;
  right: 4px;
}
[chart-holders] {
  margin-top: 16px;
}
.chart-details {
  top: 37%;
  text-align: center;
  right: 0;
  left: 0;
  margin: auto;
  font-family: SourceSansPro !important;
  font-size: 18px;
  /* font-weight: 600; */
  font-stretch: normal;
  font-style: normal;
  line-height: 1.11;
  letter-spacing: normal;
  color: #000000;
}

.chart-details p:nth-of-type(2) {
  font-family: SourceSansPro;
  font-size: 13px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.54;
  letter-spacing: normal;
  color: #000000;
}
[capex-price] {
  font-family: SourceSansPro;
  font-size: 18px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.11;
  letter-spacing: normal;
  color: #13244e;
}
[capex-details] {
  font-family: SourceSansPro;
  font-size: 16px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.25;
  letter-spacing: normal;
  color: #13244e;
}
[cappex-title] {
  font-family: SourceSansPro;
  font-size: 17px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.29;
  letter-spacing: normal;
  color: #13244e;
}
.dropdown {
  padding: 3px 20px 3px 10px;
  border-radius: 6px;
  background-color: rgba(77, 213, 153, 0.2);
  font-family: SourceSansPro;
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.43;
  letter-spacing: normal;
  color: #4dd599;
  position: relative;
}

[CAPPEX] {
  border-radius: 6px;
  box-shadow: 0 7px 64px 0 rgba(19, 36, 78, 0.07);
  background-color: #ffffff;
  padding: 8px 16px 16px;
  margin-bottom: 26px;
}

[CAPPEX] > div {
  padding-bottom: 6px;
  border-bottom: 1px;
  border-style: dashed;
  border-color: rgba(19, 36, 78, 0.07);
}
.price {
  padding: 7.6px 17px;
  border-radius: 6px;
  background-color: rgba(81, 44, 98, 0.2);
  font-family: SourceSansPro;
  font-size: 21px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.05;
  letter-spacing: normal;
  color: #512c62;
  margin-left: 20px;
}
.price.opex-price {
  border-radius: 6px;
  background-color: rgba(31, 171, 137, 0.2);
}
</style>
