<template>
  <html>
    <body>
    <div class="my-jumbotron" id="my-jumbotron">
    <nav class="navbar navbar-expand">
        <img src="/pictures/logo1.png" width="180px" height="60px" class="navbar-brand p-2"/>
        <ul class="navbar-nav">
        <li class="nav-item">
            <a class="nav-link" href="">HOME</a>
        </li>
        <li class="nav-item">
            <a class="nav-link" href="">ABOUT</a>
        </li>
        <li class="nav-item">
            <a class="nav-link" href="">PRODUCT</a>
        </li>
        </ul>
        <div class="collapse navbar-collapse">
          <ul class="nav navbar-nav ml-auto">
          <li class="nav-item mx-3 ">
              <a class="nav-link" href="" ><b-icon icon="person-fill"></b-icon></a>
          </li>
          <li class="nav-item mx-3">
              <a class="nav-link" href=""><b-icon icon="bucket-fill"></b-icon></a>
          </li>
          </ul>
        </div>
        </nav>

        <!-- banner -->
        <div>
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="3500"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- img-src="https://i.picsum.photos/id/1070/5472/3648.jpg" -->
      <!-- img-src="https://i.picsum.photos/id/1071/3000/1996.jpg" -->
      <!-- img-src="https://i.picsum.photos/id/1072/3872/2592.jpg" -->
      <!-- Text slides with image -->
      <b-carousel-slide img-src="/pictures/baner1.jpg">
        <div class="container text-center" id="jumbo-text-contain">
            <h4 class="display-4 mt-5" style="font-weight: bold;">Selamat Datang Sneaks Lovers!</h4>
            <p class="lead">Belanja Barang Branded Hanya disini</p>
            <button type="button" class="btn" id="jumbotron-btn">SHOP NOW !</button>
        </div>
      </b-carousel-slide>

      <!-- Slides with custom text -->
      <b-carousel-slide img-src="/pictures/baner2.jpg">
        <div class="container text-center" id="jumbo-text-contain">
            <h4 class="display-4 mt-5" style="font-weight: bold;">Selamat Datang Sneaks Lovers!</h4>
            <p class="lead">Belanja Barang Branded Hanya disini</p>
            <button type="button" class="btn" id="jumbotron-btn">SHOP NOW !</button>
        </div>
      </b-carousel-slide>

      <!-- Slides with image only -->
      <b-carousel-slide img-src="/pictures/baner3.jpg">
        <div class="container text-center" id="jumbo-text-contain">
            <h4 class="display-4 mt-5" style="font-weight: bold;">Selamat Datang Sneaks Lovers!</h4>
            <p class="lead">Belanja Barang Branded Hanya disini</p>
            <button type="button" class="btn" id="jumbotron-btn">SHOP NOW !</button>
        </div>
      </b-carousel-slide>
    </b-carousel>
  </div>
    </div>

    <div id="category-sect">
    <h4 class="font-weight-bold pt-5 text-center"> Our Products </h4>
      <section id="tabs" class="project-tab">
        <div class="container-fluid">
            <div class="row justify-content-center">
                <div class="col-md-12">
                    <b-tabs content-class="mt-3" fill>
                    <b-tab title="Basketball" active>
                    <ul class="container mt-4">
                          <div class="row">
                        <div v-for="(basket, index) in Basketball" :key="index" class="col-sm-4 text-center">
                          <div class="product-image">
                            <img :src="/pictures/ + filename + index + filetype" class="img-responsive h-100 w-100"/>
                            </div>
                          <div class="product-details">
                            <h6 class="display-6 mt-3">{{ basket.name }}</h6>
                            <h6 class="display-6 text-muted">Rp.{{ basket.price }}</h6>
                          </div>
                        </div>
                    </div>
                    </ul>
                    </b-tab>
                    <b-tab title="Sneakers">
                      <ul class="container mt-4">
                          <div class="row">
                        <div v-for="(sneak, index) in Sneakers" :key="index" class="col-sm-4 text-center">
                          <div class="product-image">
                            <img :src="/pictures/ + filejeneng + index + filetype" class="img-responsive h-100 w-100"/>
                            </div>
                          <div class="product-details">
                            <h6 class="display-6 mt-3">{{ sneak.name }}</h6>
                            <h6 class="display-6 text-muted">Rp.{{ sneak.price }}</h6>
                          </div>
                        </div>
                    </div>
                    </ul>
                      </b-tab>
                    <b-tab title="Pantofel">
                      <ul class="container mt-4">
                          <div class="row">
                        <div v-for="(panto, index) in Pantofel" :key="index" class="col-sm-4 text-center">
                          <div class="product-image">
                            <img :src="/pictures/ + filenama + index + filetype" class="img-responsive h-100 w-100"/>
                            </div>
                          <div class="product-details">
                            <h6 class="display-6 mt-3">{{ panto.name }}</h6>
                            <h6 class="display-6 text-muted">Rp.{{ panto.price }}</h6>
                          </div>
                        </div>
                    </div>
                    </ul>
                    </b-tab>
                  </b-tabs>

                    </div>
                </div>
            </div>
            </section>
        </div>
		
  </body>

  <footer class="page-footer blue pt-5 mt-5">
