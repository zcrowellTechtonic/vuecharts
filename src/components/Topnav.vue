<template>
  <div class="hello">
  <mdb-navbar expand="large" dark color="unique">
        <!-- NAVBAR BRAND. HOLDING ON TO THIS FOR LATER USE CASE -->
        <!-- <mdb-navbar-brand href="#">
        </mdb-navbar-brand>-->
        <!-- START OF TOP NAVBAR -->
        <mdb-navbar-toggler>
          <mdb-navbar-nav right>
            <mdb-dropdown tag="li" class="nav-item">
              <mdb-dropdown-toggle tag="a" navLink slot="toggle" waves-fixed>
                <mdb-icon fas icon="user"></mdb-icon>Profile
                <span class="caret"></span>
              </mdb-dropdown-toggle>
              <mdb-dropdown-menu>
                <mdb-dropdown-item>My Projects</mdb-dropdown-item>
                <mdb-dropdown-item>Help</mdb-dropdown-item>
                <mdb-dropdown-item>Logout</mdb-dropdown-item>
              </mdb-dropdown-menu>
            </mdb-dropdown>
            <mdb-nav-item href="#" waves-fixed>
              <mdb-icon fas icon="cog"></mdb-icon>Settings
            </mdb-nav-item>
          </mdb-navbar-nav>
        </mdb-navbar-toggler>
      </mdb-navbar>
  </div>

</template>

<script>

import {
  mdbNavbar,
  mdbNavbarBrand,
  mdbNavItem,
  mdbNavbarNav,
  mdbNavbarToggler,
  mdbIcon,
  mdbListGroup,
  mdbListGroupItem,
  mdbCardBody,
  mdbDropdownToggle,
  mdbDropdownMenu,
  mdbDropdownItem,
  mdbDropdown
} from "mdbvue";

export default {
  name: 'Topnav',
  components: {
    mdbNavbar,
    mdbNavbarBrand,
    mdbNavItem,
    mdbNavbarNav,
    mdbNavbarToggler,
    mdbListGroup,
    mdbListGroupItem,
    mdbIcon,
    mdbCardBody,
    mdbDropdown,
    mdbDropdownToggle,
    mdbDropdownMenu,
    mdbDropdownItem
  }
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
 
</style>
