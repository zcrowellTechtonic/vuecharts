<template>
  <div id="app">
    <div class="grid-container">
      <mdb-navbar expand="large" dark color="unique">
        <!-- Navbar brand -->
        <!-- <mdb-navbar-brand href="#">
        </mdb-navbar-brand>-->
        <mdb-navbar-toggler>
          <mdb-navbar-nav right>
            <mdb-dropdown tag="li" class="nav-item">
              <mdb-dropdown-toggle tag="a" navLink slot="toggle" waves-fixed>
                <mdb-icon fas icon="user"></mdb-icon>Profile
                <span class="caret"></span>
              </mdb-dropdown-toggle>
              <mdb-dropdown-menu>
                <mdb-dropdown-item>Choice One</mdb-dropdown-item>
                <mdb-dropdown-item>Choice Two</mdb-dropdown-item>
                <mdb-dropdown-item>Logout</mdb-dropdown-item>
              </mdb-dropdown-menu>
            </mdb-dropdown>
            <mdb-nav-item href="#" waves-fixed>
              <mdb-icon fas icon="cog"></mdb-icon>Settings
            </mdb-nav-item>
          </mdb-navbar-nav>
        </mdb-navbar-toggler>
      </mdb-navbar>

      <mdb-container-fluid>
        <mdb-row>
          <!-- START OF LOW RISK CARD -->
          <mdb-col col="sm">
            <mdb-card>
              <mdb-card-header class="text-center">Low Risk</mdb-card-header>
              <mdb-card-body>
                <!-- START OF ACCORDION -->
                <div role="tablist">
                  <mdb-card no-body class="mb-1">
                    <mdb-card-header header-tag="header" class="p-1" role="tab">
                      <mdb-btn block href="#" v-b-toggle.accordion-1 class="text-left" color="grey">
                        Beat Port
                        <mdb-icon fas class="circle-icon fa-lg green-text" icon="circle"></mdb-icon>
                      </mdb-btn>
                    </mdb-card-header>
                    <b-collapse id="accordion-1" accordion="my-accordion" role="tabpanel">
                      <mdb-card-body>
                        
                        <mdb-carousel showControls>
                        <mdb-carousel-item>
                          <p>Risk Rating: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <h2 class="text-center"><strong class="text-muted">10GA</strong></h2>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Project Completion: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                                <vue-circle class="progress-circle"
                                :progress="87"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Budget Used: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <vue-circle class="progress-circle"
                                :progress="43"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                       </mdb-carousel>
                      </mdb-card-body>
                    </b-collapse>
                  </mdb-card>

                  <mdb-card no-body class="mb-1">
                    <b-card-header header-tag="header" class="p-1" role="tab">
                      <mdb-btn block href="#" v-b-toggle.accordion-2 class="text-left" color="grey">
                        Sphero
                        <mdb-icon fas class="circle-icon fa-lg green-text" icon="circle"></mdb-icon>
                      </mdb-btn>
                    </b-card-header>
                    <b-collapse id="accordion-2" accordion="my-accordion" role="tabpanel">
                      <mdb-card-body>
                        
                        <mdb-carousel showControls>
                        <mdb-carousel-item>
                          <p>Risk Rating: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <h2 class="text-center"><strong class="text-muted">10GA</strong></h2>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Project Completion: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                                <vue-circle class="progress-circle"
                                :progress="87"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Budget Used: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <vue-circle class="progress-circle"
                                :progress="43"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                       </mdb-carousel>
                      </mdb-card-body>
                    </b-collapse>
                  </mdb-card>

                  <mdb-card no-body class="mb-1">
                    <b-card-header header-tag="header" class="p-1" role="tab">
                      <mdb-btn block href="#" v-b-toggle.accordion-3 class="text-left" color="grey">
                        CSA
                        <mdb-icon fas class="circle-icon fa-lg green-text" icon="circle"></mdb-icon>
                      </mdb-btn>
                    </b-card-header>
                    <b-collapse id="accordion-3" accordion="my-accordion" role="tabpanel">
                       <mdb-card-body>
                        
                        <mdb-carousel showControls>
                        <mdb-carousel-item>
                          <p>Risk Rating: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <h2 class="text-center"><strong class="text-muted">10GA</strong></h2>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Project Completion: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                                <vue-circle class="progress-circle"
                                :progress="87"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Budget Used: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <vue-circle class="progress-circle"
                                :progress="43"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                       </mdb-carousel>
                      </mdb-card-body>
                    </b-collapse>
                  </mdb-card>
                </div>
                <!-- END OF FIRST ACCORDION -->
              </mdb-card-body>
            </mdb-card>
          </mdb-col>
          <!-- END OF LOW RISK CARD -->

          <!-- START OF MEDIUM RISK CARD -->
          <mdb-col col="sm">
            <mdb-card>
              <mdb-card-header class="text-center">Medium Risk</mdb-card-header>
              <mdb-card-body>
                <!-- START OF MIDDLE ACCORDION -->
                <mdb-card no-body class="mb-1">
                  <b-card-header header-tag="header" class="p-1" role="tab">
                    <mdb-btn block href="#" v-b-toggle.accordion-4 class="text-left" color="grey">
                      MD Estimator
                      <mdb-icon fas class="circle-icon fa-lg amber-text" icon="circle"></mdb-icon>
                    </mdb-btn>
                  </b-card-header>
                  <b-collapse id="accordion-4" accordion="my-accordion" role="tabpanel">
                     <mdb-card-body>
                        
                        <mdb-carousel showControls>
                        <mdb-carousel-item>
                          <p>Risk Rating: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <h2 class="text-center"><strong class="text-muted">10GA</strong></h2>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Project Completion: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                                <vue-circle class="progress-circle"
                                :progress="87"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Budget Used: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <vue-circle class="progress-circle"
                                :progress="43"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                       </mdb-carousel>
                      </mdb-card-body>
                  </b-collapse>
                </mdb-card>
                <mdb-card no-body class="mb-1">
                  <b-card-header header-tag="header" class="p-1" role="tab">
                    <mdb-btn block href="#" v-b-toggle.accordion-5 class="text-left" color="grey">
                      Kiosk
                      <mdb-icon fas class="circle-icon fa-lg amber-text" icon="circle"></mdb-icon>
                    </mdb-btn>
                  </b-card-header>
                  <b-collapse id="accordion-5" accordion="my-accordion" role="tabpanel">
                     <mdb-card-body>
                        
                        <mdb-carousel showControls>
                        <mdb-carousel-item>
                          <p>Risk Rating: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <h2 class="text-center"><strong class="text-muted">10GA</strong></h2>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Project Completion: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                                <vue-circle class="progress-circle"
                                :progress="87"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Budget Used: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <vue-circle class="progress-circle"
                                :progress="43"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                       </mdb-carousel>
                      </mdb-card-body>
                  </b-collapse>
                </mdb-card>
                <!-- END OF MIDDLE ACCORDION -->
              </mdb-card-body>
            </mdb-card>
          </mdb-col>
          <!-- END OF MEDIUM RISK CARD -->

          <!-- START OF HIGH RISK CARD -->
          <mdb-col col="sm">
            <mdb-card>
              <mdb-card-header class="text-center">High Risk</mdb-card-header>
              <mdb-card-body>
                <!-- START OF LAST ACCORDION -->
                <mdb-card no-body class="mb-1">
                  <b-card-header header-tag="header" class="p-1" role="tab">
                    <mdb-btn block href="#" v-b-toggle.accordion-7 class="text-left" color="grey">
                      Brighter Vision
                      <mdb-icon fas class="circle-icon fa-lg red-text" icon="circle"></mdb-icon>
                    </mdb-btn>
                  </b-card-header>
                  <b-collapse id="accordion-7" accordion="my-accordion" role="tabpanel">
                     <mdb-card-body>
                        
                        <mdb-carousel showControls>
                        <mdb-carousel-item>
                          <p>Risk Rating: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <h2 class="text-center"><strong class="text-muted">10GA</strong></h2>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Project Completion: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                                <vue-circle class="progress-circle"
                                :progress="87"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Budget Used: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <vue-circle class="progress-circle"
                                :progress="43"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                       </mdb-carousel>
                      </mdb-card-body>
                  </b-collapse>
                </mdb-card>
                <mdb-card no-body class="mb-1">
                  <b-card-header header-tag="header" class="p-1" role="tab">
                    <mdb-btn block href="#" v-b-toggle.accordion-8 class="text-left" color="grey">
                      HVA
                      <mdb-icon fas class="circle-icon fa-lg red-text" icon="circle"></mdb-icon>
                    </mdb-btn>
                  </b-card-header>
                  <b-collapse id="accordion-8" accordion="my-accordion" role="tabpanel">
                     <mdb-card-body>
                        
                        <mdb-carousel showControls>
                        <mdb-carousel-item>
                          <p>Risk Rating: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <h2 class="text-center"><strong class="text-muted">10GA</strong></h2>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Project Completion: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                                <vue-circle class="progress-circle"
                                :progress="87"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Budget Used: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <vue-circle class="progress-circle"
                                :progress="43"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                       </mdb-carousel>
                      </mdb-card-body>
                  </b-collapse>
                </mdb-card>
                <mdb-card no-body class="mb-1">
                  <b-card-header header-tag="header" class="p-1" role="tab">
                    <mdb-btn block href="#" v-b-toggle.accordion-9 class="text-left" color="grey">
                      Portal
                      <mdb-icon fas class="circle-icon fa-lg red-text" icon="circle"></mdb-icon>
                    </mdb-btn>
                  </b-card-header>
                  <b-collapse id="accordion-9" accordion="my-accordion" role="tabpanel">
                     <mdb-card-body>
                        
                        <mdb-carousel showControls>
                        <mdb-carousel-item>
                          <p>Risk Rating: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <h2 class="text-center"><strong class="text-muted">10GA</strong></h2>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Project Completion: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                                <vue-circle class="progress-circle"
                                :progress="87"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Budget Used: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <vue-circle class="progress-circle"
                                :progress="43"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                       </mdb-carousel>
                      </mdb-card-body>
                  </b-collapse>
                </mdb-card>
                <mdb-card no-body class="mb-1">
                  <b-card-header header-tag="header" class="p-1" role="tab">
                    <mdb-btn block href="#" v-b-toggle.accordion-10 class="text-left" color="grey">
                      CU
                      <mdb-icon fas class="circle-icon fa-lg red-text" icon="circle"></mdb-icon>
                    </mdb-btn>
                  </b-card-header>
                  <b-collapse id="accordion-10" accordion="my-accordion" role="tabpanel">
                     <mdb-card-body>
                        
                        <mdb-carousel showControls>
                        <mdb-carousel-item>
                          <p>Risk Rating: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <h2 class="text-center"><strong class="text-muted">10GA</strong></h2>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Project Completion: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                                <vue-circle class="progress-circle"
                                :progress="87"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>Budget Used: <mdb-btn tag="a" gradient="blue" floating size="sm" class="text-white circle-icon">3</mdb-btn></p>
                          <vue-circle class="progress-circle"
                                :progress="43"
                                :size="100"
                                :reverse="false"
                                line-cap="round"
                                :fill="fill"
                                empty-fill="rgba(0, 0, 0, .1)"
                                :animation-start-value="0.0"
                                :start-angle="0"
                                insert-mode="append"
                                :thickness="10"
                                :show-percent="true"
                                @vue-circle-progress="progress"
                                @vue-circle-end="progress_end">
                              </vue-circle>
                        </mdb-carousel-item>
                       </mdb-carousel>
                      </mdb-card-body>
                  </b-collapse>
                </mdb-card>
                <!-- END OF LAST ACCORDION -->
              </mdb-card-body>
            </mdb-card>
          </mdb-col>
          <!-- END OF HIGH RISK CARDS -->
        </mdb-row>
      </mdb-container-fluid>
      <!-- END OF RISK CARDS -->
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
        &copy; 2018 Copyright:
        <a href="#">Dogs.com</a>
      </div>
      <!-- Footer -->
    </div>

    <div class="sidebar-fixed position-fixed">
      <a class="logo-wrapper">
        <img alt class="img-fluid" src>
      </a>
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
        <router-link to="/reports" @click.native="activeItem = 3">
          <mdb-list-group-item :action="true" :class="activeItem === 3 && 'active'">
            Reports
            <mdb-icon icon="print" class="text-right"/>
          </mdb-list-group-item>
        </router-link>
        <router-link to="/accountinfo" @click.native="activeItem = 3">
          <mdb-list-group-item :action="true" :class="activeItem === 3 && 'active'">
            Account Info
            <mdb-icon icon="briefcase" class="text-right"/>
          </mdb-list-group-item>
        </router-link>
      </mdb-list-group>
    </div>
  </div>
