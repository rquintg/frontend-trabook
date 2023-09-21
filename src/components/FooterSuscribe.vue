<template>
  <footer class="section">
    <!-- Suscribe -->
    <div class="row d-flex justify-content-center align-items-center rows">

      <div class="col-md-6">


        <div class="suscribe">


          <div class="text-center">

            <img src="" width="200">
            <span class="d-block mt-3 fontTitle fontBig">Subscribe and get exclusive <br> deals & offer</span>

            <div class="mx-5">


              <div class="input-group mb-5 mt-4">
                <input type="text" class="form-control" placeholder="Enter email" aria-label="Recipient's username" aria-describedby="button-addon2">
                <button class="btnSuscribe" type="button" id="button-addon2">Subscribe</button>
              </div>


            </div>

          </div>

        </div>

      </div>




    </div>

    <!-- Footer menu -->
    <div class="container-fluid mt-5">

      <div class="card1 mx-5">
        <div class="row mb-4 ">

          <div class="col-md-4 col-sm-11 col-xs-11">
            <div class="footer-text pull-left">
              <div class="d-flex">
                <div class="col col-lg-2 text-center">
                  <img class="mt-2" src="https://github.com/rquintg/backend-trabook/blob/main/src/img/Logo.png?raw=true">
                </div>
              </div>
              <p class="card-text ">Book your trip in minute, get full <br> Control for much longer.</p>

              <div class="social mt-2 mb-3">

                <i class="fa fa-facebook"></i>
                <i class="fa fa-instagram fa-lg"></i>
                <i class="fa fa-twitter fa-lg"></i>
              </div>

            </div>
          </div>


          <div class="col-md-2 col-sm-1 col-xs-1 mb-2"></div>

          <div class="col-md-2 col-sm-4 col-xs-4">

            <h5 class="heading mb-5">Company</h5>
            <ul class="card-text ms-2" >
              <li>About</li>
              <li>Careers</li>
              <li>Logistic</li>
              <li>Privacy & Policy</li>
            </ul>

          </div>


          <div class="col-md-2 col-sm-4 col-xs-4">

            <h5 class="heading mb-5">Contact</h5>
            <ul class="card-text ms-2">
              <li>Help/FAQ</li>
              <li>Press</li>
              <li>Affilates</li>
            </ul>

          </div>


          <div class="col-md-2 col-sm-4 col-xs-4">

            <h5 class="heading mb-5">More</h5>
            <ul class="card-text ms-2">
              <li>Press Centre</li>
              <li>Our Blog</li>
              <li>Low fare</li>
            </ul>

          </div>

        </div>


        <div class="divider mb-4" >
        </div>


        <div class="row" style="font-size:10px;">

          <div class="col-md-6 col-sm-6 col-xs-6">

            <div class="text-start">

              <p>Copyright, Trabook 2022. Akk rights reserved.</p>

            </div>

          </div>



          <div class="col-md-6 col-sm-6 col-xs-6">


            <div class=" text-end mr-4 ">

              <p>Terms & Conditions</p>

            </div>



          </div>



        </div>
      </div>

    </div>

  </footer>

</template>

<style scoped>
/* footer */

.suscribe{
  position: relative;
  display: flex;
  flex-direction: column;
  min-width: 0;
  color: #fff;
  background-color: rgb(255, 98, 0) ;
  background-clip: border-box;
  border: 1px solid rgba(0,0,0,0.125);
  border-radius: 0.25rem;

}



.card1{
  padding: 2% 7%;
  color: #646771;
  background-color: #f5f5f5;
  border: none;
}

ul{
  list-style-type: none;
  margin: -2rem;
  padding: 0;
}

ul >li{
  padding: 4px;
}

ul > li:hover{
  color:rgb(255, 98, 0);
  cursor: pointer;
}

hr{
  border-width: 3px;
}

.social > i{
  padding: 1%;
  font-size: 15px;
}

.social > i:hover{
  color:rgb(255, 98, 0);
  cursor:pointer;
}

.policy > div{
  padding: 4px;
}

.heading{
  font-family: 'Mate', serif;
  color: #000;
}

.divider{
  border-top: 2px solid rgba(189, 196, 203, 0.5);;
}
</style>