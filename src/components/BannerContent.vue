<template>
  <div>
    <!-- container slider and  principal text -->
    <div class="d-flex justify-content-center container-fluid">
      <div class="row mt-5">
        <!-- column left -->
        <div class="col-6 pl-5">
          <h1 class="fontTitle fontBig"> Get started your <br> Exciting <strong style="color: #ff6200;">journey</strong> <br> with us.</h1>

          <p class="mt-3 mb-4 text-secondary fontSmall">A Team of experienced tourism professionals will <br> provide you with the best advice and tips for your <br> desire place</p>

          <button type="button" class="btoutline">Discover Now</button>
        </div>
        <!-- column right -->
        <div class="col-6">
          <img src="https://github.com/rquintg/backend-trabook/blob/main/src/img/tourist-with-thumb-up__1_-removebg%201.png?raw=truegit" alt="tourist">
        </div>
      </div>

    </div>
    <!-- Menu slider -->
    <div class="d-flex justify-content-center container-fluid">
      <div class="row mt-5">
        <div class="col-3">
          <h4> Location <i class="fa-solid fa-chevron-down" style="color: #ff6200;"></i></h4>
          <p class="text-secondary arrow">
            Where ate you going
          </p>
        </div>
        <div class="col-3">
          <h4> Date <i class="fa-solid fa-chevron-down" style="color: #ff6200;"></i></h4>
          <p class="text-secondary arrow">
            When you will go
          </p>
        </div>
        <div class="col-3">
          <h4> Guest <i class="fa-solid fa-chevron-down" style="color: #ff6200;"></i></h4>
          <p class="text-secondary arrow">
            Number od guest
          </p>
        </div>
        <div class="col-3">
          <button class="bt">Explore Now</button>
        </div>

      </div>


    </div>
  </div>

</template>
<script>

</script>

<style scoped>
.btoutline{
  display: inline-block;
  background-color: transparent;
  padding: 10px 40px;
  border-radius: 0.3rem;
  color: rgb(255, 98, 0);
  font-size: 1.2rem;
  text-decoration: none;
  cursor: pointer;
  transition: all 0.3s ease-in;
  border: 1px solid rgb(255, 98, 0);
  outline: none;
  box-shadow: 0 0 10px rgba(255, 98, 0, 0.9);
}

.btoutline:hover{
  transform: translateY(-3px);
  color: #000;

}

.bt{
  display: inline-block;
  background-color: rgb(255, 98, 0);
  padding: 10px 40px;
  border-radius: 0.3rem;
  color: white;
  font-size: 1rem;
  text-decoration: none;

  cursor: pointer;
  transition: all 0.3s ease-in;
  border: none;
  outline: none;
  box-shadow: 0 0 10px rgba(255, 98, 0, 0.9);
}

.bt:hover{
  transform: translateY(-3px);
  color: #000;

}
</style>