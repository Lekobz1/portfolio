
<template>
  <div class="banniere-img">
    <div class="banniere">
      <h2>{{ message }} et bienvenu sur mon portfolio</h2>
    </div>
  </div>
</template>


<script>
export default {
  name: "Home",
 

  data() {
    return {
      message: ''
    };
  },
  mounted() {
    const currentHour = new Date().getHours();

    if (currentHour >= 6 && currentHour < 18) {
      this.message = 'Bonjour';
    } else {
      this.message = 'Bonsoir';
    }
  }
};
</script>

<style scoped>
h2{
  grid-area: title; 
    font-family: 'Montserrat', sans-serif;
    font-weight: 700;
    text-transform: uppercase;
    color: white;
    font-size: 55px;
}
.banniere-img{
    height: 50vh;
    background-image: url(../assets/test.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-position: top center;
    position: relative;
    z-index: 1;
}

.banniere-img::after{
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    height: 100%;
    width: 100%;
    background-color: black;
    opacity: 0.45;
    z-index: -1;
}
.banniere {  
    display: grid;
    height: 100%;
    grid-template-columns: 100%;
    grid-template-rows: 25% 25% 25% 25%;
    grid-auto-columns: 1fr;
    gap: 0% 0%;
    grid-auto-flow: row;
    grid-template-areas:
        "."
        "title"
        "buttons"
        ".";
    text-align: center;
}



</style>