<template>
  <div class="section2">
    <div>
      <h1 class="fontTitle text-center mt-5"> Things you need <strong style="color: #ff6200;">to do</strong></h1>

      <p class="mt-3 mb-4 text-secondary text-center">
        We ensure that you'll embark on a  perfectly planned, <br> safe vacation at a price you can afford.
      </p>
    </div>
    <!-- Cards -->
    <div class="d-flex justify-content-center container-fluid">
      <div class="row mb-5">
        <div class="col-4" v-for="util in utils" :key="util.idutil">
          <div class="card" style="width: 18rem;">
            <div class="card-body">
              <img v-bind:src="util.logo"  alt="...">
              <h4 class="card-title mt-4">{{util.title}}</h4>
              <p class="card-text text-secondary fontParagraph arrow mb-2">{{ util.description}}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

</template>

<script>
import axios from "axios";

export default {
  data(){
    return{
      utils: [],
      newUtil: {
        logo: "",
        title: "",
        description: ""
      },
    };
  },
  mounted() {
    this.getUtil();
  },
  methods: {
    getUtil(){
      axios.get('https://backend-trabook.up.railway.app/api/util')
          .then(response => {
            this.utils = response.data;
          })
          .catch(error => {
            console.log("Error al obtener los datos de la API: ", error);
          });
    }

  }
}

</script>

<style scoped>
.section2{
  background-color: #f5f5f5;
  margin: 2rem 0;
  padding: 3rem 0;
}

.fontTitle{
  font-family: 'Mate', serif;
}

.fontParagraph{
  font-family: 'Nunito', sans-serif;
}

</style>