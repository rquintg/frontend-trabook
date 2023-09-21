<template>
  <header>
    <!-- navbar -->
    <div class="container-fluid mt-5 ">
      <div class="row justify-content-md-center">
        <div class="col col-lg-2 text-center">
          <img class="mt-2" src="https://github.com/rquintg/backend-trabook/blob/main/src/img/Logo.png?raw=true" alt="logo">
        </div>
        <div class="col-md-auto">
          <ul class="nav">
            <li class="nav-item">
              <a class="nav-link active  text-dark" aria-current="page" href="#">Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link  text-dark" href="#">About</a>
            </li>
            <li class="nav-item">
              <a class="nav-link  text-dark" href="#">Destination</a>
            </li>
            <li class="nav-item">
              <a class="nav-link  text-dark" href="#">Tour</a>
            </li>
            <li class="nav-item">
              <a class="nav-link  text-dark" href="#">Blog</a>
            </li>
          </ul>
        </div>
        <!-- login y sign up -->
        <div class="col col-lg-2">
          <ul class="nav justify-content-center align-items-center">
            <li class="nav-item">
              <a class=" txt" href="#">Login</a>
            </li>
            <li class="nav-item">
              <a class="bt" href="#">Sign Up</a>
            </li>

          </ul>
        </div>
      </div>
    </div>
  </header>
</template>
<script>

</script>
<style scoped>
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

.txt{
  color: rgb(255, 98, 0);
  text-decoration: none;
  padding: 0.5rem 1rem;

}

.txt:hover{
  color: rgb(255, 98, 0);
  text-decoration: none;
  padding: 0.5rem 1rem;
  border-bottom: 2px solid rgb(255, 98, 0);
}
</style>