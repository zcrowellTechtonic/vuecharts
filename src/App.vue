<template>
  <div id="app">
    <div class="grid-container">
     <mdb-navbar expand="large" dark color="unique">
    <!-- Navbar brand -->
    <!-- <mdb-navbar-brand href="#">
    </mdb-navbar-brand> -->
    <mdb-navbar-toggler>
        <mdb-navbar-nav right>
            <mdb-nav-item href="#" waves-fixed><mdb-icon fas icon="cog"></mdb-icon> Settings</mdb-nav-item>
            <mdb-dropdown tag="li" class="nav-item">
               <mdb-dropdown-toggle tag="a" navLink slot="toggle" waves-fixed><mdb-icon fas icon="user"></mdb-icon> Profile<span class="caret"></span></mdb-dropdown-toggle>
              <mdb-dropdown-menu>
                <mdb-dropdown-item>Account</mdb-dropdown-item>
                <mdb-dropdown-item>Another action</mdb-dropdown-item>
                <mdb-dropdown-item>Something else here</mdb-dropdown-item>
              </mdb-dropdown-menu>
            </mdb-dropdown>
        </mdb-navbar-nav>
    </mdb-navbar-toggler>
  </mdb-navbar>

   <mdb-container-fluid>
    <mdb-row>
      <mdb-col col="sm">  
        <mdb-card>
          <mdb-card-header class="text-center">Low Risk</mdb-card-header>
            <mdb-card-body>
              Stats on stats
            </mdb-card-body>
        </mdb-card>
      </mdb-col>
      <mdb-col col="sm">
         <mdb-card>
          <mdb-card-header class="text-center">Medium Risk</mdb-card-header>
            <mdb-card-body>
              Stats on stats
            </mdb-card-body>
        </mdb-card>
      </mdb-col>
      <mdb-col col="sm">
         <mdb-card>
          <mdb-card-header class="text-center">High Risk</mdb-card-header>
            <mdb-card-body>
              Stats on stats
            </mdb-card-body>
        </mdb-card>
      </mdb-col>
    </mdb-row>
  </mdb-container-fluid>

  <mdb-container-fluid>
        <mdb-col>
              <mdb-card>
                <mdb-card-header class="text-center">Weekly Breakdown</mdb-card-header>
                  <mdb-card-body>
                      <div style="display: block">
                        <mdb-bar-chart :data="barChartData" :options="barChartOptions" :height="500"/>
                      </div>
                  </mdb-card-body>
              </mdb-card>
          </mdb-col>
  </mdb-container-fluid>
   <!-- Footer -->
    <div class="footer-copyright text-center py-3 footer-color" color="unique">
        &copy; 2018 Copyright: <a href="#"> Dogs.com </a>
    </div>
  <!-- Footer -->

</div>

  <div class="sidebar-fixed position-fixed">
      <a class="logo-wrapper"><img alt="" class="img-fluid" src=""/></a>
      <mdb-list-group class="list-group-flush">
        <router-link to="/dashboard" @click.native="activeItem = 1">
          <mdb-list-group-item :action="true" :class="activeItem === 1 && 'active'"><mdb-icon icon="chart-line" class="mr-3"/>Risk Dashboard</mdb-list-group-item>
        </router-link>
        <router-link to="/projects" @click.native="activeItem = 2">
          <mdb-list-group-item :action="true" :class="activeItem === 2 && 'active'"><mdb-icon icon="hammer" class="mr-3"/>Projects</mdb-list-group-item>
        </router-link>
        <router-link to="/reports"  @click.native="activeItem = 3">
          <mdb-list-group-item :action="true" :class="activeItem === 3 && 'active'"><mdb-icon icon="print" class="mr-3"/>Reports</mdb-list-group-item>
        </router-link>
        <router-link to="/accountinfo"  @click.native="activeItem = 3">
          <mdb-list-group-item :action="true" :class="activeItem === 3 && 'active'"><mdb-icon icon="briefcase" class="mr-3"/>Account Info</mdb-list-group-item>
        </router-link>
      </mdb-list-group>
    </div>
  </div>

  

</template>

