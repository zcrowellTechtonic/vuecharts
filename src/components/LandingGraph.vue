<template>
  <div class="hello">
      <mdb-container-fluid>
        <mdb-col>
          <mdb-card>
            <mdb-card-header class="text-center">Monthly Breakdown</mdb-card-header>
            <mdb-card-body>
              <div style="display: block">
                <mdb-bar-chart :data="barChartData" :options="barChartOptions" :height="500"/>
              </div>
            </mdb-card-body>
          </mdb-card>
        </mdb-col>
      </mdb-container-fluid>
  </div>
</template>

<script>
import VueCircle from "vue2-circle-progress";
import {
  mdbContainer,
  mdbCol,
  mdbCard,
  mdbBarChart
} from "mdbvue";
export default {
  name: "App",
  components: {
    mdbContainer,
    mdbCol,
    mdbCard,
    mdbBarChart,
    VueCircle,
  },
  data() {
    return {
      // PROGRESS CIRCLE COLORS
      fill: { gradient: ["#7c8fad", "#416399", "#b1d4e0"] },
      collapse2: false,
      collapse3: false,
      showFrameModalTop: false,
      showFrameModalBottom: false,
      showSideModalTopRight: false,
      showSideModalTopLeft: false,
      showSideModalBottomRight: false,
      showSideModalBottomLeft: false,
      showCentralModalSmall: false,
      showCentralModalMedium: false,
      showCentralModalLarge: false,
      showCentralModalFluid: false,
      showFluidModalRight: false,
      showFluidModalLeft: false,
      showFluidModalTop: false,
      showFluidModalBottom: false,
      methods: {
        // PROGRESS CIRCLE FUNCTIONS
        progress(event, progress, stepValue) {
          console.log(stepValue);
        },
        progress_end(event) {
          console.log("Circle progress end");
        }
      },
      // START OF CHART OPTIONS
      barChartData: {
        labels: ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul"],
        datasets: [
          {
            label: "Low",
            data: [12, 39, 3, 50, 2, 32, 84],
            backgroundColor: "rgba(142, 226, 179, 0.5)",
            borderWidth: 1
          },
          {
            label: "Medium",
            data: [56, 24, 5, 16, 45, 24, 8],
            backgroundColor: "rgba(245, 192, 50, 0.5)",
            borderWidth: 1
          },
          {
            label: "High",
            data: [12, 25, 54, 3, 15, 44, 3],
            backgroundColor: "rgba(245, 74, 85, 0.5)",
            borderWidth: 1
          }
        ]
      },
      barChartOptions: {
        responsive: true,
        maintainAspectRatio: false,
        scales: {
          xAxes: [
            {
              barPercentage: 1,
              gridLines: {
                display: true,
                color: "rgba(0, 0, 0, 0.1)"
              }
            }
          ],
          yAxes: [
            {
              gridLines: {
                display: true,
                color: "rgba(0, 0, 0, 0.1)"
              },
              ticks: {
                beginAtZero: true
              }
            }
          ]
        }
      },
      pieChartData: {
        labels: ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul"],
        datasets: [
          {
            data: [300, 50, 100, 40, 120, 24, 52],
            backgroundColor: [
              "#F7464A",
              "#46BFBD",
              "#FDB45C",
              "#949FB1",
              "#4D5360",
              "#ac64ad"
            ],
            hoverBackgroundColor: [
              "#FF5A5E",
              "#5AD3D1",
              "#FFC870",
              "#A8B3C5",
              "#616774",
              "#da92db"
            ]
          }
        ]
      },
      pieChartOptions: {
        responsive: true,
        maintainAspectRatio: false
      },
      lineChartData: {
        labels: ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul"],
        datasets: [
          {
            label: "#1",
            backgroundColor: "rgba(245, 74, 85, 0.5)",
            data: [65, 59, 80, 81, 56, 55, 40]
          },
          {
            label: "#2",
            backgroundColor: "rgba(90, 173, 246, 0.5)",
            data: [12, 42, 121, 56, 24, 12, 2]
          },
          {
            label: "#3",
            backgroundColor: "rgba(245, 192, 50, 0.5)",
            data: [2, 123, 154, 76, 54, 23, 5]
          }
        ]
      },
      lineChartOptions: {
        responsive: true,
        maintainAspectRatio: false,
        scales: {
          xAxes: [
            {
              gridLines: {
                display: true,
                color: "rgba(0, 0, 0, 0.1)"
              }
            }
          ],
          yAxes: [
            {
              gridLines: {
                display: true,
                color: "rgba(0, 0, 0, 0.1)"
              }
            }
          ]
        }
      },
      radarChartData: {
        labels: ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul"],
        datasets: [
          {
            label: "#1",
            backgroundColor: "rgba(245, 74, 85, 0.5)",
            data: [65, 59, 80, 81, 56, 55, 40]
          },
          {
            label: "#2",
            backgroundColor: "rgba(90, 173, 246, 0.5)",
            data: [12, 42, 121, 56, 24, 12, 2]
          },
          {
            label: "#3",
            backgroundColor: "rgba(245, 192, 50, 0.5)",
            data: [2, 123, 154, 76, 54, 23, 5]
          }
        ]
      },
      radarChartOptions: {
        responsive: true,
        maintainAspectRatio: false
      },
      doughnutChartData: {
        labels: ["Red", "Green", "Yellow", "Grey", "Dark Grey"],
        datasets: [
          {
            data: [300, 50, 100, 40, 120],
            backgroundColor: [
              "#F7464A",
              "#46BFBD",
              "#FDB45C",
              "#949FB1",
              "#4D5360"
            ],
            hoverBackgroundColor: [
              "#FF5A5E",
              "#5AD3D1",
              "#FFC870",
              "#A8B3C5",
              "#616774"
            ]
          }
        ]
      },
      doughnutChartOptions: {
        responsive: true,
        maintainAspectRatio: false
      }
    };
  }
};
</script>

<style>
.carousel-control-next-icon,
.carousel-control-prev-icon {
  background-color: rgb(78, 78, 78);
  margin-top: 1.5em;
}

.footer-color {
  background-color: rgb(54, 95, 128);
  margin-top: 1.5em;
  color: rgb(214, 214, 214);
}

.footer-color > a {
  color: rgb(214, 214, 214);
}

.grid-container {
  background: #16222a; /* fallback for old browsers */
  background: -webkit-linear-gradient(to bottom, #3a6073, #16222a);
  background: linear-gradient(to bottom, #3a6073, #16222a);
  width: 85%;
  /* height: 125vh; */
  float: right;
}

@media (min-width: 1200px) {
  .navbar,
  .page-footer,
  main {
    padding-left: 270px;
  }
}

@media (max-width: 1199.98px) {
  .grid-container {
    width: 100vw;
  }
}
</style>
