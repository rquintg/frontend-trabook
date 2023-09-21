<template>
  <div>
    <!-- Blog post -->
    <div>
      <h1 class="fontTitle text-center py-5">Get update with <strong style="color: #ff6200;">latest blog</strong></h1>
    </div>

    <!-- Cards -->
    <div class="d-flex justify-content-center container-fluid">
      <div class="row">
        <div class="col-3" v-for="(blog, index) in blogs" :key="index">
          <div class="card" style="width: 16rem;">
            <img v-bind:src="blog.img" class="card-img-top" alt="...">
            <div class="card-body">
              <div class="d-flex justify-content-between align-items-center">
                <p class="card-title mt-1 text-start fontTitle fontSizeCard">{{blog.title}}</p>
              </div>
              <p class="card-text text-secondary  text-start arrow mb-2">{{ blog.date }}</p>
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
import axios from  'axios';

export default {
  data(){
    return{
      blogs: [],
      newBlog: {
        title: '',
        date: '',
        img: ''
      },
    };
  },
  mounted() {
    this.getBlog();
  },
  methods: {
    getBlog(){
      axios.get(process.env.VUE_APP_ENDPOINT_BLOG)
          .then(response => {
            this.blogs = response.data;
          })
          .catch(error => {
            console.error('error al obtener los datos de la API', error);
          })
    }
  },
}
</script>


<style scoped>
.fontSizeCard{
  font-size: 1rem;
}

/* buttons rounded */
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