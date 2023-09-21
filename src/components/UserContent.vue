<template>
  <div  class="section">
    <div class="d-flex justify-content-center container-fluid mb4-5">
      <div class="row mt-5">
        <!-- Column -->
        <div class="col-6 pl-5">
          <h1 class="fontTitle"> What people say <br> <strong style="color: #ff6200;">about us.</strong></h1>

          <p class="mt-3 mb-4 text-secondary">Our clients send us bunch of smilies with our services <br> and we love them</p>

          <div class=" d-flex justify-content-around my-4">
            <div class="block mb-5">
              <ul>
                <li><a href="#"><i class="fa-solid fa-arrow-left"></i></a></li>
                <li class="active"><span><i class="fa-solid fa-arrow-right"></i></span></li>
              </ul>
            </div>
          </div>

        </div>
        <!-- Column -->
        <div class="col-6">
          <div class="card" style="width: 28rem;">
            <div class="card-body">
              <img class="rounded-circle mb-3" src="https://github.com/rquintg/backend-trabook/blob/main/src/img/profile.jpeg?raw=true" width="48" height="48" alt="...">
              <p class="card-text text-secondary fontParagraph arrow mb-2">"On the windows talking painted pasture yet its <br> express parties use. Sure last upon he same as <br> knew next. Of believed no.</p>
              <h4 class="card-title mt-4">Mike taylor</h4>
              <p class="card-text text-secondary">Lahore, Pakistan</p>
            </div>
          </div>
        </div>
      </div>


    </div>
  </div>
</template>
<script>
</script>

<style scoped>
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