<script>
  import {  mdbContainer, mdbNavbar, mdbNavbarBrand, mdbNavItem, mdbNavbarNav, mdbNavbarToggler, mdbBtn, mdbIcon, mdbListGroup, mdbListGroupItem, mdbCardBody, mdbDropdownToggle, mdbDropdownMenu, mdbDropdownItem, mdbDropdown, mdbRow, mdbCol, mdbCard, mdbCardHeader, mdbBarChart, mdbPieChart, mdbLineChart, mdbRadarChart, mdbDoughnutChart, mdbFooter} from 'mdbvue';
  // import Dashboard from './components/Dashboard';
  export default {
    name: 'App',
    components: {
      mdbContainer,
      mdbNavbar,
      mdbNavbarBrand,
      mdbNavItem,
      mdbNavbarNav,
      mdbNavbarToggler,
      mdbBtn,
      mdbListGroup,
      mdbListGroupItem,
      mdbIcon,
      mdbCardBody,
      mdbDropdown,
      mdbDropdownToggle,
      mdbDropdownMenu,
      mdbDropdownItem,
      mdbRow,
      mdbCol,
      mdbCard,
      mdbCardHeader,
      mdbFooter,
      mdbBarChart,
      mdbPieChart,
      mdbLineChart,
      mdbRadarChart,
      mdbDoughnutChart
    },
    data () {
      return {
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
        barChartData: {
          labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul'],
          datasets: [
            {
              label: '#1',
              data: [12, 39, 3, 50, 2, 32, 84],
              backgroundColor: 'rgba(245, 74, 85, 0.5)',
              borderWidth: 1
            }, {
              label: '#2',
              data: [56, 24, 5, 16, 45, 24, 8],
              backgroundColor: 'rgba(90, 173, 246, 0.5)',
              borderWidth: 1
            }, {
              label: '#3',
              data: [12, 25, 54, 3, 15, 44, 3],
              backgroundColor: 'rgba(245, 192, 50, 0.5)',
              borderWidth: 1
            }
          ]
        },
        barChartOptions: {
          responsive: true,
          maintainAspectRatio: false,
          scales: {
            xAxes: [{
              barPercentage: 1,
              gridLines: {
                display: true,
                color: 'rgba(0, 0, 0, 0.1)'
              }
            }],
            yAxes: [{
              gridLines: {
                display: true,
                color: 'rgba(0, 0, 0, 0.1)'
              },
              ticks: {
                beginAtZero: true
              }
            }]
          }
        },
        pieChartData: {
          labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul'],
          datasets: [
            {
              data: [300, 50, 100, 40, 120, 24, 52],
              backgroundColor: ['#F7464A', '#46BFBD', '#FDB45C', '#949FB1', '#4D5360', '#ac64ad'],
              hoverBackgroundColor: ['#FF5A5E', '#5AD3D1', '#FFC870', '#A8B3C5', '#616774', '#da92db']
            }
          ]
        },
        pieChartOptions: {
          responsive: true,
          maintainAspectRatio: false
        },
        lineChartData: {
          labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul'],
          datasets: [
            {
              label: '#1',
              backgroundColor: 'rgba(245, 74, 85, 0.5)',
              data: [65, 59, 80, 81, 56, 55, 40]
            },
            {
              label: '#2',
              backgroundColor: 'rgba(90, 173, 246, 0.5)',
              data: [12, 42, 121, 56, 24, 12, 2]
            },
            {
              label: '#3',
              backgroundColor: 'rgba(245, 192, 50, 0.5)',
              data: [2, 123, 154, 76, 54, 23, 5]
            }
          ]
        },
        lineChartOptions: {
          responsive: true,
          maintainAspectRatio: false,
          scales: {
            xAxes: [{
              gridLines: {
                display: true,
                color: 'rgba(0, 0, 0, 0.1)'
              }
            }],
            yAxes: [{
              gridLines: {
                display: true,
                color: 'rgba(0, 0, 0, 0.1)'
              }
            }]
          }
        },
        radarChartData: {
          labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul'],
          datasets: [
            {
              label: '#1',
              backgroundColor: 'rgba(245, 74, 85, 0.5)',
              data: [65, 59, 80, 81, 56, 55, 40]
            },
            {
              label: '#2',
              backgroundColor: 'rgba(90, 173, 246, 0.5)',
              data: [12, 42, 121, 56, 24, 12, 2]
            },
            {
              label: '#3',
              backgroundColor: 'rgba(245, 192, 50, 0.5)',
              data: [2, 123, 154, 76, 54, 23, 5]
            }
          ]
        },
        radarChartOptions: {
          responsive: true,
          maintainAspectRatio: false
        },
        doughnutChartData: {
          labels: ['Red', 'Green', 'Yellow', 'Grey', 'Dark Grey'],
          datasets: [
            {
              data: [300, 50, 100, 40, 120],
              backgroundColor: ['#F7464A', '#46BFBD', '#FDB45C', '#949FB1', '#4D5360'],
              hoverBackgroundColor: ['#FF5A5E', '#5AD3D1', '#FFC870', '#A8B3C5', '#616774']
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

.col-sm, .col-sm-4, .col-sm-8 {
    margin: .75em;

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
    background: #16222A;  /* fallback for old browsers */
    background: -webkit-linear-gradient(to bottom, #3A6073, #16222A);
    background: linear-gradient(to bottom, #3A6073, #16222A);
    width: 85%;
    /* height: 125vh; */
    float: right;
}

.sidebar-fixed {
    position: absolute;
    height: 110vh;
    width: 15%;
    -webkit-box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);
    box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);
    z-index: 5;
    background-color: #fff;
    padding: 1.5rem;
    /* padding-top: 0;  */
                }

    .sidebar-fixed .list-group .active {
      -webkit-box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);
      box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);
      -webkit-border-radius: 5px;
      border-radius: 5px; 
                                        }

    .sidebar-fixed .logo-wrapper {
      padding: 2.5rem; }
      .sidebar-fixed .logo-wrapper img {
        max-height: 50px; }
  
  @media (min-width: 1200px) {
    .navbar,
    .page-footer,
    main {
      padding-left: 270px; } }
  
  @media (max-width: 1199.98px) {
    .sidebar-fixed {
      display: none; } }

  @media (max-width: 1199.98px) {
    .grid-container {
      width: 100vw; } }

</style>
