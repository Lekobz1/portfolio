<template >
  <nav>
    <div class="nav">

      <img class="logo" src="../assets/logo site.svg" alt="Logo Jonathan Simon">
     

      <ul class="navigation">
        <router-link to="/" class="a" href="#">Accueil</router-link>
        <!-- <router-link to="/about"  class="b" href="#">Présentation</router-link>  -->
        <router-link to="/portfolio" class="c" href="#">Portfolio</router-link>
        <router-link to="/prestations" class="d" href="#">Prestations</router-link>
        <router-link to="/tarif" class="g" href="#">Tarifs</router-link>
        <router-link to="/contact" class="e" href="#">Contact</router-link>
        <router-link to="/blog" class="f" href="#">Blog</router-link>
      </ul>
      <div class="logIn">
        <a class="login" href="#">Connexion</a>
        <a class="login" href="#">Inscription</a>
      </div>
    </div>
  </nav>
</template>
 
<script>

export default {
  name: "Navbar",
  components:{
   
  },

  data() {
    return {
     
    }
  }

}
</script>

<style scoped>
.nav {
  height: 150px;
  display: grid;
  grid-template-columns: 18% 58% 18%;
  grid-template-rows: 33% 33% 33%;
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
  place-self: center;
}

.navigation {
  width: 100%;
  grid-area: navigation;
  font-family: 'PT Serif';
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 31px;
  color: rgba(30, 30, 30, 1);
  place-self: center;
  display: grid;
  grid-auto-flow: column;
  grid-template-columns: repeat(5, 1fr);

}

a, b, c, d, e, f, g {
  place-self: center;
  text-decoration: none;
  text-transform: uppercase;
  color: #1E1E1E;
}

.logIn {
  grid-area: logIn;
}

.a:hover,
.b:hover,
.c:hover,
.d:hover,
.e:hover,
.f:hover,
.g:hover,
.login:hover {
  color: rgba(197, 137, 64, 1);
}

.logo {
  width: 300px;
  height: 300px;
}

.login {
  box-sizing: border-box;
  background: #F9F4ED;
  border: 2px solid #1E1E1E;
  box-shadow: 4px 4px 4px #C58940;
  border-radius: 10px;
  font-family: 'PT Serif';
  font-style: normal;
  font-weight: 700;
  font-size: 12px;
  color: rgba(30, 30, 30, 1);
  padding: 5px;
  

}</style>