</template>

<script>
import VueCircle from 'vue2-circle-progress';
import {
  mdbContainer,
  mdbNavbar,
  mdbNavbarBrand,
  mdbNavItem,
  mdbNavbarNav,
  mdbNavbarToggler,
  mdbBtn,
  mdbIcon,
  mdbListGroup,
  mdbListGroupItem,
  mdbCardBody,
  mdbDropdownToggle,
  mdbDropdownMenu,
  mdbDropdownItem,
  mdbDropdown,
  mdbRow,
  mdbCol,
  mdbCard,
  mdbCardHeader,
  mdbBarChart,
  mdbPieChart,
  mdbLineChart,
  mdbRadarChart,
  mdbDoughnutChart,
  mdbFooter,
  mdbCarousel,
  mdbCarouselItem
} from "mdbvue";
// import Dashboard from './components/Dashboard';
export default {
  name: "App",
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
    mdbDoughnutChart,
    mdbCarousel,
    mdbCarouselItem,
    VueCircle
  },
  data() {
    return {
      // PROGRESS CIRCLE COLORS
      fill : { gradient: ["#7c8fad", "#416399", "#b1d4e0"] },
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
        progress(event,progress,stepValue){
          console.log(stepValue);
        },
        progress_end(event){
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
.circle-icon {
  float: right;
  line-height: 1.25em;
}

.progress-circle {
  margin-left: 4em;
}

.col-sm,
.col-sm-4,
.col-sm-8 {
  margin: 0.75em;
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

@media (min-width: 1200px) {
  .navbar,
  .page-footer,
  main {
    padding-left: 270px;
  }
}

@media (max-width: 1199.98px) {
  .sidebar-fixed {
    display: none;
  }
}

@media (max-width: 1199.98px) {
  .grid-container {
    width: 100vw;
  }
}
</style>
