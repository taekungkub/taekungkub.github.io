<template>
  <div class="container">
    <br />
    <br />
    <br />
    <br />

    
      <div class="container">
    <fieldset>
      <div class="field">
        <label class="label">Name</label>
        <div class="control">
          <input class="input" type="text" placeholder="" v-model="inputField" v-on:keyup.enter="addTodo"/>
        </div>
      </div>

      <div class="field">
        <label class="label">Description</label>
        <div class="control">
          <input class="input" type="text" placeholder=""  v-model="inputField2" v-on:keyup.enter="addTodo"/>
        </div>
      </div>
    </fieldset>
  </div>
  <br>
 <div class="field is-grouped">
  <p class="control">
    <a class="button is-primary" @click="addTodo" >
      Add product
    </a>
  </p>
  <p class="control">
    <a class="button is-light">
      Cancel
    </a>
  </p>
</div>

<table class="table">
  <thead>
    <tr>
      <th><abbr title="Position">ID</abbr></th>
      <th>Name</th>
      <th><abbr title="Played">Description</abbr></th>
        <th><abbr title="Played">Edit</abbr></th>
          <th><abbr title="Played">Delete</abbr></th>
    
    </tr>
  </thead>

  <tbody>
    <tr  v-for="(todo,index) in todoList">
      <th>{{index+1}}</th>
      <td>{{todo.name}}</td>
      <td>{{todo.description}}</td>
       <td><button class="button is-warning" >Edit</button></td>
        <td><button class="button is-danger" @click="deleteTodo" >Delete</button></td>

    </tr>
 

    </tr>
  </tbody>
</table>
      

  </div>
</template>
<script>
export default {
  data() {
    return {
      inputField: "",
      todoList: [{
          name:"test",
          description:"description",
      }]
    };
  }, //data
  methods: {
    addTodo: function(todo,todo2) {
     
      todo = this.inputField;
       todo2 = this.inputField2;
          if(todo == "" && todo2 ==""){
            alert("Test")
        } else {
                 this.todoList.push({ name: todo,description:todo2, complete: false });
      this.inputField = "";
         this.inputField2 = "";
      console.log(this.todoList);
        }
     
    },
    deleteTodo: function(todo) {
      var index = this.todoList.indexOf(todo);
      this.todoList.splice(index, 1);
      console.log(this.todoList);
   },
   clearall(){
       this.todoList = [];
   }
  } //method
};
</script>