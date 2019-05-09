<template>
  <div class="hello">
    <!-- START OF SIDEBAR NAV -->
    <div id="sidenav" class="sidebar-fixed position-fixed">
      <div class="d-flex justify-content-center">
        <a>
          <img alt class="sidenavlogo" src="../assets/logo_transparent.png">
        </a>
      </div>
      <mdb-list-group class="list-group-flush">
        <!-- <router-link to="/dashboard" @click.native="activeItem = 1"> -->
        <mdb-list-group-item :action="true" :class="activeItem === 1 && 'active'">
          Risk Dashboard
          <mdb-icon icon="chart-line" class="text-right"/>
        </mdb-list-group-item>
        <!-- </router-link> -->
        <!-- <router-link to="/projects" @click.native="activeItem = 2"> -->
        <mdb-list-group-item :action="true" :class="activeItem === 2 && 'active'">
          Projects
          <mdb-icon icon="hammer" class="text-right"/>
        </mdb-list-group-item>
        <!-- </router-link> -->
        <!-- <router-link to="/reports" @click.native="activeItem = 3"> -->
        <mdb-list-group-item :action="true" :class="activeItem === 3 && 'active'">
          Reports
          <mdb-icon icon="print" class="text-right"/>
        </mdb-list-group-item>
        <!-- </router-link> -->
        <!-- <router-link to="/accountinfo" @click.native="activeItem = 3"> -->
        <mdb-list-group-item :action="true" :class="activeItem === 3 && 'active'">
          Account Info
          <mdb-icon icon="briefcase" class="text-right"/>
        </mdb-list-group-item>
        <!-- </router-link> -->
      </mdb-list-group>
    </div>
    <!-- END OF SIDEBAR NAV -->
  </div>
</template>

<script>
import { mdbIcon, mdbListGroup, mdbListGroupItem } from "mdbvue";

export default {
  name: "Sidenav",
  components: {
    mdbListGroup,
    mdbListGroupItem,
    mdbIcon
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.sidenavlogo {
  width: 9em;
}

#sidenav {
  /* CAN BE USED TO COLOR SIDENAV LATER */
}

.sidebar-fixed {
  position: absolute;
  height: 110vh;
  width: 15%;
  -webkit-box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16),
    0 2px 10px 0 rgba(0, 0, 0, 0.12);
  box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);
  z-index: 5;
  background-color: #fff;
  padding: 1.5rem;
  /* padding-top: 0;  */
}

.sidebar-fixed .list-group .active {
  -webkit-box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16),
    0 2px 10px 0 rgba(0, 0, 0, 0.12);
  box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);
  -webkit-border-radius: 5px;
  border-radius: 5px;
}

.sidebar-fixed .logo-wrapper {
  padding: 2.5rem;
}
.sidebar-fixed .logo-wrapper img {
  max-height: 50px;
}

@media (max-width: 1199.98px) {
  .sidebar-fixed {
    display: none;
  }
}
</style>
