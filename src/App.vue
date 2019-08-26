<template>
  <div id="app">
    <navbar></navbar>
    <br>  
    <br>
  
    <br />
    <br />
    <customer></customer>
    <work></work>
    <skills></skills>
    <about></about>
    <whatDo></whatDo>
    <project></project>
    <br />
    <br />
    <br />
    <bottom></bottom>
    
    <!-- <div id="logo">
      <img alt="Vue logo" src="./assets/logo.png" />
      <HelloWorld msg="Welcome to Your Vue.js App"/>

      <helloTest v-if="view == 1"></helloTest>

      <p>{{dataTest.title}}</p>

      <p v-if="view == 2">
        <customer></customer>
      </p>

      <button v-on:click="btnOpenPage2">Submit</button>
      <button v-on:click="btnAxios">btnAxios</button>
    </div>-->
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import helloTest from "./components/helloTest.vue";
import customer from "./components/customer.vue";

import navbar from "./components/navbar.vue";
import about from "./components/about.vue";
import skills from "./components/skills.vue";
import work from "./components/work.vue";
import bottom from "./components/bottom.vue";
import whatDo from "./components/whatDo.vue";
import project from "./components/project.vue";

import AOS from 'aos';

export default {
  name: "app",
  components: {
    HelloWorld,
    helloTest,
    customer,
    navbar,
    about,
    skills,
    work,
    bottom,
    whatDo,
    project
  },
  mounted: function() {
    console.log("mou");
    // this.btnAxios();
  },
  created(){
  AOS.init({
    duration:1500,
  })
  },
  data: function() {
    return {
      count: 0,
      view: 0,
      dataTest: []
    };
  }, //data

  methods: {
    btnOpenPage2() {
      this.view = 2;
      console.log("Test");
    },

    btnAxios() {
      axios
        .get("https://jsonplaceholder.typicode.com/todos/1")
        .then(result2 => {
          console.log(result2);
          this.dataTest = result2.data;
        })
        .catch(function(error) {
          console.log(error);
        });
    },

    w3_open:function () {
      if (mySidebar.style.display === "block") {
        mySidebar.style.display = "none";
      } else {
        mySidebar.style.display = "block";
      } 
    }, //w3_open
    w3_close:function(){
      mySidebar.style.display = "none";
    } //w3_close
  } //methods
}; //export default
</script>
<style>
@import url("https://fonts.googleapis.com/css?family=Lexend+Deca&display=swap");

@import url("https://fonts.googleapis.com/css?family=Mitr&display=swap");

#app {
  font-family: "Lexend Deca", sans-serif;

  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

#logo {
  text-align: center;
}

.nav-item {
  font-family: "Mitr", sans-serif;
  font-weight: 400;
}

h1 {
  font-family: "Mitr", sans-serif;
}
h2 {
  font-family: "Mitr", sans-serif;
}
h5 {
  font-family: "Mitr", sans-serif;
}
h6 {
  font-family: "Mitr", sans-serif;
}


.b {
  font-family: "Mitr", sans-serif;
}
</style>
