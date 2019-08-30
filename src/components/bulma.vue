<template>
  <div class="container">
    <div class="columns">
      <div class="column"></div>
      <div class="column is-four-fifths">
        <div class="notification">
          <div class="columns">
            <div class="column">
              <img src="https://bulma.io/images/placeholders/256x256.png" class="imgMargin" />
              <img src="https://bulma.io/images/placeholders/256x256.png" class="imgMargin" />
              <img src="https://bulma.io/images/placeholders/256x256.png" class="imgMargin" />
            </div>

            <div class="column">
              <img src="https://bulma.io/images/placeholders/256x256.png" class="imgMargin" />
              <img src="https://bulma.io/images/placeholders/256x256.png" class="imgMargin" />
              <img src="https://bulma.io/images/placeholders/256x256.png" class="imgMargin" />
            </div>

            <div class="column">
              <img src="https://bulma.io/images/placeholders/256x256.png" class="imgMargin" />
              <img src="https://bulma.io/images/placeholders/256x256.png" class="imgMargin" />
              <img src="https://bulma.io/images/placeholders/256x256.png" class="imgMargin" />
            </div>
          </div>
        </div>
      </div>

      <div class="column">
        <div class="notification">
          <aside class="menu">
            <p class="menu-label">General</p>
            <ul class="menu-list">
              <li>
                <a>Dashboard</a>
              </li>
              <li>
                <a>Customers</a>
              </li>
            </ul>

            <p class="menu-label">Transactions</p>
            <ul class="menu-list">
              <li>
                <a>Payments</a>
              </li>
              <li>
                <a>Transfers</a>
              </li>
              <li>
                <a>Balance</a>
              </li>
            </ul>
          </aside>
        </div>
      </div>
    </div>

    <div class="text-center">
      <p class="title is-2">Product</p>
      <br>
    </div>
       <nav class="panel">
      <p class="panel-heading">Add a new product</p>
      <div class="panel-block">
        <br>
           <div class="container">
   

      <div class="columns  w3-padding-16">
        <div class="column">
          <div class="field is-horizontal">
            <div class="field-label is-normal">
              <label class="label">ID</label>
            </div>
            <div class="field-body">
              <div class="field">
                <div class="control">
                  <input class="input" type="text" placeholder="" />
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="column">
          <div class="field is-horizontal">
            <div class="field-label is-normal">
              <label class="label">Name</label>
            </div>
            <div class="field-body">
              <div class="field">
                <div class="control">
                  <input class="input" type="text" placeholder="" />
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="column">
          <div class="field is-horizontal">
            <div class="field-label is-normal">
              <label class="label">Price</label>
            </div>
            <div class="field-body">
              <div class="field">
                <div class="control">
                  <input class="input" type="text" placeholder="" />
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="column ">
          <div class="control">
            <button class="button is-info">Add</button>
          </div>
        </div>
      </div>
    </div>

      </div>
     
    </nav>
 
    <br>


    <nav class="panel">
      <p class="panel-heading">Product List</p>
      <div class="panel-block">
        <table class="table">
          <thead>
            <tr>
              <th>ProductID</th>
              <th>ProductName</th>
              <th>ProductPrice</th>
                 <th>Action</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>1</td>
              <td>Sunsu</td>
              <td>3500</td>
              <td ><a class="button is-white"><i class="fas fa-edit"></i></a> <a class="button is-white"><i class="fas fa-trash"></i></a> <a class="button is-white"><i class="fas fa-eye"></i></a></td>
            </tr>
          </tbody>
        </table>
      </div>
    </nav>


  </div>
</template>
<style>
.imgMargin {
  margin-bottom: 2%;
}
</style>