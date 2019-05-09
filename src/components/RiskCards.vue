<template>
  <div class="hello">
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
                        <mdb-carousel showControls data-interval="false">
                          <mdb-carousel-item>
                            <p>
                              Risk Rating:
                              <mdb-btn
                                tag="a"
                                gradient="blue"
                                floating
                                size="sm"
                                class="text-white circle-icon"
                              >3</mdb-btn>
                            </p>
                            <h2 class="text-center">
                              <strong>10GA</strong>
                            </h2>
                          </mdb-carousel-item>
                          <mdb-carousel-item>
                            <p>
                              Project Completion:
                              <mdb-btn
                                tag="a"
                                gradient="blue"
                                floating
                                size="sm"
                                class="text-white circle-icon"
                              >3</mdb-btn>
                            </p>
                            <div class="d-flex justify-content-center">
                              <vue-circle
                                class
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
                                @vue-circle-end="progress_end"
                              ></vue-circle>
                            </div>
                          </mdb-carousel-item>
                          <mdb-carousel-item>
                            <p>
                              Budget Used:
                              <mdb-btn
                                tag="a"
                                gradient="blue"
                                floating
                                size="sm"
                                class="text-white circle-icon"
                              >3</mdb-btn>
                            </p>
                            <div class="d-flex justify-content-center">
                              <vue-circle
                                class
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
                                @vue-circle-end="progress_end"
                              ></vue-circle>
                            </div>
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
                            <p>
                              Risk Rating:
                              <mdb-btn
                                tag="a"
                                gradient="blue"
                                floating
                                size="sm"
                                class="text-white circle-icon"
                              >3</mdb-btn>
                            </p>
                            <h2 class="text-center">
                              <strong>9GA</strong>
                            </h2>
                          </mdb-carousel-item>
                          <mdb-carousel-item>
                            <p>
                              Project Completion:
                              <mdb-btn
                                tag="a"
                                gradient="blue"
                                floating
                                size="sm"
                                class="text-white circle-icon"
                              >3</mdb-btn>
                            </p>
                            <div class="d-flex justify-content-center">
                              <vue-circle
                                class
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
                                @vue-circle-end="progress_end"
                              ></vue-circle>
                            </div>
                          </mdb-carousel-item>
                          <mdb-carousel-item>
                            <p>
                              Budget Used:
                              <mdb-btn
                                tag="a"
                                gradient="blue"
                                floating
                                size="sm"
                                class="text-white circle-icon"
                              >3</mdb-btn>
                            </p>
                            <div class="d-flex justify-content-center">
                              <vue-circle
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
                                @vue-circle-end="progress_end"
                              ></vue-circle>
                            </div>
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
                            <p>
                              Risk Rating:
                              <mdb-btn
                                tag="a"
                                gradient="blue"
                                floating
                                size="sm"
                                class="text-white circle-icon"
                              >3</mdb-btn>
                            </p>
                            <h2 class="text-center">
                              <strong>8GA</strong>
                            </h2>
                          </mdb-carousel-item>
                          <mdb-carousel-item>
                            <p>
                              Project Completion:
                              <mdb-btn
                                tag="a"
                                gradient="blue"
                                floating
                                size="sm"
                                class="text-white circle-icon"
                              >3</mdb-btn>
                            </p>
                            <div class="d-flex justify-content-center">
                              <vue-circle
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
                                @vue-circle-end="progress_end"
                              ></vue-circle>
                            </div>
                          </mdb-carousel-item>
                          <mdb-carousel-item>
                            <p>
                              Budget Used:
                              <mdb-btn
                                tag="a"
                                gradient="blue"
                                floating
                                size="sm"
                                class="text-white circle-icon"
                              >3</mdb-btn>
                            </p>
                            <div class="d-flex justify-content-center">
                              <vue-circle
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
                                @vue-circle-end="progress_end"
                              ></vue-circle>
                            </div>
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
                          <p>
                            Risk Rating:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <h2 class="text-center">
                            <strong>12GA</strong>
                          </h2>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>
                            Project Completion:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <div class="d-flex justify-content-center">
                            <vue-circle
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
                              @vue-circle-end="progress_end"
                            ></vue-circle>
                          </div>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>
                            Budget Used:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <div class="d-flex justify-content-center">
                            <vue-circle
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
                              @vue-circle-end="progress_end"
                            ></vue-circle>
                          </div>
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
                          <p>
                            Risk Rating:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <h2 class="text-center">
                            <strong>16GA</strong>
                          </h2>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>
                            Project Completion:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <div class="d-flex justify-content-center">
                            <vue-circle
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
                              @vue-circle-end="progress_end"
                            ></vue-circle>
                          </div>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>
                            Budget Used:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <div class="d-flex justify-content-center">
                            <vue-circle
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
                              @vue-circle-end="progress_end"
                            ></vue-circle>
                          </div>
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
                          <p>
                            Risk Rating:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <h2 class="text-center">
                            <strong>21GA</strong>
                          </h2>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>
                            Project Completion:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <div class="d-flex justify-content-center">
                            <vue-circle
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
                              @vue-circle-end="progress_end"
                            ></vue-circle>
                          </div>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>
                            Budget Used:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <div class="d-flex justify-content-center">
                            <vue-circle
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
                              @vue-circle-end="progress_end"
                            ></vue-circle>
                          </div>
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
                          <p>
                            Risk Rating:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <h2 class="text-center">
                            <strong>23GA</strong>
                          </h2>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>
                            Project Completion:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <div class="d-flex justify-content-center">
                            <vue-circle
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
                              @vue-circle-end="progress_end"
                            ></vue-circle>
                          </div>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>
                            Budget Used:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <div class="d-flex justify-content-center">
                            <vue-circle
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
                              @vue-circle-end="progress_end"
                            ></vue-circle>
                          </div>
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
                          <p>
                            Risk Rating:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <h2 class="text-center">
                            <strong>32GA</strong>
                          </h2>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>
                            Project Completion:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <div class="d-flex justify-content-center">
                            <vue-circle
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
                              @vue-circle-end="progress_end"
                            ></vue-circle>
                          </div>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>
                            Budget Used:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <div class="d-flex justify-content-center">
                            <vue-circle
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
                              @vue-circle-end="progress_end"
                            ></vue-circle>
                          </div>
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
                          <p>
                            Risk Rating:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <h2 class="text-center">
                            <strong>47GA</strong>
                          </h2>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>
                            Project Completion:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <div class="d-flex justify-content-center">
                            <vue-circle
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
                              @vue-circle-end="progress_end"
                            ></vue-circle>
                          </div>
                        </mdb-carousel-item>
                        <mdb-carousel-item>
                          <p>
                            Budget Used:
                            <mdb-btn
                              tag="a"
                              gradient="blue"
                              floating
                              size="sm"
                              class="text-white circle-icon"
                            >3</mdb-btn>
                          </p>
                          <div class="d-flex justify-content-center">
                            <vue-circle
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
                              @vue-circle-end="progress_end"
                            ></vue-circle>
                          </div>
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
  </div>

