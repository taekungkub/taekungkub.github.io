<template>
<div>
  
  <div class="w3-top">
  <div class="w3-bar w3-white w3-card" id="myNavbar">
    <a href="#home" class="w3-bar-item w3-button w3-wide">LOGO</a>
    <!-- Right-sided navbar links -->
    <div class="w3-right w3-hide-small">
      <a href="#about" class="w3-bar-item w3-button">ABOUT</a>
      <a href="#team" class="w3-bar-item w3-button"><i class="fa fa-user"></i> TEAM</a>
      <a href="#work" class="w3-bar-item w3-button"><i class="fa fa-th"></i> WORK</a>
      <a href="#pricing" class="w3-bar-item w3-button"><i class="fa fa-usd"></i> PRICING</a>
      <a href="#contact" class="w3-bar-item w3-button"><i class="fa fa-envelope"></i> CONTACT</a>
    </div>
    <!-- Hide right-floated links on small screens and replace them with a menu icon -->

    <a href="javascript:void(0)" class="w3-bar-item w3-button w3-right w3-hide-large w3-hide-medium" v-on:click="w3_open">
      <i class="fa fa-bars"></i>
    </a>
  </div>
</div>

<!-- Sidebar on small screens when clicking the menu icon -->
<nav class="w3-sidebar w3-bar-block w3-black w3-card w3-animate-left w3-hide-medium w3-hide-large" style="display:none" id="mySidebar">
  <a href="javascript:void(0)" v-on:click="w3_close" class="w3-bar-item w3-button w3-large w3-padding-16">Close ×</a>
  <a href="#about" v-on:click="w3_close" class="w3-bar-item w3-button">ABOUT</a>
  <a href="#team" v-on:click="w3_close" class="w3-bar-item w3-button">TEAM</a>
  <a href="#work" v-on:click="w3_close" class="w3-bar-item w3-button">WORK</a>
  <a href="#pricing" v-on:click="w3_close" class="w3-bar-item w3-button">PRICING</a>
  <a href="#contact" v-on:click="w3_close" class="w3-bar-item w3-button">CONTACT</a>
</nav>


    </div>
</template>
<script>
export default {
  data: function() {
    return {
      count: 0,
      view: 0
    };
  }, //data
  methods: {
    w3_open: function() {
      if (mySidebar.style.display === "block") {
        mySidebar.style.display = "none";
      } else {
        mySidebar.style.display = "block";
      }
    }, //w3_open
    w3_close: function() {
      mySidebar.style.display = "none";
    }
  } //methods
};
</script>

<style>
    .w3-bar  {
  padding: 10px;
}
</style>