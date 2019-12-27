<template>
  <div id="app">
    <!-- <navbar></navbar> -->
    <navbar2></navbar2>
    <br>  
    <br>

  <div class="container" v-for="friend,i in friends">

    <div v-if="editFriend === friend.id">
         <li class="list-group-item"><input class="w3-input w3-border w3-round" type="text" style="width:20%" v-model="friend.name" v-on:keyup.13="updateFriend(friend)"> <input class="w3-input w3-border w3-round" type="text" style="width:20%" v-model="friend.email" v-on:keyup.13="updateFriend(friend)"><button class="w3-button button round w3-small  w3-green" v-on:click="updateFriend(friend)">Save</button></li>
    </div>

    <div v-else>
         <li class="list-group-item">{{friend.id}} : {{friend.name}}  {{friend.email}}   <button class="w3-button button round w3-small w3-red" v-on:click="deleteFriend(friend.id,i)">Delete</button><button class="w3-button button round w3-small w3-teal" v-on:click="editFriend = friend.id">Edit</button></li>
    </div>
  </div>
  <div></div>
  
    <br />
    <br />
    <customer></customer>
    <work></work>
    <skills></skills>
    <about></about>
    <whatDo></whatDo>
    <project></project>
    <br>
    <br>
    <bulma></bulma>
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
import navbar2 from "./components/navbar2.vue";
import about from "./components/about.vue";
import skills from "./components/skills.vue";
import work from "./components/work.vue";
import bottom from "./components/bottom.vue";
import whatDo from "./components/whatDo.vue";
import project from "./components/project.vue";
import bulma from "./components/bulma.vue";

import AOS from 'aos';
import 'bulma/css/bulma.css';

export default {
  name: "app",
  components: {
    HelloWorld,
    helloTest,
    customer,
    navbar,
    navbar2,
    about,
    skills,
    work,
    bottom,
    whatDo,
    project,
    bulma
  },
  mounted: function() {
    console.log("mou");
      fetch('https://jsonplaceholder.typicode.com/users')
    .then(response => response.json()) // response.json() returns a promise
    .then((data) => {
     this.friends = data;
     console.log("I have friend " + this.friends)
    })
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
      dataTest: [],
      editFriend: null,
      friends: []
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
    }, //w3_close

    deleteFriend(id,i){
       fetch('https://jsonplaceholder.typicode.com/users' + id,{
         method: "DELETE"
       })
       .then(()=>{
         this.friends.splice(i,1)
         console.log("delete")
       })
    
    },
    updateFriend(friend){
       fetch('https://jsonplaceholder.typicode.com/users' + friend.id, {
         body: JSON.stringify(friend),
         method: "PUT",
         headers: {
           "Content-Type" : "application/json",
         },
       })
       .then(()=>{
           this.editFriend = null;
       })
    }

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