</template>

<script>
import VueCircle from "vue2-circle-progress";
import {
  mdbContainer,
  mdbBtn,
  mdbIcon,
  mdbCardBody,
  mdbRow,
  mdbCol,
  mdbCard,
  mdbCardHeader,
  mdbCarousel,
  mdbCarouselItem,
} from "mdbvue";

export default {
  name: 'LowRiskCards',
  components: {
    mdbContainer,
    mdbBtn,
    mdbIcon,
    mdbCardBody,
    mdbRow,
    mdbCol,
    mdbCard,
    mdbCardHeader,
    mdbCarousel,
    mdbCarouselItem,
    VueCircle
  },  
  data(){
    return {
      // COlOR SELECTION FOR PROGRESS CIRCLES
      fill: { gradient: ["#7c8fad", "#416399", "#b1d4e0"] }
    };
  },
  methods: {
    // PROGRESS CIRCLE FUNCTIONS
    progress(event, progress, stepValue) {
      console.log(stepValue);
    },
    progress_end(event) {
      console.log("Circle progress end");
    }
  }
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
 .carousel-control-next-icon,
 .carousel-control-prev-icon {
  background-color: rgb(78, 78, 78);
  margin-top: 1.5em;
  }

.circle-icon {
  float: right;
  line-height: 1.25em;
}

.col-sm,
.col-sm-4,
.col-sm-8 {
  margin: 0.75em;
}
</style>
