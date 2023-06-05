<template>
    <div>
      <p>{{ message }} et bienvenu sur mon portfolio</p>
    </div>
  </template>
  
  <script>
  export default {
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




</style>