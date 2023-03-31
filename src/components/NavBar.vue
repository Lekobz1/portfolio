<template >
<header class="header">
  <nav>
    <div class="nav">
      <div class="logo">
        <img class="imglogo" src="../assets/logo site.svg" alt="Logo Jonathan Simon">
      </div>
      <div class="navigation">
        <ul class="links">
          <router-link to="/" class="a" href="#">Accueil</router-link>
          <!-- <router-link to="/about"  class="b" href="#">Présentation</router-link>  -->
          <router-link to="/portfolio" class="c" href="#">Portfolio</router-link>
          <router-link to="/prestations" class="d" href="#">Prestations</router-link>
          <router-link to="/contact" class="e" href="#">Contact</router-link>
          <router-link to="/blog" class="f" href="#">Blog</router-link>
        </ul>
      </div>
      <div class="logIn">
        <a class="login" href="#">LogIn/SignIn</a>
      </div>
    </div>
</nav>
</header>
   
 </template>
 
 <script>
 export default {
   name: "Navbar"

 }
 </script>

<style scoped>

.nav {
  display: grid; 
  grid-template-columns: 18% 58% 18%; 
  grid-template-rows: 5% 5% 5%; 
  gap: 0% 3%; 
  grid-template-areas: 
    ". . ."
    "logo navigation logIn"
    ". . ."; 
  background-color: rgba(249, 244, 237, 1);
  box-shadow: 5px 4px 4px rgba(0, 0, 0, 0.25);

}
.logo { 
  grid-area: logo; 
}
.navigation { 
  grid-area: navigation;
  font-family: 'PT Serif';
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 31px;
  color: rgba(30, 30, 30, 1);
  
}
.logIn { 
  grid-area: logIn; 
}
.a:hover, .b:hover, .c:hover, .d:hover, .e:hover, .f:hover, .login:hover{
  color: rgba(197, 137, 64, 1);
}
.imglogo{
width: 150px;
height: 150px;
}
.login {
box-sizing: border-box;
background: #F9F4ED;
border: 3px solid #1E1E1E;
box-shadow: 4px 4px 4px #C58940;
border-radius: 10px;
font-family: 'PT Serif';
font-style: normal;
font-weight: 700;
font-size: 24px;
line-height: 31px;
color: rgba(30, 30, 30, 1);
}
</style>

