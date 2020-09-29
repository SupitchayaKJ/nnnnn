<template>
  <div id="app">
<div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
  <ol class="carousel-indicators">
    <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
  </ol>
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="https://wallpaperaccess.com/full/14358.jpg" class="d-block w-100" alt="...">
    </div>
    <div class="carousel-item">
      <img src="https://wallpaperset.com/w/full/e/6/b/183984.jpg" class="d-block w-100" alt="...">
    </div>
    <div class="carousel-item">
      <img src="https://i.ytimg.com/vi/STSlmmqaJks/maxresdefault.jpg" class="d-block w-100" alt="...">
    </div>
  </div>
  <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>

<p></p>
    <div class="row ">
      <div class="col">
        <h2 v-on:click="counter1 += 1">
          <img src="https://res.cloudinary.com/prvnbist/image/upload/v1492531171/XZOPuv9_eyqlr2.png" width="50" height="50" alt /></h2>
        <h1>{{ counter1 }}</h1>
      </div>

      <div class="col">
        <h2 v-on:click="counter2 += 10">
          <img src="https://res.cloudinary.com/prvnbist/image/upload/v1492531172/uIjLl6R_cmbnqb.png" width="50" height="50" alt /></h2>
        <h1>{{ counter2 }}</h1>
      </div>

      <div class="col">
        <h2 v-on:click="counter3 += 5">
          <img src="https://res.cloudinary.com/prvnbist/image/upload/v1492531177/lsHmtDy_ycqnbp.png" width="50" height="50" alt /></h2>
        <h1>{{ counter3 }}</h1>
      </div>

      <div class="col">

        <h2 v-on:click="counter4 += 20">
          <img src="https://cdn.freebiesupply.com/logos/large/2x/facebook-wow-logo-png-transparent.png" width="50" height="50" alt /></h2>
        <h1>{{ counter4 }}</h1>
      </div>

      <div class="col">
        <h2 v-on:click="counter5 -= 5">
          <img src="https://res.cloudinary.com/prvnbist/image/upload/v1492531172/JJuD9qb_a7gkmu.png" width="50" height="50" alt /></h2>
        <h1>{{ counter5 }}</h1>
      </div>

      <div class="col">
        <h2 v-on:click="counter6 -= 50">
          <img src="https://res.cloudinary.com/prvnbist/image/upload/v1492531178/VDM3zOV_qy9fqj.png" width="50" height="50" alt /></h2>
        <h1>{{ counter6 }}</h1>
      </div>

      <div class="col">
        <h1>Total: {{counter1+counter2+counter3+counter4+counter5+counter6}}</h1>
        <button @click="reset" class="btn btn-primary">Reset</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  props: {
    label1: String,
    label2: String,
    label3: String,
  },
  data: function () {
    return {
      counter1: 0,
      counter2: 0,
      counter3: 0,
      counter4: 0,
      counter5: 0,
      counter6: 0,
      reset1: 0,
      classObject: {
        active: true,
        "text-danger": false,
        weight: 20,
      },
    };
  },
  methods: {
    reset() {
      Object.assign(this.$data, this.$options.data());
    },
  },
};
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

body {
    background-image: url("https://wallpaper.campus-star.com/app/uploads/2016/05/Wallpapers%E0%B8%AA%E0%B8%B5%E0%B8%82%E0%B8%B2%E0%B8%A7%E0%B8%AA%E0%B8%9A%E0%B8%B2%E0%B8%A2%E0%B8%95%E0%B8%B2-2.jpg");
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}
</style>