<template>
  <div id="app">
    <NavBar />
    <BannerContent />
    <CardsUtil />
    <TravelsCards />
    <BestCards />
    <User />
    <BlogsCards />
    <Footer />
  </div>
</template>

<script>

import NavBar from './components/NavBar.vue'
import BannerContent from './components/BannerContent.vue'
import CardsUtil from './components/CardsUtil.vue'
import TravelsCards from './components/TravelsCards.vue'
import BestCards from './components/BestCards.vue'
import User from './components/UserContent.vue'
import BlogsCards from "./components/BlogsCards.vue";
import Footer from "./components/FooterSuscribe.vue";

export default {
  name: 'App',
  components: {
    NavBar,
    BannerContent,
    CardsUtil,
    TravelsCards,
    BestCards,
    User,
    BlogsCards,
    Footer
  }
}
</script>

<style>
.fontTitle{
  font-family: 'Mate', serif;
}
.fontParagraph{
  font-family: 'Nunito', sans-serif;
}

.fontBig{
  font-size: 4rem;
}

.section{
  background-color: #f5f5f5;
  margin: 2rem 0;
  padding: 3rem 0;
}

p, h4{
  font-family: 'Nunito', sans-serif;
  font-size: 1.2rem;
}

.arrow{
  font-size: 0.8rem;
}

a{
  font-family: 'Nunito', sans-serif;
}

a:hover{
  color: rgb(255, 98, 0);
  text-decoration: none;
  padding: 0.5rem 1rem;
  border-bottom: 2px solid rgb(255, 98, 0);
}

</style>
