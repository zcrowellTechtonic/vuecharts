<template>
  <mdb-container class="mt-5">
    <mdb-row class="mt-5 align-items-center justify-content-start">
      <h4 class="demo-title"><strong>Tooltips</strong></h4>
      <a href="https://mdbootstrap.com/docs/vue/advanced/tooltips/?utm_source=DemoApp&utm_medium=MDBVueFree" waves-fixed class="border grey-text px-2 border-light rounded ml-2" target="_blank"><mdb-icon icon="graduation-cap" class="mr-2"/>Docs</a>
    </mdb-row>
    <hr />
    <div class="mt-5 pt-5 d-flex justify-content-center">
      <mdb-tooltip trigger="hover" :options="{placement: 'top'}">
        <span slot="tip">
          Who's there?
        </span>
        <mdb-btn slot="reference" color="primary">
          Knock Knock
        </mdb-btn>
      </mdb-tooltip>
    </div>
  </mdb-container>
</template>

<script>
import { mdbTooltip, mdbContainer, mdbBtn, mdbIcon, mdbRow } from 'mdbvue';

export default {
  name: 'TooltipPage',
  components: {
    mdbTooltip,
    mdbContainer,
    mdbBtn,
    mdbIcon,
    mdbRow
  },
};
</script>
