<template>
  <div>
    <main role="main">
      <div class="container marketing">
        <div class="row">
          <div class="col-lg-4">
            <h2></h2>
          </div>
          <div class="col-lg-4">
            <img
              class="rounded-circle"
              src="data:image/gif;base64,R0lGODlhAQABAIAAAHd3dwAAACH5BAAAAAAALAAAAAABAAEAAAICRAEAOw=="
              alt="Generic placeholder image"
              width="140"
              height="140"
            />
            <h4 style="margin-top:20px;">Developer</h4>
            <h2>Kieattisak Suparit</h2>
            <p>Hello every one I'm age 22, I'm from thailand, this first time my website resume</p>
            <p>
              <a class="btn btn-secondary" href="#" role="button">View details &raquo;</a>
            </p>
          </div>
          <div class="col-lg-4"></div>
        </div>
      </div>

      <div class="container">
        <div class="w3-row w3-center">
          <div class="w3-col m4">
            <h2>Programmming</h2>

            <span class="w3-tag w3-green w3-round">HTML</span>
            <span class="w3-tag w3-green w3-round w3-margin">CSS</span>
            <span class="w3-tag w3-green w3-round ">IonicFramwork</span>
            <span class="w3-tag w3-green w3-round w3-margin">Vue.js</span>
            <span class="w3-tag w3-green w3-round ">MySQL</span>
               <span class="w3-tag w3-green w3-round w3-margin">Firebase</span>
          </div>
          <div class="w3-col m4">
            <h2>Software</h2>
            <h3 class="badge badge-info w3-medium w3-margin">GoogleApps</h3>
            <h3 class="badge badge-info w3-medium">Ms Office</h3>
          </div>
          <div class="w3-col m4">
            <h2>Hardware</h2>
            <h3 class="badge badge-primary w3-medium">Computer</h3>
            <h3 class="badge badge-primary w3-medium w3-margin">Network</h3>
            <h3 class="badge badge-primary w3-medium">Printer</h3>
          </div>
        </div>

      </div>
    </main>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      count: 0,
      view: 0,
      skills: ["HTML", "Js", "TypeScript", "IonicFramwork", "PHP"],
      dataTest: []
    };
  } //data
  /*  created(){
    fetch('https://jsonplaceholder.typicode.com/photos')
    .then(response => response.json()) // response.json() returns a promise
    .then((response) => {
      this.dataTest = response
      console.log("DataTest: " + this.dataTest)
    })
  } */
};
</script>

<style>
.marketing .col-lg-4 {
  margin-bottom: 1.5rem;
  text-align: center;
}
.marketing h2 {
  font-weight: 400;
}
.marketing .col-lg-4 p {
  margin-right: 0.75rem;
  margin-left: 0.75rem;
}

/* Featurettes
------------------------- */

.featurette-divider {
  margin: 5rem 0; /* Space out the Bootstrap <hr> more */
}

.featurette-heading {
  font-weight: 300;
  line-height: 1;
  letter-spacing: -0.05rem;
}

@import url("https://fonts.googleapis.com/css?family=Prompt&display=swap");
</style>