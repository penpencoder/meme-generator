<template>
  <div class="hello">
    <div class="container p-5">
      <div class="d-flex flex-column min-vh-100 justify-content-center align-items-center">
        <div class="card p-5">
          <div class="card-body">
            <h1 class="mb-5">{{ msg }}</h1>
            <div class="row" >
              <div class="col-md-4 p-3" v-for="meme in results.memes" :key="meme">
                <img v-bind:src="meme.url" width="300">
              </div>
            </div>
            <button class="btn btn-dark" @click="created()">Generate Meme</button>
          </div>
          <div class="text-center">
            Made with stupidity by yours truly: Stephen "Pogi" Pascual 
          </div>
        </div>
        
      </div>
      
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeMeme',
  props: {
    msg: String
  },
  data: function(){
    return{
      results: [],
    }
  },
  methods: {
      async created() {
        // GET request using fetch with async/await
        const response = await fetch("https://meme-api.herokuapp.com/gimme/6");
        this.results = await response.json();
        console.log(this.results);
      }
  },
  created(){
    this.created()
  }
}


</script>

