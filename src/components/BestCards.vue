<template>
  <div>
    <div class="mt-5">
      <h1 class="fontTitle text-center pt-5">Best <strong style="color: #ff6200;">vacation plan</strong></h1>

      <p class="mt-3 mb-4 text-secondary text-center">
        Plan your perfect vacation with our travel agency. Choose <br> among hundreds of all-inclusive offers!
      </p>
    </div>
    <!-- Buttons rounded -->
    <div class=" d-flex justify-content-around my-4">
      <div></div>
      <div>
        <div class="block">
          <ul>
            <li><a href="#"><i class="fa-solid fa-arrow-left"></i></a></li>
            <li class="active"><span><i class="fa-solid fa-arrow-right"></i></span></li>
          </ul>
        </div>
      </div>
    </div>

    <!-- Cards -->
    <div class="d-flex justify-content-center container-fluid mb-5">
      <div class="row pb-4">
        <div class="col-4" v-for="travel in travels" :key="travel.idbesttravel">
          <div class="card" style="width: 20rem;">
            <img v-bind:src="travel.img" class="card-img-top" alt="...">
            <div class="card-body">
              <div class="d-flex justify-content-between align-items-center">
                <p class="card-title mt-1 text-start fontTitle">{{travel.city}},{{travel.pais}}</p>

                <p class="text-end"  style="color: rgb(255, 98, 0)">
                  {{travel.price}}
                </p>
              </div>
              <div class="d-flex justify-content-between align-items-center">
                <div class="d-flex">
                  <i class="fa-solid fa-location-arrow" style="color: rgb(255, 98, 0);"></i>
                  <p class="card-text text-secondary  text-end arrow mb-2">{{travel.time}}</p>
                </div>
                <div class="d-flex">
                  <p><i class="fa-solid fa-star" style="color: #ffc109;"></i> {{travel.score}}</p>
                </div>

              </div>

            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

</template>

<script>
import axios from  'axios';

export default {
  data(){
    return{
      travels: [],
      nuevoViaje: {
        pais: '',
        city: '',
        price: '',
        time: '',
        score: '',
        img: '',
      },
    };
  },
  mounted() {
    this.gettravel();
  },
  methods: {
    gettravel(){
      axios.get(process.env.VUE_APP_ENDPOINT_BEST)
          .then(response => {
            this.travels = response.data;
          })
          .catch(error => {
            console.error('error al obtener los datos de la API', error);
          })
    }
  },
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
  border: 1px solid transparent; }


</style>