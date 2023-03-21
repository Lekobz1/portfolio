<template >
<header class="header">
<nav class="nav">
    <div class="logo">
      <img class="imglogo" src="../assets/logo blanc sans bg.png" alt="">
    </div>
    <div class="lien">
        <ul class="links">
          <router-link to="/" class="a" href="#"> Accueil</router-link>
          <router-link to="/about"  class="b" href="#">Présentation</router-link> 
          <router-link to="/portfolio" class="c" href="#">Portfolio </router-link>
          <router-link to="/prestations" class="d" href="#">Prestations</router-link>
          <router-link to="/contact" class="e" href="#">Contact</router-link>
          <router-link to="/blog" class="f" href="#">Blog</router-link>
        </ul>
    </div>
    <div class="log">
      <a class="login" href="#">LogIn/SignIn</a>
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
.header {
  display: grid;
}
.nav{
  background-color: rgba(37, 35, 35, 1);
  display: flex;
  flex-direction: row;
  
}

.links {
display: flex;
flex-direction: row;
flex: 80%;
color: rgba(236, 236, 236, 1);
font-size: 24px;
transition: .5s;
}

ul li{
  list-style:none;
  margin:100px 20px;
  transition:0.5s;
}

.a:hover{
  color: orange;
}
.b:hover{
  color: orange;
}
.c:hover{
  color: orange;
}
.d:hover{
  color: orange;
}
.e:hover{
  color: orange;
}
.f:hover{
  color: orange;
}

ul:hover li a{
  transform:scale(1.5);
  opacity:0.2;
  filter:blur(5px);
}

ul li a:hover{
  transform:scale(2);
  opacity:1;
  filter:blur(0);
  text-decoration:none;
  color:#fff;
}

ul li a:before{
  content:'';
  position:absolute;
  top:0;
  left:0;
  width:100%;
  height:100%;
  background:orange;
  transition:0.5s;
  transform-origin:right;
  transform:scaleX(0);
  z-index:-1;
}

ul li a:hover:before{
  transition:transform 0.5s;
  transform-origin:left;
  transform:scaleX(1);
}

.logo{
  margin:50px 20px;
}

.imglogo{
flex: 10%;
width: 100px;
height: 100px;
margin-left: 10%;

}

.log{
  margin:100px 20px;

}

.login {
  flex: 10%;
  color: rgba(236, 236, 236, 1);
}

.login:hover{
  color: orange;
}





</style>