<div class="container-fluid text-center text-md-left">
      <div class="row">
        <div class="col-md-6 mt-md-0 mt-3">
          <img class="px-5" src="/pictures/footer.png" height="100px" />
          <p class="text-md-left px-5">Sneakpeak adalah sebuah lapak toko sepatu online, kami menyediakan berbagai
            macam sepatu branded yg ada di indonesia ataupun tidak terjual di indonesia dengan harga yg terjangkau.
            Belanja mudah dan belanja terjangkau hanya di Sneakpeak Authentic Store.
          </p>

        </div>

        <hr class="clearfix w-100 d-md-none pb-3">
        <div class="col-md-3 mb-md-0 mb-3">

          <h5 class="text-uppercase">Layanan Kami</h5>
          <br>
          <ul class="list-unstyled">
            <li>
              <a href="#!">Home</a>
            </li>
            <br>
            <li>
              <a href="#!">About Us</a>
            </li>
            <br>
            <li>
              <a href="#!">Products</a>
            </li>
            <br>
          </ul>

        </div>
        <div class="col-md-3 mb-md-0 mb-3">

          <h5 class="text-uppercase">Contact Us</h5>
          <br>
          <ul class="list-unstyled">
            <li>
              <a href="#!">Instagram</a>
            </li>
            <br>
            <li>
              <a href="#!">Twitter</a>
            </li>
            <br>
            <li>
              <a href="#!">Whatsapp</a>
            </li>
            <br>
            <li>
              <a href="#!">Line</a>
            </li>
          </ul>

        </div>

      </div>

    </div>
    <br><br>
    <div class="footer-copyright text-center py-3 mr-3">© 2020 Copyright: IbborStore
    </div>
  </footer>

  </html>
</template>

<script>
import axios from 'axios'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

export default {
    data() {
      return {
        slide: 0,
        filetype:".jpg",
        filename:"basketball",
        filejeneng:"sneakers",
        filenama:"pantofel",
        sliding: null,
        Basketball: [],
        Sneakers: [],
        Pantofel: []
      }
    },
  async created () {
    const baseURI = 'https://my-json-server.typicode.com/robbipratama/utsjson/db'
    axios.get(baseURI)
      .then((result) => {
        this.Basketball = result.data.Basketball
        this.Sneakers = result.data.Sneakers
        this.Pantofel = result.data.Pantofel
      })
  }
  }
</script>

<style>
#my-jumbotron {
    background-size: cover;
    overflow: hidden;
}
#jumbo-text-contain {
    color: whitesmoke;
    min-height: 300px;
}
#jumbotron-btn {
    font-size: 15px;
    border: 2px solid ;
    border-radius: 20px;
    transition: 0.3s;
    color: white;
}
#jumbotron-btn:hover {
    background-color: white;
    color:darkslategrey ;
    border: 2px solid white;
}
#products-container li{
    list-style-type: none;
    height: 250px;
}
.product-image {
    background: #f4f4ef;
    border-radius: 50px;
    width: 350px;
    height: 350px;
    margin-top: 30px;
    margin-right: 70px;
    transition: 0.5s ease-in-out;
}
.img-responsive {
  border-radius: 50px;
}
.product-image:hover {
  box-shadow: 0px 5px 8px 8px rgb(34, 41, 61);
}
.product-details {
  margin-top: 30px;
}
.project-tab {
    padding: 10%;
    margin-top: -8%;
}
.project-tab #tabs{
    background: black;
    color: #eee;
}
.project-tab #tabs h6.section-title{
    color: #eee;
}
.project-tab #tabs .nav-tabs .nav-item.show .nav-link, .nav-tabs .nav-link.active {
    color: #20232a;
    background-color: transparent;
    border-color: transparent transparent #f3f3f3;
    border-bottom: 3px solid !important;
    font-size: 16px;
    font-weight: bold;
}
.project-tab .nav-link {
    border: 1px solid transparent;
    border-top-left-radius: .25rem;
    border-top-right-radius: .25rem;
    color: #acbebe;
    font-size: 16px;
    font-weight: 600;
}
.project-tab .nav-link:hover {
    border: none;
}
.project-tab thead{
    background: #f3f3f3;
    color: #333;
}
.project-tab a{
    text-decoration: none;
    color: #333;
    font-weight: 600;
}
.page-footer {
    color: white;
    background: rgb(34, 41, 61);
}
.row {
  justify-content: center;
}
</style>
