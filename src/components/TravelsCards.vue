<template>
  <div>
    <div class="mt-5">
      <h1 class="fontTitle text-center pt-5">Exclusive <strong style="color: #ff6200;">deal & discounts</strong></h1>

      <p class="mt-3 mb-4 text-secondary text-center">
        Discover our fantastic early booking discounts <br> & start planning your journey.
      </p>
    </div>
    <!-- Cards  price-->
    <div class="d-flex justify-content-center container-fluid">
      <div class="row">
        <div class="col-3" v-for="travel in travels" :key="travel.idtravels">
          <div class="card" style="width: 14rem;">
            <img v-bind:src="travel.img" class="card-img-top" alt="...">
            <div class="card-body">
              <div class="d-flex justify-content-between align-items-center">
                <p class="card-title mt-1 text-start fontTitle">{{ travel.city }}</p>

                <p class="text-end">
                  <i class="fa-solid fa-star" style="color: #ffc109;"></i>{{travel.score}}</p>
              </div>
              <div class="d-flex justify-content-between align-items-center">
                <div class="d-flex">
                  <i class="fa-solid fa-location-dot me-1" style="color: #a0a6b0;"></i>
                  <p class="card-text text-secondary  text-end arrow mb-2">{{ travel.pais}}</p>
                </div>
                <div class="d-flex">
                  <p class="card-text text-secondary  text-start arrow me-3"><del>${{travel.price_off}}</del></p>
                  <p class="card-text text-secondary  text-end arrow mb-2">${{travel.price}}</p>
                </div>

              </div>

            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Buttons rounded -->
    <div class=" d-flex justify-content-center align-items-center my-4">
      <div class="block mb-5">
        <ul>
          <li><a href="#"><i class="fa-solid fa-arrow-left"></i></a></li>
          <li class="active"><span><i class="fa-solid fa-arrow-right"></i></span></li>
        </ul>
      </div>
    </div>
  </div>

</template>

<script>
import axios from 'axios'

export default {
  data(){
    return{
      travels: [],
      newTravel: {
        pais: '',
        price: '',
        img: '',
        price_off: '',
        score: '',
        time: ''
      },
    };
  },
  mounted() {
    this.getTravels();
  },
  methods: {
    getTravels(){
      axios.get(process.env.VUE_APP_ENDPOINT_TRAVEL)
          .then((response) => {
            this.travels = response.data;
          })
          .catch((error) => {
            console.error('Error al obtener los datos de la API:', error);
          });
    }
  }
}

</script>

<style scoped>
.block ul {
  padding: 0;
  margin: 0; }
.block ul li {
  display: inline-block;
  margin-bottom: 4px;
  font-weight: 400; }
.block ul li a, .block ul li span {
  color: rgb(0, 0, 0);
  text-align: center;
  display: inline-block;
  width: 40px;
  height: 40px;
  line-height: 40px;
  border-radius: 50%;
  border: 1px solid #e6e6e6; }
.block ul li.active a, .block ul li.active span {
  background: rgb(255, 98, 0);
  color: #fff;
  border: 1px solid transparent;
}
</style>