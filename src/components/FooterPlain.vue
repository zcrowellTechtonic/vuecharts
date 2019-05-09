<template>
  <div class="hello">
  <div class="footer-copyright text-center py-3 footer-color" color="unique">
        &copy; 2019 Copyright:
        <a href="#">Handle.com</a>
      </div>
  </div>

</template>

<script>
export default {
  name: 'FooterPlain',
  components: {
    
  }
};

</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
 .footer-color {
  background-color: rgb(54, 95, 128);
  margin-top: 1.5em;
  color: rgb(214, 214, 214);
}

.footer-color > a {
  color: rgb(214, 214, 214);
}
</style>
